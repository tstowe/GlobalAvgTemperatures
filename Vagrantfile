# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version, unedited
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # The Vagrant configuration below builds a commonly used box known as "Trusty64".
  # The box runs Ubuntu 14.04.4 LTS
  config.vm.define :web do |web_config|
      web_config.vm.box = "ubuntu/trusty64"
      web_config.vm.hostname = "web"
	  #This sets the VM to local host 8080 so we can see the finished product on our web browser.
	  web_config.vm.network "forwarded_port", guest: 8088, host: 8080
	  web_config.vm.network :private_network, ip: "10.0.15.10"
      web_config.vm.provider "virtualbox" do |vb|
		vb.memory = "2048"
	  end
	end  
  # This checks if you are running Vagrant from a Windows machine.
  # Thanks to a plugin from Git user "vovimayhem", we are able to run Ansible Provisioning from Vagrant 
  # inside the guest machine in the case you're using Windows like me.
  
	if Vagrant::Util::Platform.windows?
		config.vm.provision :guest_ansible do |ansible|
			ansible.playbook = "playbook.yml"
			ansible.sudo = true
			ansible.verbose = true
		end
	else
		config.vm.provision "ansible" do |ansible|
		    ansible.verbose = true
			ansible.playbook = "playbook.yml"
			ansible.sudo = true
		end
    end
	  
end
