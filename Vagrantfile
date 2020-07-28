Vagrant.configure("2") do |config|

# config.vm.provider "virtualbox" do |v|
 #   v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  #  v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
 #end

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.10.100"
  config.hostsupdater.aliases = ["development.local"]


  # sync folder from your OS to VM
  config.vm.synced_folder ".", "/home/vagrant/app"  
  # automating the nginx install
  config.vm.provision "shell", path: "environment/provision.sh"
end
