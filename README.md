# SSH mit dem Pi
Von der Platine zum SHH gesteuerten Roboter
[Einführug](#1)  
[Den Pi in den Betrieb setzen](#2)  
[Der erste Start](#3)  

## 1. Start - Was ist der Pi? <a name="1"></a>
Der Raspberry Pi ist ein Mini-Computer, der vieles von dem, was ein normaler Computer auch kann: Er hat eine graphische Oberfläche1, einen Internetbrowser und andere Programme. 
Es gibt aktuell drei Versionen des Pi, die Funktionen sind größtenteils gleich. Das neueste Modell hat auch WLAN und Bluetooth an Board.

## 2.Den Pi in Betrieb setzen

Der Pi besitzt keine Festplatte oder anderweitige interne Speicher (außer den Arbeitsspeicher4 natürlich), weshalb wir einen „basteln“ müssen: Das geht ganz einfach mit einer SD-Karte die über mindestens 8GB5 verfügt und komplett leer ist, denn sie wird im weiteren Verlauf formatiert6.

Als erstes müssen wir das Betriebssystem für den Pi herunterladen, welches [hier](https://downloads.raspberrypi.org/raspbian_latest) verfügbar ist: Es heißt Raspbian und ist kostenlos. 
Nun haben wir eine Zip-Datei, die wir entpacken müssen: Jetzt haben wir anstatt der Zip Datei eine IMG Datei. 
Die SD-Karte wird nun in einen Computer gesteckt um die IMG-Datei darauf zu installieren. Jetzt kommt es auf das Betriebssystem an, welches benutzt wird: 

## Windows 
Wir laden nun das Program [Win32DiskImager](http://sourceforge.net/projects/win32diskimager/). Wieder erhalten wir eine Zip-Datei die wir entpacken und das Programm ausführen. 

## Mac 
Als erstes müssen wir sicherstellen, dass die SD-Karte im Format MS-DOS (FAT) formatiert ist: Dafür öffnen wir das Festplattendienstprogramm. Non klicken wir auf die SD-Karte an der linken Seite: Wichtig ist das wir auf obere klicken, nicht die untere. Nun wählen wir aus der oberen Leiste Löschen aus und wählen dann einen Namen (Ohne Titel), das Format (MS-DOS-Dateisytem (FAT)), und das Schema (GUID). Nun klicken wir auf Löschen. 
Jetzt merken wir uns die Zahl die unten rechts im Feld Gerät steht diskx.
Nun öffnen wir das Terminal (Programme -> Terminal) und geben den Befehl: sudo dd bs=1m if=path_of_your_image.img of=/dev/rdiskx ein.
Statt path_of_your_image.img geben wir den Pfad der IMG Datei ein. Diesen können wir aus dem Finder kopiert. Dafür wählen wir die IMG-Datei aus und rechts-klicken auf die Datei und wählen Informationen aus. Für x setzen wir die Zahl aus dem Festpalttendienstprogramm ein und führen den Befehl aus. 
Schlägt der Befehl fehl, kann man statt rdisk auch nur disk verwenden.
Ist der Befehl ausgeführt, kann die SD-Karte ausgeworfen werden und wir stecken sie in den Pi. 

#3. Der erste Start
Nun nehmen wir ein Display zur Hand, das wir entweder direkt direkt über HDMI oder Composite anschließen. Dann stecken wir die SD-Karte, auf der das Raspbian installiert ist, ein und versorgen den Pi über ein Micro-USB-Kabel mit Strom. 
Nun behinnt der Pi den Startvorgang. In der Zeit können wir ein LAN-Kabel zur Versorgung mit Internet anschließen. (die Pis der Schule müssen nur angeschlossen werden, sie haben schon Internet. Eigene Pi's müssen erst registriert werden: Wendet euch einfach an Herrn Buhl oder die NV.

# Zugriff auf den Pi 
Der Pi ist nach etwa 2 Minuten bereit um mit ihm zu arbeiten und auf ihn zuzugreifen. Das machen wir mittels SSH: SSH ist ein ___
Das Herstellen einer SSH-Verbindung zum Rasperry Pi ist sehr nützlich zum Ausführen von Befehlen. Man kann sich dann das anschließen von Monitor und Tastatur an den Pi sparen und vom eigenem Laptop oder Schulrecher aus den Pi steuern.

Je nach Betriebsystem ist das Verbinden zum Pi unterschiedlich. Dise Anleitung gilt für Linux, OSX und Windows.

## Verbindung aufbauen

### Linux, OSX

OSX basiert auf Linux und da Linux einen SSH-Klienten mitbringt, gelten diese Schritte auch für OSX.

Wir öffnen das Terminal und führen folgenen Befehlen aus: 

ssh pi@ip
ip ist die Adresse unter der wir den Pi erreichen. Sie findet wir zuhause über den Router und in der Schule mittels  
Wir sind nun auf dem Raspberry Pi eingewehlt und können Befehle und Programme direkt auf dem Pi ausführen. 
Falls wir die Verbindung beenden wollen senden wir entweder den Befehl exit oder schließen das Terminal 










