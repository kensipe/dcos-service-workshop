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

[README.md](https://github.com/dcos/dcos-vagrant) has configuration options, troubleshooting and prerequisites

## Outline

1. Tour and Understanding Mesos and DCOS

  Lesson Objectives
  1. Multi-level scheduler (Mesos/Agents/Framework)
  1. DCOS Eco-system (Exhibitor/Mesos-DNS/Admin Router/Docker/Cosmos/Universe)
  1. Marathon
  1. Reasons to build a new Framework
  1. Debugging in a Mesos environment

  Lab: Setup DCOS environment (cloud or dcos-vagrant)
  
  1. Deploy service via Marathon
  1. Deploy a service
  1. Create your own universe

2. Taxonomy of a Framework / Service

  1. Schedulers
  1. Executors
  1. mesos.proto
  1. Offers / Tasks

3. State and Coordination

  1. Coordination
  1. State
  1. DNS

4. Universe and Packaging

  1. Your own Universe
  1. Packaging
  1. Admin Router and Web access

6. Adding a CLI

7. Advanced Services

  1. Reservations
  1. Persistent Volumes

Topics to add:
  roles
  static partitioning
  offers received are role + *
  taskId vs taskName
