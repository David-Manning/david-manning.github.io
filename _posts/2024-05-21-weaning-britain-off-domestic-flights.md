---
layout: post
title: Weaning Britain off Domestic Flights
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [eda, climate, hs2, rail, trains, air, travel, transport, aviation, environment, carbon, emissions, high speed rail]
comments: true
---

This post is aimed at looking at the impact that Britain copying France's policy banning short term flights might have. The policy in France states that no flights can be taken where train journeys of under two-and-a-half hours exist. This was originally planned to be a four hour limit but was watered down. Connecting flights are not affected by this policy, presumably because it would cause those passengers to have a layover in another country and not change anything in terms of emissions.

The policy would have little effect on domestic flights under current circumstances, since only two major routes have train journeys of less than four hours, however connecting Scotland to London via a high speed rail network could have saved 877,000 tons of CO2 per year. There is potential for saving emissions on international train services, but extra capacity would need to be found.

## Flights to/from London
For this, London airports are Heathrow, City, Gatwick, Biggin Hill, Lydd, Luton, Stansted and Southend.

This table shows the daily passenger numbers (averaged over the year) and equivalent (full) trains for the busiest ten domestic flights from London. 
Only Manchester and Newcastle come under the policy (Manchester under the actual policy and Newcastle only under the original proposal). Anecdotally, I have not heard of anyone flying from Manchester to London without an onward connection and all flights are to Heathrow, so I assume most come under the connecting flight exception and London already complies with the French policy, in both its original and implemented form.

|Destination | Passengers| 
|:-----------|----------:|
|Edinburgh   |       3840|
|Belfast     |       3193|
|Glasgow     |       2774|
|Aberdeen    |       1087|
|Manchester  |        804|
|Inverness   |        739|
|Newcastle   |        608|
|Newquay     |        158|
|Derry       |         91|
|Dundee      |         40|

* Manchester is just over two hours on the train, so the 5-8 daily flights from London would come under this policy, except for connecting flights. Since all flights from Manchester are to Heathrow, I assume that most flights are connecting flights, and most flights are probably compliant with the French policy anyway.
* Newcastle is around three hours on the train, so the six flights per day would apply to the original proposal but not the policy as implemented. These also go to Heathrow, but since the train is longer than to Manchester, it may be the case that a few more of these are not connecting flights.
* Belfast and Derry cannot be done in one train journey.
* Glasgow and Edinburgh are both well over four hours from London, so do not come under the policy. Since Aberdeen, Dundee, and Inverness are further north, those trains will take even longer.
* Newquay does not have direct trains to London, and the Cornish city Truro is more than four hours from London. 

## London-Manchester: Train vs Plane
Here is why I don't think there are many people flying between London and Manchester. 

If I want to go from the front door of London Euston to the front door of Manchester Picadilly, I would have a 2h 06m journey:

* Walk for two to three minutes to the platform
* Get on a train
* Travel for two hours and six minutes (while working)
* Walk for another two to three minutes to the front door

If I want to do the same by flying, I would have a 1h 44m journey, saving (at best) 22 minutes.

* Spend ten minutes going through security
* Walk for two to three minutes to the gate
* Board the plane thirty minutes before the flight
* Spend five minutes taxiing
* Fly for 45 minutes (working for perhaps 30 minutes)
* Another five minutes taxiing
* Five minutes to leave the plane
* Another two to three minute walk to the front door

This assumes that there is no journey time to get to the airport or station, but most people will be going to the city centre on at least one end, which adds extra travel time to the flight.

A second argument is to compare to flights to/from Inverness, which has similar numbers to flights to/from Manchester despite having less than a tenth of the population, not having as many surrounding cities, and not having a quick train service (eight hours each way), or perhaps Belfast where every journey is a flight, which despite having only a slightly smaller population has several times the number of airline passengers.

## Flights Elsewhere
Next, we can look at the rest of the country. 
Here are the passenger numbers for the busiest ten routes excluding London and Northern Ireland:

|City 1     |City 2      | Passengers|
|:----------|:-----------|----------:|
|Bristol    |Edinburgh   |        587|
|Bristol    |Glasgow     |        411|
|Birmingham |Edinburgh   |        298|
|Birmingham |Glasgow     |        227|
|Bristol    |Newcastle   |        199|
|Edinburgh  |Southampton |        124|
|Glasgow    |Southampton |        121|
|Bristol    |Inverness   |        116|
|Manchester |Newquay     |        104|
|Aberdeen   |Manchester  |         99|

