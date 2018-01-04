# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_url = "../trusty_amd64.box"
  config.vm.host_name = "postgresql" 

  config.vm.provision :shell, :path => "bootstrap.sh"
  
  # PostgreSQL Server port forwarding
  config.vm.network :forwarded_port, guest: 5432, host: 15432
end
