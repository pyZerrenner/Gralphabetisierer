# Gralphabetisierer

Ein Libre Office Writer Makro zur automatischen Transkription von Texten in das Greifensteiner Alphabet - das **_Gralphabet!_**

**!!! Erlaube nur Makros in Libre Office, denen du wirklich vertraust !!!**


## Installation

Installiere die Schriftart "Gralphabet" von der Datei "resources/Gralphabet-Font.ttf".
Sie muss in Libre Office verfügbar sein.


### Makros in Libre Office aktivieren

**!!! Erlaube nur Makros in Libre Office, denen du wirklich vertraust !!!**

1. Öffne Libe Office Writer und gehe ins Menü "Extras" > "Optionen"
2. Wähle "LibreOffice" > "Sicherheit" aus.
3. Klicke die Schaltfläche "Makrosicherheit...".
3. Setze die Sicherheits-Stufe zu "Mittel".

Beim Öffnen einer Datei mit Makros wird nun immer gefragt, ob die Ausführung von Makros erlaubt werden soll oder nicht.


## Verwendung

**!!! Erlaube nur Makros in Libre Office, denen du wirklich vertraust !!!**

1. Ersetze den Text in dem LO Writer Dokument "Gralphabetisierer.odt" mit dem zu transkribierenden Text.
   Der gesamte Text in dem Dokument wird transkribiert.
   
2. Klick auf die Schaltfläche "Gralphabetisieren"
	
   *ODER*
   
   Führe das Makro "Gralphabetisieren" aus: \
   Extras > Makros > Makros ausführen ... > Gralphabetisierer.odt > Standard > Gralphabetisierer > Gralphabetisieren
  
  
## Ablauf der Transkription

Die Transkription erfolgt in den folgenden Schritten:

 1. Konvertiere den gesamten Text zu Großbuchstaben
 2. Ersetze alle "GR" mit "g"
 3. Ersetze alle "ST" mit "t"
 4. ~~Ersetze alle "AU" mit "..."~~ *NOT YET IMPLEMENTED*
 5. ~~Ersetze alle "EU" mit "..."~~ *NOT YET IMPLEMENTED*
 6. Ersetze alle "EI" mit "i"
 7. Ersetze alle "SCH" mit "s"
 8. Ersetze alle "CH" mit "c"
 9. Ersetze alle "ẞ" mit "SS"
10. Änderung der Schriftart zu "Gralphabet"


### Bekannte Probleme

- Die Schriftzeichen für "AU" und "EU" sind noch nicht in der Schriftart implementiert.
- Vorkommen von "S-CH" werden als "SCH" transkribiert. \
   Z.B. "BISSCHEN" wird als "BIS-SCH-EN" transkribiert anstatt als "BISS-CH-EN".
- Der Anfang von Wörtern wird noch nicht durch "GR" erweitert.


## Referenzen für Makros in Libre Office
[LibreOffice Basic Help](https://help.libreoffice.org/latest/en-US/text/sbasic/shared/main0601.html?DbPAR=BASIC)

[Information and resources for LibreOffice macros](https://wiki.documentfoundation.org/Macros)

[LibreOffice 24.2 API Documentation](https://api.libreoffice.org/)

[Libre Office Basic examples](https://api.libreoffice.org/examples/examples.html#Basic_examples)


### Bearbeitung der Schaltfläche

1. Aktiviere den Entwurfsmodus im Menü "Formular".
2. Rechtsklick die Schatfläche für Optionen.
1. Deaktiviere den Entwurfsmodus im Menü "Formular".