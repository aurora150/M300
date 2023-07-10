# :sparkles: 7.7.23 :sparkles: 
# :shipit:
- Logging:
![image](https://github.com/aurora150/M300/assets/52505952/d1753017-d953-4eaf-bf2e-0eb8b33127b7)
- Überwachen und Benachrichtigen:
![image](https://github.com/aurora150/M300/assets/52505952/77054d48-fcf8-4526-acbc-9e3ca80d53ee)

# Sicherheitsaspekte:

Kernel Exploits: Durch die gemeinsame Nutzung des Kernels von allen Containern und dem Host hat ein Kernel-Exploit im Container weitreichende Auswirkungen auf den gesamten Host, im Gegensatz zu virtuellen Maschinen, wo zusätzliche Hürden überwunden werden müssen, um den Host-Kernel anzugreifen.

Denial-of-Service-(DoS-)Angriffe: Durch die gemeinsame Nutzung von Ressourcen im Kernel können Container andere Container durch monopolisieren bestimmter Ressourcen wie Speicher oder User IDs (UIDs) daran hindern, das System oder Teile davon ansprechen zu können, was zu einem Denial-of-Service-Angriff führen kann.

Container-Breakouts: Wenn ein Angreifer Zugriff auf einen Container erhält, besteht die Gefahr, dass er auf andere Container oder den Host zugreifen kann, da die Benutzer in den Containern nicht vollständig voneinander isoliert sind. Dies kann zu Privilege-Escalation-Angriffen führen, bei denen der Angreifer im Container erlangte Rechte auch auf den Host ausweiten kann. Es ist wichtig, die Möglichkeit von Container-Breakouts zu berücksichtigen und entsprechende Sicherheitsvorkehrungen zu treffen.

Vergiftete Images: Es besteht die Gefahr, dass unsichere oder manipulierte Images verwendet werden, die potenziell den Host und die darin enthaltenen Daten gefährden könnten. Zusätzlich ist es wichtig sicherzustellen, dass die verwendeten Images aktuell sind und keine bekannten Sicherheitslücken aufweisen.

Verratene Geheimnisse: Container, die auf sensible Datenbanken oder Services zugreifen müssen, benötigen oft Zugriffsgeheimnisse wie API-Schlüssel oder Benutzername und Passwort. Wenn ein Angreifer Zugriff auf diese Geheimnisse erhält, kann er den Service ebenfalls nutzen. Dieses Risiko wird in einer Microservices-Architektur verstärkt, in der Container häufig gestoppt und neu gestartet werden, im Vergleich zu einer Architektur mit wenigen dauerhaften virtuellen Maschinen.