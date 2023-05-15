Heute Neues habe ich nicht wircklich viel gelernt, aber ich habe einfach die ganze umgebung eingerichtet und lauft
basic vagrant vm herstellen:

```
1. cd Wohin/auch/immer
2. mkdir MeineVagrantVM
3.  cd MeineVagrantVM
4. vagrant init ubuntu/xenial64                                                      #Vagrantfile erzeugen
5. vagrant up --provider virtualbox                                                  #Virtuelle Maschine erstellen & starten
6. cd Pfad/zu/meiner/Vagrant-VM      #Zum Verzeichnis der VM wechseln
7. vagrant ssh                   
```