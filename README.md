# Ansible LAMP Stack Playbook with Wordpress

Ansible playbook and roles for installing Apache2, Mysql, Php and Wordpress.

## Requirements:

- Ansible 2.0
- Ubuntu 16.04. (The vagrantfile already has Ubuntu bionic set for this).

## Instructions

### 1. Configure your web server for ssh
You can run this any way you like. You could run everything inside a vagrant machine or you could run the ansible playbook from your development machine.
For ansible to work from your development machine, you need to set your remote server to allow connections using ssh. Inside the Vagrantfile, the private network ip is set
therefore it can be used as the host address.
To allow ssh connections, you can use `ssh-copy-id` to share keys. After this, you only need to run `ssh [IP ADDRESS]`. If you will be using a vagrant machine, you will need
to use a vagrant prefix followed by the IP address.

### 2. Clone the Repo
```
`git clone git@github.com:natalie-elizabeth/LAMP-ansible.git`
```
### 3. Run the playbook
While inside the vagrant machine run `ansible-playbook playbook.yml` and `ansible-playbook playbook.yml -i hosts` from outside the application
```
To view the application on the browser go to `http://[IP_ADDRESS]`
```
