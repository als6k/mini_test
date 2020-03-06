Projektpfad: /web/fundamentals/_project.yaml book_path: /web/fundamentals/_book.yaml Beschreibung: Übersicht über den Bildschirmfokus in der Barrierefreiheit

{# wf_blink_components: Blink> Barrierefreiheit #} {# wf_updated_on: 2019-06-08 #} {# wf_published_on: 2016-10-04 #}

# Einführung in Focus {: .page-title}

{% include "web / _shared / Contributors / megginkearney.html"%} {% include "web / _shared / Contributors / dgash.html"%} {% include "web / _shared / Contributors / robdodson.html"%}

In dieser Lektion sprechen wir über den *Fokus* und wie Sie ihn in Ihrer Anwendung verwalten können. Der Fokus bezieht sich darauf, welches Steuerelement auf dem Bildschirm (ein Eingabeelement wie ein Feld, ein Kontrollkästchen, eine Schaltfläche oder ein Link) derzeit Eingaben von der Tastatur und aus der Zwischenablage erhält, wenn Sie Inhalte einfügen.

Dies ist ein großartiger Ort, um etwas über Barrierefreiheit zu lernen, da wir alle wissen, wie man eine Tastatur benutzt, es einfach ist, sich darauf zu beziehen und sie zu testen, und es praktisch allen Benutzern zugute kommt.

Benutzer mit motorischen Beeinträchtigungen, die von einer dauerhaften Lähmung bis zu einem verstauchten Handgelenk reichen können, verlassen sich möglicherweise auf eine Tastatur oder ein Schaltgerät, um auf Ihrer Seite zu navigieren. Daher ist eine gute Fokusstrategie entscheidend, um ihnen eine gute Erfahrung zu bieten.

Und für die Hauptbenutzer, die jede Tastenkombination auf ihrem Computer kennen, wird die Möglichkeit, schnell mit der Tastatur allein auf Ihrer Website zu navigieren, sie sicherlich produktiver machen.

Eine gut implementierte Fokusstrategie stellt somit sicher, dass jeder, der Ihre Anwendung verwendet, eine bessere Erfahrung hat. Wir werden in den kommenden Lektionen sehen, dass die Bemühungen, die Sie in den Mittelpunkt stellen, eine wichtige Grundlage für die Unterstützung von Benutzern mit unterstützender Technologie und in der Tat aller Benutzer sind.

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

Wenn Sie das Formular ohne Eingabefehler erfolgreich ausgefüllt und die Schaltfläche Suchen aktiviert haben, wird das Formular einfach gelöscht und zurückgesetzt. Füllen Sie das Formular aus und kehren Sie dann zurück.

at type hängt auch von den Pfeiltasten ab, oder Sie können "w", "a" oder "n" eingeben, um zu einer Sitzoption zu springen. Anschließend können Sie die Standardeinstellung für Werbeangebote deaktivieren, indem Sie die Leertaste drücken, während das Kontrollkästchen aktiviert ist. Konzentrieren Sie sich schließlich auf die Schaltfläche Suchen und drücken Sie die `Enter` , um das Formular zu senden.

Es ist sehr praktisch, mit einem Formular nur über die Tastatur zu interagieren und nicht zur Maus und zurück zu wechseln, um eine Aufgabe zu erledigen. Da alle im Formular verwendeten Elemente native HTML-Tags mit implizitem Fokus sind, funktioniert das Formular problemlos mit der Tastatur, und Sie müssen keinen Code schreiben, um das Fokusverhalten hinzuzufügen oder zu verwalten.
