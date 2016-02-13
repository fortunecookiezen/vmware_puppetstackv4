# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
 config.vm.boot_timeout = 600
 config.vm.define "puppet" do |puppet|
  puppet.vm.box = "box-cutter/centos67"
  puppet.vm.hostname = 'puppet'
  puppet.vm.network :private_network, ip: "192.168.100.15"
  puppet.vm.provider "vmware_workstation" do |v|
    v.vmx["memsize"] = "2048"
  end
 end

 config.vm.define "client" do |client|
  client.vm.box = "box-cutter/centos67"
  client.vm.hostname ='client'
  client.vm.network :private_network, ip: "192.168.100.16"
  client.vm.provider "vmware_workstation" do |v|
    v.vmx["memsize"] = "512"
  end
 end
end
