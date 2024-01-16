## Recovery durchführung

Da das Backup funktioniert, muss noch getestet werden ob es in einem Fall von komplettem Datenverlust, wir die Daten wiederherstellen können.

Dafür musste ich erst auf meiner Aktuellen VM, auf Duplicati und mein Minecraft Backup aufklappen. Dort hatte ich die Option unter Konfiguration, Exportieren auszuwählen.

![Alt text](Konifiguration.png)

Als nächstes konnte man es als Befehl für Kommandozeile oder als Datei exportieren. Ich wählte als Datei. Hier kann noch entschieden werden, ob, die Datei verschlüsselt und als Passwort exportiert werden sollte. Ich würde aus Sicherheitsgründen, beides auswählen.



![Alt text](<Konfiguration mit passwort.png>)

Sobald auf Exportieren geklickt wurde, wird die Configdatei Heruntergeladen.

![Alt text](<Konfiguration exportiert.png>)

Jetzt habe ich die Nötige Datei, um einen Restore zu ermöglichen.

## Teil 2 VM erstellen

Im 2.Teil werde ich eine weiter VM erstellen. Wir gehen davon aus das wir alle Daten und Backups verloren haben. Deshalb müssen wir wieder eine neue VM erstellen. 

Die Neue VM bekommt den namen m143-Recovery.
Dies wird mit dem Befehl auf der Commandozeile durchgeführt:

#### Multipass multipass launch -c4 -d 80G -m 4G -n m143-Recovery docker

![Alt text](<neue VM erstellt.png>)

Die VM kann mit "Multipass shell m143-Recovery" gestartet werden.

Sobald dies funktioniert hat, müssen wir das docker-compose file wiederherstellen. Dies erledigen wir indem wir ein neues nano file öffnen.

#### nano docker-compse.yaml

dort geben wir wieder die Konfigurationen ein, die wir schon bei der ersten VM bestimmt haben.

![Alt text](<docker.compose für recovery.png>)

Die Container können danach gestartet werden. mit dem Befehl:

#### sudo docker compose up -d

![Alt text](<sudo docker comopose up recovery.png>)

Als nächstes muss duplicati geöffnet werden. wir nehmen die IP der neuen VM und den Port von duplicati also 8200.

Um unsere Backups wiederherzustellen, müssen wir hier auch ein Backup erstellen, nur das wir diesmal "von einer Datei importieren" auswählen.

![Alt text](<recovery import.png>)


