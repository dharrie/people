Vagrant.configure("2") do |config|

  config.vm.box = "trusty64"
  config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.network :forwarded_port, guest: 8080, host: 8080  #webpack-dev-server

  config.vm.synced_folder "", "/vagrant", disabled: true
  config.vm.synced_folder "", "/var/src"

  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.cpus = 2
  end

  config.vm.provision "shell", path: "./provisioning/bootstrap.sh"
end