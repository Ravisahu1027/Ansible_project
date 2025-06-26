# Ansible_project

Our Task is to Setup 3 ubuntu server where 
1. Ansible server
2. Target_1 server
3. Target_2 server
Task 1. - install ansible in Ansible server by using Ansible Documentation
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo add-apt-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible

Task 2. Connect Both target server to Ansible server using ssh token.
In all three server generate token
$ ssh-keygen

then from ansible server copy public key
$ cd .ssh
$ ls -la
$ cat id_ed25519.pub

login to other two server and paste public token 
ssh-keygen
$ cd .ssh
$ ls -la
$ vi authorized_keys

Task 3 - Enable public key access
$ vi /etc/ssh/sshd_config
PasswordAuthentication yes
PermitRootLogin yes

Now try ssh into both server 
$ ssh ubuntu@172.31.89.93

