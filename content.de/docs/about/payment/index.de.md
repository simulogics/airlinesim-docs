---
title: "Zahlungssystem"
weight: 4
---

# Zahlungssystem

AirlineSim verwendet ein Zahlungsmodell, das auf Fairness, Transparenz und Benutzerfreundlichkeit ausgerichtet ist.

Hier erfahrt ihr alles, was ihr über Credits, Creditverbrauch, Preise, Zahlungsmethoden sowie die Premium-Features des Spiels wissen müsst. Bei Fragen zum Zahlungsvorgang werft gerne einen Blick auf unsere [Zahlungs-FAQ]({{< relref "docs/faqs/payments.de.md" >}}).

## Motivation

AirlineSim ist ein sehr "nischiges" Spiel (= vergleichsweise wenige aktive Spieler*innen). Zudem ist es als ernsthafte Wirtschaftssimulation gedacht, auf deren Servern aufwendige Simulationsmodelle laufen, die sehr ressourcenintensiv sind (= hohe Betriebskosten).

Vor diesem Hintergrund gibt es bestimmte Anforderungen, die unser Zahlungsmodell erfüllen muss:

1. Es muss relativ hohe Kosten pro aktivem Spielerkonto decken.
2. Es muss flexibel genug sein, um unterschiedliche Nutzungsintensitäten zu berücksichtigen, wie z.B. unterschiedliche Mengen aktiver Holdings pro Spielerkonto oder länger laufende Spielwelten.
3. Es darf keine In-Game-Vorteile für echtes Geld bieten, außer einem anfänglichen "Anti-Cheat-Unlock" durch einen einzelnen Kauf (Details siehe unten).
4. Es muss trotz einer relativ kleinen Spielerbasis genügend Umsatz generieren.
5. Es muss Spieler*innen, die kein Geld ausgeben können oder wollen, immer noch ein dauerhaft kostenloses Spiel ermöglichen.
6. Es muss Spieler*innen gegenüber so fair wie möglich sein, denn das ist uns wichtig.

Diese Anforderungen schließen die meisten gängigen Zahlungsmodelle aus:

- Ein **einmaliger Kauf** würde die laufenden Serverkosten nicht decken.
- Ein obligatorisches **wiederkehrendes Abonnement** verleitet Spieler*innen dazu, auch dann noch zu zahlen, wenn sie das Spiel nicht mehr nutzen, ist nicht sehr flexibel und verursacht einen höheren technischen und administrativen Aufwand.
- Ein **werbefinanziertes Modell** ist einfach "meh" und würde aufgrund der geringen Zahl an Spieler*innen wahrscheinlich nicht genug Umsatz generieren, um unsere Ausgaben zu decken.
- Die meisten **Free-2-Play-Modelle** scheiden aus, da sie entweder **Pay-2-Win-Mechanismen** erfordern, die für eine ernsthafte Simulation wie AirlineSim nicht in Frage kommen, und/oder darauf aufbauen, eine Handvoll Spieler*innen für sinnlose kosmetische In-Game-Items auszubeuten, was angesichts der Größe von AirlineSim weder fair noch machbar ist.

Aus diesem Grund haben wir ein auf Credits basierendes System implementiert, das uns im Laufe der Jahre sehr gute Dienste geleistet hat.

## Credits: So Funktioniert unser Zahlungsmodell

Unser Zahlungsmodell dreht sich um sogenannte **Credits**. Nach der Anmeldung bei AirlineSim verfügt euer Konto zu Beginn über ein Guthaben von **60 kostenlosen Credits**.

In den meisten Spielwelten wird euch für jede von euch erstellte [Holding]({{< relref "docs/advanced/setup/holdings-vs-subsidiaries.de.md" >}}) eine kleine Menge an Credits berechnet. Dieser Betrag variiert je nach Dauer der Spielwelt. Angesichts der anfänglichen Menge an kostenlosen Credits und der typischen Kosten einer kurzfristigen Spielwelt von 4 Credits/Tag könntet ihr eine solche Spielwelt bis zu 15 Tage lang kostenlos ausprobieren.

