Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"

  config.vm.hostname = "lemp"
  config.vm.network "private_network", ip: "192.168.50.5"

  config.vm.synced_folder "drupal/", "/var/www/sites/drupal.dev/www"

  # Needed to match the hosts.
  config.vm.define :lemp do |lemp|
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.sudo = true
  end
end
