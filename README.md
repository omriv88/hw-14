# hw-14

Tasks:


- 1. Write a tasks file that installs vim and zip on the servers:

  - root@:~/# git clone https://github.com/omriv88/hw-14.git

  - root@:~/# cat install/tasks/main.yml


- 2. Write an ansible role called common that uses the role from task 1:

  - root@:~/# cat config.yml


- 3. Write a playbook to call your role from the main directory:

  - ansible-playbook config.yml





- 4. Challenge:




  - 4.1. Create a task deploys a file with the following content to /tmp/test1 in all hosts "Hello world!":

    - root@:~/# cat copyfile/tasks/main.yml

    - root@:~/# ansible-playbook configcp.yml


- 4.2. Create a role that deploys a template with the following content to /tmp/test2 in all hosts "This servers conteiner is: <the server’s hostname>":

  - root@:~/# cat template.yml

    - run the template:

    - root@:~/# ansible-playbook template.yml

  
