# Testkonzept und Testresultate

Unser Team startete sehr zurückhaltend in das Testing, wir wollten von Anfang an einen grossen Fokus auf das Testing legen, jedoch nahm die Implementation von Features und das Einarbeiten in die neuen Technologien viel Zeit in Anspruch nahm. Nach dem Einrichten der Testing Frameworks Jest und Rspec verlief das Testing ohne grössere Probleme.

## Unit Tests

Im Backend werden als Unit Tests vor allem die Controller und Models getestet. Dies soll sicher stellen, dass die Interaktion zwischen Frontend und Datenbank wie erwartet abläuft und auch die Datenbankmodelle den Vorstellungen entsprechen. So werden zum Beispiel Grenzfälle und Foreign-Constraints der Datenbank in den Modell Test geprüft oder upload Responses und preconditions an die Daten aus dem Frontend in den Controller Tests überprüft.

Im Frontend wird mit den Unit Tests getestet, ob

* der *Difference Highlighter* funktioniert
* die Filterbuttons korrekt funktionieren
* Differences korrekt angezeigt werden

## Datenbank Tests

Die Datenbank perse wird in unserem Produkt nicht getested, wir haben automated Unit Tests der Modelle auf welchen die Datenbank basiert geschrieben. Diese stellen sicher, dass keine ungültige Daten in die Datenbanken gefüllt werden.

## Integration Tests / Feature Tests

Wir haben mit dem Kunden abgemacht, dass wir die Feature Tests auf das Hochladen eines Katalogs und Transition File beschränken.

Die Feature Tests werden mit RSpec und Headless Chrome gemacht. Headless Chrome simuliert hierbei einen Webbrowser und automatisiert so z.B. dass Hochladen eines Files.
