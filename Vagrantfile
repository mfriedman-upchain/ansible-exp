# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    (1..2).each do |i|
        config.vm.define "nginx-#{i}" do |node|
            node.vm.box = "minimal/xenial64"
            node.vm.network "forwarded_port", guest: 80, host: "999#{i}"

            node.vm.hostname = "nginx-#{i}"
            node.vm.network :private_network, ip: "192.168.33.1#{i}"

            config.vm.provision "ansible" do |ansible|
                ansible.playbook = "playbooks/example/playbook.yml"
            end
        end
    end
end

