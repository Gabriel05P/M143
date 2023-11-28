# M143
## Konzept:
![Alt text](image.png)

Um die VM's und Testumgebungen zu erstellen, benutze ich dafür Multipass. Ich Betreibe einen Minecraft Server. Ich benutze die Cloud Mega.nz und dazu noch einen Docker für mehr sicherheit, da ich dort die Umgebung isolieren kann. Duplicati benutz ich da man mit der Applikation Backups verschlüsseln und in die Cloud speichern kann. Netdata wird für die Überwachung verwendet.

## Schritt 2. VM Erstellen.

Ich habe als erstes eine VM auf Mutlipass erstellt. Dafür muss Mutlipass schon installiert und anwendungsbereit sein. Multipass kann man hier installieren:

https://multipass.run/docs/installing-on-windows#heading--install-upgrade-uninstall

Wenn dies gemacht ist, müssen wir das CMD öffnen und können uns dann dort unsere erste VM erstellen. Dies machen wir mit diesem Befehl:

### multipass launch -c4 -d 80G -m 4G -n m143 docker

multipass launch: Dieser Teil des Befehls startet eine neue virtuelle Maschine (VM) mit Multipass.

-c4: Dieser Parameter gibt an, dass die VM über 4 CPUs (Kerne) verfügen soll.

-d 80G: Dieser Parameter legt die Größe der virtuellen Festplatte auf 80 Gigabyte (GB) fest.

-m 4G: Dieser Parameter gibt den VM 4 Gigabyte (GB) Arbeitsspeicher (RAM).

-n m143: Dieser Parameter weist der VM einen Namen zu, in diesem Fall "m143".

docker: Dieser Teil des Befehls gibt an, dass Docker in der virtuellen Maschine installiert werden soll.

![Alt text](image-1.png)

Wie man im Screenshot sieht, kann man mit "multipass List" kontrollieren, ob die instanz wirklich erstellt wurde.



