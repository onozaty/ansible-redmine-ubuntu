Vagrant.configure(2) do |config|
  config.vm.box = "bento/ubuntu-20.04"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.synced_folder ".", "/vagrant/ansible-redmine-ubuntu", create: true, mount_options: ['dmode=755','fmode=655']
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get install software-properties-common
    sudo apt-add-repository --yes --update ppa:ansible/ansible
    sudo apt-get install -y ansible git

    cd /vagrant/ansible-redmine-ubuntu

    sudo ansible-playbook -i hosts playbook.yml
  SHELL
end
