Vagrant.configure("2") do |config|
    # Use the lightweight Ubuntu Minimal box
    config.vm.box = "ubuntu/bionic64"
    config.vm.box_check_update = false
    config.vm.hostname = "Mac-Server"

    config.vm.network "forwarded_port", guest: 80, host: 9998, host_ip: "127.0.0.1"
    
  
    config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.cpus = 1
      vb.memory = "512"
    end
  
    # Provisioning: install Apache server
    config.vm.provision "shell", path: "provision/script.sh"
  end


# Vagrant.configure("2") do |config|
# config.vm.box = "ubuntu/bionic64"
# config.vm.box_check_update = false
# config.vm.hostname = "Lightweight-Server"
# config.vm.network "forwarded_port", guest: 80, host: 5558, host_ip: "127.0.0.1"
# config.vm.provider "virtualbox" do |vb|
#     vb.gui = false
#     vb.cpus = 1
#     vb.memory = "512"
# end
# config.vm.provision "shell", inline: <<-SHELL
#     apt-get update
#     apt-get install -y apache2
# SHELL
# end

# Vagrant.configure("2") do |cfg|
#     cfg.vm.define "server" do |config|
#       config.vm.box = "ubuntu/bionic64"
#       config.vm.hostname = "Mac-Server"
#       config.vm.provider :virtualbox do |v, override|
#          v.gui = false 
#          v.cpus = 2
#          v.memory = 2048
#       end
  
#       config.vm.network :private_network,
#           :ip => 172.16.2.101
#       config.vm.network :private_network,
#           :ip => 10.10.10.101
#       #Run script
#       config.vm.provision "shell", path: "provision/script.sh"
#     end



# Vagrant.configure("2") do |config|
#     config.vm.box = "ubuntu/focal64"
#     config.vm.box_check_update = false
  
#     # Create a forwarded port mapping which allows access to a specific port
#     # within the machine from a port on the host machine. In the example below,
#     # accessing "localhost:8080" will access port 80 on the guest machine.
#     # NOTE: This will enable public access to the opened port
#     config.vm.network "forwarded_port", guest: 80, host: 8080
  
#     # Create a forwarded port mapping which allows access to a specific port
#     # within the machine from a port on the host machine and only allow access
#     # via 127.0.0.1 to disable public access
#     config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  
#     # Create a private network, which allows host-only access to the machine
#     # using a specific IP.
#     config.vm.network "private_network", ip: "192.168.33.10"
  
#     # Create a public network, which generally matched to bridged network.
#     # Bridged networks make the machine appear as another physical device on
#     # your network.
#     config.vm.network "public_network"
  
  
#     config.vm.provider "virtualbox" do |vb|
#       # Display the VirtualBox GUI when booting the machine
#       vb.gui = true
    
#       # Customize the amount of memory on the VM:
#       vb.memory = "1024"
#     end

#     config.vm.provision "shell", inline: <<-SHELL
#       apt-get update
#       apt-get install -y apache2
#     SHELL
#   end
  

