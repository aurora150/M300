# :sparkles: 15.5.23 :sparkles: :shipit:
Heute  habe ich nicht wircklich viel Neues gelernt, aber ich habe einfach die ganze umgebung eingerichtet und lauft

Jedoch war das ganze verstehen des Vagrant nicht schlecht :sparkle:

basic vagrant vm herstellen: :trollface:	

``` bash
cd Wohin/auch/immer
mkdir MeineVagrantVM
cd MeineVagrantVM
vagrant init ubuntu/xenial64                                                      #Vagrantfile erzeugen
vagrant up --provider virtualbox                                                  #Virtuelle Maschine erstellen & starten
cd Pfad/zu/meiner/Vagrant-VM      #Zum Verzeichnis der VM wechseln
vagrant ssh                   
```

reminder:
vagrant init "C:\Users\aurora\Documents\ubuntu-22.04.1-desktop-amd64\ubuntu-22.04.1-desktop-amd64.iso"
