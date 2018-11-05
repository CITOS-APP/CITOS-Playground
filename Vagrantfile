# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "local" do |local|
    local.vm.hostname = "local"
    local.vm.box = "ubuntu/bionic64"
    local.vm.network "private_network", ip: "192.168.99.50"
    #local.vm.network :forwarded_port, guest: 3000, host: 3000
    local.vm.provision "shell", path: "provision.sh"
    local.vm.synced_folder "sync_dir/", "/home/vagrant/test"
    local.ssh.forward_agent = true
    local.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
    
  end

#  config.vm.network "private_network", ip: "192.168.99.10"
#  config.vm.network :forwarded_port, guest: 8000, host: 8000
#  config.vm.network :forwarded_port, guest: 8001, host: 8001
#  config.vm.network :forwarded_port, guest: 8080, host: 8080
#  config.vm.network :forwarded_port, guest: 8443, host: 8443
#  config.vm.network :forwarded_port, guest: 8444, host: 8444

 config.vm.define "db" do |db|
    db.vm.hostname = "db"
    db.vm.box = "ubuntu/bionic64"
    db.vm.network "private_network", ip: "192.168.99.100"
    #db.vm.network :forwarded_port, guest: 8000, host: 8000
    db.vm.provision "shell", path: "provision.sh"
    db.vm.synced_folder "sync_dir/", "/home/vagrant/test"
    db.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
    end
    
  end

end