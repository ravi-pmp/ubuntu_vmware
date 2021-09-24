Vagrant.configure("2") do |config|

  config.vm.define "master" do |master|
    master.vm.box = "bento/ubuntu-20.04"
    master.vm.hostname = "master.ravi.local"
    master.vm.network "private_network",  ip: "192.168.4.155" 
    master.vm.disk :disk, name: "data", size: "50GB"
  end
  config.vm.define "node1" do |node1|
    node1.vm.box = "bento/ubuntu-20.04"
    node1.vm.hostname = "node1.ravi.local"
    node1.vm.network "private_network",  ip: "192.168.4.156"
    node1.vm.disk :disk, name: "data", size: "50GB"
  end
  config.vm.define "node2" do |node2|
    node2.vm.box = "bento/ubuntu-20.04"
    node2.vm.hostname = "node2.ravi.local"
    node2.vm.network "private_network",  ip: "192.168.4.157" 
    node2.vm.disk :disk, name: "data", size: "50GB"
  end
  config.vm.define "node3" do |node3|
    node3.vm.box = "bento/ubuntu-20.04"
    node3.vm.hostname = "node3.ravi.local"
    node3.vm.network "private_network",  ip: "192.168.4.158" 
    node3.vm.disk :disk, name: "data", size: "50GB"
  end
  config.vm.provider "parallels" do |v|
    v.memory = 4000
    v.cpus = 2
    v.linked_clone = false
  end
end
