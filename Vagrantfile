# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "web_1" do |web_1|
      web_1.vm.provider :virtualbox do |vb|
        vb.name = "server1"
      end
      web_1.vm.box = "alpine/alpine64"
      web_1.vm.provision "shell", path: "script.sh"
      web_1.vm.network "forwarded_port", guest: 80, host: 8009
      web_1.vm.synced_folder "D:/ClasesUnivalle/SO/vagrant/taller2/vagrantso/www1/", "/var/www/localhost/htdocs"
  end
  config.vm.define "web_2" do |web_2|
      web_2.vm.provider :virtualbox do |vb|
        vb.name = "server2"
      end
      web_2.vm.box = "alpine/alpine64"
      web_2.vm.provision "shell", path: "script.sh"
      web_2.vm.network "forwarded_port", guest: 80, host: 8008
      web_2.vm.synced_folder "D:/ClasesUnivalle/SO/vagrant/taller2/vagrantso/www2/", "/var/www/localhost/htdocs"
  end
end
