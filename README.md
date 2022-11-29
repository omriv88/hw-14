# hw-14

1. Write a tasks file that installs vim and zip on the servers:

root@:~/# git clone https://github.com/omriv88/hw-14.git

root@:~/# cat install/tasks/main.yml


---
- name: install Zip and vim
apt: name=vim,zip state=present
.     
 
 
 
 
 

2) Write an ansible role called common that uses the role from task 1 
   root@root:~/# cat config.yml
   ---
   - hosts: servers

     roles:
       - install
   

3) Write a playbook to call your role from the main directory:
    ansible-playbook config.yml
 
4) Challenge:
4.1) Create a task deploys a file with the following content to /tmp/test1 in all
      hosts(Hello world!):
      
      
      
   
   4.2)  Create a role that deploys a template with the following content to /tmp/test2 in all
         hosts:
         (https://github.com/omriv88/hw-14/blob/main/template.yml)
          ---
          - hosts: servers
            serial: 1
            tasks:

            - name: Get hostname
              template:
                  src: hostname.j2
                  dest: /var/tmp/hostname.conf

 
 
 
  
