# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "ansible-server" do |node|
    node.vm.hostname = "ansible-server"
    node.vm.box = "boxcutter/centos72"
    node.vm.network :private_network, ip: "192.168.66.61"
    node.vm.synced_folder "./quick_master_provision", "/quick_master_provision", :mount_options => ['dmode=775', 'fmode=664']
    node.vm.provision "shell", inline: <<-SHELL
      sudo yum -y install epel-release
      sudo yum -y --enablerepo=epel install ansible
      sudo yum -y update
    SHELL
  end

  config.vm.define "www-server" do |node|
    node.vm.hostname = "www-server"
    node.vm.box = "boxcutter/centos72"
    node.vm.network :private_network, ip: "192.168.66.62"
    node.vm.provision "shell", inline: <<-SHELL
      sudo yum -y install epel-release
      sudo yum -y update
    SHELL
  end

end
