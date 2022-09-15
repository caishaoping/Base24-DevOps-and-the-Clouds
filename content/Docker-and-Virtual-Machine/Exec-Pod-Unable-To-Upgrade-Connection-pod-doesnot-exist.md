# Kubenet node interal IP address incorrectly assigned can lead the issue to exec pod command, most likly following error:
   error: unable to upgrade connection: pod does not exist

## Summary of Issue
Some how, I cannot run kubectl exec pod command on pods assigned to worker node, I am getting "unable to upgrade connection.." when running following command:

vagrant@cp:~/app1$ for name in try1-7f7c6fdc54-dqgjj try1-7f7c6fdc54-f8k5m try1-7f7c6fdc54-jxq57
>do 
>kubectl exec $name -- touch /tmp/healthy
>done

error: unable to upgrade connection: pod does not exist
error: unable to upgrade connection: pod does not exist
error: unable to upgrade connection: pod does not exist

## Check node's internal IP, both nodes associated to the same internal-ip

vagrant@cp:~/app1$ k get nodes -o wide
NAME     STATUS   ROLES           AGE     VERSION   INTERNAL-IP   EXTERNAL-IP   OS-IMAGE             KERNEL-VERSION      CONTAINER-RUNTIME
cp       Ready    control-plane   5d21h   v1.24.1   10.0.2.15     <none>        Ubuntu 20.04.5 LTS   5.4.0-125-generic   containerd://1.6.8
worker   Ready    <none>          5d21h   v1.24.1   10.0.2.15     <none>        Ubuntu 20.04.5 LTS   5.4.0-125-generic   containerd://1.5.9

## A look at both nodes' interface
### vagrant@worker:~$ ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:a2:6b:fd brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.15/24 brd 10.0.2.255 scope global dynamic eth0
       valid_lft 83690sec preferred_lft 83690sec
    inet6 fe80::a00:27ff:fea2:6bfd/64 scope link
       valid_lft forever preferred_lft forever
3: eth1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:27:ec:1d brd ff:ff:ff:ff:ff:ff
    inet 172.16.0.102/24 brd 172.16.0.255 scope global eth1
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fe27:ec1d/64 scope link
       valid_lft forever preferred_lft forever
4: cali8411b8a20c9@if3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
    link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netns cni-a97e0666-5f6a-cd5b-83b8-bfebf7c585e2
    inet6 fe80::ecee:eeff:feee:eeee/64 scope link
       valid_lft forever preferred_lft forever
5: tunl0@NONE: <NOARP,UP,LOWER_UP> mtu 1480 qdisc noqueue state UNKNOWN group default qlen 1000
    link/ipip 0.0.0.0 brd 0.0.0.0
    inet 192.168.171.64/32 scope global tunl0
       valid_lft forever preferred_lft forever
8: cali12d4a061371@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
    link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netns cni-cf125b5d-855b-33b3-0509-4e7eeadbe74b
    inet6 fe80::ecee:eeff:feee:eeee/64 scope link
       valid_lft forever preferred_lft forever
9: cali90199617297@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
    link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netns cni-8f41548a-827d-f09b-d73a-de797ed83644
    inet6 fe80::ecee:eeff:feee:eeee/64 scope link
       valid_lft forever preferred_lft forever
vagrant@worker:~$


### vagrant@cp:~$ ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:a2:6b:fd brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.15/24 brd 10.0.2.255 scope global dynamic eth0
       valid_lft 83551sec preferred_lft 83551sec
    inet6 fe80::a00:27ff:fea2:6bfd/64 scope link
       valid_lft forever preferred_lft forever
3: eth1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:13:16:91 brd ff:ff:ff:ff:ff:ff
    inet 172.16.0.100/24 brd 172.16.0.255 scope global eth1
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fe13:1691/64 scope link
       valid_lft forever preferred_lft forever
4: tunl0@NONE: <NOARP,UP,LOWER_UP> mtu 1480 qdisc noqueue state UNKNOWN group default qlen 1000
    link/ipip 0.0.0.0 brd 0.0.0.0
    inet 192.168.242.64/32 scope global tunl0
       valid_lft forever preferred_lft forever
