# -*- mode: ruby -*-
# vi: set ft=ruby :

#Parte 1 - Vagrant

Vagrant.configure("2") do |config|
  config.vm.box = "roboxes/ubuntu2204"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "ThiagoSouza"
    vb.gui = false
    vb.memory = "1024"
  end
  config.vm.network "private_network", ip: "192.168.57.10"
  config.vm.hostname = "ThiagoSouza"
  
  # Configuracao para chamar o Ansible

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook_ansible.yml"
  end
end
  
