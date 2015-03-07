# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 3000, host: 3030
  config.vm.synced_folder "myrailsprojects", "/home/vagrant/myrailsprojects/"
  config.vm.provision "puppet" do |puppet|
    puppet.manifests_path = "provision/manifests"
    puppet.manifest_file  = "site.pp"
    puppet.module_path = "provision/modules"
  end
  config.vm.hostname = "vagrant.example.com"
end
