ansible-apache-swift
===================

Apache reverse proxy for Openstack components Swift and Keystone

Install Vagrant 1.4+

Install Vagrant Plugin openstack

Install Ansible

Enter your credentials ENV[OS_XXX] in the Vagrantfile

Update the hosts file with your public @ip of your vm.

>vagrant up --provider=openstack
