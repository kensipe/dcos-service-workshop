##  DCOS Service Workshop

## System Requirements
Hardware
laptop (16G ram)

Software 
Java 1.8 JDK
Docker
Vagrant 1.8.1
VirtualBox

Install dcos-vagrant  (this is a large download and needs to be done prior to the conference)
https://github.com/dcos/dcos-vagrant

Abbreviated setup (if you have the prerequisites)

1. git clone https://github.com/dcos/dcos-vagrant
2. cd dcos-vagrant
3. VBoxManage list hostonlyifs | grep vboxnet0 -q || VBoxManage hostonlyif create
4. VBoxManage hostonlyif ipconfig vboxnet0 --ip 192.168.65.1
5. vagrant plugin install vagrant-hostmanager
6. curl -O https://downloads.dcos.io/dcos/EarlyAccess/dcos_generate_config.sh
7. vagrant box add https://downloads.dcos.io/dcos-vagrant/metadata.json
8. vagrant up m1 a1 p1 boot

README.md has configuration options, troubleshooting and prerequisites 


