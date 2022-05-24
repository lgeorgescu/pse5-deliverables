# Testkonzept und Testresultate

Unser Team startete sehr zurückhaltend in das Testing, wir wollten von Anfang an einen grossen Fokus auf das Testing legen, jedoch nahm die Implementation von Features und das Einarbeiten in die neuen Technologien viel Zeit in Anspruch nahm. Nach dem Einrichten der Testing Frameworks Jest und Rspec verlief das Testing ohne grössere Probleme.

Das Konzept orientiert sich an der Testing Pyramide, welches wir bei Zühlke gelernt haben.
![testing_pyramid](/Testresultate/testing_pyramid.png)

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

## Installationstest

Da es bei uns bei der Installation keine Probleme gegeben hat, und dass Produkt am Schluss sowieso auf einem Linuxbetriebssystem genutzt wird, mussten wir hier nichts weiter testen. Die Installationsanweisungen im [README](../Produkt/README.md) sind vollständig und verständlich.

## GUI Tests

Die Funktionalität des GUIs wurde bereits in den [Feature Tests](#integration-tests--feature-tests) getested. Das visuelle des GUIs wird von Hand getestet. Da es nicht sonderlich gross ist, sollte dies auch reichen.

## Stress Tests

Die Webapp muss nicht grossen Belastungen standhalten, da sie auch nur von (voraussichtlich) einer einzigen Person benutzt wird. Das einzige Bottleneck ist das Hochladen eines Transitionfile. Dies dauert ca. 2 Minuten. Als Nutzer muss man hier also kurz warten. Dieses Verhalten ist okay, da dies nur einmal pro Jahr gemacht werden muss.

## Usability-Test

Ein Usability-Test wird mit dem Endnutzer durchgeführt.

## Testresultate

Zu den Testresultaten gibt es nicht allzu viel zu sagen.

Die Tests im Backend sind alle erfolgreich.
![result1](/Testresultate/result1.png)
![result2](/Testresultate/result2.png)

Auch im Frontend werden alle Tests bestanden.

![result3](/Testresultate/result3.png)

In den beiden Screenshots sind alle Testsausgaben, so wie sie von den Testrunnern *RSpec* und *Jest* angezeigt werden.
Da wir wie erwähnt mit dem Testing am Anfang ein wenig in Verzug geraten sind und wir bis dahin vor allem *sehr* viel von Hand getestet haben, haben die Tests eher das *Expected Behavior* bestätigt und gezeigt, dass das was wir von Hand getestet und so erwartet haben, auch im automatisierten Testing genau so gemacht wurde.

Wahrscheinlich der lehrreichste Test war tatsächlich der Usability Test:

Anschliessend an das Kundenmeeting der 4.Iteration haben wir einen Usability-Test mit dem Kunden geplant.
Da unsere Application am Schluss hauptsächlich von einer Person benutzt wird, haben wir den Usability gerade mit ihr durchgeführt.
Wir haben uns mit der Endnutzerin vor einem fast fertigen Build der Application gesetzt und sie die Usecases durchspielen lassen. Es wurde schnell ersichtlich, dass es einige Punkte gab, welche nicht in den vorherigen Meetings vom Kunden spezifiziert wurden. Dabei handelte es sich jedoch nur um kleine Änderungen, welche innerhalb einer Stunde implementiert waren. Der Usability-Test zeigte uns, dass es einen Unterschied macht ob man die Sicht eines Developers oder eines potenziellen Endnutzer hat. So war zum Beispiel die Ungeduldigkeit bei Ladezeiten ein Punkt, welchen wir mit einem Spinner als UserFeedback beheben konnten.
