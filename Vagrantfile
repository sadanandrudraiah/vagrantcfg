# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.box_check_update = false
  
  config.vm.provider :virtualbox do |vb|
   vb.customize ["modifyvm", :id, "--memory", "256"]
  end

# Controller.
 config.vm.define "controller" do |cont|
	cont.vm.hostname = "controller.dev"
	cont.vm.box = "geerlingguy/centos7"
	config.vm.network "public_network"
 end

# App server.
 config.vm.define "app1" do |app|
	app.vm.hostname = "app1.dev"
	app.vm.box = "geerlingguy/centos7"
	config.vm.network "public_network"
 end
 
end 
