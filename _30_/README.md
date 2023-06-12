# :sparkles: 12.6.23 :sparkles: 
# :shipit:
Merken:
egal wie wenig Benutzer,immer Gruppen herstellen
--
![image](https://github.com/aurora150/M300/assets/52505952/e3706552-aabe-4d37-977e-6e8317f023db)

```bash
Vagrant.configure("2") do |config|
  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/xenial64"
    web.vm.network "private_network", ip: "192.168.55.101"
    web.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y apache2
      sudo ufw allow 80/tcp
    SHELL
  end

  config.vm.define "database" do |database|
    database.vm.box = "ubuntu/xenial64"
    database.vm.network "private_network", ip: "192.168.55.100"
    database.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server
      sudo ufw allow 3306/tcp
    SHELL
  end

  config.vm.define "proxy" do |proxy|
    proxy.vm.box = "ubuntu/xenial64"
    proxy.vm.network "private_network", ip: "192.168.55.102"
    proxy.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y apache2
      sudo apt-get install -y libapache2-mod-proxy-html
      sudo apt-get install -y libxml2-dev
      sudo a2enmod proxy
      sudo a2enmod proxy_html
      sudo a2enmod proxy_http
      sudo ufw allow 80/tcp
      sudo ufw allow from 192.168.55.101 to any port 80
      sudo ufw allow from 192.168.55.100 to any port 3306
      sudo systemctl restart apache2
    SHELL
  end

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
  end

  config.ssh.insert_key = false
end

```
ich kann mich aber noch nicht mit ssh verbinden
