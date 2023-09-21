# Basic Commands


## NANO
```nano ilikelinux.md```

```
    • Strg + O: Speichern der aktuellen Datei.
    • Strg + X: Beenden von Nano.
    • Strg + G: Zeige die Hilfe für verfügbare Tastenkombinationen an.
    • Strg + K: Ausschneiden einer Zeile oder eines Blocks.
    • Strg + U: Einfügen des zuvor ausgeschnittenen Texts.
    • Strg + W: Suchen nach einem Text in der Datei.
```


# Wichtige Linux-Befehle

## Dateiverwaltung

- `ls`: Listet Dateien und Verzeichnisse auf.
- `cd`: Wechselt das Verzeichnis.
- `pwd`: Zeigt das aktuelle Arbeitsverzeichnis an.
- `touch`: Erstellt eine leere Datei.
- `mkdir`: Erstellt ein neues Verzeichnis.
- `cp`: Kopiert Dateien oder Verzeichnisse.
- `mv`: Verschiebt oder benennt Dateien oder Verzeichnisse um.
- `rm`: Löscht Dateien oder Verzeichnisse.
- `cat`: Zeigt den Inhalt einer Datei an.
- `less` oder `more`: Zeigt Dateien seitenweise an.
- `head` und `tail`: Zeigt den Anfang oder das Ende einer Datei an.

## Dateioperationen

- `touch`: Erstellt eine leere Datei.
- `cp`: Kopiert Dateien oder Verzeichnisse.
- `mv`: Verschiebt oder benennt Dateien oder Verzeichnisse um.
- `rm`: Löscht Dateien oder Verzeichnisse.

## Systeminformationen

- `uname`: Zeigt Informationen über das Betriebssystem an.
- `df`: Zeigt Informationen über die Festplattenbelegung an.
- `free`: Zeigt den verfügbaren Arbeitsspeicher an.
- `top`: Zeigt laufende Prozesse und Systemressourcen an.

## Benutzerverwaltung

- `who`: Zeigt angemeldete Benutzer an.
- `whoami`: Zeigt den aktuellen Benutzernamen an.
- `passwd`: Ändert das Passwort eines Benutzers.
- `useradd`: Fügt einen neuen Benutzer hinzu.
- `userdel`: Löscht einen Benutzer.
- `groups`: Zeigt Gruppenzugehörigkeiten an.

## Paketverwaltung

- `apt-get` (Debian/Ubuntu) oder `yum` (Red Hat/Fedora): Installiert, aktualisiert oder entfernt Softwarepakete.

## Netzwerk

- `ifconfig` oder `ip`: Zeigt Netzwerkkonfigurationen an.
- `ping`: Testet die Erreichbarkeit eines Hosts.
- `ssh`: Öffnet eine sichere Verbindung zu einem Remote-Server.
- `scp`: Kopiert Dateien über SSH.
- `wget` oder `curl`: Lädt Dateien aus dem Internet herunter.
- `netstat`: Zeigt Netzwerkstatistiken an.

## Prozessverwaltung

- `ps`: Zeigt laufende Prozesse an.
- `kill`: Beendet Prozesse.
- `killall`: Beendet Prozesse anhand des Namens.

## Archivierung und Komprimierung

- `tar`: Archiviert und extrahiert Dateien.
- `gzip` und `gunzip`: Komprimiert und dekomprimiert Dateien.
- `zip` und `unzip`: Arbeitet mit ZIP-Archiven.

## Textverarbeitung

- `grep`: Sucht nach Text in Dateien.
- `sed`: Stream Editor für Textmanipulation.
- `awk`: Textverarbeitungswerkzeug für Datenmanipulation.

## Berechtigungen

- `chmod`: Ändert Dateiberechtigungen.
- `chown`: Ändert Dateibesitzer und -gruppen.

## Hilfe und Dokumentation

- `man`: Zeigt die Handbuchseiten für Befehle an.
- `info`: Zeigt detaillierte Informationen zu Befehlen an.

   
## Ohmyz

```
sudo apt-get install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## createData.sh

```
#!/bin/bash

RANDOM_NUMBER=$(( ( RANDOM % 100 ) + 1 ))
RANDOM_CPP="main$RANDOM_NUMBER.cpp"

# Datei mit inhalt füllen, da sie ansonsten nicht commited werden
echo "Hier steht bald ganz wichtiger Code von der Datei $RANDOM_CPP" > $RANDOM_CPP

git add .
git commit -m "$RANDOM_CPP hinzugefügt"
git log --oneline --graph
```
