# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"

  config.vm.define "host1" do |host1|
    host1.vm.network "private_network", ip: "192.168.0.10"
  end
  
  config.vm.define "host2" do |host2|
    host2.vm.network "private_network", ip: "192.168.0.11"
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/mesos.yml"
  end

end

