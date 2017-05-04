Imgprep Skript
===============

* Zur Ausführung vor der Image Erstellung
* Muss angepasst werden!
* Man kann sich das mit der Hintergrunderzeugung natürlich rauskopieren und wunschgemäß anpassen. The Code is the Documentation ;)

Hintergrunderzeugung
---------------------

* Der Inhalt des verzeichnisses background_files muss nach /home/linuxadmin/.backgrounds/ kopiert werden. (Die xcf-Dateien sind nicht nötig, außer wenn man die Wasserzeichen noch ändern will).
* Man muss sicherstellen, dass /home/linuxadmin/.backgrounds/desktop.jpg und /home/linuxadmin/.backgrounds/login.jpg von jedem Benutzer lesbar sind.
* Dann stellt man als linuxadmin /home/linuxmuster/.backgrounds/desktop.jpg als Desktop-Hintergrund ein, /home/linuxadmin/.backgrounds/login.jpg als Login Hintergrund. 
* Um den Hintergrund zu ändern, kopiert man das gewünschte Hintergrundbild nach /home/linuxmuster/.backgrounds/desktop_input.jpg und lässt anschließend qgm-imgprep laufen. Dieses erzeugt dann aus den Dateien desktop_logo.png und login_logo.png als Overlay automatisch die beiden Hintergrundbilder, wobei das Login-Bild S/W gemacht wird. 
