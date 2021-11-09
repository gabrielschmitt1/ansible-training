Vagrant.configure("2") do |config|

    config.vm.box = "ubuntu/focal64"

    config.vm.provider "virtualbox" do |v|
        v.memory = 1024
    end

    config.vm.define "wordpress" do |m|
        m.vm.network "forwarded_port", guest: 80, host:8080
        m.vm.network "private_network", ip: "172.17.177.20"
        m.vm.network "public_network", ip: "192.168.0.19"
    end

    config.vm.define "mysql" do |m|
        m.vm.network "forwarded_port", guest: 80, host:8081
        m.vm.network "private_network", ip: "172.17.177.42"
        m.vm.network "public_network", ip: "192.168.0.20"
    end

end