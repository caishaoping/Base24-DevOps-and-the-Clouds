# Prerequsite
- This the continuation with the assumption that you have completed the install of Ubuntu on VirgualBox via Vagrant;
- If not, please following the steps in [this link](https://github.com/caishaoping/Base24-DevOps-and-the-Clouds/blob/main/Vagrant%20and%20Virtualbox%20with%20Ubuntu.md)

# Recap of where you are with your logins to newly installed Ubuntu VirtualBox
## When using Vagrant ssh command, it can successfully to establish an SSH session into Ubuntu virtual machine
  $ **vagrant ssh**  
    ![ssh login](Vagrant.ssh.JPG)
## When you try to use Putty, it failed to establish the SSH session
  - When you use Putty to login, it will fail because of missing authentication setup

  ![Putth SSH failure](putty.failure.JPG)

# why vagrant ssh succeses but Putty is failing
## First, let us have a look your newly created Ubuntu virtual machine
- vagrant ssh login to Ubuntu virtual machine  
    $ vagrant ssh  
    Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 4.15.0-184-generic x86_64)  
    ...  
    Last login: Wed Jun 15 02:17:42 2022 from 10.0.2.2  
- Go to folder ~/.ssh and look for "authorized_keys" file  
    $ cd ~./ssh  
    $ ls -al  
    drwx------ 2 vagrant vagrant 4096 Jun 15 01:35 .  
    drwxr-xr-x 5 vagrant vagrant 4096 Jun 15 01:59 ..  
    -rw------- 1 vagrant vagrant  389 Jun 15 01:35 authorized_keys  

- SSH Public key already created for user id "vagrant"  
    $ cat authorized_keys  
    ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCZSXUEnxcvuEa4VvkovXwmOCXjdxQezTFLE01lCvnSifKhqegxNS+QIgxSuk3JIUfoPe0Gfh5x0r0pZKpZBWT4HFEzYo02RRvSZ23/TOav7BVgWpqQprEYyfLIcLlUb1tl5JOrqWb0qVwj4bKqrHXnK5y9opE8TnoJSV9CtaLahv0wI7Sjxdw0nyAft3Xt1NL+Y73RNpbiT4SnuV1llq1EIWhfB//QwOPHOnuVh/LpK+Bhac08F8WJRmtCo1BCX933CCgxFwkWybEt5Qm6QebJyGDtdywT7I+cTLhEpcQQh6uhCP+000TdIJLYwhPa+/86SLCGf3IA6XSfwFZLb9ij **vagrant**  

## Second, confirm that private key has been setup and used by vagrant ssh
- when ssh private key for user id of "vagrant", vagrant ssh command will simply use the private key to establish ssh connection to Ubuntu virtual machine, there is no need for providing user's password, instead, the private key is the credential.  
- From Git Bash, go to virtual box folder as shown below, then confirm the existence of  
    ~/ubuntu-for-k8s-dev/shared/.vagrant/machines/default/virtualbox  
    $ pwd  
    /c/Users/caish/ubuntu-for-k8s-dev/shared/.vagrant/machines/default/virtualbox  
    $ ls -al  
    total 16  
    drwxr-xr-x 1 caish 197609    0 Jun 14 20:35 ./  
    drwxr-xr-x 1 caish 197609    0 Jun 14 20:34 ../  
    ...  
    -rw-r--r-- 1 caish 197609 1702 Jun 14 20:35 **private_key**   
    -rw-r--r-- 1 caish 197609  144 Jun 15 15:49 synced_folders    
    -rw-r--r-- 1 caish 197609   40 Jun 14 20:34 vagrant_cwd  
- A peek of the content of private key   
    -----BEGIN RSA PRIVATE KEY-----  
    MIIEowIBAAKCAQEAmUl1BJ8XL7hGuFb5KL18Jjgl43cUHs0xSxNNZQr50onyoano  
    MTUvkCIMUrpNySFH6D3tBn4ecdK9KWSqWQVk+BxRM2KNNkUb0mdt/0zmr+wVYFqa  
    ...  
    xBQQa54g1R3Dv78K63slogBv+3dNvC4//wNSgxqzjADQNGKenk4ssDxU39t0Ggh7  
    IsVyY0KxvYZSEl1hoRGthvCeC+K5mTSOGzUaQ8Ljtpl309rXe4OG  
    -----END RSA PRIVATE KEY-----  

## Now, it is so obvious that Putty needs the same private key for ssh access
    The following steps will show you how to install the paired private key to Putty in orde for it to connect to Unbutu virtual machine. As Putty does not support ssh key format, so we will first use PuttyGen to convert vagrant ssh used  private key from ssh key format to Putty compatiable format, then, we will load the putty format private key to Putty as the ssh session key for the access. 

## Use PuttyGen to convert SSH formated private key to Putty compatiable key format
    - Open **PuttyGen** and choose **Conversions** in the main menu and then select **Imports** in the dropdown list   
    - Import **private_key** file from /c/Users/caish/ubuntu-for-k8s-dev/shared/.vagrant/machines/default/virtualbox  
    - Save Putty format private key to a new file like **~/.ssh/ubuntu-for-k8s-dev.ppk**, this file will be used in next step     
    - Sample PuttGen key conversions screen is shown below  
   ![PuttyGen](puttygen.convertkey.JPG)
    - Check and confirm that new Putty format key is saved as expected  
        $ ls -al ~/.ssh  
        total 58  
        drwxr-xr-x 1 caish 197609    0 Jun 15 16:07 ./  
        drwxr-xr-x 1 caish 197609    0 Jun 19 14:09 ../  
        ...  
        -rw-r--r-- 1 caish 197609 1464 Jun 15 16:07 **ubuntu-for-k8s-dev.ppk**  
        drwxr-xr-x 1 caish 197609    0 Dec 13  2021 vagrant_k8s_nodes/  
  
## On Putty, import newly converted Putty formated key in new Putty Session
    - From **Putty**, enter the host IP of the new virtual machine and then import previously formated key   
    - Then, save as a named session  
    - Sample screen is shown as below  
   ![Putty](putty.ssh.importkey.JPG)

## Test the newly setup Putty session profile
    login as: **vagrant**  
    Authenticating with public key "imported-openssh-key"  
    Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 4.15.0-184-generic x86_64)  
    ...  
    System information as of Wed Jun 15 21:13:05 UTC 2022  
    System load:  0.0               Processes:             99  
    Usage of /:   3.9% of 38.71GB   Users logged in:       0  
    Memory usage: 2%                IP address for enp0s3: 10.0.2.15  
    Swap usage:   0%                IP address for enp0s8: **192.168.5.30**    
    *** System restart required ***  
    Last login: Wed Jun 15 21:10:15 2022 from 192.168.5.1  
    vagrant@ubuntu-bionic:~$  
# Congratulations! Your have successfully setup passwordless access from Putty to the new virtual machine. 


  


