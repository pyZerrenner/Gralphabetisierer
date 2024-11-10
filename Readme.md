# Gralphabetisierer

Libre Office Writer Makros zur automatischen Umsetzung der Greifensteiner Sprache
- Gräfixieren: Ersetze die Angangskonsonanten eines Wortes mit "Gr"
- Gralphabetisieren: Transkription in das Greifensteiner Alphabet - das **_Gralphabet!_**

**!!! Erlaube nur Makros in Libre Office, denen du wirklich vertraust !!!**


## Installation

1. Installiere [Libre Office](https://www.libreoffice.org/).
2. Installiere die Schriftart "Gralphabet" von der Datei "resources/Gralphabet-Font.ttf".
   Die Schriftart wurde von Helmfried, Burggraf der Herbstburt, erstellt.


### Makros in Libre Office aktivieren

**!!! Erlaube nur Makros in Libre Office, denen du wirklich vertraust !!!**

1. Öffne Libe Office Writer und gehe ins Menü "Extras" > "Optionen"
2. Wähle "LibreOffice" > "Sicherheit" aus.
3. Klick die Schaltfläche "Makrosicherheit...".
3. Setze die Sicherheits-Stufe zu "Mittel".

Beim Öffnen einer Datei mit Makros wird nun immer gefragt, ob die Ausführung von Makros erlaubt werden soll oder nicht.


## Verwendung

**!!! Erlaube nur Makros in Libre Office, denen du wirklich vertraust !!!**

1. Ersetze den Text in dem LO Writer Dokument "Gralphabetisierer.odt" mit deinem Text.
   Der gesamte Text in dem Dokument wird bearbeitet.
   (Der Beispieltext in dem Dokument wurde mittels ChatGPT generiert.)

2. Zum Ersetzen der Anfangskonsonanten aller Wörter mit "Gr" bzw. "gr", klick auf die Schaltfläche "Gräfixieren".
   
   *ODER*
   
   Führe das Makro "Graefixieren" aus: \
   Extras > Makros > Makros ausführen ... > Gralphabetisierer.odt > Standard > Gralphabetisierer > Graefixieren

3. Zum Transkribieren des Textes in das Gralphabet, klick auf die Schaltfläche "Gralphabetisieren"
   
   *ODER*
   
   Führe das Makro "Gralphabetisieren" aus: \
   Extras > Makros > Makros ausführen ... > Gralphabetisierer.odt > Standard > Gralphabetisierer > Gralphabetisieren

## Ablauf der Gräfixierung

Die Gruffixierung eines Wortes erfolgt in den folgenden Schritten:

1. Finde den ersten Vokal im Wortes.
   Vokale sind definiert als a, e, i, o, u, ä, ö, ü und y (es geht hier um die Aussprache).
2. Ersetze alle Zeichen vor dem ersten Vokal mit
   - "Gr", falls das Wort groß geschrieben ist.
     Ein groß geschriebener Vokal am Wortanfang wird in einen Kleinbuchstaben umgewandelt.
   - "gr" falls das Wort klein geschrieben ist
3. Gibt es keinen Vokal in dem Wort, wird der erste Buchstabe des Wortes klein geschrieben und der ensprechende Suffix ("Gr"/"gr") dem Wort vorangestellt.
   Zum Beispiel "Hmmm" wurd zu "Grhmmm".

### Bekannte Probleme

- Großbuchstaben innerhalb eines Wortes (z.B. ein Wort in NUR Großbuchstaben) werden nicht unterstützt.
  Sie erhalten den normalen Präfix "Gr" ("NUR" wird zu "GrUR").
- Nicht ausgeschriebene Zahlen sind nicht unterstützt.
  Z.B. "15 Äpfel" wird zu "Gr15 Gräpfel", aber "Fünfzehn Äpfel" wird zu "Grünfzehn Gräpfel".
- Abkürzungen sollten vermieden werden bzw. erst nach der Gräfixierung eingeführt werden.
  Z.B. "Jhd." wird zu "Grjhd.", aber "Jahrhundert" wird zu "Grahrhundert" und kann dann als "Grhd." abgekürzt werden (abgesehen davon wird in der Greifensteiner Sprache das Wort "Hundergrutzend" bevorzugt).

## Ablauf der Gralphabetisierung

Die Gralphabetisierung erfolgt in den folgenden Schritten:

 1. Konvertiere den gesamten Text zu Großbuchstaben
 2. Ersetze alle "GR" mit "g"
 3. Ersetze alle "ST" mit "t"
 4. ~~Ersetze alle "AU" mit "..."~~ *NOCH NICHT IMPLEMENTIERT*
 5. ~~Ersetze alle "EU" mit "..."~~ *NOCH NICHT IMPLEMENTIERT*
 6. Ersetze alle "EI" mit "i"
 7. Ersetze alle "SCH" mit "s"
 8. Ersetze alle "CH" mit "c"
 9. Ersetze alle "ẞ" mit "SS"
10. Änderung der Schriftart zu "Gralphabet"

### Bekannte Probleme

- Die Schriftzeichen für "AU" und "EU" sind noch nicht in der Schriftart implementiert.
- Ziffern sind in der Schriftart nicht implementirt.
  Es sollten ausgeschriebene Zahlen verwendet werden.
- Vorkommen von "S-CH" werden immer als "SCH" transkribiert. \
   Z.B. "BISSCHEN" wird als "BIS-SCH-EN" transkribiert anstatt als "BISS-CH-EN".


## Referenzen für Makros in Libre Office
[LibreOffice Basic Help](https://help.libreoffice.org/latest/en-US/text/sbasic/shared/main0601.html?DbPAR=BASIC)

[Information and resources for LibreOffice macros](https://wiki.documentfoundation.org/Macros)

[LibreOffice 24.2 API Documentation](https://api.libreoffice.org/)

[LO SDK API Reference](https://api.libreoffice.org/docs/idl/ref/namespacecom_1_1sun_1_1star.html)

[Libre Office Basic examples](https://api.libreoffice.org/examples/examples.html#Basic_examples)


### Bearbeitung der Schaltflächen

1. Aktiviere den Entwurfsmodus im Menü "Formular".
2. Linksklick die Schaltfläche zur Positionierung. \
   Rechtsklick die Schatfläche zur Auswahl von Optionen.
1. Deaktiviere den Entwurfsmodus im Menü "Formular".