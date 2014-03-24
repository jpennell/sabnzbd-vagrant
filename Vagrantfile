Vagrant.require_plugin "vagrant-berkshelf"
Vagrant.require_plugin "vagrant-omnibus"

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "precise64"
  config.omnibus.chef_version = :latest
  config.berkshelf.enabled = true

  config.vm.network "forwarded_port", guest: 6000, host: 5000

  config.vm.provision :chef_solo do |chef|
    chef.add_recipe "sabnzbd"
  end

end
