## Userstory: Minecraft Server Backup und Wiederherstellung

**Weitere Unterlagen:**

Das Datenschutzkonzept, ist hier zu finden: [Datensicherungskonzept](Datensicherungskonzept.md)

Die Betriebsdokumentation, ist hier zu finden: [Betriebsdokumentation](README.md)

Die Restore Dokumentation, ist hier zu finden: [Recovery Dokumentation](Recovery.md)

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








