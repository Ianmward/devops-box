Vagrant.configure(2) do |config|
#    config.vm.synced_folder "D:/", "/usb"
	config.vm.define "devops-box" do |devbox|
		devbox.vm.box = "ubuntu/xenial64"
    		devbox.vm.network "private_network", ip: "192.168.199.9"
    		#devbox.vm.hostname = "devops-box"
      		devbox.vm.provision "shell", path: "scripts/install.sh"
    		devbox.vm.provider "virtualbox" do |v|
    		  v.memory = 8192
    		  v.cpus = 2
    		end
	end
	
	config.disksize.size = "50GB"
end
