# no such host error when trying to pull image from docker.io
   vagrant@cp:~/app1$ sudo podman build -t simpleapp .
   STEP 1/4: FROM python:3
   ✔ docker.io/library/python:3
   Trying to pull docker.io/library/python:3...
   Error: error creating build container: initializing source docker://python:3: pinging container registry registry-1.docker.io: Get "https://registry-1.docker.io/v2/": dial tcp: lookup registry-1.docker.io: no such host
   vagrant@worker:~/app1$


# update /etc/hosts is not applicable option, as you need to add hosts under *.docker.io
   ##If we add host IP for registry-1.docker.io
   vagrant@cp:~/app1$ cat /etc/hosts
   127.0.0.1 localhost
   127.0.1.1 vagrant
   54.83.42.45 registry-1.docker.io

## Docker pull image will failur wnen access auth.docker.io:
   ✔ docker.io/library/python:3
   Trying to pull docker.io/library/python:3...
   WARN[0031] Failed, retrying in 2s ... (1/3). Error: initializing source docker:/            /python:3: pinging container registry registry-1.docker.io: Get "https://registr            y-1.docker.io/v2/": dial tcp 54.83.42.45:443: i/o timeout
   Error: error creating build container: initializing source docker://python:3: Ge            t "https://auth.docker.io/token?scope=repository%3Alibrary%2Fpython%3Apull&servi            ce=registry.docker.io": dial tcp: lookup auth.docker.io: no such host


# the option is to add DNS nameservers via netplan, a new network utility since Ubuntu 18.04

## First, find the eathernet interface
   vagrant@cp:~/app1$ ip a
   1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
   ...
   2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
      link/ether 08:00:27:a2:6b:fd brd ff:ff:ff:ff:ff:ff
      inet 10.0.2.15/24 brd 10.0.2.255 scope global dynamic eth0
         valid_lft 85406sec preferred_lft 85406sec
      inet6 fe80::a00:27ff:fea2:6bfd/64 scope link
         valid_lft forever preferred_lft forever
   3: eth1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
      link/ether 08:00:27:13:16:91 brd ff:ff:ff:ff:ff:ff
      inet 172.16.0.100/24 brd 172.16.0.255 scope global eth1
         valid_lft forever preferred_lft forever
      inet6 fe80::a00:27ff:fe13:1691/64 scope link
         valid_lft forever preferred_lft forever
   4: tunl0@NONE: <NOARP,UP,LOWER_UP> mtu 1480 qdisc noqueue state UNKNOWN group default qlen 1000
   ...
   7: calide9edeb0dba@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
   ...
   8: calicae2e1fc5ca@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
   ...
   9: cali6364940989e@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
   ...
   10: cni-podman0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN group default qlen 1000
   ...
   vagrant@cp:~/app1$

## update /etc/netplan/50-vagrant.yaml

### before update
   vagrant@cp:~/app1$ cat /etc/netplan/50-vagrant.yaml
   ---
   network:
   version: 2
   renderer: networkd
   ethernets:
      eth1:
         addresses:
         - 172.16.0.100/24

### update via sudo vim /etc/netplan/50-vagrant.yaml

### after update
   vagrant@cp:~/app1$ sudo cat /etc/netplan/50-vagrant.yaml
   ---
   network:
   version: 2
   renderer: networkd
   ethernets:
      eth1:
         addresses:
         - 172.16.0.100/24
         nameservers:
         addresses: [1.1.1.1,1.0.0.1,8.8.8.8,8.8.4.4]

## sudo netplan try
   vagrant@worker:~/app1$ sudo netplan try
   Do you want to keep these settings?
   Press ENTER before the timeout to accept the new configuration
   Changes will revert in  99 seconds
   Configuration accepted.
   vagrant@worker:~/app1$

## sudo netplan apply

## now success in pull docker image from docker.io
   vagrant@cp:~/app1$ sudo podman build -t simpleapp .

   STEP 1/4: FROM python:3
   ✔ docker.io/library/python:3
   Trying to pull docker.io/library/python:3...
   Getting image source signatures
   Copying blob d8092d56ded5 done
   ...
   Copying config 4f9baf941f done
   Writing manifest to image destination
   Storing signatures
   STEP 2/4: ADD simple.py /
   --> 67c70cf04f4
   STEP 3/4: RUN pip install pystrich
   Collecting pystrich
   Downloading pyStrich-0.8.tar.gz (981 kB)
      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 981.2/981.2 kB 13.7 MB/s eta 0:00:00
   Preparing metadata (setup.py): started
   Preparing metadata (setup.py): finished with status 'done'
   Collecting Pillow
   Downloading Pillow-9.2.0-cp310-cp310-manylinux_2_28_x86_64.whl (3.2 MB)
      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.2/3.2 MB 29.0 MB/s eta 0:00:00
   Building wheels for collected packages: pystrich
   Building wheel for pystrich (setup.py): started
   Building wheel for pystrich (setup.py): finished with status 'done'
   Created wheel for pystrich: filename=pyStrich-0.8-py3-none-any.whl size=1107377 sha256=c44737beaa073b01010e76cf5436600c0dfd8f6564fe54ddac8fe982694539a1
   Stored in directory: /root/.cache/pip/wheels/d6/1b/c0/54096f53b41958f530a72c94148777b543d44cde0719beae8a
   Successfully built pystrich
   Installing collected packages: Pillow, pystrich
   Successfully installed Pillow-9.2.0 pystrich-0.8
   WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
   --> 253288b13a5
   STEP 4/4: CMD [ "python", "./simple.py" ]
   COMMIT simpleapp
   --> 4b57e3e7644
   Successfully tagged localhost/simpleapp:latest
   4b57e3e76443577fdc644cd69dde6c5825c7f09483405690f20b96b1c5d1a758


![netplan Reference](https://netplan.io/reference)