# Beleg webbasiertes Lernprogramm

## Übersicht
Als Beispiel für eine Progressive Web App (PWA) soll ein webbasiertes Lernprogramm zum Lernen von Noten erstellt werden.
Der Beleg dient zur praktischen Anwendung der Kenntnisse zu HTML, CSS und Javascript. Die Umsetzung als PWA ermöglicht auch die einfache und komfortable Nutzung in mobilen Geräten. 


## Beschreibung
Das Lernprogramm soll mindestens folgende Funktionalität besitzen:
- zufällige Auswahl und Darstellung einer Note mit 4 Auswahlmöglichkeiten
- Anzeige des Lernfortschritts
- Wahl zwischen Violin- und Bassschlüssel
- Anzeige einer Statistik am Ende eines Durchlaufs
- neue Lernmodule sollten sich von einem Webserver per Ajax laden lassen
- die Anzeige sollte sich an verschiedene Anzeigegeräte sinnvoll anpassen


## Technische Umsetzung
- nutzen Sie für die Umsetzung HTML5/CSS3/JS 
- nutzen Sie in JS den strikten Modus 
- der Beleg sollte im aktuellen Firefox oder Google Chromium lauffähig sein, es wird keine Abwärtskompatibilität erwartet
- entsprechend einer PWA sollte die Anwendung auch offline funktionieren und sich installieren lassen
- vermeiden Sie nach Möglichkeit weitere Frameworks wie jquery, Bootstrap etc. und versuchen Sie die Funktionalität von ECMAScript und CSS3 in den aktuellen Browsern auszunutzen
- Als Entwicklungsumgebung empfiehlt sich die Nutzung der Entwickertools im Browser Chromium
- zum Testen Funktionalität auf einem Smartphone kann die Device Toolbar in o.g. Entwickertools genutzt werden
- für die grafische Notendarstellung sollte die JS-Bibliothek [Vexflow](https://github.com/0xfe/vexflow) mit der Notensprache EasyScore genutzt werden
- das Format der vom Server nachladbaren Fragen ist JSON entsprechend folgendem Fragment (a - Aufgabe für Violinschlüssel, l - Lösungen, die erste ist korrekt ):
```
 	var aufg = { 
	  note: [
  	  {"a":"C4", "b":"C2", "l":["C","D","E","H"]},
  	  {"a":"D4", "b":"D2", "l":["D","C","G","F"]},
  ], 
  };
```
- Aufgaben für den Bassschlüssel können durch Transformation der gegebenen Aufgaben um zwei Oktaven nach unten abgeleitet werden


## Mögliche Erweiterungen
- Notenbezeichnungen wahlweise deutsch oder englisch
- Wichtung der Aufgabenstellung anhand der bisherigen Ergebnisse
- Auswahl der Fragen zwischen Einzelnoten, Akkorden mit Umkehrungen und Septakkorden mit Umkehrungen
- Rhythmusübungen (vorgegebener Takt im Notenbild  und entsprechendes drücken einer Taste)
- Nutzerverwaltung