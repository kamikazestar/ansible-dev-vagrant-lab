VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Use the same key for each machine
  config.ssh.insert_key = false

  config.vm.define "centos8" do |centos8|
    centos8.vm.box = "centos/8"
    centos8.vm.hostname = "centos8"
    centos8.vm.network "private_network", ip: "192.168.123.10", netmask: "255.255.255.0"
    centos8.vm.provider "virtualbox" do |vb|
      vb.name = "centos8.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #centos8.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end

  config.vm.define "centos7" do |centos7|
    centos7.vm.box = "centos/7"
    centos7.vm.hostname = "centos7"
    centos7.vm.network "private_network", ip: "192.168.123.11", netmask: "255.255.255.0"
    centos7.vm.provider "virtualbox" do |vb|
      vb.name = "centos7.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #centos7.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end

  config.vm.define "fedora31" do |fedora31|
    fedora31.vm.box = "fedora/31-cloud-base"
    fedora31.vm.hostname = "fedora31"
    fedora31.vm.network "private_network", ip: "192.168.123.12", netmask: "255.255.255.0"
    fedora31.vm.provider "virtualbox" do |vb|
      vb.name = "fedora31.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #fedora31.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end

  config.vm.define "fedora30" do |fedora30|
    fedora30.vm.box = "fedora/30-cloud-base"
    fedora30.vm.hostname = "fedora30"
    fedora30.vm.network "private_network", ip: "192.168.123.13", netmask: "255.255.255.0"
    fedora30.vm.provider "virtualbox" do |vb|
      vb.name = "fedora30.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #fedora30.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end

  # Amazon Linux 2 currently won't be supported
  # TODO: Support for Amazon Linux 2
  #config.vm.define "amznlinux2" do |amaznliux2|
  #  amznlinux2.vm.box = "centos/8"
  #  amznlinux2.vm.hostname = "amznlinux2"
  #  amznlinux2.vm.network "private_network", ip: "192.168.123.14", netmask: "255.255.255.0"
  #  amznlinux2.vm.provider "virtualbox" do |vb|
  #    vb.name = "amznlinux2.ansible-dev.local"
  #    vb.customize [
  #      "modifyvm", :id,
  #      "--groups", "/ansible-dev.local",
  #      "--memory", "512",
  #      "--cpus", "1"
  #    ]
  #  end
  #  # This section can provision custom configuration for the node like i.e. ntp or user account
  #  #amznlinux2.vm.provision :ansible do |ansible|
  #  #  #ansible.ask_vault_pass = true
  #  #  ansible.compatibility_mode = "2.0"
  #  #  ansible.playbook = "bootstrap.yml"
  #  #end
  #end

  config.vm.define "ubuntu1804" do |ubuntu1804|
    ubuntu1804.vm.box = "ubuntu/bionic64"
    ubuntu1804.vm.hostname = "ubuntu1804"
    ubuntu1804.vm.network "private_network", ip: "192.168.123.15", netmask: "255.255.255.0"
    ubuntu1804.vm.provider "virtualbox" do |vb|
      vb.name = "ubuntu1804.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #ubuntu1804.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end

  config.vm.define "ubuntu1604" do |ubuntu1604|
    ubuntu1604.vm.box = "ubuntu/xenial64"
    ubuntu1604.vm.hostname = "ubuntu1604"
    ubuntu1604.vm.network "private_network", ip: "192.168.123.16", netmask: "255.255.255.0"
    ubuntu1604.vm.provider "virtualbox" do |vb|
      vb.name = "ubuntu1604.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #ubuntu1604.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end

  config.vm.define "debian10" do |debian10|
    debian10.vm.box = "debian/buster64"
    debian10.vm.hostname = "debian10"
    debian10.vm.network "private_network", ip: "192.168.123.17", netmask: "255.255.255.0"
    debian10.vm.provider "virtualbox" do |vb|
      vb.name = "debian10.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #debian10.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end
  
  config.vm.define "debian9" do |debian9|
    debian9.vm.box = "debian/stretch64"
    debian9.vm.hostname = "debian9"
    debian9.vm.network "private_network", ip: "192.168.123.18", netmask: "255.255.255.0"
    debian9.vm.provider "virtualbox" do |vb|
      vb.name = "ubuntu1804.ansible-dev.local"
      vb.customize [
        "modifyvm", :id,
        "--groups", "/ansible-dev.local",
        "--memory", "512",
        "--cpus", "1"
      ]
    end
    # This section can provision custom configuration for the node like i.e. ntp or user account
    #debian9.vm.provision :ansible do |ansible|
    #  #ansible.ask_vault_pass = true
    #  ansible.compatibility_mode = "2.0"
    #  ansible.playbook = "bootstrap.yml"
    #end
  end
end
