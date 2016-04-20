Global Average Temperatures Over 200 Years

This is an automated deployment of a web app built using [Caravel](https://github.com/airbnb/caravel) to visualize average temperature readings for major global cities since 1750. The data set comes from user Berkeley Earth on [Kaggle](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data)
This build utilizes Vagrant for virtualization and Ansible for provisioning.

Required:
-Vagrant
-VirtualBox

If using Windows:
-[Vagrant-Ansible Plugin](https://github.com/vovimayhem/vagrant-guest_ansible)
-Cygwin

Installation Instructions:
In your directory
>`vagrant up`

When Ansible completes provisioning
> `vagrant ssh`

This will load the app
> `sudo caravel runserver`

Navigate to
>localhost:8080
