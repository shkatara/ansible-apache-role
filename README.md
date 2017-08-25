# ansible-apache-role

This role works with ansible version 2.3.1.0 or above. 

This is the ansible role used for:
1. Installing httpd server on a number of hosts.
2. Starting the service.
3. Enabling the service.
4. Configuring a virtual host from a jinja2 template. 
5. Initializing the document root with a bare index.html file.
6. Opening ports and allowing services in firewalld. 

How to use:
===========
1. Insert the IP or hostname of nodes to be managed in the "inv" file. 
2. Insert the files and folders required to be present at the document root of your apache web server on managed hosts in ansible-role-httpd-service/files/html/ directory. 
3. Setup passwordless ssh in systems or keep password same for all the managed hosts. While running playbook, ansible will ask for password and it will use the same password once given for all the nodes. 
4. Run the apache_playbook.yml file with --become or -b option for making use of escalated privileges.
5. Relax.
