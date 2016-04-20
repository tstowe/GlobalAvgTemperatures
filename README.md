Global Average Temperatures Over 200 Years

This is an automated deployment of a web app built using [Caravel](https://github.com/airbnb/caravel) to visualize average temperature readings for major global cities since 1750. The data set comes from user Berkeley Earth on [Kaggle](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data)
This build utilizes Vagrant for virtualization and Ansible for provisioning.

Required:
Vagrant
VirtualBox

If using Windows:
[Vagrant-Ansible Plugin](https://github.com/vovimayhem/vagrant-guest_ansible)
Cygwin

Installation Instructions:
Navigate to the directory in your terminal and enter 
`vagrant up`



When Ansible completes provisioning, Enter 
`vagrant ssh`

This will load the dashboard, then Enter
`sudo caravel runserver`

Navigate to
Localhost:8080
