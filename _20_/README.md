# :sparkles: 22.5.23 :sparkles: 
# :shipit:
Heute  habe ich nicht unbedingt neu ,aber wichtiges aufrischend gelernt.

Witchitge Vagrant Befehle 🙇‍♂️:

``` bash
vagrant init
#Initialisiert im aktuellen Verzeichnis eine Vagrant-Umgebung und erstellt, falls nicht vorhanden, ein Vagrantfile

vagrant up
#Erzeugt und Konfiguriert eine neue Virtuelle Maschine, basierend auf dem Vagrantfile

vagrant ssh
#Baut eine SSH-Verbindung zur gewünschten VM auf

vagrant status
#Zeigt den aktuellen Status der VM an

vagrant port
#Zeigt die Weitergeleiteten Ports der VM an

vagrant halt
#Stoppt die laufende Virtuelle Maschine

vagrant destroy
#Stoppt die Virtuelle Maschine und zerstört sie.               
```

- reminder:
Boxen können explizit durch den Befehl vagrant box add [box-name] oder vagrant box add [box-url] heruntergeladen und durch vagrant box remove [box-name] entfernt werden. Ein "box-name" ist dabei durch Konvention wie folgt aufgebaut: Entwickler/Box (z.B. ubuntu/xenial64).
- Konfiguration 
Die gesamte Konfiguration erfolgt im Vagrantfile, das im entsprechenden Verzeichnis liegt. Die Syntax ist dabei an die Programmiersprache Ruby) angelehnt:

    Vagrant.configure("2") do |config|
        config.vm.define :apache do |web|
            web.vm.box = "bento/ubuntu-16.04"
            web.vm.provision :shell, path: "config_web.sh"
            web.vm.hostname = "srv-web"
            web.vm.network :forwarded_port, guest: 80, host: 4567
            web.vm.network "public_network", bridge: "en0: WLAN (AirPort)"
    end
