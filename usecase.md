## User Story: Minecraft Server Backup und Wiederherstellung

### Beschreibung

Benutzergeschichte:

Als Mitglied der Backmine-Community von Minecraft möchte ich, dass regelmäßige Backups meines Spielstands auf dem Server erstellt werden, um sicherzustellen, dass keine Ressourcen oder Fortschritte verloren gehen, falls unvorhergesehene Probleme auftreten.


Beschreibung:

 Wir haben uns entschieden, in unserer Backmine Minecraft-Community regelmässige Backups der Spieler-Spielstände auf unserem Server zu implementieren. Diese Massnahme wurde ergriffen, um die kostbare Zeit und Energie zu schützen, die unsere Spieler in den Aufbau ihrer Welten investieren.

Problembeschreibung:

 Wir möchten das Hauptproblem lösen, nämlich den potenziellen Verlust von Spielständen aufgrund von Serverausfällen, technischen Problemen oder anderen unvorhergesehenen Zwischenfällen, indem wir diese Backup-Routine einführen. In der Vergangenheit war die Community frustriert und unzufrieden, als Spieler wertvolle Ressourcen und kreative Leistungen verloren haben.



Lösungskonzept:
Um dieses Problem zu beheben, arbeite ich an einem detaillierten Konzept für die Implementierung eines automatischen Backup-Systems für die Spieler-Spielstände auf dem Backmine Minecraft-Server.

## Kriterien

1. #### Use-Case Beurteilung:

**Virtuelle Maschine**

Die virtuelle Maschine (VM) wird erfolgreich mit Multipass erstellt und enthält eine Docker-Instanz für den Minecraft-Server sowie eine Duplicati-Instanz.

**Konfigurationen**

Die Konfiguration der VM und der Container erfolgt mithilfe von Docker-Compose, wobei die Ressourcen (CPU, RAM, Festplattengrösse) angemessen festgelegt sind.

**Docker-Container**

Die Docker-Container (Minecraft-Server und Duplicati) können erfolgreich gestartet werden, und die Anwendungen sind funktionsfähig.

**Minecraft-Server**

Der Minecraft-Server kann über die VM-IP und den entsprechenden Port erreicht werden, und ein Spielstand kann erfolgreich gespeichert und wiederhergestellt werden.

**Duplicati**

Duplicati ist korrekt konfiguriert und kann regelmässige verschlüsselte Backups der Minecraft-Daten in der Mega.nz-Cloud erstellen.

**Portainer**

Portainer wird erfolgreich installiert und ermöglicht die Überwachung und Verwaltung der Docker-Container über eine benutzerfreundliche Benutzeroberfläche.

**Mega.nz**

Die Mega.nz-Cloud ist eingerichtet, und Duplicati kann erfolgreich auf den Cloud-Speicher zugreifen und Backups durchführen.

**Recovery Key**

Der Benutzer hat einen Recovery Key für den Mega.nz-Account erstellt und sicher gespeichert.
Die Wiederherstellung des Minecraft-Spielstands aus dem Duplicati-Backup wurde erfolgreich durchgeführt.


 ## Inkrementelle Backup

Im Rahmen dieses Projekts wurde die Backup-Strategie der inkrementellen Backups gewählt, um effiziente Sicherungen von Minecraft-Spielständen und Systemkonfigurationen zu ermöglichen. Dieser Ansatz wurde im Vergleich zu einem vollständigen (Full) Backup gewählt, um bestimmte Vorteile zu nutzen.

**Inkrementelle Backups im Überblick:**

Definition: Inkrementelle Backups sichern nur die seit dem letzten Backup geänderten oder hinzugefügten Daten.

**Vorteile:**

Speicherplatzoptimierung: Inkrementelle Backups benötigen weniger Speicherplatz, da nur Änderungen seit dem letzten Backup gesichert werden.

Zeiteffizienz: Da nur inkrementelle Änderungen gesichert werden, ist der Backup-Prozess schneller im Vergleich zu einem Full Backup.

**Vergleich mit einem Full Backup:**

Full Backup:
Definition: Ein Full Backup sichert alle Daten, unabhängig davon, ob sie seit dem letzten Backup geändert wurden.

**Vorteile:**

Einfache Wiederherstellung: Die Wiederherstellung ist einfach, da alle Daten in einem Backup enthalten sind.

**Nachteile:**

Hoher Speicherplatzbedarf: Full Backups benötigen mehr Speicherplatz, da sie alle Daten umfassen, auch wenn sie sich nicht geändert haben.

Zeitaufwändig: Die Durchführung eines Full Backups kann mehr Zeit in Anspruch nehmen, insbesondere bei grossen Datenmengen.

Warum die Wahl auf inkrementelle Backups fiel:
Die Entscheidung für inkrementelle Backups wurde getroffen, um den spezifischen Anforderungen des Projekts gerecht zu werden:

**Ressourcenschonung:** Durch die Speicherplatzoptimierung wird der Ressourcenverbrauch minimiert, was besonders in Cloud-Speicherlösungen von Vorteil ist.

**Schnellere Backup-Zeiten:** Die inkrementelle Backup-Strategie ermöglicht schnellere Backup-Zeiten, was den kontinuierlichen Spielbetrieb und andere Dienste minimale Ausfallzeiten gewährleistet.

**Effizientes Rücksichern:** Im Falle einer Wiederherstellung müssen nur die inkrementellen Änderungen seit dem letzten Backup wiederhergestellt werden, was die Prozesse beschleunigt.

Die Wahl der Backup-Strategie wurde somit auf die spezifischen Anforderungen des Projekts und die Notwendigkeit einer effizienten Datensicherung abgestimmt.

8.	#### Zusätzliche Sicherheit:

•	Zusätzliche Sicherheitsmassnahmen wie die Verschlüsselung von Backups sind implementiert und dokumentiert.
•	Sicherheitsüberlegungen für den Zugriff auf die Cloud und die verwendeten Dienste sind dokumentiert.
Zusätzliche Informationen
Die detaillierte Dokumentation mit Screenshots und Erklärungen für die einzelnen Schritte ist im Dokument [Readme.md](README.md) verfügbar.




