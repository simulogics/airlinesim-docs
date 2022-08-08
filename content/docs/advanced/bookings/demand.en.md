---
title: "Demand Calculation"
weight: 2
---

# Demand Calculation

To help you get a better understanding of how demand works in AirlineSim, here is a general Q&A.

## Does the time of day matter when it comes to flights?

No, passengers will treat all flight departure and arrival times equally. Total travel time does affect the flight rating, though.

## Does passenger demand vary seasonally?

No, seasonal changes currently don't play a role when it comes to demand.

## Do passengers care which day they fly?

Passengers book flights only within the next three days, but will book any of those if some days are full or unavailable. If there are no flights available, those passengers never book a flight - they'll have to drive, hitchhike or swim for this trip!

## Can I increase load factors by scheduling flights less often than once a day?

Yes, many routes with low demand can be served with flights that don't occur everyday. This won't work if you plan further than 3 days ahead, however, as passengers don't consider flights that lie more than 3 days in the future.

## Do passengers have an exact destination in mind or are they flexible enough to pick nearby airports?

Passengers are generated with a demand to reach a specific airport. However, ground travel can form a component of a trip. See [Flight Rating System]({{< relref "docs/advanced/bookings/flight-rating-system/index.md" >}}) for more details. 

## Is there any way to translate the green demand blocks for each airport into an exact number of passengers that want to fly between them?

Nope! You'll have to try it and see.

## If two flights have different ratings for the same route, will all passengers book the higher flight or are they allocated proportionally?

They are choosing the flights proportionally to the total rating for the given connections between two airports.
