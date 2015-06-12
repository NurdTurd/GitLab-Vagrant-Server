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
7. Next, enter the commands below one by one:
8. `sudo yum install curl openssh-server postfix cronie`
9. `sudo service postfix start`
10. `sudo chkconfig postfix on`
11. `sudo lokkit -s http -s ssh`
13. Now to run the install script: `curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh | sudo bash`
14. Now to install GitLab: `sudo yum install gitlab-ce`
15. After that installed the package, run: `sudo gitlab-ctl reconfigure`
16. Head over to [http://localhost:2436](http://localhost:2436) and login with `root` as the username and `5iveL!fe`.
17. You should be good to go after that. Enjoy :)
18. If you find any issues please report them and I will get to the ASAP.

### Extra Info

GitLab url is: [`http://localhost:2436`](http://localhost:2436)

For easier access, add this to your ~/.ssh/config:
````
Host local-gitlab
   hostname 127.0.0.1
   port 2222
````

