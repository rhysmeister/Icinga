Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "192.168.44.127"
  config.vm.hostname = "icinga"
  config.vm.provider :virtualbox do |vbox|
    vbox.linked_clone = true
    vbox.name = "icinga"
    vbox.memory = 2048
    vbox.cpus = 1
  end
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "icinga.yaml"
  end
end
