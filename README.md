# YOC-2024

Hier ist der Export unserer Assembly aus dem Hub.

Könnte als Grundlage für nächstes Jahr hergenommen werden.

Es funktioniert Markdown so:

Diese Seite beschreibt, wie Links, Tabellen und anderes in Wikiseiten eingefügt und Text formatiert werden kann (fett, kursiv, etc).

Das Wiki unterstützt alle grundlegende Formatierungen aus der Markdown-Spezifikation. Jedoch werden einige Funktionen nicht unterstützt, darunter Bilder und Container.

### Neue Seiten anlegen

Um eine neue Wiki-Seite anzulegen kannst du entweder die URL öffnen auf der die Seite angelegt werden soll, z.B.: `https://events.ccc.de/congress/2024/hub/en/wiki/my-awesome-page`, oder einen Link auf einer anderen Seite einfügen, z.B.: `[[my-awesome-page]]`. Sobald du die Seite öffnest kannst du dort neuen Inhalt anlegen.

### Überschriften und formatieren von Text

**Überschriften**

Überschriften werden mit Raute-Symbolen `##` eingeleitet. Es können dabei zwischen 1 und 6 Rauten pro Überschrift verwendet werden. 6 Rauten werden als die kleinste verfügbare Überschrift interpretiert. Wird nur 1 Raute genutzt, wird dies als die größte/Haupt- Überschrift abgebildet.

⚠️ Idealerweise nutzt du nur die Überschriften 2-6, da der Seiten-Titel bereits als Überschrift 1 angezeigt wird.

Übrigens: Strenggenommen beschreibt die Anzahl der Rauten nicht die Größe der Überschrift, sondern die Hierarchie der Überschriften. Das bedeutet z.B., dass Überschriften mit einer einzelnen Raute nur einmal pro Wikiseite vorkommen sollten (da nunmal jedes Dokument nur eine Hauptüberschrift haben kann, sonst wären es ja zwei Dokumente).
In diesem Wiki wird diese Überschrift (mit 1 Raute) bereits für Seiten-Titel verwendet, deshalb sollten aus technischer Korrektheit alle Übeschriften im Text mit zwei oder mehr Rauten eingeleitet werden.

```
# Überschrift 1 (bereits für Seiten-Titel in Verwendung)
## Überschrift 2
### Überschrift 3
#### Überschrift 4
##### Überschrift 5
###### Überschrift 6
```

**Fett/Kursiv/Durchgestrichen**

Beispiele: **Dieser Text ist fett** *Dieser Text ist kursiv* ~~Dieser Text ist durchgestrichen~~

Text kann fett, kursiv oder durchgestrichen formatiert werden, indem er mit `**`, `*` respektive `~~` umrahmt wird:

```
**Dieser Text ist fett**

*Dieser Text ist kursiv*

~~Dieser Text ist durchgestrichen~~
```

**Absätze**

Absätze werden automatisch eingefügt, sobald mindestens eine Leerzeile entsteht:

```
Das ist der erste Absatz.

Das ist der zweite Absatz.
```

### Links

**Links zu Seiten ausserhalb des Wikis**

Der Link-Text wird in eckigen Klammern `[]` und der Link selbst in runden Klammern `()` direkt hintereinander angegeben:

```
[Linktext](https://example.com)
```

⚠️ Wird ein externer Link angeklickt, schaltet das Wiki immer eine Warnseite zwischen, um zu verhindern dass externe Seiten sich unbemerkt als offizielle Hub-Seiten verkleiden können.

**Links zu anderen Seiten im Wiki**

Andere Seiten des Wikis können über den Seitennamen verlinkt werden:

```
[[Seitenname]]

[[Seitenname|Linktext]]
```

**Nutzer verlinken**

Beispiel: @admin

Ein Nutzer kann durch ein vorangestelltes `@` verlinkt werden:

```
@admin
```

**Assembly/Projekt/Raum verlinken**

Manche Elemente können direkt über ihren technischen Namen (Slug) verlinkt werden. Dieser ist im Backoffice einsehbar und auch Teil der URL unter der das Element aufrufbar ist. 

Elemente können wie folgt verlinkt werden:

```
[Ein Link zu einer Assembly](assembly://slug-der-assembly)

[Ein Link zu einem Projekt](project://slug-des-projekts)

[Ein Link zu einem Raum](room://slug-des-raums)
```

### Listen

**Unnummerierte Listen**

Beispiel:
* Beispielliste
* Ein zweiter Eintrag in der Liste
* Ein dritter Eintrag in der Beispielliste
  * ...mit einer Unterliste
    * Die sogar noch eine Unterliste hat!

Pro Listeneintrag wird ein Sternchen-Zeichen `*` vorangestellt. Um einem Listeneintrag eine Unterliste zu geben, müssen die Einträge um 2 Leerzeichen eingerückt werden.

Statt dem Sternchen-Zeichen kann auch das Minus-Zeichen `-` verwendet werden.

```
* Mein erster Listeneintrag
* Ein zweiter Eintrag in der Liste
  * ...mit einer Unterliste
    * Die sogar noch eine Unterliste hat!
```

**Nummerierte Listen**

Beispiel:
1. Nummer Eins der Liste
2. Nummer Zwei der Liste
3. Nummer Drei der Liste

Jedem Listeneintrag wird eine Ziffer vorangestellt.

Übrigens: Unabhängig davon, welche Ziffer vorangestellt wird, wird in der Darstellung im Wiki automatisch trotzdem jeder Eintrag um 1 hochgezählt. Die folgenden beiden Beispiele werden im Wiki identisch dargestellt - nummeriert von eins bis drei.

```
1. Nummer Eins der Liste
2. Nummer Zwei der Liste
3. Nummer Drei der Liste
```
```
1. Nummer Eins der Liste
1. Nummer Zwei der Liste
1. Nummer Drei der Liste
```

### Tabellen

Tabellen-Spalten werden mit einem `|` getrennt. Eine neue Zeile entspricht einer neuen Zeile in der Tabelle.

```
| Spalte 1 | Spalte 2 |
| Wert 1   | Wert 2   |
```

Ergibt:

| Spalte 1 | Spalte 2 |
| Wert 1   | Wert 2   |

Eine Kopfzeile in der Tabelle wird durch eine Zeile mit `-` als Zellen-Wert angelegt:

```
| Spalte 1 | Spalte 2 |
| -------- | -------- |
| Wert 1   | Wert 2   |
```

### Inline-Code/vorformattierter Text

Text zwischen 2 Zeilen mit ``` Symbolen wird nicht von Markdown interpretiert und in einer Monospace-Font angezeigt.

Ideal um Code zu formattieren oder eine bestehende Formattierung beizubehalten.

````
```
Dieser Text wird nicht von Markdown interpretiert. Perfekt für ein wenig Python:

if True:
  print("Hello World")
```
````

### Kommentare anlegen die nicht angezeigt werden

Wenn du in deiner Seite ein Kommentar verstecken möchtest, kannst du das schreiben: `[//]: # (YOURTEXT)`

```
[//]: # (This may be a comment)
```

### Info-Boxen

Um Inhalte hervorzuheben gibt es verschiedene Info-Boxen:

!!! danger
  Eine Box für gefährliche Dinge

!!! warning
  Eine Box für Warnungen

!!! info
  Eine Box für Infos

!!! success
  Eine Box für Erfolge

Diese können wie folgt genutzt werden:

```
!!! danger
  Eine Box für gefährliche Dinge

!!! warning
  Eine Box für Warnungen

!!! info
  Eine Box für Infos

!!! success
  Eine Box für Erfolge
```
