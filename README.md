# vagrant-centOS-oracle-xe

Solves the Error message in the ansible script
Express Edition requires 2048 MB of swap space. This system has 0 MB
of swap space.  Configure more swap space on the system and retry the 
installation.


Oracle setup commands
put oracle-xe-11.2.0-1.0.x86_64.rpm.zip in the shared /vagrant folder

run
cd /vagrant
sudo yum -y install ansible
sudo ansible-playbook -i "localhost," -c local oracle-xe.yml -v

log out of ssh
log back in
run 'sqlplus' to check if setup successful

should get the output something like

[vagrant@localhost ~]$ sqlplus
SQL*Plus: Release 11.2.0.2.0 Production on
Copyright (c) 1982, 2011, Oracle.  All rights reserved.
Enter user-name:
