# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "puppet"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 90, host: 8090
  config.vm.network "forwarded_port", guest: 443, host: 8443

  config.vm.provision "shell",
    inline: "sudo /usr/local/bin/restart_pe_services.rb all -f"
end
