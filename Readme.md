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
   
2. Zum Ersetzen der Anfangskonsonanten aller Wörter mit "Gr" bzw. "gr", klick auf die Schaltfläche "Gruffixieren".
   
   *ODER*
   
   Führe das Makro "Gruffixieren" aus: \
   Extras > Makros > Makros ausführen ... > Gralphabetisierer.odt > Standard > Gralphabetisierer > Gruffixieren
     
3. Zum Transkribieren des Textes in das Gralphabet, klick auf die Schaltfläche "Gralphabetisieren"
   
   *ODER*
   
   Führe das Makro "Gralphabetisieren" aus: \
   Extras > Makros > Makros ausführen ... > Gralphabetisierer.odt > Standard > Gralphabetisierer > Gralphabetisieren

## Ablauf der Gruffixierung

Die Gruffixierung eines Wortes erfolgt in den folgenden Schritten:

1. Finde den ersten Vokal im Wortes.
   Vokale sind definiert als a, e, i, o, u, ä, ö, ü und y (es geht hier um die Aussprache).
2. Ersetze alle Zeichen vor dem ersten Vokal mit
   - "Gr", falls das Wort groß geschrieben ist
   - "gr" falls das Wort klein geschrieben ist
3. Gibt es keinen Vokal in dem Wort, wird der erste Buchstabe des Wortes klein geschrieben und der ensprechende Suffix ("Gr"/"gr") dem Wort vorangestellt.
   Zum Beispiel word "Hmm" zu "Grhmm".

### Bekannte Probleme

- Falls mehrere Konsonat am Wortanfang Großbuchstabe sind weiterhin "Gr" statt "GR" verwendet.

## Ablauf der Gralphabetisierung

Die Gralphabetisierung erfolgt in den folgenden Schritten:

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


## Referenzen für Makros in Libre Office
[LibreOffice Basic Help](https://help.libreoffice.org/latest/en-US/text/sbasic/shared/main0601.html?DbPAR=BASIC)

[Information and resources for LibreOffice macros](https://wiki.documentfoundation.org/Macros)

[LibreOffice 24.2 API Documentation](https://api.libreoffice.org/)

[LO SDK API Reference](https://api.libreoffice.org/docs/idl/ref/namespacecom_1_1sun_1_1star.html)

[Libre Office Basic examples](https://api.libreoffice.org/examples/examples.html#Basic_examples)


### Bearbeitung der Schaltflächen

1. Aktiviere den Entwurfsmodus im Menü "Formular".
2. Rechtsklick die Schatfläche für Optionen.
1. Deaktiviere den Entwurfsmodus im Menü "Formular".