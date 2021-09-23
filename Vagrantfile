Vagrant.configure("2") do |config|
  #config.hostmanager.enabled = true
  #config.hostmanager.manage_host = true
  #config.hostmanager.manage_guest = true
  #config.hostmanager.ignore_private_ip = false
  #config.hostmanager.include_offline = true
#

  config.vm.define "master" do |master|
    master.vm.box = "bento/ubuntu-20.04"
    master.vm.hostname = "master.ravi.local"
    master.vm.network "private_network",  auto_config: false
  end
  config.vm.define "node1" do |node1|
    node1.vm.box = "bento/ubuntu-20.04"
    node1.vm.hostname = "node1.ravi.local"
    node1.vm.network "private_network",  auto_config: false
    node1.vm.provision "file", source: "/Users/ravindrakumar/PycharmProjects/ubuntu_vmware/node1.yaml", destination: "/tmp/"
    node1.vm.provision "shell",
    inline: "mv /tmp/node1.yaml /etc/netplan/; netplan apply"
  end
  config.vm.define "node2" do |node2|
    node2.vm.box = "bento/ubuntu-20.04"
    node2.vm.hostname = "node2.ravi.local"
    node2.vm.network "private_network",  auto_config: false
    node2.vm.provision "file", source: "/Users/ravindrakumar/PycharmProjects/ubuntu_vmware/node2.yaml", destination: "/tmp/"
    node2.vm.provision "shell",
    inline: "mv /tmp/node2.yaml /etc/netplan/; netplan apply"
  end

  config.vm.define "node3" do |node3|
    node3.vm.box = "bento/ubuntu-20.04"
    node3.vm.hostname = "node3.ravi.local"
    node3.vm.network "private_network",  auto_config: false
    node3.vm.provision "file", source: "/Users/ravindrakumar/PycharmProjects/ubuntu_vmware/node3.yaml", destination: "/tmp/"
    node3.vm.provision "shell",
    inline: "mv /tmp/node3.yaml /etc/netplan/; netplan apply"
  end



  config.vm.provider "vmware_desktop" do |v|
    v.memory = 4000
    v.cpus = 2
  end
end
