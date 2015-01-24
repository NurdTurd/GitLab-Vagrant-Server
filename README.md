# GitLab-Vagrant-Server

## GitLab running on a Vagrant CentOS6.5 server

### Requirements
* Be able to follow instructions carefully

### Installation
1. Clone this repository: `git clone https://github.com/NurdTurd/GitLab-Vagrant-Server.git`
2. cd into the repo: `cd GitLab-Vagrant-Server`
3. Enter on your **local** machine: `wget -cv https://downloads-packages.s3.amazonaws.com/centos-6.6/gitlab-7.7.1_omnibus.5.4.1.ci-1.el6.x86_64.rpm`
4. Enter: `vagrant up` in your terminal to start the vagrant VM
5. Once the box is up and running enter: `vagrant ssh`
6. Now you should be in the ssh'd VM console.
7. 1. (Optional: `yum update -y`)
8. In the VM enter: `sudo rpm -i gitlab-7.7.1_omnibus.5.4.1.ci-1.el6.x86_64.rpm`
9. After that installed the package, enter: `sudo gitlab-ctl reconfigure`