## Global Average Temperatures

This is an automated deployment of a web app built using [Caravel](https://github.com/airbnb/caravel) to visualize average temperature readings for major global cities since 1750. 

The data set comes from user Berkeley Earth on [Kaggle](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data) and has been uploaded into a sqlite database.

This build utilizes Vagrant for virtualization and Ansible for provisioning. 

### Required:
- [Vagrant](https://www.vagrantup.com/)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Vagrant-Ansible Plugin](https://github.com/vovimayhem/vagrant-guest_ansible)

###### For running on Windows:
- [Cygwin](https://www.cygwin.com/)

### Installation Instructions:
1. Navigate to your directory and enter
>`vagrant up`

2. When build is complete, enter
> `vagrant ssh`

3. Load the app by entering
> `sudo caravel runserver`

4. In your browser, navigate to
>localhost:8080

5. Login with 
>- Username: admin
>- Password: password

### Known Issues:
- This build of Caravel is not connecting to the .db file properly, meaning Caravel loads as a blank slate.
- Automating the last step (running the server) causes Ansible to enter an infinite loop, so additional installation instructions were added above as a workaround.
- Using a local install of Ansible instead of the linked plugin causes issues with provisioning.
- Tests coming soon