Sobald die Credits aufgebraucht sind, müsst ihr euer Konto aufladen, um weiterspielen zu können. Das Creditsystem ist also ein Prepaid-Modell und somit völlig flexibel. Der Kauf von Credits stellt kein wiederkehrendes Abonnement dar. Ihr könnt Credits kaufen, wann immer ihr möchtet. Wenn ihr euch jemals dazu entschließt, nicht weiterzuspielen, müsst ihr nur eure Credits auslaufen lassen.

Und das ist schon fast alles! Mit einer Einschränkung: Es gibt einen Unterschied zwischen kostenlosen Konten (also solchen, die noch nie eine Zahlung abgeschlossen haben) und Premiumkonten (also solchen, die irgendwann mindestens eine Zahlung abgeschlossen haben). Aber darauf werden wir weiter unten eingehen.

## Creditverbrauch & Auslaufen von Credits

Sobald ihr eine Holding erstellt, werden täglich Credits von eurem Konto abgezogen. In Spielwelten, in denen ihr mehr als eine Holding erstellen könnt, gelten für jede zusätzliche Holding Rabatte.

Derzeit betragen die üblichen Kosten:
* Kurzfristige Spielwelten: 4 Credits/Tag (2 pro zusätzlicher Holding)
* Mittelfristige Spielwelten: 5 Credits/Tag (3 pro zusätzlicher Holding)
* Langfristige Spielwelten: 6 Credits/Tag (4 pro zusätzlicher Holding)

Wenn euch die Credits ausgehen, werden die Holdings und Unternehmen eures Kontos gesperrt, bis ihr euer Guthaben auffüllt. Während dieser Zeit werden weiterhin Credits zum normalen Tagessatz abgezogen, was bedeutet, dass euer Guthaben zunehmend negativ wird. Damit soll verhindert werden, dass Unternehmen einen unfairen Vorteil erlangen, indem sie einen Account aufgeben, mehrere Wochen später aber zu ihm zurückkehren, ohne für ihr Wachstum und die in der Zwischenzeit belegten Spielressourcen zahlen zu müssen.

{{% hint info %}}
**Beispiel**
Wenn ein Konto eine Holding in einer Kurzzeitspielwelt besitzt und die Credits ausgehen, hat es nach 5 Tagen ein Guthaben von -20 Credits. Diese müssen bezahlt werden, bevor der Zugriff auf das Spiel wiederhergestellt wird.
{{% /hint %}}

Wenn das Guthaben eines Kontos länger als 28 Tage negativ bleibt, werden **alle Holdings und Airlines** dieses Kontos **auf allen Spielwelten** gelöscht, um blockierte Spielressourcen wie Slots und Flugzeuge freizugeben, die anderen Spieler*innen sonst nicht zugänglich wären. Das AirlineSim-Konto selbst bleibt aktiv und das Guthaben wird automatisch auf die anfänglichen 60 Credits aufgefüllt, wodurch euer Konto effektiv auf seinen ursprünglichen Status zurückgesetzt wird. Wenn es zuvor Premiumstatus hatte, bleibt dieser auch nach dem Zurücksetzen erhalten.

Bitte beachtet, dass die Kulanzperiode von 28 Tagen für Premiumkonten gilt, für die zuvor Credits erworben wurden. Bei Testkonten dauert es nach Auslaufen der Credits 7 Tage, bis die Airlines gelöscht werden.

{{% hint danger %}}
**Achtung!**
Bitte beachtet, dass automatische Löschungen aufgrund eines negativen Guthabens **alle Spielwelten** betreffen, in denen ein Konto Holdings hat, **auch kostenlose**!
{{% /hint %}}

## Kostenlos Spielen: Kostenlose vs. Premium-Konten

AirlineSim bietet kostenlose Kurzzeitspielwelten an, auf denen keine Credits berechnet werden, um zu spielen. Daher könnt ihr AirlineSim unbegrenzt spielen, ohne einen Cent zu bezahlen.

