# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do|config|
	config.ssh.insert_key = false
	config.vm.provider :virtualbox do|vb|
		vb.customize ["modifyvm", :id, "--memory", "2048"]
	end

	#Web Server
        config.vm.define "web1" do|web|
		web.vm.hostname = "mwiweb02"
		web.vm.box = "geerlingguy/centos7"
		web.vm.network "public_network", ip: "192.168.43.14"
	end


	#Application Server1
	config.vm.define "app1" do|app|
		app.vm.hostname = "mwivmapp01"
		app.vm.box = "geerlingguy/centos7"
		app.vm.network "public_network", ip: "192.168.43.11"
	end


	#Application Server2
	config.vm.define "app2" do|app|
		app.vm.hostname = "mwivmapp02"
		app.vm.box = "geerlingguy/centos7"
		app.vm.network "public_network", ip: "192.168.43.12"
	end

	#Database Server
	config.vm.define "db" do|db|
		db.vm.hostname = "mwisqldb01"
		db.vm.box = "geerlingguy/centos7"
		db.vm.network "public_network", ip: "192.168.43.13"
	end
	config.vm.box_check_update = false
	#config.vbguest.auto_update = false

end
