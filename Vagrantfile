Vagrant.configure("2") do |config|
  config.vm.box = "bento/centos-7.1"
  config.vm.network "private_network", type: "dhcp"
  config.omnibus.chef_version = :latest
  config.vm.provision :chef_client do |chef|
    chef.provisioning_path = "/etc/chef"
    chef.chef_server_url = "https://api.chef.io/organizations/innocore"
    chef.validation_key_path = ".chef/muthulaksh.pem"
    chef.validation_client_name = "muthulaksh"
    chef.node_name = "centos-server"
  end
end
