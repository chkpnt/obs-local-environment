Vagrant.configure("2") do |config|
    config.vm.box = "Tumbleweed.x86_64"
    config.vm.box_url = "https://download.opensuse.org/repositories/Virtualization:/Appliances:/Images:/openSUSE-Tumbleweed/openSUSE_Tumbleweed/boxes/Tumbleweed.x86_64.json"

    config.vm.provision :ansible do |ansible|
        ansible.force_remote_user = true
        ansible.compatibility_mode = "2.0"
        ansible.verbose = true
        ansible.playbook = "provisioning/playbook.yml"
        ansible.extra_vars = "provisioning/credentials.yml"
        ansible.config_file = "provisioning/ansible.cfg"
    end

    config.vm.provider "virtualbox" do |vb|
        vb.memory = 4096
        vb.cpus = 2
    end
end
