# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define 'ns01' do |ns01|
    ns01.vm.box = 'centos/stream8'
    ns01.vm.host_name = 'ns01'
   # Add network
    ns01.vm.network "forwarded_port", guest: 22, host: 2210, protocol: "tcp"
    ns01.vm.network "private_network", ip: '192.168.50.10', virtualbox__intnet: 'dns'
    # Change memory size
    ns01.vm.provider :virtualbox do |vb|
      vb.memory = 1024
    end
  end
end

Vagrant.configure("2") do |config|

  config.vm.define 'ns02' do |ns02|
    ns02.vm.box = 'centos/stream8'
    ns02.vm.host_name = 'ns02'
    # Add network
    ns02.vm.network "forwarded_port", guest: 22, host: 2211, protocol: "tcp"
    ns02.vm.network "private_network", ip: '192.168.50.11', virtualbox__intnet: 'dns'
    # Change memory size
    ns02.vm.provider :virtualbox do |vb|
      vb.memory = 1024
    end
  end
end

Vagrant.configure("2") do |config|

  config.vm.define 'cl01' do |cl01|
    cl01.vm.box = 'centos/stream8'
    cl01.vm.host_name = 'cl01'
   # Add network
    cl01.vm.network "forwarded_port", guest: 22, host: 2215, protocol: "tcp"
    cl01.vm.network "private_network", ip: '192.168.50.15', virtualbox__intnet: 'dns'
    # Change memory size
    cl01.vm.provider :virtualbox do |vb|
      vb.memory = 1024
    end
  end
end

Vagrant.configure("2") do |config|

  config.vm.define 'cl02' do |cl02|
    cl02.vm.box = 'centos/stream8'
    cl02.vm.host_name = 'cl02'
    # Add network
    cl02.vm.network "forwarded_port", guest: 22, host: 2216, protocol: "tcp"
    cl02.vm.network "private_network", ip: '192.168.50.16', virtualbox__intnet: 'dns'
    # Change memory size
    cl02.vm.provider :virtualbox do |vb|
      vb.memory = 1024
    end
  end
end
