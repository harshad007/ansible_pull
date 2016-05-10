# ansible_pull

This role implements "ANSIBLE PULL" architecture usingf Ansible's PUSH mechanism.


#NOTE
PLEASE CHANGE REPOSITORY URL AND IP ADDRESSES IN HOSTS FILE

#for VIRTUAL BOX

IN VIRTUAL BOX ENVIRONMENT IP GIVEN TO INSTANCES ARE NOT ACCESSIBLE BY GITHUB DIRECTLY.

YOU MAY NEED TO GET SOME INFORMATION RELATED TO BRIDGE AND NAT OPTIONS IN VIRTUALBOX.

#setup

SETUP 3 INSTANCES (UBUNTU) IN VIRTUALBOX WITH DIFFERENT IP ADDRESSES AND 1 UBUNTU SYSTEM WITH ANSIBLE INSTALLED

#HOSTS FILE
[local]
localhost

[servers] 
192.168.33.21
192.168.33.22
192.168.33.23

[datacenter:children]
servers

[datacenter:vars]
ansible_user=vagrant
ansible_password=vagrant

#NOTE
IF YOU DON'T WANT TO SPECIFY PASSWORD IN HOSTS FILE

"------------------------------------------------------------------------------	
 	YOU CAN MAKE PASSWORDLESS AUTHENTICATION FOR MORE SECURITY
 -------------------------------------------------------------------------------"
