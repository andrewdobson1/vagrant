# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "gyptazy/ubuntu22.04-arm64"

  #config.vm.network "forwarded_port", guest: 5672, host: 5672       # Rabbitmq
  #config.vm.network "forwarded_port", guest: 15672, host: 15672     # Rabbitmq dashboard
  #config.vm.network "forwarded_port", guest: 4000, host: 4000
  #config.vm.network "forwarded_port", guest: 4001, host: 4001
  #config.vm.network "forwarded_port", guest: 4002, host: 4002
  config.vm.network "forwarded_port", guest: 8001, host: 8001 # For the Kubernetes dashboard.

  config.vm.synced_folder "/Users/andrewdobson/Projects", "/projects"

  config.vm.provision "shell", path: "./scripts/provision-dev-vm.sh"
end