None of these routes are under four hours, so do not come under the policy, and looking through the full dataset, the busiest route which does have scheduled flights and would come under the policy was Manchester-Edinburgh which takes just over three hours by train and is a flight route that no longer exists, so the rest of England also de facto complies with this policy.

* Birmingham to Edinburgh / Glasgow trains all take just over four hours, so are not affected. As before, this also means trains from Birmingham to Aberdeen/Inverness or Glasgow/Edinburgh to Bristol are not affected by the policy either.
* Bristol to Newcastle takes just under five hours.
* Manchester has no direct trains to Cornwall, and it takes more than four hours to get to Exeter, which is in Devon, so is not included.
* Manchester has no direct trains to Aberdeen, and it takes around six hours with connections.
* Southampton has no direct trains to Scotland, and, unsurprisingly, it takes around seven hours.

## International Trains
London also has international train services to Lille, Paris, Brussels, Rotterdam, and Amsterdam. All are reachable within the original four hour limit and Lille, Paris, and Brussels are easily less than two-and-a-half. I want to look at what capacity increase is needed if the policy applied to international travel as well as domestic. The Eurostar is often fully booked and the limiting factors here are the space for passport control and the tunnel, which also carries a lot of freight -- I am not claiming that the capacity is easy to unlock.

Eurostar trains carry 902 people each, so the table also shows how many extra full trains are needed to meet the flight demand. Clearly, there are many flights to the main capitals and this *would* have a big impact on CO2 emissions, if there was capacity to do so. Less than half of trains to Brussels go on to Amsterdam, so those six or seven extra trains would need to be scheduled and capacity found somewhere. There is no standing on Eurostar trains, so the capacity cannot be found by simply squeezing people in as often happens on domestic trains.

|Country     |Euro City |British City | Passengers| Trains|
|:-----------|:---------|:------------|:----------|:------|
|Netherlands |Amsterdam |London       |       4873|   5.40|
|France      |Paris     |London       |       2880|   3.19|
|Belgium     |Brussels  |London       |        814|   0.90|

## The Effect of Introducing High Speed Rail to Scotland
London is 550 miles / 885km from Aberdeen and 568 miles / 914km from Inverness. This puts both in range for a four hour train journey. This section looks at how much CO2 can be saved by taking a high speed train, if such lines existed. The numbers here are only provided for the routes on a London-Scotland line and only for the routes listed above (ignoring smaller routes).

The base case for this is Manchester: with a population of 550k and 800 passengers per day, it has a population of 687 per daily passenger. Applying this to some of the other cities we get this (CO2 saved is tons based on a single round trip on an A320, from myclimate.org). This only counts flights from London.

|City      |Population |Passengers |Ratio |New Pass |CO2 Saved |
|:---------|:----------|:----------|:-----|:--------|:---------|
|Aberdeen  |261k       |1087       |240   |410      |0.379t    |
|Edinburgh |536k       |3840       |140   |841      |0.347t    |
|Glasgow   |635k       |2774       |229   |997      |0.354t    |
|Inverness |47k        |739        |64    |74       |0.400t    |

This represents a potential annual saving of 877,000 tons of CO2, or the equivalent of removing 183,000 American passenger vehicles from the road.

Assuming that all flights from Scotland to Birmingham and Manchester were no longer viable, these flights would save 70,170 tons of CO2 per year.

|City 1     |City 2      |Passengers |CO2 Saved |
|:----------|:-----------|:----------|:---------|
|Birmingham |Edinburgh   |        298|0.305t    |
|Birmingham |Glasgow     |        227|0.310t    |
|Aberdeen   |Manchester  |         99|0.313t    |

## The Data
Data were taken from the CAA's website and apply to the whole of [2023](https://www.caa.co.uk/data-and-analysis/uk-aviation-market/airports/uk-airport-data/uk-airport-data-2023/annual-2023/), tables `12 1` (international air passengers) and `12 2` (domestic air passengers).
The data are **total** travellers so I divided by 2 to get the traffic each way and then by 365 to get the daily average. This does not account for seasonality and the data are for the whole of 2023. The data do not cover all of the smaller airports around the highlands and islands of Scotland, but high speed rail is unlikely to be economical in those areas.
