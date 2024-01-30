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

**Zusätzliche Sicherheit:**

Zusätzliche Sicherheitsmassnahmen wie die Verschlüsselung von Backups sind dokumentiert.
Zusätzliche Informationen
Die detaillierte Dokumentation mit Screenshots und Erklärungen für die einzelnen Schritte ist im Dokument [Readme.md](README.md) verfügbar.


**Differentielle Sicherung (Differential Backup):**

Warum gewählt:

**Effiziente Datenverwaltung:**

 Die Differentielle Sicherung sichert nur die Daten, die sich seit der letzten Voll­sicherung geändert haben. Dies ermöglicht eine effiziente Nutzung des Speicherplatzes im Vergleich zu regelmäßigen Voll­sicherungen.

**Schnellere Wiederherstellung:**

 Im Falle eines Datenverlusts müssen nur die differentiellen Backups seit der letzten Voll­sicherung wiederhergestellt werden. Dies beschleunigt den Wiederherstellungsprozess im Vergleich zu inkrementellen Backups, bei denen alle inkrementellen Sicherungen seit der letzten Voll- oder Differenzialsicherung benötigt werden.

**Vorteile:**

Zeitersparnis bei der Wiederherstellung:

Die Wiederherstellung erfolgt schneller im Vergleich zu inkrementellen Backups, da nur die differentiellen Backups seit der letzten Voll­sicherung benötigt werden.

Speicherplatzoptimierung:

 Im Vergleich zu regelmäßigen Voll­sicherungen ist der Speicherplatzbedarf für differentielle Backups geringer, da nur die Änderungen seit der letzten Voll­sicherung gesichert werden.

Einfache Verwaltung:

 Die Verwaltung von differentiellen Backups ist einfacher als bei inkrementellen Backups, da nur die differentiellen Backups und die letzte Voll­sicherung berücksichtigt werden müssen.


**Vergleich mit einem Full Backup:**

Full Backup:
Definition: Ein Full Backup sichert alle Daten, unabhängig davon, ob sie seit dem letzten Backup geändert wurden.

**Vorteile:**

Einfache Wiederherstellung: Die Wiederherstellung ist einfach, da alle Daten in einem Backup enthalten sind.

**Nachteile:**

Hoher Speicherplatzbedarf: Full Backups benötigen mehr Speicherplatz, da sie alle Daten umfassen, auch wenn sie sich nicht geändert haben.

Zeitaufwändig: Die Durchführung eines Full Backups kann mehr Zeit in Anspruch nehmen, insbesondere bei grossen Datenmengen.






