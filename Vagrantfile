# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.require_version ">= 1.4.3"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  memory = 1024

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider :virtualbox do |vb|
   vb.name = "vagrant_kong"
   vb.memory = memory
  end

  config.vm.box = "hashicorp/precise64"

  # config.vm.network :forwarded_port, guest: 5432, host: 15432
  # config.vm.network :forwarded_port, guest: 8000, host: 18000
  # config.vm.network :forwarded_port, guest: 8001, host: 18001
  # config.vm.network :forwarded_port, guest: 8443, host: 18443

  config.vm.provision "shell", path: "provision.sh"

  # FIXME: remove this from here to a init.d script
  config.vm.provision "shell", inline: "kong start", run: "always"

end