7: calicae2e1fc5ca@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
    link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netns cni-be6d1e35-2c6d-53b5-6af6-bd714169d327
    inet6 fe80::ecee:eeff:feee:eeee/64 scope link
       valid_lft forever preferred_lft forever
8: calide9edeb0dba@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
    link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netns cni-dc17c457-89cb-99cf-aa01-3dcc1b4c6d39
    inet6 fe80::ecee:eeff:feee:eeee/64 scope link
       valid_lft forever preferred_lft forever
9: cali6364940989e@if4: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1480 qdisc noqueue state UP group default
    link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netns cni-d976e140-cde4-50ff-ddff-98d9f074a3ac
    inet6 fe80::ecee:eeff:feee:eeee/64 scope link
       valid_lft forever preferred_lft forever
vagrant@cp:~$

## Container sections in Pod definition:
    spec:
      containers:
      - image: 10.101.72.139:5000/simpleapp
        imagePullPolicy: Always
        name: simpleapp
        readinessProbe:
          exec:
            command:
            - cat
            - /tmp/healthy
          initialDelaySeconds: 5
          periodSeconds: 10
        resources: {}
        terminationMessagePath: /dev/termination-log
        terminationMessagePolicy: File
      - image: k8s.gcr.io/goproxy:0.1
        name: goproxy
        ports:
        - containerPort: 8080
        readinessProbe:
          tcpSocket:
            port: 8080
          initialDelaySeconds: 5
          periodSeconds: 10
        livenessProbe:
          tcpSocket:
            port: 8080
          initialDelaySeconds: 15
          periodSeconds: 20


## A look at Pods
vagrant@cp:~/app1$ k get po -o wide
NAME                       READY   STATUS    RESTARTS       AGE    IP                NODE     NOMINATED NODE   READINESS GATES
busybox                    1/1     Running   1 (117m ago)   177m   192.168.171.121   worker   <none>           <none>
nginx-6488f757bc-rp4wv     1/1     Running   5 (117m ago)   42h    192.168.171.120   worker   <none>           <none>
registry-d4cf9fd7d-9c52d   1/1     Running   5 (117m ago)   42h    192.168.171.122   worker   <none>           <none>
try1-79f8557b4d-2w2sp      1/2     Running   0              32m    192.168.171.66    worker   <none>           <none>
try1-79f8557b4d-449sp      1/2     Running   0              32m    192.168.171.68    worker   <none>           <none>
try1-79f8557b4d-fx676      1/2     Running   0              32m    192.168.242.91    cp       <none>           <none>
try1-79f8557b4d-gb5pt      1/2     Running   0              32m    192.168.171.67    worker   <none>           <none>
try1-79f8557b4d-jck92      1/2     Running   0              32m    192.168.242.89    cp       <none>           <none>
try1-79f8557b4d-k4788      1/2     Running   0              32m    192.168.242.90    cp       <none>           <none>

## To fix, need to assign internal IPs to nodes

## The update on worker node:

sudo vim /etc/systemd/system/kubelet.service.d/10-kubeadm.conf to add below line:
Environment="KUBELET_EXTRA_ARGS=--node-ip=172.16.0.102"

vagrant@worker:~$ sudo systemctl daemon-reload

vagrant@worker:~$ sudo systemctl restart kubelet.service

vagrant@worker:~$ sudo systemctl status kubelet
● kubelet.service - kubelet: The Kubernetes Node Agent
     Loaded: loaded (/lib/systemd/system/kubelet.service; enabled; vendor preset: enabled)
    Drop-In: /etc/systemd/system/kubelet.service.d
             └─10-kubeadm.conf
     Active: active (running) since Thu 2022-09-15 00:02:18 UTC; 20s ago
       Docs: https://kubernetes.io/docs/home/
   Main PID: 76949 (kubelet)
      Tasks: 15 (limit: 2315)
     Memory: 34.6M
     CGroup: /system.slice/kubelet.service
             └─76949 /usr/bin/kubelet --bootstrap-kubeconfig=/etc/kubernetes/bootstrap-kubelet.conf --kubeconfig=/etc/kubernetes/kubelet.conf --c>

