# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # vagrant plugin install vagrant-disksize
  config.disksize.size = '40GB'
  
  # empty vm with net boot as default
  config.vm.box = "sridhav/empty"

  config.vm.synced_folder ".", "/vagrant", type: 'virtualbox'
  
  config.vm.provider :virtualbox do |vb|
    
    vb.name = "pxe-client"
    vb.memory = "2048"
    vb.gui = true
    
    # vb.boot = "net"
    # clientes com no minimo 2048 MB de RAM
    # vboxmanage modifyvm vm-pxe-teste --boot1 net --boot2 disk --boot3 none --boot4 none #
    # rede do cliente deve apontar para mesma rede do SERVER Network > Host-only adapter > vboxnetXX
  end

	config.vm.define 'pxe-client' do |s|
		s.vm.hostname = "pxe-client.hans.lan"
	end
end
