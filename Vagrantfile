# Vagrantfile
Vagrant.configure("2") do |config|
    config.vm.box = "debian-sandbox/bookworm64"
    config.vm.network "forwarded_port", guest: 80, host: 8080
  
    config.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "docker_setup.yml"
      ansible.extra_vars = { ansible_python_interpreter: "/usr/bin/python3" }
    end
  end
  