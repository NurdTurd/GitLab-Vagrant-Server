# GitLab-Vagrant-Server

## GitLab running on a Vagrant CentOS6.5 server

### Requirements
* Be able to follow instructions carefully

### Installation
1. Clone this repository: `git clone https://github.com/NurdTurd/GitLab-Vagrant-Server.git`
2. cd into the repo: `cd GitLab-Vagrant-Server`
3. Enter on your **local** machine: `curl -O https://downloads-packages.s3.amazonaws.com/centos-6.6/gitlab-7.9.2_omnibus-1.el6.x86_64.rpm`
4. Enter: `vagrant up` in your terminal to start the vagrant VM
5. Once the box is up and running enter: `vagrant ssh`
6. Now you should be in the ssh'd VM console.
7. 1. (Optional: `yum update -y`)
8. Next, enter the commands below
9. `sudo yum install openssh-server`
10. `sudo yum install postfix`
11. `sudo yum install cronie`
12. `sudo service postfix start`
13. `sudo chkconfig postfix on`
14. `sudo lokkit -s http -s ssh`
15. Next enter: `sudo rpm -i gitlab-7.9.2_omnibus-1.el6.x86_64.rpm`
16. After that installed the package, enter: `sudo gitlab-ctl reconfigure`
17. You should be good to go after that. Enjoy :)
18. If you find any issues please report them and I will get to the ASAP.