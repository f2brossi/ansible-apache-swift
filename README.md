ansible-apache-swift
===================

Apache reverse proxy for Openstack components Swift and Keystone.

## Prereqs

Install the following applications on your local machine first:

 * [Vagrant](http://vagrantup.com)
 * [Vagrant openstack plugin] (https://github.com/ggiamarchi/vagrant-openstack-provider)
 * [Ansible](http://ansibleworks.com)
 
## Quick Start

After installing the applications above, the quickest way to get
started is to specify all the details manually within a `config.vm.provider`
block in the Vagrantfile

Create a Vagrantfile that looks like the following, filling in your information
where necessary.

This Vagrantfile shows the minimal needed configuration.

```ruby
require 'vagrant-openstack-provider'

Vagrant.configure('2') do |config|

  config.vm.box       = 'openstack'
  config.ssh.username = 'stack'

  config.vm.provider :openstack do |os|
    os.openstack_auth_url = 'http://keystone-server.net/v2.0/tokens'
    os.username           = 'openstackUser'
    os.password           = 'openstackPassword'
    os.tenant_name        = 'myTenant'
    os.flavor             = 'm1.small'
    os.image              = 'ubuntu'
    os.floating_ip_pool   = 'publicNetwork'
  end
end
```

Update the hosts file with your public @ip of your vm.

And then run `vagrant up --provider=openstack`.


