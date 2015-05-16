# GitLab-Vagrant-Server

## GitLab running on a Vagrant CentOS6.5 server

### Requirements
* Be able to follow instructions carefully

### Installation
1. Clone this repository: `git clone https://github.com/NurdTurd/GitLab-Vagrant-Server.git`
2. cd into the repo: `cd GitLab-Vagrant-Server`
4. Enter: `vagrant up` in your terminal to start the vagrant VM
5. Once the box is up and running enter: `vagrant ssh`
6. Now you should be in the ssh'd VM console.
7. 1. (Optional: `sudo yum update -y`)
8. Next, enter the commands below one by one:
9. `sudo yum install openssh-server postfix cronie`
10. `sudo service postfix start`
11. `sudo chkconfig postfix on`
12. `sudo lokkit -s http -s ssh`
13. Next enter: `curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh | sudo bash`
14. After that, run: `sudo yum install gitlab-ce`
14. After that installed the package, enter: `sudo gitlab-ctl reconfigure`
15. Head over to [http://localhost:2436](http://localhost:2436) and login with `root` as the username and `5iveL!fe`.
16. You should be good to go after that. Enjoy :)
17. If you find any issues please report them and I will get to the ASAP.
