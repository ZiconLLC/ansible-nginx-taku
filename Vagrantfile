# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANT_VERSION = 2
Vagrant.configure(VAGRANT_VERSION) do |config|
	config.vm.define "nginx-taku" do |server|
		server.vm.box = "hashicorp/precise64"
		server.vm.hostname = "nginx-taku"
		server.vm.provision :ansible do |ansible|
			ansible.playbook = "test.yml"
			ansible.skip_tags = "encrypted"
		end
	end
end
