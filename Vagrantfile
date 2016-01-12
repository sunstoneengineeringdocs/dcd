Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise32"
  config.vm.box_download_insecure = "true"
  config.vm.network :forwarded_port, host: 4000, guest: 4000
  config.vm.provision :shell,
    :inline => "sudo apt-get update && sudo apt-get -y install build-essential git ruby2.0.0 && sudo gem install jekyll --no-ri --no-rdoc"
  config.vm.provision :shell,
  	:inline => "cd /vagrant && jekyll serve --watch "
end