---
layout: post
title: Building a Fixed Link to Ireland
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [eda, climate, hs2, rail, trains, air, travel, transport, aviation, environment, carbon, emissions, irish tunnel, irish rail, irish sea, infrastructure]
comments: true
---

This post is a follow up to my last one about high speed rail in Britain, about the capacity needed for a fixed Irish Sea crossing, replacing flights. It isn't intended to be a full feasibility study, rather a back of an envelope calculation to get a basic idea of viability. I am not taking into account any geological or political issues here.

Even with some very favourable assumptions, the tunnel does come close to adding up and construction costs alone would cost each passenger £445 per round trip.

## Assumptions

I am assuming a lot of here:

* A high speed network can already connect major cities on each island. This would put both islands on a high speed rail footing similar to Germany. 
* Trips to London will be reduced to the same rate that London-Manchester has now (637 population per daily passenger, each way).
* Trips elsewhere will be banned.
* Trains can carry 528 passengers, the size of trains on HS2.
* The tunnel will go from Holyhead to Dublin, which maximises the viable routes on either side of the sea.

## London Flights

There are only seven airports on Ireland serving London. Derry and Kerry airports are both very small - I have set the number of flights to Derry to 0 because there would be a negative number of flights there. Knock is a village and serves a large area of small towns, I have kept this in the table on the basis that it doesn't influence the numbers too much. Kerry's population is for County Kerry.

|City     | Passengers| Population| Train Pass| Trains per Day|
|:--------|----------:|----------:|----------:|--------------:|
|Belfast  |      3,193|    341,877|      2,656|           5.03|
|Cork     |      1,206|    208,669|        878|           1.66|
|Derry    |         91|    105,884|          0|           0.00|
|Dublin   |      6,275|  1,173,179|      4,433|           8.40|
|Kerry    |        251|    147,707|         19|           0.04|
|Knock    |        512|        963|        510|           0.97|
|Limerick |        856|     94,192|        708|           1.34|

As before, these trips are each way. This is a total of 9204 people who would now get the train every day, requiring 17.4 trains per day.

## Non-London Flights

There are 56 routes going to other cities - many are small, but since trains can collect passengers at multiple stops and I am not interested in the details of timetables, I will just sum up the total number of passengers: 13507, requiring 25.6 full trains to travel through each day. Some of these routes can share demand from London, so I am happy to let them average out.

|Irish City |British City  | Passengers| Trains per Day|
|:----------|:-------------|----------:|--------------:|
|Dublin     |Manchester    |      1,340|           2.54|
|Dublin     |Birmingham    |      1,116|           2.11|
|Dublin     |Edinburgh     |      1,004|           1.90|
|Belfast    |Manchester    |        940|           1.78|
|Belfast    |Edinburgh     |        765|           1.45|
|Belfast    |Liverpool     |        708|           1.34|

## Total Throughput and Costs
Under my assumptions, we would see 43 trains travelling each way under the Irish Sea per day - if they ran for 18 hours per day then this would average one full train every 25 minutes, which is perfectly feasible and leave some capacity for overnight freight or extra services to cover extra demand. There would be 22711 people using it each way per day, or 8.3 million per year, or 414 million over the first fifty years.
Assuming this route has the same cost of the much shorter tunnel from Scotland to Northern Ireland ([£209bn](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/1035650/a-fixed-link-between-great-britain-and-northern-ireland-technical-feasibility.pdf)), this would cost each passenger £505 per round trip, just for the construction cost. Hmm.

One ton of CO2 will cost at least [£92](https://www.gov.uk/government/publications/traded-carbon-values-used-for-modelling-purposes-2023/traded-carbon-values-used-for-modelling-purposes-2023) in the 2040s. The 414 million people using the train over flights would save 340kg of CO2 each for each round trip (myclimate.org). 
With a best logical case assumption that carbon costs £172/ton at all times and the train produces no carbon, this would cost £58 per passenger per round trip, reducing the (already probably far lower than reality) tunnel construction costs per passenger to £445. Hmm.

One final assumption: if all 35,000 people travel by train and extra demand doubles this to 70,000, then 1.28 billion people would use it in the first fifty years. Would it still be worth it? It would still cost £108 per person traveling just for the (already probably far lower than reality) tunnel construction cost. Hmm.
