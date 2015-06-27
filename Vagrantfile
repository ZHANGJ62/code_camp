Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty32"
  config.vm.hostname = "codecamp"
  config.vm.synced_folder "./", "/home/vagrant"
  config.vm.network "forwarded_port", guest: 8100, host: 8100
  config.vm.network "forwarded_port", guest: 35729, host: 35729
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y git nodejs nodejs-legacy npm git
    sudo npm install -g cordova ionic bower
  SHELL
end
