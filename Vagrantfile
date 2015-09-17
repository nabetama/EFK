# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.define :node1 do |node|
    node.vm.box = "CentOS-6.5-x86_64"
    node.vm.network :forwarded_port,  guest: 22,  host: 2001,  id: "ssh"
    node.vm.network :private_network,  ip: "192.168.33.11"
  end

  config.vm.define :node2 do |node|
    node.vm.box = "CentOS-6.5-x86_64"
    node.vm.network :forwarded_port, guest: 22, host: 2002, id: "ssh"
    node.vm.network :forwarded_port, guest: 80, host: 8000, id: "http"
    node.vm.network :forwarded_port, guest: 9200, host: 9200, id: "elasticsearch"
    node.vm.network :private_network, ip: "192.168.33.12"
  end
end
