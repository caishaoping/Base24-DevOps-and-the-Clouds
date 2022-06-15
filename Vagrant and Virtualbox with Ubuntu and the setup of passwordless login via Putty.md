Vagrant and Virtualbox with Ubuntu and the setup of passwordless login via Putty on Windows 10

# Preinstalled software installed on your Windows 10
- Vagrant has been installed: if not, go to [download Vagrant](https://www.vagrantup.com/downloads)
- VirtualBox has been installed: if not, go to [download VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- PuTTYgen has been installed: if not, go to [install PuTTYgen](https://www.puttygen.com/)
- PuTTY has been installed: if not, go to [install PuTTY](https://www.putty.org/)
- Git Bash has been installed: if not, go to [Git Bash for windows](https://gitforwindows.org/)

#  Get to know these tools in one statement
- Vagrant: Hashcorp's tool to manage Virtual machines
- VirtualBox: A kind of hypervisor from Oracle
- PuTTYgen: A tool to manage/convert public/private keys
- PuTTY: A tool for SSH and Telnet terminal on Windows
- Git Bash: A tool to run Git commands from Windows
- Ubuntu: A kind of Linux distribution

# Install Ubuntu on VirtualBox 

## Create a directory to host your future virtual machine envornment

  - start git bash and go to your home directory ($ is git bash command prompt)
  - $ cd ~
  - $ mkdir ./ubuntu-for-k8s-dev && cd ./ubuntu-for-k8s-dev && mkdir shared && cd ./shared && pwd
    /c/Users/caish/ubuntu-for-k8s-dev/shared
  - $ touch Vagrantfile
## Install Ubuntu on VirtualBox via Vagrant command line tool
  - From Git Bash, run Vagrant to install Ubuntu
  
    $ vagrant box add ubuntu/bionic64
    
    ==> box: Loading metadata for box 'ubuntu/bionic64'
        box: URL: https://vagrantcloud.com/ubuntu/bionic64
    ==> box: Adding box 'ubuntu/bionic64' (v20220610.0.0) for provider: virtualbox
        box: Downloading: https://vagrantcloud.com/ubuntu/boxes/bionic64/versions/20220610.0.0/providers/virtualbox.box
    Download redirected to host: cloud-images.ubuntu.com
        box:
    ==> box: Successfully added box 'ubuntu/bionic64' (v20220610.0.0) for 'virtualbox'!
  - From Git Bash, run Vagrant to check listed Ubuntu
  
    $ vagrant box list | grep bionic64
    
    ubuntu/bionic64 (virtualbox, 20210319.0.0)
    **ubuntu/bionic64 (virtualbox, 20220610.0.0)**^1]: Newly installed ubuntu/bionic64

## Init newly installed Virtual Machine Ubuntu   
  - From Git Bash, run vagrant init command

    $ vagrant init ubuntu/bionic64
    
    `Vagrantfile` already exists in this directory. Remove it before
     running `vagrant init`.

  - Try again, with --force option to override Vagrantfile

    caish@ThinkCentre MINGW64 ~/ubuntu-for-k8s-dev/shared
    
    $ vagrant init ubuntu/bionic64 --force
    
    A `Vagrantfile` has been placed in this directory. You are now
    ready to `vagrant up` your first virtual environment! Please read
    the comments in the Vagrantfile as well as documentation on
    `vagrantup.com` for more information on using Vagrant.