## The update on CP ndoe:

sudo vim /etc/systemd/system/kubelet.service.d/10-kubeadm.conf to add below line:
Environment="KUBELET_EXTRA_ARGS=--node-ip=172.16.0.100"

vagrant@worker:~$ sudo systemctl daemon-reload

vagrant@worker:~$ sudo systemctl restart kubelet.service

vagrant@worker:~$ sudo systemctl status kubelet

## Re-deploy  and the pods are 1/2

vagrant@cp:~/app1$ k get po -o wide
NAME                       READY   STATUS    RESTARTS        AGE     IP                NODE     NOMINATED NODE   READINESS GATES
busybox                    1/1     Running   1 (5h32m ago)   6h32m   192.168.171.121   worker   <none>           <none>
nginx-6488f757bc-rp4wv     1/1     Running   5 (5h32m ago)   46h     192.168.171.120   worker   <none>           <none>
registry-d4cf9fd7d-9c52d   1/1     Running   5 (5h32m ago)   46h     192.168.171.122   worker   <none>           <none>
try1-76c5655c48-5xcpw      1/2     Running   0               13s     192.168.242.87    cp       <none>           <none>
try1-76c5655c48-d8lnv      1/2     Running   0               13s     192.168.242.92    cp       <none>           <none>
try1-76c5655c48-dvdcz      1/2     Running   0               13s     192.168.171.73    worker   <none>           <none>
try1-76c5655c48-kk55c      1/2     Running   0               13s     192.168.242.88    cp       <none>           <none>
try1-76c5655c48-rlvrg      1/2     Running   0               13s     192.168.171.74    worker   <none>           <none>
try1-76c5655c48-w7tnt      1/2     Running   0               13s     192.168.171.72    worker   <none>           <none>

## Create /tmp/healthy file and pods will be 2/2:

vagrant@cp:~/app1$ for name in $(k get po -l app=try1 -o name)
> do
> k exec $name -c simpleapp -- touch /tmp/healthy
> done


## POD is up and running 2/2:
vagrant@cp:~/app1$ k get po -o wide
NAME                       READY   STATUS    RESTARTS        AGE     IP                NODE     NOMINATED NODE   READINESS GATES
busybox                    1/1     Running   1 (5h34m ago)   6h33m   192.168.171.121   worker   <none>           <none>
nginx-6488f757bc-rp4wv     1/1     Running   5 (5h34m ago)   46h     192.168.171.120   worker   <none>           <none>
registry-d4cf9fd7d-9c52d   1/1     Running   5 (5h34m ago)   46h     192.168.171.122   worker   <none>           <none>
try1-76c5655c48-5xcpw      2/2     Running   0               81s     192.168.242.87    cp       <none>           <none>
try1-76c5655c48-d8lnv      2/2     Running   0               81s     192.168.242.92    cp       <none>           <none>
try1-76c5655c48-dvdcz      2/2     Running   0               81s     192.168.171.73    worker   <none>           <none>
try1-76c5655c48-kk55c      2/2     Running   0               81s     192.168.242.88    cp       <none>           <none>
try1-76c5655c48-rlvrg      2/2     Running   0               81s     192.168.171.74    worker   <none>           <none>
try1-76c5655c48-w7tnt      2/2     Running   0               81s     192.168.171.72    worker   <none>           <none>

## Check one pod to verify that the True for Readiness, and Container is also ready.
vagrant@cp:~/app1$ k describe po pod/try1-76c5655c48-w7tnt | grep -E 'State|Ready'
error: there is no need to specify a resource type as a separate argument when passing arguments in resource/name form (e.g. 'kubectl get resource/<resource_name>' instead of 'kubectl get resource resource/<resource_name>'
vagrant@cp:~/app1$ k describe po try1-76c5655c48-w7tnt | grep -E 'State|Ready'
    State:          Running
    Ready:          True
    State:          Running
    Ready:          True
  Ready             True
  ContainersReady   True
vagrant@cp:~/app1$

