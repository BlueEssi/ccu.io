CCU.IO
======

*aktuelle Version: 1.0.18*

## Dokumentation

siehe http://ccu.io/


## Todo/Roadmap

* adapter/skeleton-ipc.js
* Prozesse überwachen (und evtl abgestürzte Adapter/Script-Engine neu starten?)
* Log über Weboberfläche ansehen (tail)
* Logrotate für ccu.io.log
* settings.html für diverse Adapter
* diverse Adapter auf ipc umstellen?
* Pushover Callbacks (Nachrichten bestätigen, callback Methode aufrufen)
* Weboberfläche Ladeanzeige
* Weboberfläche Datenpunkte anlegen, löschen
* Weboberfläche Devices in Baumstruktur anzeigen
* Weboberfläche Objekte neu laden wenn CCU.IO neue Objekte von Adaptern/Scripts erhalten hat
* Persistente Objekte in regaIndex aufnehmen!
* ArtNet (DMX) Adapter
* Rocket LED Adapter
* iTunes Adapter
* Script-Engine Addins (von Addons "mitgebrachte" Methoden)?
* Anymote Adapter (control Google TV)
* Doku, Doku, Doku
* CMS für Homepage?
* CCU2-Paket für einfache Installation
* .msi für einfache Installation unter Windows (ccu.io als Service registrieren)
* .pkg für einfache Installation unter Mac OS X
* BIN-RPC Implementierung vervollständigen
* rega.js weiter ausbauen (... Variablen/Räume/Gewerke anlegen/bearbeiten/löschen/umbenennen, Geräte/Kanäle umbenennen, Favortien anlegen/bearbeiten/löschen/umbenennen, Kanäle/Variablen/Programme zu Favoriten zuordnen, ......? -> wäre notwendig für Portierung von "HQ WebUI" auf CCU.IO

## Changelog

### 1.0.18
* (Hobbyquaker) Bugfix SlimUI Install

### 1.0.17
* (Hobbyquaker) neue SimpleAPI Methode: getBulk
* (Hobbyquaker) SlimUI zu Addon-Install hinzugefügt
* (Hobbyquaker) Bugfix: Adapter-Restart wenn Beenden des Prozesses fehlschlägt
* (Bluefox) Add /lang/lang.js to get CCU.IO language
* (Bluefox) Translate jsGrid
* (Thorque) Refactored yamaha adapter. Contains now out of a service with a small api and some tests.

### 1.0.16
* (Eisbaeeer) Node Modul piface-node hinzugefügt
* (Hobbyquaker) Bugfix: Encoding von Datenpunkt-Namen

### 1.0.15
* (Hobbyquaker) Bugfix File Uploads via https
* (Hobbyquaker) Update Highstock 1.3.9
* (Eisbaeeer) Adapter Onkyo: Update 0.9.2

### 1.0.14
* (Bluefox) Backup über Weboberfläche
* (Bluefox) Mehrsprachigkeit
* (Bluefox) diverse Änderungen/Neuerungen/Bugfixes Adapter Sonos, SayIt, LGTV, Fritzbox, Ping
* (BasGo) Adapter Dreambox v0.8
* (Vader722) Adapter iCal: Style-Anpassungen
* (Eisbaeeer) Adapter rpi: Unterstützung für PiFace
* (Thorque) Neuer Adapter: yamaha (AV-Receiver)
* (Hobbyquaker) Neuer Adapter: growl

### 1.0.13
* (Eisbaeeer) adapter Onkyo: Added array to command variable, major changes to variables (split to feedback and set variables)
* (Eisbaeeer) adapter Onkyo: Small bugfix setVar, Remove function to empty set var
* (Vader722) adapter iCal: bugfix for fulltime dates
* (Vader722) adapter iCal: new code for processing dates, now full-time dates working
* (BasGo) adapter Dreambox: fixed issue that some objects are stored
* (BasGo) adapter Dreambox: fixed error and added documentation
* (BasGo) adapter Dreambox: fixed bool recognition for openwebif
* (BasGo) adapter Dreambox: multiple boxes and some small fixes

### 1.0.12
* (Bluefox) new listen adapter (not finished yet)
* (Bluefox) new textCommand adapter (not finished yet)
* (Bluefox) Add hmSelectDialog to www/lib/js
* (Bluefox) Listen and textCommand adapters improving. (not yet finished)
* (Bluefox) Changes for sayIt and listen adapters.
* (Bluefox) Add cache properties for Web Server of ccu.io.js
* (Bluefox) Remove warnings if security for non SSL enabled
* (Bluefox) Adapter Fritzbox: Add HTML table for missed calls
* (Bluefox) Adapter Fritzbox: Add new data point ringing number.
* (Bluefox) Adapter Fritzbox: Add description for RINGING_NUMBER.
* (Bluefox) Edit adapter_ids.txt

### 1.0.11
* (Hobbyquaker) Adapter rpi: Standalone-Modus
* (Hobbyquaker) Adapter rpi: Datenpunkte für RAM und Swap Usage
* (Hobbyquaker) Adapter rpi: Unterstützung für 1-Wire Temperatur-Sensoren
* (Hobbyquaker) Neue Socket.IO Methode "log" für standalone-adapter logging
* (Vader722) Adapter iCal: now reading up to 3 calendar, custom font color, changeable fulltime
* (Vader722) Adapter iCal: fixed syntax
* (Vader722) Adapter iCal: another syntax fix
* (Vader722) Adapter iCal: logging in case of error
* (BasGo) added new adapters for Dreambox and Fritzbox
* (Eisbaeeer) Adapter Onkyo: Added array to command variable, major changes to variables (split to feedback and set variables)

### 1.0.10
* (Hobbyquaker) Neuer Adapter: Telnet-Client
* (Hobbyquaker) Lirc-Adapter ....
* (Hobbyquaker) LogMove via node-schedule, Vorbereitung für ccu.io.log
* (Hobbyquaker) Adapter können nun einzeln neu gestartet werden
* (Eisbaeeer) Neuer Adapter: Onkyo


### 1.0.9
* (Hobbyquaker) Bugfix rega post request errors
* (Hobbyquaker) Bugfix saving of persitent objects and datapoints
* (Bluefox) Fix error with volume for SayIt adapter


### 1.0.8
* (Bluefox) execScript() - fork Node Child-Process - required for Browse function (Sonos, LGTV)
* (Bluefox) SayIT adapter: Support volume for system …	8c0fda7
* (Bluefox) Shift firstId for LG Tv, because of conflict with LIRC	ec7099c
* (Bluefox) Fix small errors for browser function (LG TV and Sonos)	bf48aed
* (Bluefox) Add disk usage to RPi Adapter (only for "/")
* (Hobbyquaker) fehlendes Node-Modul "lazy-socket" ergänzt (benötigt für Graphite Adapter)

### 1.0.7
* (Bluefox) New adapter: LG TV, to control LG tv over ethernet
* (Bluefox) Browse function for SONOS adapter by settings
* (Bluefox) SayIt adapter changed: first user variable is 72910, new variable 72903 to output the text over all configured variables, MP24 settings for every variable (to control different Tablets and Android devices)
* (Vader722) Adapter iCal, Bugfixes, farbliche Hervorhebungen, debugging

### 1.0.6
* (Hobbyquaker) neuer Adapter: LIRC
* (Hobbyquaker) neuer Adapter: Graphite
* (Hobbyquaker) Adapter MySQL Bugfix
* (Hobbyquaker) several Bugfixes
* (Hobbyquaker) persistent Objects and Datapoints (save on quit)
* (Hobbyquaker) Bugfix getState()
* (Hobbyquaker) Adapter muell_stuttgart: Konfigurationsseite


### 1.0.5
* (Hobbyquaker) Neue Methode touchFile
* (Hobbyquaker) rpi Adapter: fixed settings.json - added firstId
* (Bluefox) SayIt Adapter: Support of mixer settings for raspberry PI
* (Bluefox) SayIt Adapter: Support of new config concept and support of playing sound on Windows and linux servers.


### 1.0.4
* (Hobbyquaker) CCU.IO kann sich nun selbst updaten
* (Hobbyquaker) Neue Script-Methode getState()
* (Hobbyquaker) Bugfix settings.js
* (Hobbyquaker) fehlendes gpio Modul für rpi-Adapter hinzugefügt
* (Hobbyquaker) Bugfix: STATE DP erlaubt nun numerische Werte
* (Bluefox) sayit-Adapter: FTP option by sayit.js
* (Bluefox) sonsos-Adapter: New sonos version. Mute function
* (Vader722) iCal-Adapter: Adapter kann im Intervall den Kalender einlesen
* (Vader722) iCal-Adapter: Datum und Uhrzeit der Termine jetzt Bold Font


### 1.0.3
* (Hobbyquaker) Adapter rpi unterstützt nun GPIOs
* (Hobbyquaker) Addon-Update an neue Addon-Verzeichnisstruktur angepasst
* (vader722) Neuer Adapter iCal
* (Hobbyquaker) Bugfix update-addon.js - warten bis unzip fertig ist
* (Hobbyquaker) CCU.IO Update. Noch nicht in Weboberfläche verfügbar aber kann über "node update-self.js" manuell aufgerufen werden

### 1.0.2
* (Bluefox) ID des sayit Adapter verschoben
* (Bluefox) SayIt supports Home24-MediaPlayer
* (vader722) Neuer Adapter IRTrans

### 1.0.1
* (Hobbyquaker) neuer Adapter: rpi - liest loadavg und Temperatur aus (nur für RaspberryPi) - TODO Freier Speicher und GPIOs
* (Hobbyquaker) Start-Verhalten geändert, Adapter werden nun mit größeren Pausen aufgerufen, Script-Engine als letztes.
* (Hobbyquaker) Fehler in logger.js abgefangen. Hat u.U. zu einem CCU.IO Crash geführt
* (Hobbyquaker) Addon-Update-Funktion mit Pausen ausgestattet, sollte zuverlässiger laufen
* (Hobbyquaker) Bugfix: global.js wurde u.U. 2x von der Script-Engine geladen
* (Hobbyquaker) Addon-Update-Funktion: alert-popup wenn Update-Script beendet ist
* (Hobbyquaker) Addon-Update-Funktion: Bugfix beim Versionsnummern-Vergleich
* (Hobbyquaker) muell_stuttgart Adapter ausgearbeitet, settings.html angelegt
* (Bluefox) Neuer Adapter "sayit" (Text-to-Speech)
* (Bluefox) settings.html für Sonos und Ping Adapter
* (Bluefox) Mark enabled Adapters with bold green text

### 1.0.0
* (Bluefox) neuer Adapter: Sonos
* (Bluefox) Bugfix Ping-Adapter unter Windows
* (Hobbyquaker) settings-System umgebaut. Es müssen nun keine Dateien mehr editiert werden. Es gibt keine settings-dist mehr.
* (Hobbyquaker) neue Methode getNextId - gibt nächste freie ID zurück, Start-Wert kann als Parameter übergeben werden
* (Hobbyquaker) neues Objekt-Attribut _persistent - sorgt dafür das Objekte auch nach einem CCU.IO Neustart mit der gleichen ID erhalten bleiben
* (Hobbyquaker) Start-Verhalten geändert. Webserver startet immer sofort, Adapter und Script-Engine erst wenn Rega-Daten geladen sind oder sofort falls CCU nicht erreichbar ist
* (Hobbyquaker) Addon-Update nun via nodejs - funktioniert nun auf allen Plattformen
* (Hobbyquaker) Addon-Installation über die Weboberfläche
* (Hobbyquaker) Möglichkeit CCU.IO über die Oberfläche neu zu starten
* (Hobbyquaker) Methode readRawFile fügt keine Anführungszeichen mehr hinzu
* (Hobbyquaker) Anzeige ob CCU erreichbar ist, ob ReGa läuft, ob Daten geladen sind, ob Inits durchgeführt wurden
* (Hobbyquaker) Unterordner ccu.io entfernt, alles verschoben
* (Hobbyquaker) _global.js entfernt. Script-Engine ruft nun global.js auf.
* (Hobbyquaker) Versions-Nummern Check beim Addon-Update verbessert
* (Hobbyquaker) Toolbar-Filter in Event-Tabelle jetzt case-insensitive und "contains-suche"


### 0.9.87
* (Hobbyquaker) fehlende jQuery UI Themes hinzugefügt (hat dazu geführt dass DashUI >= 0.9beta39 nicht mehr funktioniert hat)
* (Bluefox) Ping Adapter: minimal-Intervall wird geprüft
* (Smiling-Jack) readdirStat Methode: fängt leere Verzeichnisse ab

### 0.9.86
* (Hobbyquaker) Hue-Adapter: Colormode-Wechsel verbessert, Bugfixes

### 0.9.85
* (Hobbyquaker) Bugfixs re-init
* (Hobbyquaker) Adapter Geofency Geräte-Definition geändert, Datum formatiert
* (Hobbyquaker) Adapter DWD, Bugfixes, Datum formatiert
* (Smiling-Jack) neue Methode readdirStat

### 0.9.84
* (Hobbyquaker) Neuer Adapter Geofency

### 0.9.83
* (Hobbyquaker) Neuer Adapter DWD Wetterwarnungen
* (Hobbyquaker) Bugfix ALDPs

### 0.9.82
* (Hobbyquaker) Simple-API Methode setBulk nun auch via POST nutzbar
* (Hobbyquaker) metaScripts Variable von settings.js nach ccu.io.js verlagert
* (Hobbyquaker) abfangen fehlender Optionen in settings.js

### 0.9.81
* (Hobbyquaker) neue Methode writeRawFile(path, content, callback) - path relativ zum ccu.io Verzeichnis

### 0.9.80
* (Hobbyquaker) Methode setObject legt nicht vorhandene Räume/Gewerke/Favoriten an
* (Hobbyquaker) Neuer Adapter: Pushover (keine Datenpunkte - steht in Script-Engine zur Verfügung)
* (Hobbyquaker) Neuer Adapter: Email (keine Datenpunkte - steht in Script-Engine zur Verfügung)
* (Hobbyquaker) Bugfix in clearRegaData Methode
* (Hobbyquaker) Bugfixes Script-Engine

### 0.9.79
* (Hobbyquaker) Bugfix re-init

### 0.9.78
* (Bluefox) Socket.io Authentication
* (Hobbyquaker) clearRegaData Methode hinzugefügt für reloadRegaData und reconnect
* (Hobbyquaker) Bugfixes

### 0.9.77
* (Hobbyquaker) Default id des rego-Adapter geändert
* (Hobbyquaker) Funktion hinzugefügt die prüft ob noch Events empfangen werden und ggf erneuten RPC Init durchführt
* (Hobbyquaker) diverse Bugfixes
* (Hobbyquaker) Hue Adapter umgebaut, nutzt nun nicht mehr das Modul node-hue-api

### 0.9.76
* (Anli) rego-Adapter added (adapter for ivt rego 600series heating controller)
* (Hobbyquaker) Bugfixes Logging
* (Hobbyquaker) added Logging of virtual Variables
* (Hobbyquaker) Bugfix Hue Adapter

### 0.9.75
* (Hobbyquaker) Ping Adapter: bool statt string als value, Punkte aus IP-Adresse werden in Name/Address Attributen durch Unterstriche ersetzt

### 0.9.74
* (Bluefox) Fix Debug Mode
* (Bluefox) added Ping Adapter

### 0.9.73
* (Hobbyquaker) Bugfix es wurden immer wieder überflüssige Adapter-Prozesse gespawnt

### 0.9.72

* (Hobbyquaker) Bugfix setObject - hat u.U. dazu geführt das Kanäle mehrfach zu den selben Räumen/Gewerken/Favoriten zugeordnet wurden

### 0.9.71

* (Hobbyquaker) Hue Adapter: Bugfix Polling
* (Hobbyquaker) Hue Adapter: Fallunterscheidung "Dimmable Plug-In Unit" (Zwischensteck-Dimmer)

### 0.9.70

* (Hobbyquaker) Bugfix Steuerung HM-CC-TC
* (Hobbyquaker) setState Methode akzeptiert nun auch Namen oder Adressen statt IDs
* (Hobbyquaker) setObject Methode können Räume, Gewerke und Favoriten mitgegeben werden
* (Hobbyquaker) Hue Adapter: Lampen können nun Räumen, Gewerken und Favoriten zugeordnet werden
* (Hobbyquaker) Hue Adapter: Fallunterscheidung "Color Light" (LivingColors) und "Extended Color Light" (Hue) - nur verfügbare Datenpunkte werden angelegt
* (Hobbyquaker) Hue Adapter: Status Polling


### 0.9.69

* (Stryke) Installer: Non root ccu.io update and CCUIO_UPDATE parameter
* (Hobbyquaker) neuer Adapter: Hue
* (Hobbyquaker) Bugfix: Fehler beim Laden der Stringtable (betrifft nur CCU1)

### 0.9.68

* (Hobbyquaker) Übersetzung der stringtable (nur bei CCU2)

### 0.9.67

* (Stryke) Installer: Bugfix für QNAP
* (Hobbyquaker) Simple API: neue Methode setBulk (setzen mehrerer Datenpunkte auf einmal)
* (Hobbyquaker) Script-Engine: neue Datei _global.js für Funktionen die in mehreren Scripts genutzt werden
* (Hobbyquaker) Script-Engine: Beispiel-Scripts hinzugefügt
* (Hobbyquaker) diverse Bibliotheken zu www/lib hinzugefügt

### 0.9.66
* (Hobbyquaker) neue Methode delRawFile
* (Hobbyquaker) www/lib/jquery-1.10.2.min.js ausgetauscht, map File hinzugefügt

### 0.9.65
* (Hobbyquaker) Bugfix datapoints.fn
* (Hobbyquaker) channels.fn STATE Datenpunkt von SMOKE_DETECTOR hinzugefügt

### 0.9.64
* (Hobbyquaker) datapoints.fn STATE Datenpunkt von SMOKE_DETECTOR hinzugefügt

### 0.9.63
* (Hobbyquaker) Alarm-Datenpunkte hinzugefügt


### 0.9.62
* (Hobbyquaker) diverse Dateien zum Verzeichnis /www/lib hinzugefügt
* (Stryke) Bugfixes Installer

### 0.9.61
* (Hobbyquaker) diverse kleine Verbesserungen und Bugfixes
* (Hobbyquaker) Update-Button in der Addon-Tabelle (falls neue Version zur Verfügung steht). Ruft install/ccu.io.install.sh auf
* (Hobbyquaker) neuer Button unter CCU.IO->Control um RPC Inits zu erneuern
* (Hobbyquaker) neue Anzeige unter CCU.IO->Info: Zeit seit letztem Event

### 0.9.60
* (Hobbyquaker) Erkennen ob CCU erreichbar/nicht erreichbar/wieder erreichbar ist

### 0.9.59
* (Hobbyquaker) Bugfixes

### 0.9.58
* (Stryke) Installer: Laufende ccu.io Erkennung endgültig gefixt

### 0.9.57
* (Hobbyquaker) Bugfix: File Upload funktionierte u.U. nicht
* (Hobbyquaker) Bugfix: PRESS_SHORT, PRESS_LONG und PRESS_OPEN funktionierte nicht
* (Stryke) Installer: Laufende ccu.io erkennung verbessert

### 0.9.56
* (Hobbyquaker) Bugfix "Hänger" beim Beenden von CCU.IO
* (Stryke) Installer: Parameter gesteuerter Aufruf und Config Datei


### 0.9.55
* (Hobbyquaker) Neue Methode "getPlainValue" in Simple API
* (Hobbyquaker) Tool hinzugefügt um CUxD Logs ins CCU.IO-Format zu konvertiern

### 0.9.54
* (Hobbyquaker) "Simple API" implementiert, einfaches Abfragen und Setzen von Werten/Objekten via HTTP GET (executeProgram noch nicht implementiert)

### 0.9.53
* (Hobbyquaker) Bugfix Werte an CCU senden (impact z.B. bei RAMP_TIME Datenpunkt)

### 0.9.52
* (Hobbyquaker) Bugfix in setObject Methode
* (Hobbyquaker) Neue Datenpunkte yr-Adapter (rain24h, rain48h, minTemp24h, maxTemp24h, minTemp48h, maxTemp48h)

### 0.9.51

* (Hobbyquaker) Oberfläche weiter ausgebaut
* (Stryke) Bugfix Startscript

### 0.9.50
* (Stryke) Installer v0.3.1

### 0.9.49
* (Hobbyquaker) Der Wert eines Datenpunkts kann nun direkt in der CCU.IO Oberfläche bearbeitet werden
* (Hobbyquaker) Bugfix Button reloadScriptEngine
* (Hobbyquaker) automatisches Anpassen der datapoints und events Ansicht an Browser Breite/Höhe

### 0.9.48

* (Hobbyquaker) Bugfix für Variablen 41 und 40 (Anzahl Alarm- und Servicemeldungen)

### 0.9.47

* (Hobbyquaker) Zeitmodul mit Astro-Funktion für die Script-Engine
* (Hobbyquaker) Neue Optionen longitude und latitude in settings.js (wird für Astrofunktion benötigt)
* (Hobbyquaker) BIN-RPC Bug behoben (hatte kein Impact, hat aber unschöne Log-Meldung generiert)
* (Hobbyquaker) fehlende Dateien in ccu.io/www/lib ergänzt, führte dazu dass die Reiter datapoints und events in der CCU.IO-Oberfläche leer waren

### 0.9.46

* (Hobbyquaker) setValue nun (wenn möglich) via binrpc statt ReGa
* (Hobbyquaker) Neue Methode setObject() in script-engine
* (Hobbyquaker) Polling Trigger implementiert (über virtuelle Taste kann sofortiges Pollen der Variablen angestoßen werden)
* (Hobbyquaker) wenn regaObject[id].dontLog wird kein Logging durchgeführt
* (Hobbyquaker) Neue Option für MySQL-Adapter: nur geänderte Datenpunkte loggen


### 0.9.45

* (Hobbyquaker) Beenden der Kind-Prozesse (Adapter, Script-Engine) beim Beenden von CCU.IO
* (Hobbyquaker) diverse Kleinigkeiten, Bugfixes
* (Hobbyquaker) Variable 40 und 41 (Anzahl Servicemeldungen und Anzahl Alarme) zu variables.fn hinzugefügt
* (Hobbyquaker) Neue Methode setObject
* (Hobbyquaker) MySQL-Adapter: Variablen werden nur bei Änderungen in event-Tabelle geschrieben
* (Hobbyquaker) Bugfix MySQL-Adapater: ValueUnit wurde nicht in Datenbank geschrieben

### 0.9.44
* (Hobbyquaker) MySQL-Adapter ausgearbeitet

### 0.9.43
* (Hobbyquaker) Bei Änderungen an SET_TEMPERATURE und MANU_MODE nächsten temp und mode Event vom Thermostat ignorieren
* (Hobbyquaker) Neuer Adapter für Logging in MySQL Datenbank

### 0.9.42
* (Stryke) Installer/Updater v0.1 integriert

### 0.9.41

* (Hobbyquaker) Script-Engine ausgearbeitet und Dokumenation begonnen (steckt in scripts/example.js)

### 0.9.40

* (Hobbyquaker) Script-Engine implementiert (proof-of-concept, wird sich noch einiges ändern!)

### 0.9.39

* (Hobbyquaker) Adapter implementiert
* (Hobbyquaker) Basic Auth füt http und https getrennt aktivierbar

### 0.9.38

* (Hobbyquaker) Bugfix wenn settings.authentication in settings.js fehlt
* (Hobbyquaker) Bugfixes wenn ioListenPort fehlt (Betrieb nur mit ssl)

### 0.9.37

* (Bluefox) SSL Support
* (Bluefox) Basic Auth

### 0.9.36

* (Hobbyquaker) Bugfix file upload

### 0.9.35

* (Hobbyquaker) Anonymisierungs-Funktion anonymisiert nun auch Adressen
* (Hobbyquaker) fehlende Node-Module hinzugefügt, überflüssige entfernt
* (Hobbyquaker) Speichern von nicht-json-Dateien im Datastore verhindert

### 0.9.34

* (Hobbyquaker) fehlende Dateien ergänzt

### 0.9.33

* (Hobbyquaker) neue CCU.IO Oberfläche
* (Hobbyquaker) Button in CCU.IO Oberfläche um Objekte neu von der CCU zu laden (damit man nicht immer neustarten muss nach Änderungen auf der CCU)
* (Hobbyquaker) Button zum "anonymisieren" von regaObjects und regaIndex (aus-x-en der BidCos-Adressen)


## Lizenz

Copyright (c) 2013-2014 hobbyquaker [http://hobbyquaker.github.io](http://hobbyquaker.github.io)

Lizenz: [CC BY-NC 3.0](http://creativecommons.org/licenses/by-nc/3.0/de/)

Sie dürfen das Werk bzw. den Inhalt vervielfältigen, verbreiten und öffentlich zugänglich machen,
Abwandlungen und Bearbeitungen des Werkes bzw. Inhaltes anfertigen zu den folgenden Bedingungen:

  * **Namensnennung** - Sie müssen den Namen des Autors/Rechteinhabers in der von ihm festgelegten Weise nennen.
  * **Keine kommerzielle Nutzung** - Dieses Werk bzw. dieser Inhalt darf nicht für kommerzielle Zwecke verwendet werden.

Wobei gilt:
Verzichtserklärung - Jede der vorgenannten Bedingungen kann aufgehoben werden, sofern Sie die ausdrückliche Einwilligung des Rechteinhabers dazu erhalten.

Die Veröffentlichung dieser Software erfolgt in der Hoffnung, daß sie Ihnen von Nutzen sein wird, aber OHNE IRGENDEINE GARANTIE, sogar ohne die implizite Garantie der MARKTREIFE oder der VERWENDBARKEIT FÜR EINEN BESTIMMTEN ZWECK. Die Nutzung dieser Software erfolgt auf eigenes Risiko!