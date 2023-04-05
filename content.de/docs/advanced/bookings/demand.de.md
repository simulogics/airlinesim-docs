---
title: "Aufkommensberechnung"
weight: 2
---

# Aufkommensberechnung

Damit ihr besser nachvollziehen könnt, wie die Nachfrage in AirlineSim funktioniert, findet ihr hier ein kleines Q&A.

## Spielt die Tageszeit bei Flügen eine Rolle?

Nein, die Passagiere werden alle Abflug- und Ankunftszeiten gleich behandeln. Die Gesamtreisezeit beeinflusst jedoch die Flugbewertung.

## Schwankt die Passagiernachfrage saisonal?

Nein, saisonale Schwankungen spielen für die Nachfrage derzeit keine Rolle.

## Ist es den Fluggästen wichtig, an welchem Tag sie fliegen?

Die Fluggäste buchen nur Flüge innerhalb der nächsten drei Tage, aber sie buchen jeden dieser Tage, wenn einige Tage voll oder nicht verfügbar sind. Sind keine Flüge verfügbar, nehmen die Passagiere keine Buchung vor - sie müssen dann mit dem Auto fahren oder schwimmen!

## Kann ich die Auslastung erhöhen, indem ich weniger als einmal pro Tag Flüge einplane?

Ja, viele Strecken mit geringer Nachfrage können mit Flügen bedient werden, die nicht täglich stattfinden. Dies funktioniert jedoch nicht, wenn ihr weiter als 3 Tage im Voraus plant, da Flüge, die mehr als 3 Tage in der Zukunft liegen, nicht von Passagieren berücksichtigt werden.

## Haben die Fluggäste ein genaues Ziel vor Augen oder sind sie flexibel genug, um auf nahe gelegene Flughäfen auszuweichen?

Die Fluggäste haben den Wunsch, einen bestimmten Flughafen zu erreichen. Allerdings kann auch der Bodenverkehr Bestandteil einer Reise sein. Siehe [Flight Rating System]({{< relref "docs/advanced/bookings/flight-rating-system/index.de.md" >}}) für weitere Einzelheiten.

## Gibt es eine Möglichkeit, den grünen Nachfragebalken eines Flughafens eine genaue Anzahl von Passagieren zuzuordnen, die zwischen zwei Flughäfen fliegen wollen?

Nein! Das müsst ihr selbst ausprobieren.

## Wenn zwei Flüge für dieselbe Strecke unterschiedliche Bewertungen haben, buchen dann alle Passagiere den höher bewerteten Flug oder werden sie proportional verteilt?

In diesem Fall wählen Passagiere die Flüge proportional zur Gesamtbewertung für die gegebenen Verbindungen zwischen zwei Flughäfen aus.
