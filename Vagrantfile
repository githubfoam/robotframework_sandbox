# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|

  config.vm.define "master" do |master|
    master.vm.box = "bento/ubuntu-16.04"
    master.vm.hostname = "master"
    master.vm.network "private_network", ip: "172.16.1.11"
    master.vm.provider "virtualbox" do |vb|
        vb.memory = "4096"
    end
    master.vm.provision :shell, :path => "provision.sh"
    # master.vm.provision "ansible/master", type: "ansible" do |ansible|
    # master.vm.provision "ansible/master", type: "ansible_local" do |ansible|
    #     ansible.playbook = "ansible/provision-master.yml"
    #     ansible.compatibility_mode = "2.0"
    #     ansible.version = "2.2.1.0"
    #     ansible.verbose = "v"
    #     ansible.extra_vars = {
    #         "target" => "master",
    #         "master_ip" => "172.16.1.11",
    #         # "join_file" => "join.txt"
    #         # "join_file" => "/tmp/join.txt"
    #     }
    # end
  end


end
