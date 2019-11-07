# Arbeitsauftrag für Lernende
##  Inhaltsverzeichnis
- 01-Autoren, Versionisierung
- 02-Nextcloud
- 03-Materialliste
- 04-Installationsanleitung
- 05-Qualitätskontrolle
- 06-Error-Handling

## Autoren, Versionisierung
### Autoren
Janosch Bühler, Mike Spengler
### Versionisierung
Wir nutzen Github und haben alle Dokumentationen in einem Repository. Dadurch ist die Versionierung duch Github gehandhabt.

## Nextcloud
Nextcloud ist eine Open-Source Alternative zu Dropbox, G-Drive etc. Das Hauptziel von Nextcloud ist, dass man selber Kontrolle über seine eigenen Daten hat und nicht ein Technologieriese, welcher mit den Daten tun kann was er will. 

Nextcloud kann sehr einfach auf einemn Server installiert werden und benötigt nur wenige Ressourcen. Sogar auf einem Raspberry Pi kann Nextcloud installiert werden. Für einen Produktivserver ist der Raspberry Pi jedoch ungeeingnet, da er zu wenig Leistung hat. 

### Einführung

#### Projektauftrag

Die Firma Anwälte Winkler&Cameri nutzt für ihre Datenablage zur Zeit Dropbox. Diese Art der Datenablage ist zwar gut, jedoch nicht sicher. Die Mitarbeiter laden ihre Dateien und Kundendokumente auf Dropbox. So haben sie von überall her Zugriff auf diese Dokumente. Die Firma macht sich Sorgen um die Sicherheit dieser Daten, da diese sehr sensibel sind. 

#### Zielsetzung: 
Wir wollen in der Vorstudie evaluieren, welches OS auf dem Server installiert sein soll und welche Ressourcen wichtig sind für den Nextcloud Server.

#### Vorgehensweise

    Raspberry Pi Betriebssystem installieren
    Grundkonfiguration Betriebssystem vornehmen
    Prerequisits für Nextcloud installieren
    Nextcloud installieren
    Web Gui Configurieren


Zeitaufwand

    Grundauftrag: 4-6 Lektionen
   
## 03-Materialliste

### Hardware
-   Computer (Raspberry Pi 3) (auch andere Versionen möglich)
-   Micro USB Netzteil
-   Micro SD Karte mit mindestens 4 GB
-   Netzwerk- und Internetverbindung

### Software
Wir haben ein Raspbian Stretch auf dem Raspberry Pi installiert. Darauf haben wir php7.3 und apache2 installiert.
Zudem wurde Nextcloud selber installiert. 

Nextcloud benötigt php und apache bzw einen Webserver um zu funktionieren.

Softwareanforderungen: 
php7.1
Webserver (apache2, nginx o.ä)

SW-Packages php:
```
php7.3 php7.3-gd php7.3-sqlite3 php7.3-curl php7.3-zip php7.3-xml php7.3-mbstring
```
SW-Packages sql:
```
sqlite
```
SW-Packages apache:
```
libapache2-mod-php7.3
```

## 04-Installationsanleitung
Für dieses Projekt soll Nextcloud als Cloudlösung aufgesetzt werden. Dieses soll direkt auf das Betriebssystem Raspbian Stretch auf dem Raspberry Pi installiert werden.
```
- Den Raspberry Pi mit Raspbian Buster als Betriebssystem aufsetzen
- Prerequisits von Nextcloud installieren
- Nextcloud installieren
- Web Gui konfigurieren
- Fortgeschritten: automatisches Backup durch Cronjobs (z.B. über Telegram)
```

## 05-Qualitätskontrolle
Mit einem Browser auf das Web Gui der Cloud zugreifen.
Über das Web Gui ist es nun möglich, Dateien in die Cloud zu laden. Die Hochgealdenen Dateien können nun auch wieder heruntergeladen werden. Ausserdem soll der Sync Client funktionieren (Download, Upload, automatisches synchronisieren). 

Die Installation zusätzlicher Apps soll funktionieren und das Aussehen von Nextcloud soll über das Theming App anpassbar sein. 
## 06-Error-Handling
Im Internet finden sich viele verschiedene Anleitungen um Nextcloud zu installieren. Zudem findet man im Internet viele Foren in denen Probleme und deren Lösungen diskutiert werden.

Das Error-Log von Nextcloud kann über den Command ``occ logs:watch`` überprüft werden. Die Datei occ befindet sich im über den Webserver freigegeben Ordner für Nextcloud.