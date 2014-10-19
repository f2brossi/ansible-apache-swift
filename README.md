ansible-apache-swift
===================

Apache reverse proxy for Openstack components Swift and Keystone.

## Prereqs

Install the following applications on your local machine first:

 * [Vagrant](http://vagrantup.com)
 * [Vagrant openstack plugin] (https://github.com/ggiamarchi/vagrant-openstack-provider)
 * [Ansible](http://ansibleworks.com)
 
## Configuration

Enter your credentials ENV[OS_XXX] in the Vagrantfile

Update the hosts file with your public @ip of your vm.

>vagrant up --provider=openstack
