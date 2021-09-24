Vagrant.configure("2") do |config|
    # Ubunut image
    config.vm.box = "generic/ubuntu2004"
  
    # VM settings
    config.vm.provider :vmware_desktop do |vmware|
      vmware.utility_certificate_path = "/opt/vagrant-vmware-desktop/certificates"
      vmware.cpus = "2"
      vmware.memory = "4096"
    end
  
    # Run ansible playbook
    config.vm.provision "ansible" do |ansible|
    ansible.playbook = "deploy_fleetdm.yml"
        ansible.inventory_path = ".vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory"
        ansible.extra_vars = {
            variable_host: "default"
        }

  end
  end