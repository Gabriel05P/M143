## User Story: Minecraft Server Backup und Wiederherstellung

### Beschreibung

Als Betreiber eines Minecraft-Servers möchte ich regelmäßig meine Spielstände sichern, um im Falle von Datenverlust oder Serverproblemen den Spielstand schnell wiederherzustellen. Die Datensicherung und der Restore-Prozess werden basierend auf einem Use-Case untersucht und angewendet. Dabei werden verschiedene Methoden miteinander verglichen und anhand von spezifischen und quantifizierbaren Kriterien wird das geeignetste Verfahren ausgewählt. Die Sicherung von Benutzerdaten und Systemdaten (Systemkonfigurationsdaten oder Systembilder) sind konzeptionell voneinander getrennt.

## Kriterien

1. #### Use-Case Beurteilung:

Die virtuelle Maschine (VM) wird erfolgreich mit Multipass erstellt und enthält eine Docker-Instanz für den Minecraft-Server sowie eine Duplicati-Instanz.
Die Konfiguration der VM und der Container erfolgt mithilfe von Docker-Compose, wobei die Ressourcen (CPU, RAM, Festplattengröße) angemessen festgelegt sind.
Die Docker-Container (Minecraft-Server und Duplicati) können erfolgreich gestartet werden, und die Anwendungen sind funktionsfähig.
Der Minecraft-Server kann über die VM-IP und den entsprechenden Port erreicht werden, und ein Spielstand kann erfolgreich gespeichert und wiederhergestellt werden.
Duplicati ist korrekt konfiguriert und kann regelmäßige verschlüsselte Backups der Minecraft-Daten in der Mega.nz-Cloud erstellen.
Portainer wird erfolgreich installiert und ermöglicht die Überwachung und Verwaltung der Docker-Container über eine benutzerfreundliche Benutzeroberfläche.
Die Mega.nz-Cloud ist eingerichtet, und Duplicati kann erfolgreich auf den Cloud-Speicher zugreifen und Backups durchführen.
Der Benutzer hat einen Recovery Key für den Mega.nz-Account erstellt und sicher gespeichert.
Die Wiederherstellung des Minecraft-Spielstands aus dem Duplicati-Backup wurde erfolgreich durchgeführt.
Eine detaillierte Dokumentation für den Recovery-Prozess ist verfügbar.

2.	#### Restore-Prozess:

•	Der Restore-Prozess ist detailliert beschrieben und funktional dokumentiert.
•	Der Restore-Prozess wurde erfolgreich getestet, um die Funktionalität sicherzustellen.

3.	#### Unterscheidung von Datenarten:

•	Konzeptuell ist eine klare Unterscheidung zwischen der Sicherung von Benutzerdaten (Spielstände) und den Systemdaten (z. B. Docker- und VM-Konfigurationen) vorhanden.
•	Die Sicherung und Wiederherstellung von Benutzerdaten und Systemdaten erfolgt getrennt und ist in der Dokumentation festgehalten.
4.	#### Technologische Umsetzung:

•	Die gewählte technologische Umsetzung ist auf den definierten Use-Case angewendet.
•	Konkrete Anweisungen für die Datensicherung sind für verschiedene Services (Minecraft-Server, Docker, VM) konkret festgehalten.
•	Die gewählten Sicherungsverfahren sind in Bezug auf die verschiedenen Services angemessen begründet.

5.	#### Mega.nz Integration:

•	Die Integration von Mega.nz als Cloud-Speicher für Duplicati ist erfolgreich durchgeführt.
•	Die Sicherung und Wiederherstellung von Daten auf Mega.nz wurde erfolgreich getestet.

6.	#### Recovery Key:

•	Der Benutzer hat einen Recovery Key für den Mega.nz-Account erstellt und sicher gespeichert.

7.	#### Zusätzliche Sicherheit:

•	Zusätzliche Sicherheitsmaßnahmen wie die Verschlüsselung von Backups sind implementiert und dokumentiert.
•	Sicherheitsüberlegungen für den Zugriff auf die Cloud und die verwendeten Dienste sind dokumentiert.
Zusätzliche Informationen
Die detaillierte Dokumentation mit Screenshots und Erklärungen für die einzelnen Schritte ist im Dokument [Readme.md](README.md) verfügbar.
