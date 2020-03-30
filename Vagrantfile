# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.box_check_update = false
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.synced_folder "../data", "/vagrant_data"
  config.vm.provision "shell", inline: <<-SHELL
    yum install -y -q wget mailx
    echo "salut $(cat /vagrant/quijesuis)"
    echo ""
    echo "      (s'il n'y a pas ton nom la t'es mal)"
    echo ""
    echo "attends je t'evalue"
    echo ""
    wget -qO - http://learnlinux.fr/scr/evalvag | bash
  SHELL
end
