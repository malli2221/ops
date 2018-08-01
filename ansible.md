Ansible :

**Use of ansible** : Ansible is an automation tool.it can configure systems, deploy software, and orchestrate more advanced IT tasks such as continuous deployments or zero downtime rolling updates.

Ansible main golas are simplicity ans ease of use,it also has a strong focus on security and reliability, featuring a minimum of moving parts, usage of OpenSSH for transport (with other transports and pull modes as alternatives), and  a language that is designed around auditability by humans even those not familiar with the program.

Its working based on push machnism.



Ansible installtion :

ansible installation prerequesies was python 2.6 we required, after that using &quot;apt-get install ansible&quot;

once install the ansible then we need to the host entry, in host we have enter the node machine ipaddress then generate the ssh-key using that key we have to communicate the node machie.

Once we have this steps we to check the connection between those server,using &quot;ansible -m ping all &quot; check the connection once it done we have communicate the remote servers.

Installtion :

vi /etc/ansible/hosts : here we have to mention the remote servers ip address.

[webserver]

192.168.33.51

192.168.33.51

192.168.33.71

modules : ansible performs remote configuration of server by using in built modules. These have been created using python each module is deigns for performing a specific task.

  Impotant module in ansible :

1.command

2. file

3.shell module

4. copy

5.fetch

6.apt

7.yum

8.service

9. debug

10.pig

11.url

copy : using below command  i copy the file master machine to node machines.

ansible all -m copy -a &quot;src=atlanta dest=/tmp/&quot;

file : using below command i created the file in remote machine.

ansible all -m file -a &#39;name=file123 state=touch&#39;

 git install in remote machine : using below command i install git in remote machine.

ansible all -b -m apt -a &#39;name=git state=latest&#39;

uninstall purpose :

ansible all -b -m apt -a &#39;name=git state=absent&quot;



install apache : using below command i install the apache2 in the remote machine

ansible all -b -m apt -a &#39;name=git state=apache2&quot;

uninstall apache :

ansible all -b -m apt -a &#39;name=git state=absent&quot;

![an](https://github.com/malli2221/ops/blob/master/imgt/ansible1.png)

![an](https://github.com/malli2221/ops/blob/master/imgt/ansible2.png)

![an](https://github.com/malli2221/ops/blob/master/imgt/ansible3.png)

![an](https://github.com/malli2221/ops/blob/master/imgt/anisble4.png)
1/8/2018 : 

Today i worked on ansible playbooks i write a playbook for git intsallation and apache2 installation and nginx and java.

Apache2 installation using ansible playbook.
---
- name : creating users and capturing username and  home dir
  hosts : all
  become : yes
  tasks :
   - name : install apache2
     apt :
        name : apache2
        state : present
   - name : starting apache service
     service :
       name : apache2
       statei : started

Using ansible create the directory:
---
- name : creating users and capturing username and  home dir
  hosts : all
  become : yes
  tasks :
   - name : install apache2
     apt :
        name : apache2
        state : present
   - name : starting apache service
     service :
         name : apache2
       statei : started
Using ansible playbook install the git.
---
- hosts : all
  become : yes
  tasks : 
   - name : install git
     apt : 
       name : git
        state : present


Using ansible playbook install nginx;
---
- name : creating users and capturing username and  home dir
  hosts : all
  become : yes
  tasks :
   - name : install apache2
     apt :
        name : nginx
        state : present
   - name : starting apache service
     service :
       name : nginx
       statei : started

Using ansible playbook clone the git reposotory:
ansible@vagrant-ubuntu-trusty-64:/opt/ansible$ cat clone.yml 
---
- hosts : all
  become : yes
  tasks : 
   - name : git clone
     git : 
       repo : https://github.com/malli2221/ops.git
       dest : /opt/ansible

