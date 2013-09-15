Vagrant.configure("2") do |config|
  config.vm.provision :shell, :inline => "echo Hello"

  config.vm.define :web1 do |web1|
    web1.vm.box = "precise64"
    web1.vm.network :private_network, ip: "192.168.2.2"
  end

  config.vm.define :web2 do |web2|
    web2.vm.box = "precise64"
    web2.vm.network :private_network, ip: "192.168.2.3"
  end

  config.vm.define :db do |db|
    db.vm.box = "precise64"
    db.vm.network :private_network, ip: "192.168.2.4"
  end
end
