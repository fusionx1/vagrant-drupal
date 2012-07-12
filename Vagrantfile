Vagrant::Config.run do |config|
  config.vm.box = "base-lucid32"
  config.vm.box_url = "http://files.vagrantup.com/lucid32.box"

  config.vm.customize ["modifyvm", :id, "--memory", "1024"]

  config.vm.network :hostonly, "33.33.33.33"

  config.vm.share_folder("web", "/var/www", "web")

 config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file = "default.pp"
    puppet.module_path = "modules"
  end

end
