Vagrant.configure("2") do |config|
    config.vm.box = "Leap-15.1.x86_64"
    config.vm.box_url = "https://download.opensuse.org/repositories/Virtualization:/Appliances:/Images:/openSUSE-Leap-15.1/images/boxes/Leap-15.1.x86_64.json"

    config.vm.provision :ansible do |ansible|
        ansible.force_remote_user = true
        ansible.compatibility_mode = "2.0"
        ansible.verbose = true
        ansible.playbook = "provisioning/playbook.yml"
        ansible.extra_vars = "provisioning/credentials.yml"
    end
end
