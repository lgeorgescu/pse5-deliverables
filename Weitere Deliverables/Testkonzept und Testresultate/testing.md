# Testkonzept und Testresultate

Unser Team startete sehr zurückhaltend in das Testing, wir wollten von Anfang an einen grossen Fokus auf das Testing legen, jedoch nahm die Implementation von Features und das Einarbeiten in die neuen Technologien viel Zeit in Anspruch nahm. Nach dem Einrichten der Testing Frameworks Jest und Rspec verlief das Testing ohne grössere Probleme.

## Unit Tests

Im Backend werden als Unit Tests vor allem die Models getestet. Dies soll sicher stellen, dass keine invaliden Daten in die Datenbanken gefüllt werden.

Im Frontend wird mit den Unit Tests getestet, ob

* der *Difference Highlighter* funktioniert
* die Filterbuttons korrekt funktionieren
* Differences korrekt angezeigt werden

## Datenbank Tests

TODO

## Integration Tests / Feature Tests

Wir haben mit dem Kunden abgemacht, dass wir die Feature Tests auf das Hochladen eines Katalogs und Transition File beschränken.

Die Feature Tests werden mit RSpec und Headless Chrome gemacht. Headless Chrome simuliert hierbei einen Webbrowser und automatisiert so z.B. dass Hochladen eines Files.
