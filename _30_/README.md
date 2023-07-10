# :sparkles: 26.6.23 :sparkles: 
# :shipit:
# Container
Merkmale 

Container teilen sich Ressourcen mit dem Host-Betriebssystem
Container können im Bruchteil einer Sekunde gestartet und gestoppt werden
Anwendungen, die in Containern laufen, verursachen wenig bis gar keinen Overhead
Container sind portierbar --> Fertig mit "Aber bei mir auf dem Rechner lief es doch!"
Container sind leichtgewichtig, d.h. es können dutzende parallel betrieben werden.
Container sind "Cloud-ready"!

---------------------- 
Wir benutzen dafür jetzt zum testen docker

Docker ist eine Open-Source-Plattform, die es Entwicklern ermöglicht, Anwendungen in isolierten und portablen Containern zu erstellen, bereitzustellen und auszuführen.

---
Umgebungs variablen:
Netzwerkplan
schichtenmodell 
sicherheitsaspekte
---------
ICH WAR AM KÄMPFEN MIT DEM DOCKERDESKTOP WEGENN DERN HYPER-V

schlussendlich habe ich das Problem gelöst in dem das ich das auf der Virtuelle machine des vagrant drauf getan habe

---
Installation:
 ![image](https://github.com/aurora150/M300/assets/52505952/f4898b17-2760-4dd5-b086-e64adb0df34d)
![image](https://github.com/aurora150/M300/assets/52505952/b0c01a11-7d4d-4e01-a244-32803e0f255f)
Befehle:
![image](https://github.com/aurora150/M300/assets/52505952/52a4ea25-2e55-4819-84b2-df811b4d1812)

```bash
Standard-Test:

    $ docker run hello-world


Startet einen Container mit einer interaktiven Shell (interactive, tty):

    $ docker run -it ubuntu /bin/bash


Startet einen Container, der im Hintergrund (detach) läuft:

    $ docker run -d ubuntu sleep 20


Startet einen Container im Hintergrund und löscht (remove) diesen nach Beendigung des Jobs:

    $ docker run -d --rm ubuntu sleep 20


Startet einen Container im Hintergrund und legt eine Datei an:

    $ docker run -d ubuntu touch /tmp/lock


Startet einen Container im Hintergrund und gibt das ROOT-Verzeichnis (/) nach STDOUT aus:

    $ docker run -d ubuntu ls -l
```

docker ps :
![image](https://github.com/aurora150/M300/assets/52505952/8f623156-6a30-40d4-8fca-c0cad7590f43)

Zeigt eigentlich welche maschinen an sind und ist sehr nützlich
Dockerfile:
![image](https://github.com/aurora150/M300/assets/52505952/2b7bf9fc-5e9a-4fbf-acb1-d9ebd51e71e3)

Ich konnte SQL iwi nicht installieren und habe es weiter versucht jedoch hatte ich einen grossen  Zeit problem



