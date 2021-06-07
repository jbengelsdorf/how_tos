---
updated: 2021-06-03
author: jbengelsdorf
author_url: https://github.com/jbengelsdorf
---

# How To: Generate Content

## Was ist Content?

Content entspricht dem **Inhalt** des Experimentes, d. h. er umfasst primär Texte und Bilder, welche innerhalb des Experimentes präsentiert werden sollen.


## Instruktionen

Um die Instruktionen optimal in das Experiment einbinden zu können, sollten sie in Form einer **Python-Datei** bereitgestellt werden.
Eine solche Python-Datei kann sehr leicht mithilfe von **Sublime Text** erstellt werden. (Installation von Sublime Text: https://www.sublimetext.com/3)<br>
Nach der Installation von Sublime Text, kann Sublime Text geöffnet werden und es erscheint zunächst ein leeres Fenster. 
Wenn nun unten rechts auf "Plain Text" geklickt wird, kann "Python" ausgewählt werden. 
Nun kann für jeden Text eine Variable gemäß folgender Syntax eingefügt werden.

```python
begruessung = """
Liebe:r Versuchsteilnehmer:in,<br>
vielen Dank für Ihr Interesse an unserer Studie. Im Rahmen dieser Studie wird <b>XYZ</b> untersucht.
"""
```

Explizit entspricht die Synax dem Variablennamen (hier: begruessung), einem Gleichheitszeichen (=), drei Anführungszeichen ("""), dem zu präsentierenden Text und abschließend erneut drei Anführungszeichen ("""). Hierbei kann der Variablenname prinzipiell frei gewählt werden. Allerdings sollte der Variablenname keine Leerzeichen, keine Umlaute oder Großbuchstaben beinhalten. Beispielsweise wären "instr_1", "instr_textentry", "suspicion_check" oder "manipulation_check" sehr gute Variablennamen. Zusätzlich muss der Variablenname innerhalb der Datei einzigartig sein, sodass z.B. "begruessung" nur ein einziges Mal innerhalb der Datei als Variablenname verwendet wird.
Im Anschluss an eine Variable, kann direkt die nächste Variable deklariert werden:

```python
begruessung = """
Liebe:r Versuchsteilnehmer:in,<br>
vielen Dank für Ihr Interesse an unserer Studie. Im Rahmen dieser Studie wird <b>XYZ</b> untersucht.
"""

instruction = """
Dies ist die Instruktion.
"""

title1 = """
Begrüßung
"""
```

Innerhalb der Anführungzeichen kann HTML-Syntax (z.B. in Form von HTML-Tags) verwendet werden.<br>
Hier eine Auflistung der wichtigsten HTML-Tags im Kontext der Experiment-Erstellung:

```
<br>-Tag: Erzeugt einen Zeilenumbruch
<b>-Tag: Text, welcher von <b> und </b> umschlossen wird, wird fett präsentiert.
<u>-Tag: Text, welcher von <u> und </u> umschlossen wird, wird unterstrichen präsentiert
```

Abschließend oder zwischendurch kann die Python-Datei abgespeichert werden, indem in der Menü-Leiste von Sublime Text (oben) auf "File" und dann auf "Save as" geklickt wird.
Hierbei ist es wichtig darauf zu achten, dass die Datei auf **.py** endet. Als Dateiname empfielt sich z.B. "content", sodass die Datei final den Namen **content.py** trägt.

## Variierende Informationen

Variierende Informationen sind beispielsweise der Name der Bilddatei und die Beschreibung des Bildes, wenn sich das präsentierte Bild von Trial zu Trial unterscheidet.
Solche Daten müssen in Form einer **CSV-Datei** bereitgestellt werden. Eine CSV-Datei kann sehr leicht mithilfe von Excel erstellt werden. 
Hierfür kann bei Excel einfach eine normale Tabelle erstellt werden, wobei die erste Zeile für Überschriften verwendet werden sollte.
Nach Einfügen der Daten kann in der Menü-Leiste von Excel auf "Datei", "Speichern unter" geklickt werden und anschließend beim Dateiformat **CSV UTF-8** ausgewählt werden.

## Bilder

Bilder sollten gesammelt in einem Ordner in gängigen Dateiformaten (z.B. png, jpg) und mit möglichst komprimierter Dateigröße vorliegen.
Beispielsweise eignen sich geteilte **Owncloud-Ordner** sehr gut, um die Bilder zur Verfügung zu stellen.<br>
Die Bezeichnungen der Bild-Dateien sollten **keine Umlaute** beinhalten und einer **logischen Benennung** folgen (z.B. bild_001, bild_002, etc.).<br>
Sofern in Abhängikeit des präsentierten Bildes bestimmte Werte (z.B. Bezeichnungen, wahre Werte, etc.) präsentiert oder gespeichert werden sollen, sollten diese variierenden Informationen als **CSV-Datei** bereitgestellt werden. (Siehe: "Variierende Informationen")

## Checkliste
+ Sind alle innerhalb des Experimentes zu präsentierende Texte in einer **Python-Datei** vorzufinden? <br>
+ Liegen alle variierenden Informationen in Form einer **CSV-Datei** vor?<br>
+ Befinden sich alle Bilder in einem **geteilten Ornder** und sind **logisch, ohne Umlaute** benannt?

