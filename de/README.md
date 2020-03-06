Projektpfad: /web/fundamentals/_project.yaml book_path: /web/fundamentals/_book.yaml Beschreibung: Übersicht über den Bildschirmfokus in der Barrierefreiheit

{# wf_blink_components: Blink> Barrierefreiheit #} {# wf_updated_on: 2019-06-08 #} {# wf_published_on: 2016-10-04 #}

# Einführung in Focus {: .page-title}

{% include "web / _shared / Contributors / megginkearney.html"%} {% include "web / _shared / Contributors / dgash.html"%} {% include "web / _shared / Contributors / robdodson.html"%}

In dieser Lektion sprechen wir über den *Fokus* und wie Sie ihn in Ihrer Anwendung verwalten können. Der Fokus bezieht sich darauf, welches Steuerelement auf dem Bildschirm (ein Eingabeelement wie ein Feld, ein Kontrollkästchen, eine Schaltfläche oder ein Link) derzeit Eingaben von der Tastatur und aus der Zwischenablage erhält, wenn Sie Inhalte einfügen.

## Was ist der Fokus?

Der Fokus bestimmt, wohin Tastaturereignisse zu einem bestimmten Zeitpunkt auf der Seite verschoben werden. Wenn Sie beispielsweise ein Texteingabefeld fokussieren und mit der Eingabe beginnen, empfängt das Eingabefeld die Tastaturereignisse und zeigt die von Ihnen eingegebenen Zeichen an. Während es den Fokus hat, erhält es auch eingefügte Eingaben aus der Zwischenablage.

![Tastaturfokus in einem Textfeld](../imgs/keyboard-focus.png)

Das aktuell fokussierte Element wird häufig durch einen *Fokusring* angezeigt, dessen Stil sowohl vom Browser als auch von dem vom Seitenautor angewendeten Stil abhängt. Chrome beispielsweise hebt fokussierte Elemente normalerweise mit einem blauen Rand hervor, während Firefox einen gestrichelten Rand verwendet.

![Anmeldeschaltfläche](../imgs/sign-up.png)

Einige Benutzer bedienen ihren Computer fast ausschließlich mit der Tastatur oder einem anderen Eingabegerät. Für diese Benutzer ist der Fokus entscheidend. Es ist ihr primäres Mittel, um alles auf dem Bildschirm zu erreichen. Aus diesem Grund wird in der Web-AIM-Checkliste in Abschnitt 2.1.1 angegeben, dass [alle](https://webaim.org/standards/wcag/checklist#sc2.1.1) Seitenfunktionen [über die Tastatur](https://webaim.org/standards/wcag/checklist#sc2.1.1) {: .external} [verfügbar sein sollten, es](https://webaim.org/standards/wcag/checklist#sc2.1.1) sei denn, dies ist mit einer Tastatur nicht möglich, z. B. Freihandzeichnen.

![Dialogfeld ](../imgs/system-prefs2.png)

Die Reihenfolge, in der der Fokus durch interaktive Elemente über die `Tab` vorwärts und rückwärts erfolgt, wird nicht überraschend als *Registerkartenreihenfolge bezeichnet* . Ein wichtiger Schritt, den wir später behandeln werden, ist es, sicherzustellen, dass Sie Ihre Seite mit einer logischen Tabulatorreihenfolge gestalten.

## Was ist fokussierbar?

Integrierte interaktive HTML-Elemente wie Textfelder, Schaltflächen und *Auswahllisten* sind *implizit fokussierbar. Dies* bedeutet, dass sie automatisch in die Registerkartenreihenfolge eingefügt werden und über eine integrierte Tastaturereignisbehandlung ohne Eingreifen des Entwicklers verfügen.

![implizit fokussierbare Felder](../imgs/implicitly-focused.png)

Aber nicht alle Elemente sind fokussierbar. Absätze, Divs und verschiedene andere Seitenelemente werden beim Durchblättern der Seite nicht fokussiert, und das ist beabsichtigt. Es besteht im Allgemeinen keine Notwendigkeit, etwas zu fokussieren, wenn der Benutzer nicht damit interagieren kann.

![Nicht alle Elemente sind fokussierbar](../imgs/not-all-elements.png)

## Fokus erleben

Lassen Sie uns einige der Fokustechniken ausprobieren, die wir gerade besprochen haben. Rufen Sie mit Chrome die Modellseite {: .external} dieser [Airline-Website auf](http://udacity.github.io/ud891/lesson2-focus/01-basic-form/) und suchen Sie nach einem bestimmten Ticket, **indem Sie nur die Tastatur** eingeben. Die Seite akzeptiert keine Mauseingaben, daher können Sie die Übung nicht verfälschen (nicht, dass wir Ihnen nicht vertrauen ;-).

![Airline-Site-Modell](../imgs/airlinesite2.png)

hahahahahahhahahahhahahaahha

lioklioklioklioklioklioklioklioklioklioklkioklioklliokliokliok
