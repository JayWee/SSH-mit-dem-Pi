# SSH mit dem Pi
Von der Platine zum SHH gesteuerten Roboter
Einführug 

# 1. Start - Was ist der Pi?
Der Raspberry Pi ist ein Mini-Computer, der vieles von dem, was ein normaler Computer auch kann: Er hat eine graphische Oberfläche1, einen Internetbrowser und andere Programme. 
Es gibt aktuell drei Versionen des Pi, die Funktionen sind größtenteils gleich. Das neueste Modell hat auch WLAN und Bluetooth an Board.

# 2.Den Pi in Betrieb setzen

Der Pi besitzt keine Festplatte oder anderweitige interne Speicher (außer den Arbeitsspeicher4 natürlich), weshalb wir einen „basteln“ müssen: Das geht ganz einfach mit einer SD-Karte die über mindestens 8GB5 verfügt und komplett leer ist, denn sie wird im weiteren Verlauf formatiert6.

Als erstes müssen wir das Betriebssystem für den Pi herunterladen, welches [hier](https://downloads.raspberrypi.org/raspbian_latest) verfügbar ist: Es heißt Raspbian und ist kostenlos. 
Nun haben wir eine Zip-Datei, die wir entpacken müssen: Jetzt haben wir anstatt der Zip Datei eine IMG Datei. 
Die SD-Karte wird nun in einen Computer gesteckt um die IMG-Datei darauf zu installieren. Jetzt kommt es auf das Betriebssystem an, welches benutzt wird: 

Windows 
Wir laden nun das Program [Win32DiskImager](http://sourceforge.net/projects/win32diskimager/). Wieder erhalten wir eine Zip-Datei die wir entpacken und das Programm ausführen. 

Mac 
Als erstes müssen wir sicherstellen, dass die SD-Karte im Format MS-DOS (FAT) formatiert ist: Dafür öffnen wir das Festplattendienstprogramm. Non klicken wir auf die SD-Karte an der linken Seite: Wichtig ist das wir auf obere klicken, nicht die untere. Nun wählen wir aus der oberen Leiste Löschen aus und wählen dann einen Namen (Ohne Titel), das Format (MS-DOS-Dateisytem (FAT)), und das Schema (GUID). Nun klicken wir auf Löschen. 
Jetzt merken wir uns die Zahl die unten rechts im Feld Gerät steht diskx.
Nun öffnen wir das Terminal (Programme -> Terminal) und geben den Befehl: sudo dd bs=1m if=path_of_your_image.img of=/dev/rdiskx ein.
Statt path_of_your_image.img geben wir den Pfad der IMG Datei ein. Diesen können wir aus dem Finder kopiert. Dafür wählen wir die IMG-Datei aus und rechts-klicken auf die Datei und wählen Informationen aus. Für x setzen wir die Zahl aus dem Festpalttendienstprogramm ein und führen den Befehl aus. 
Schlägt der Befehl fehl, kann man statt rdisk auch nur disk verwenden.
Ist der Befehl ausgeführt, kann die SD-Karte ausgeworfen werden und wir stecken sie in den Pi. 

# 3. Der erste Start
Nun nehmen wir ein Display zur Hand, das wir entweder direkt 








