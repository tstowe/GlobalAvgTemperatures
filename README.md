Global Average Temperatures Over 200 Years

This is an automated deployment of the open source web app, Caravel (https://github.com/airbnb/caravel), to visualize average temperature readings for major global cities since 1750. 
This build utilizes Vagrant for virtualization and Ansible for provisioning.

Required:
Vagrant
VirtualBox

Vagrant-Ansible Plugin (https://github.com/vovimayhem/vagrant-guest_ansible)

Installation Instructions:
Navigate to the directory in your terminal and enter 
“vagrant up”

When Ansible completes provisioning, Enter 
“vagrant ssh”

This will load the dashboard
Enter
“Sudo caravel runserver -d”

Navigate to
Localhost:8080
