Imgprep Skript
===============

* Zur Ausführung vor der Image Erstellung
* Muss angepasst werden!
* Man kann sich das mit der Hintergrunderzeugung natürlich rauskopieren und wunschgemäß anpassen. The Code is the Documentation ;)

Hintergrunderzeugung
---------------------

* Der Inhalt des Verzeichnisses background_files muss nach /home/linuxadmin/.backgrounds/ kopiert werden. (Die xcf-Dateien sind nicht nötig, außer wenn man die Wasserzeichen noch ändern will).
* Dann stellt man als linuxadmin /home/linuxmuster/.backgrounds/desktop.jpg als Desktop-Hintergrund ein. 
* Um den Login-Hintergrund unter Ubuntu 16.04 einzustellen, muss man folgendermaßen vorgehen:
  * Als linuxmadmin anmelden und mit `sudo -i` root werden
  * mit `su lightdm -s /bin/bash` eine Shell als Benutzer lightdm öffnen
  * In dieser Shell den dconf-editor öffnen und dort den Schlüssel `com -> canonical -> unity-greeter -> background` auf den Wert `/usr/share/backgrounds/qgm.jpg` setzen. Wenn man einen anderen Dateinamen will, muss man das Skript entsprechend anpassen. *Der Trick ist also, den Schlüssel für den Benutzer lightdm zu ändern, wenn man das als linuxadmin macht hat es keinen Effekt!*
* Um einen neuen Hintergrund zu setzen (das mache ich für jedes neue Image, so kann ich direkt sehen, welches Image auf einem Rechner läuft), kopiert man das gewünschte Hintergrundbild nach /home/linuxmuster/.backgrounds/desktop_input.jpg und lässt anschließend qgm-imgprep laufen. Dieses erzeugt dann aus den Dateien desktop_logo.png und login_logo.png als Overlay automatisch die beiden Hintergrundbilder, wobei das Login-Bild S/W gemacht wird. Die Login Bilder werden an die passenden Stellen kopiert - qgm-imgprep muss aus naheligenenden Gründen also als Benutzer root ausgeführt werden.
