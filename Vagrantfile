# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos65-gitlab"
  config.vm.box_url = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-6.5_chef-provisionerless.box"

  config.vm.network "forwarded_port", guest: 80, host: 2436

  config.vm.synced_folder "./", "/home/vagrant" # Directory where 'Vagrantfile' is will become a synced/linked directory to the vagrant home directory (DO NOT REMOVE THIS OR ELSE THE SERVER WILL NOTRUN CORRECTLY)
end


# Extra Info
#
# GitLab url is:
#
#   http://localhost:2436
#
# add ~/.ssh/config:
#
#   Host gitlab
#       hostname 127.0.0.1
#       port 2222
#
# and repository url is:
#
#   git@gitlab:repo.git
