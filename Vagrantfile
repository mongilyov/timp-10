# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "virtualMachine1" do |virtualMachine1|
    virtualMachine1.vm.box = "bento/ubuntu-22.04-arm64"
    virtualMachine1.vm.hostname = 'virtualMachine1'
  end

  config.vm.define "virtualMachine2" do |virtualMachine2|
    virtualMachine2.vm.box = "bento/ubuntu-22.04-arm64"
    virtualMachine2.vm.hostname = 'virtualMachine2'
    #virtualMachine2.vm.network "forwarded_port", guest: 8000, host: 7887
  end

  #config.ssh.private_key_path = "~/.ssh/id_rsa"
  config.ssh.forward_agent = true
end
