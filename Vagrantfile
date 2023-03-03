Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04-arm64"
  config.vm.hostname = "ubuntu"
  # config.vm.network "private_network", type: "dhcp"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.provider "parallels"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "./ansible/provision.yml"
    ansible.compatibility_mode = "2.0"
  end
end