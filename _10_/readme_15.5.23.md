# _10_
Heute Neues habe ich nicht wircklich viel gelernt, aber ich habe einfach die ganze umgebung eingerichtet und lauft
basic vagrant vm herstellen:

``` bash
 cd Wohin/auch/immer
 mkdir MeineVagrantVM
  cd MeineVagrantVM
 vagrant init ubuntu/xenial64                                                      #Vagrantfile erzeugen
 vagrant up --provider virtualbox                                                  #Virtuelle Maschine erstellen & starten
 cd Pfad/zu/meiner/Vagrant-VM      #Zum Verzeichnis der VM wechseln
 vagrant ssh                   
```