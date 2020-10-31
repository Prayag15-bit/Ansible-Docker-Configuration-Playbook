# Ansible Playbook for Docker Configuration
Hello everyone, in this repository, I created an Ansible Playbook to configure Docker Engine in a Linux Operating System

# Pre-requisites to run the Playbook
Before running the Playbook, make sure that Ansible is installed in your Linux Operating system
If you want to install and configure Ansible in your system, follow these steps :-
1. Go to the Terminal and type this command : *pip3 install ansible*

2. Now, confirm the installation of ansible by using the command : *ansible --version*

3. After confirming the installation, it's time to configure your INVENTORIES

4. Go to the Terminal and use this command to create a text file : touch /etc/<text_file_name>.txt

5. Open the text file using any text editor (vi/vim/gedit) and add this syntax as shown below :-
<IP_of_the_system_to_be_configured>   ansible_ssh_user=root   ansible_ssh_pass=<root_account_password>

Eg:- *1.2.3.4  ansible_ssh_user=root  ansible_ssh_pass=1234*

6. Now, open the ansible configuration file using the text editor and add the content :-

[defaults]

inventory = /etc/<text_file_name>.txt

# After doing everything right, your system is ready to use Ansible

# How to run the Playbook :-
1. First, open the text file (/etc/<text_file_name>.txt) and update the IP of the system you want to configure through Ansible
2. Make sure you have the proper connectivity with the system you want to configure. You can check the connectivity using this command : *ansible all -m ping*
3. Create an empty directory in your system : *mkdir /root/<your_directory_name>*
4. Go inside the directory using the command : *cd /root/<your_directory_name>*
5. Now, clone the repository using the command : *git clone https://github.com/Prayag15-bit/Ansible_task_1.git*
6. After cloning the code, run the playbook using the command : *ansible-playbook <playbook_name>*
7. Now, wait for the playbook to be executed completely

# BOOM!! After complete execution, you can check the other system that Docker is configured. Also, this playbook will create a container with the name *php-interpreter* with a Docker Image configured to be a webserver, and also will be exposed to the outside world. If you want to see the hosted webpage, go to your web browser and type like this:-

*<IP_of_the_configured_system>:85/php_code.php*

# In case of any difficulty, you can refer the below artice to take reference :-

<https://www.linkedin.com/pulse/using-ansible-integrate-docker-linux-prayag-magotra/>
