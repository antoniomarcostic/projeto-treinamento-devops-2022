Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "public_network", ip: "10.1.1.88", bridge: "Realtek PCIe Gbe Family Controller #2"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.synced_folder "../data", "/vagrant_data"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "DESAFIO-01"
  end

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y vim curl telnet unzip wget net-tools htop nmap nginx
    adduser --home /home/antonio antonio
   SHELL
end
