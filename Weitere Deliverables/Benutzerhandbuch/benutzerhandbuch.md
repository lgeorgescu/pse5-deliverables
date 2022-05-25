# Benutzerhandbuch ChopDiff

## Dateien Importieren

### Nur Kalender Hochladen
Dieser Schritt ist nur notwendig, wenn noch kein Kalender vom alten Jahr vorhanden ist. Das ist der Fall, wenn die Applikation zum ersten Mal benutzt wird, in den darauffolgenden Jahren kann dieser Schritt übersprungen werden und direkt ein Kalender und Transitionfile hochgeladen werden.

Um ausschliesslich den Kalender des letzten Jahres hochzuladen, muss "+ Dateien Importieren" angeklickt werden. Es erscheint nun ein Popup mit einem Eingabefeld für das Jahr des Katalogs. Hier muss das alte Jahr eingegeben werden. Darunter kann nun der alte Katalog ausgewählt werden, dieser muss in einem .csv Format sein. Wir wollen keine Überleitung hochladen, darum wird das Feld "Nur Katalog hochladen" ausgewählt. Über den Button "Dateien importieren" kann der Katalog jetzt hochgeladen werden. Dies kann einige Sekunden dauern.
![](C:\Users\marti\Documents\Git\pse5-deliverables\Weitere Deliverables\Benutzerhandbuch\Nur_Kalender_Hochladen.png)

### Kalender und Transitionfile hochladen

Um einen Kalender und ein Transitionfile hochzuladen, muss "+ Dateien importieren" angeklickt werden. Es erscheint nun ein Popup mit einem Eingabefeld für das Jahr des Katalogs. Hier muss das neue Jahr eingegeben werden. Darunter wird über "+ Datei" der Neue Katalog ausgewählt. Dieser muss in einem .csv Format sein. Auf die selbe Weise muss jetzt das Transitionfile in einem .xslx Format ausgewählt werden. Über den Button "Dateien importieren" werden die Dateien hochgeladen. Dies kann mehr als eine Minute dauern.

![](C:\Users\marti\Documents\Git\pse5-deliverables\Weitere Deliverables\Benutzerhandbuch\Kalender_und_Transitionfile_hochladen.png)

### Katalog oder Transition löschen

Bereits hochgeladene Kataloge können nicht gelöscht werden, es ist aber möglich diese zu überschreiben indem ein neuer Katalog desselben Jahres hochgeladen wird. Diese Aktion ist sehr gefährlich, da bestehende Kommentare und somit Arbeit verloren gehen können. Um bestehende Kataloge oder Transitions zu löschen sollte darum ein Systemadministrator beigezogen werden.

#### Welche Daten gehen verloren wenn ein Katalog überschrieben wird?

Jede Transition ist vom alten und vom neuen Katalog abhängig und wird gelöscht, wenn einer der beiden Kataloge gelöscht oder überschrieben wird. Wenn der Katalog von 2020 überschrieben wird, werden sowohl die Transition 2019-2020 als auch 2020-2021 mit allen ihren Kommentaren gelöscht.

## Übersicht Navigation

![](C:\Users\marti\Documents\Git\pse5-deliverables\Weitere Deliverables\Benutzerhandbuch\Uebersicht_Navigation.png)

1. Hier kann ausgewählt werden, welche Überleitung angezeigt werden soll.
2. Zeigt an, wie viele gültige Chops es im neuen Katalog der Transition gibt.
3. Zeigt an, wie viele gültige Chops es im alten Katalog der Transition gibt.
4. Hier können neue Kataloge und Transitionfiles hochgeladen werden.

## Differenzen sortieren und filtern

![](C:\Users\marti\Documents\Git\pse5-deliverables\Weitere Deliverables\Benutzerhandbuch\Differenzen_sortieren_und_filtern.png)

Alle Differenzen werden sind einer Kategorie zugeordnet (z.B. "Titelerweiterung"). Mit einem Klick auf den Pfeil (1) kann eine Kategorie aufgeklappt werden. Bei Kategorien mit vielen Differenzen, kann dabei eine kleine Ladezeit geben. Bei (2) kann ausgewählt werden wie die Differenzen innerhalb der Kategorie sortiert werden sollen. Mit der Option Status werden alle roten Differenzen zuoberst angezeigt.

Mit einem Klick auf "+ Filter Hinzufügen" (3) können die Differenzen gefiltert werden. 

![](C:\Users\marti\Documents\Git\pse5-deliverables\Weitere Deliverables\Benutzerhandbuch\Filtern.png)

Mit einem Klick auf bereits ausgewählte Filter (1) können diese wieder entfernt werden.

## Differenzen kommentieren und markieren

![](C:\Users\marti\Documents\Git\pse5-deliverables\Weitere Deliverables\Benutzerhandbuch\Differnz_eingeklappt.png)



Mit einem Klick auf den Pfeil (1) kann eine Differenz ausgeklappt werden, wodurch die Details sichtbar werden.

![](C:\Users\marti\Documents\Git\pse5-deliverables\Weitere Deliverables\Benutzerhandbuch\Differenz_ausgeklappt.png)

Jetzt ist der neue und der alte Text des Chops sichtbar. Auf der linken Seite wird der neue Chop dargestellt. Dabei sind alle Textstellen welche nicht im alten Chop vorkommen grün markiert (1). Auf der Rechten Seite ist der alte Chop. Alle Textstellen welche nicht mehr im neuen Chop vorhanden sind werden sind rot markiert (2).

Im Kommentarfeld (3) kann ein beliebiger Kommentar zu dieser Differenz angegeben werden. Dieser wird erst mit dem Button "Speichern" (4) gespeichert. 

Im Statuspunkt (4) wird der Status der Differenz angezeigt. Dabei sind die Farben gelb, grün und rot möglich. Der Status kann verändert werden, indem auf den Punkt geklickt wird. Ein gelber Status wird durch ein einmaliges Klicken grün. Sollte er auf rot gestellt werden, muss noch ein weiteres Mal geklickt werden. Durch einen dritten Klick, wird der Status wieder gelb.