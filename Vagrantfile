# -*- mode: ruby -*-
# vi: set ft=ruby :

=begin

Before you do anything.

	(Optional: 'yum update -y')

Enter: wget -cv https://downloads-packages.s3.amazonaws.com/centos-6.6/gitlab-7.7.1_omnibus.5.4.1.ci-1.el6.x86_64.rpm # on your local machine
After that.
Enter: vagrant up
Once the box is up and running
Enter: vagrant ssh
Then Enter: sudo rpm -i gitlab-7.7.1_omnibus.5.4.1.ci-1.el6.x86_64.rpm
After that ran
Enter: sudo gitlab-ctl reconfigure
=end

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos65"
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