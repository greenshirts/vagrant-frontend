# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.29.92"
  # config.vm.network "public_network"
  config.vm.synced_folder "host_synced", "/home/vagrant/host_synced"
  config.vm.synced_folder ".", "/home/vagrant/sync", disabled: true
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "1024"
  end
  config.vm.provision :shell, path: "bootstrap.sh"
end
