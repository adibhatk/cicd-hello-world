Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    
    config.vm.network "forwarded_port", guest: 8080, host: 8080
  
    config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "jenkins"
      vb.cpus = 2
      vb.memory = "4096"
    end
    
    config.vm.provision "shell" do |shell|
      shell.path = "vagrant/jenkins.sh"
    end
  end