Es gibt jedoch einige Einschränkungen: Sofern ihr nicht mindestens eine Zahlung abgeschlossen habt, bleibt euer Konto im **kostenlosen oder Teststatus**. Dies bedeutet, dass euch einige Funktionen des Spiels auch dann nicht zur Verfügung stehen, wenn ihr auf kostenlosen Spielwelten spielt.

Die meisten dieser Funktionen erfordern eine direkte Interaktion zwischen mehreren Konten, und die Anforderung, mindestens eine Zahlung abzuschließen, ist ein sehr wirksamer Mechanismus gegen Cheating. Features dieser Kategorie sind:

* Erstellen von mehr als einer Holding
* Mehrere Airlines in einer Holding
* Anbieten oder Annehmen privater Verträge (z.B. für das Leasing von Flugzeugen oder Interlining)
* Verkauf von Flugzeugen
* Bieten auf nicht-offizielle Flugzeugangebote
* Entlassungen (da entlassenes Personal in einem Pool landet, der anderen Spieler*innen zur Verfügung steht)
* Börsenfunktionen ([Börsengänge]({{< relref "docs/advanced/finances/initial-public-offerings/index.de.md" >}}) und Aktienhandel)
* Eigene Gebäude

Es gibt einige Features, die vor allem aus historischen Gründen eingeschränkt sind. Als das AirlineSim der aktuellen Generation auf den Markt kam – etwa 2007 – verursachten diese Funktionen eine höhere Belastung unserer Server und waren daher auf Premium-Konten beschränkt:

* [Das Online Reservation System (ORS)]({{< relref "docs/advanced/bookings/online-reservation-system/index.de.md" >}})
* Integrierte Flight-Operations-Kontrolle

Diese Einschränkungen werden wahrscheinlich wegfallen, sobald diese Features modernisiert werden.

## Preise

AirlineSim bietet ein gestaffeltes Preismodell mit unterschiedlichen Paketgrößen, sodass ihr für jede Situation die richtige Menge an Credits auswählen könnt: Kauft ein kleines Paket, wenn ihr nur mal reinschnuppern oder günstig den Premium-Status erlangen möchtet. Kauft größere Pakete, wenn ihr länger spielen und von Mengenrabatten profitieren möchtet.

Zum Zeitpunkt des Verfassens dieses Artikels kostet das kleinste Paket mit 50 Credits 2,49 EUR. Auf dieser Stufe würde ein einfaches Konto mit einem täglichen Verbrauch von 4 Credits also etwa 6 EUR pro Monat kosten. Bei den deutlich gängigeren 500 Credits für 19,10 EUR liegt dieser Preis bereits bei rund 4,60 EUR.

Eine vollständige und aktuelle Liste aller Preise und der jeweiligen Mengenrabatte findet ihr auf eurer [Kontoverwaltungsseite](https://accounts.airlinesim.aero/account/credits).

## Zahlungsarten & Checkout

Um Credits für AirlineSim zu kaufen, loggt euch einfach in euer Konto ein und klickt auf Credits kaufen. Hier könnt ihr die gewünschte Paketgröße auswählen, optional einen Gutscheincode eingeben (aktuell nur außerhalb von Steam) und eure Zahlungsart auswählen.

{{% hint info %}}
**Info**
Aktuell sind beim Checkout folgende Zahlungsarten möglich: Kredit- oder Debitkarte (Visa, MasterCard, American Express), PayPal, paysafecard, Online-Überweisung und Vorkasse. Beim Spielen über Steam stehen euch alle von Steam angebotenen Zahlungsarten zur Verfügung.
{{% /hint %}}

Bitte beachtet: Welche Zahlungsmethoden tatsächlich verfügbar sind, kann sowohl von dem Land abhängen, aus dem ihr bezahlt, als auch von der gewählten Paketgröße.

Sobald eure Zahlung verarbeitet wurde, werden die Credits eurem Konto gutgeschrieben.