# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant::Config.run do |config|
        config.vm.box = "debian-squeeze-64-magento"
        config.vm.box_url = "http://web13.site.flagbit.com/mageinstall/debian-squeeze-64-magento"
        config.ssh.host = "127.0.0.1"
        config.vm.forward_port 22, 2222, :auto => true
        config.vm.forward_port 80, 8080, :auto => true
        config.ssh.max_tries = 10
        config.ssh.timeout = 15
        config.vm.share_folder "www", "/usr/local/src/magento/deployment/", "../src/"
        config.vm.share_folder "vagrant", "/usr/local/src/vagrant/", "../.vagrant/"
        config.vm.customize ["modifyvm", :id, "--memory", 2048]
        config.vm.customize ["modifyvm", :id, "--name", "Magento MageHealth"]
        config.vm.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
end
