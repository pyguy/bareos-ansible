# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define :bareos_ubuntu_server do |bareos_ubuntu_server|
    bareos_ubuntu_server.vm.box = "ubuntu/bionic64"
    bareos_ubuntu_server.vm.hostname = "bareos-ubuntu-server"
    bareos_ubuntu_server.vm.network :private_network, ip: "172.20.17.10"
  end
  config.vm.define :bareos_centos_server do |bareos_centos_server|
    bareos_centos_server.vm.box = "centos/7"
    bareos_centos_server.vm.hostname = "bareos-centos-server"
    bareos_centos_server.vm.network :private_network, ip: "172.20.17.11"
  end
  config.vm.define :bareos_ubuntu_client do |bareos_ubuntu_client|
    bareos_ubuntu_client.vm.box = "ubuntu/bionic64"
    bareos_ubuntu_client.vm.hostname = "bareos-ubuntu-client"
    bareos_ubuntu_client.vm.network :private_network, ip: "172.20.17.12"
  end
  config.vm.define :bareos_centos_client do |bareos_centos_client|
    bareos_centos_client.vm.box = "centos/7"
    bareos_centos_client.vm.hostname = "bareos-centos-client"
    bareos_centos_client.vm.network :private_network, ip: "172.20.17.13"
  end
  config.vm.provision "shell", path: "./vagrant/provision.sh"
end
