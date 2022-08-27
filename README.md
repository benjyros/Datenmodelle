# Datenmodelle
This is a contribution about data models.

# Lern-Bericht
Datenmodelle implementieren - Benjamin Peterhans

## Einleitung

Bei diesem Modul habe ich mir vorgenommen, ein konzeptionelles Datenmodell in einem Datenbanktool, und zwar Access, zu implementieren. Dazu möchte ich noch ein Formular erstellen, bei dem man mit Schaltflächen das Formular bedienen kann.

![alt text](https://github.com/benjyros/Datenmodelle/blob/main/Images/access-logo.png?raw=true)

## Ziele

Meine Ziele:

- Z1: Ich kann ein konzeptionelles Datenmodell in ein logisches Datenmodell überführen.

Modulziele:
- LZ 12: Ich kann mit Hilfe eines geeigneten Werkzeugs eine Datenbank auf der Grundlage eines logischen Datenmodells implementieren.
- LZ 14: Ich kann mit Hilfe einer Datenbanksoftware Benutzerschnittstellen zur Erfassung, Veränderung und Auswertung von Daten in einer Datenbank erstellen.
- LZ 15: Ich kann auf der Basis wichtigster Gestaltungsregeln die Benutzerschnittstellen so entwerfen, dass sie intuitiv bedienbar sind.

## Produkt - Das logische Datenmodell
### Beschreibung

Für das logische Datenmodell habe ich mir ein konzeptionelles Modell aus einem Auftrag herausgesucht (unter "Downloads" unten). Ich habe mir eines genommen, bei dem mehrere Beziehungstypen vorkommen, damit ich eben alle etwas besser unterscheiden kann und weiss, wie man vorgehen muss.

![alt text](https://github.com/benjyros/Datenmodelle/blob/main/Images/n_zu_m_beziehung.PNG.png?raw=true)

Zum Beispiel musste bei dieser n:m Beziehung hier zuerst eine Zwischentabelle dafür erstellt werden. In diesem Fall wurde die Tabelle "Ausleihung" (siehe oben rechts unter "Ergebnis") erstellt.
Falls jetzt die Tabelle "Ausleihung" gelöscht werden sollte, werden auch "Bibliothekbenutzer" und "Medium" durch die Komposition mitgelöscht (Vereinfachung: Wenn es keine Ausleihe gibt, kann es auch keine Bibliotheksbenutzer oder Medien geben)

### Ergebnis

![alt text](https://github.com/benjyros/Datenmodelle/blob/main/Images/das_logische_datenmodell.png?raw=true)

## Produkt - Implementierung Access
### Beziehungen in Access

![alt text](https://github.com/benjyros/Datenmodelle/blob/main/Images/beziehungen_in_access.PNG.png?raw=true)

### Vorgehen in Access

Um ein logisches Datenmodell in Access zu implementieren, muss man zu jeder Tabelle, wer hätte es gedacht, eine Tabelle erstellen. Auch alle Attribute sowie die Primär- und Fremdschlüssel werden übernommen. Man muss auch darauf achten, dass die Attribute den richtigen Datentyp enthält.

Um Beziehungen zu erstellen, muss man unter den Tabellen auf die Entwurfsansicht gehen. Dort unter den Datentypen, kann man einen "Nachschlage-Assistenten" auswählen, wobei man dort nach dem Primärschlüssel, den man mit der Tabelle verknüpfen will, sucht.

Anschliessend habe ich noch bei den Beziehungen die referentielle Integrität anzeigen lassen (1:n etc.) und auch noch definiert, ob es eine Komposition ist. Falls eine Beziehung eine Komposition beinhaltet, gab ich an, dass es eine "Löschweitergabe an verwandte Datensätze" sei.

Zur Demonstration beim nächsten Punkt habe ich noch ein paar Datensätze hinzugefügt, sodass es nicht so leer aussieht.

## Produkt - Das Formular
### Das Formular

![alt text](https://github.com/benjyros/Datenmodelle/blob/main/Images/das_formular.PNG.png?raw=true)

### Erstellung eines Formulars

Zu der Tabelle "Ausleihe" in Access habe ich zusätzlich ein Formular erstellt.

Da ich das Formular mit Navigationsschaltflächen im Formular erstellen wollte, musste ich zuerst andere Navigationsschaltflächen (von Access selbst) entfernen. Dafür musste ich lediglich, wenn man das Formular bearbeitet, unter den Formulareigenschaften/Format die Option "Navigationsschaltflächen" auf "Nein" stellen.
Darauffolgend habe ich unter dem Formularentwurf eine neue Schaltfläche hinzugefügt. Darunter kann man dann auswählen, was man für eine Aktion für diese Schaltfläche ausführen will. In meinem Fall habe das Anzeigen der vorherigen und der nächsten, sowie das Löschen und Speichern von Datensätzen ausgewählt. Das habe ich dann insgesamt noch dreimal wiederholt. Im Screenshot rechts nebenan können Sie sehen, wie es aussehen sollte, wenn man eine neue Schaltfläche hinzufügt.

### Hinzufügen einer Schaltfläche

![alt text](https://github.com/benjyros/Datenmodelle/blob/main/Images/neues_steuerelement.PNG.png?raw=true)

## Verifikation

Meine Ziele:

- Z1: Wird mit dem Block "Ergebnis" unter "Produkt - Das logische Datenmodell" validiert.

Modulziele:
- LZ12: Wird mit "Produkt - Implementierung Access" und dem Download der Access-Datei validiert.
- LZ14: Wird mit "Produkt - Das Formular", dem Screenshot "Das Formular" und der Access-Datei validiert.
- LZ15: Wird mit "Produkt - Das Formular", dem Screenshot "Hinzufügen einer Schaltfläche" und der Access-Datei validiert.

# Reflektion zum Arbeitsprozess

Bei der Bearbeitung dieses Auftrages hatte ich mehrheitlich keine Probleme. Durch die ganzen Übungen und Aufträge während der Stunde konnte ich diesen Auftrag eigentlich recht schnell lösen. Wenn man während der Stunde aufmerksam mitmacht, wird man das Thema auch leicht verstehen. Das Implementieren in Access, sowie die Erstellung eines Formulars fielen mir sehr leicht. Beim logischen Datenmodell hatte ich, würde ich sagen, keine Mühe gehabt. Ich brauchte dort einfach länger, um die Beziehungen zueinander zu verstehen. Die n:m Beziehungen waren meiner Meinung nach einfach zu verstehen und auch einfach umzusetzen. Bei den anderen musste ich halt zuerst überlegen, ob es eine Aggregation oder eine Komposition ist, um dann auch noch entscheiden, welche Tabelle den Fremdschlüssel einer anderen Tabelle hat etc.
Allgemein, vor der Bearbeitung dieses Auftrags, hatte ich anfangs schon etwas Probleme mit Access und deren Anwendung gehabt. Mit etwas Hilfe von meinen Kollegen, oder auch durch die Demonstrationen, die der Lehrer projektiert hatte, konnte ich anschliessend das meiste verstehen und auch selbst ausführen.
