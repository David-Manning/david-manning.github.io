---
layout: post
title: Electoral Calculus' MRP Poll - 2024-05-31
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [uk election 2024, polling, mrp, electoral calculus, survey]
comments: true
---

Electoral Calculus published an MRP poll showing that the Conservatives will be down to 72 seats after the election, or 66 with tactical voting. It is also clear that Reform are taking votes away from the Conservatives, but there has not been much analysis of the impact on that in terms of seats. This analysis is done on the no tactical voting scenario (there is a good analysis [here](https://www.electoralcalculus.co.uk/blogs/ec_tactical_20240531.html)) and assumes uniform swings to this poll.

## The Poll
The [poll](https://www.electoralcalculus.co.uk/blogs/ec_vipoll_20240531.html) was conducted from 20th to 27th May 2024 in Great Britain only (so excluding Northern Ireland). It doesn't show Reform winning any seats, but taking 12% of the vote (mostly from the Conservatives).

| Party        | Vote % | Seats (no TV) | Seats (TV) |
|:-------------|:-------|:--------------|:-----------|
| Labour       | 46%    | 493           | 476        |
| Conservative | 19%    | 72            | 66         |
| Lib Dem      | 10%    | 39            | 59         |
| SNP          | 3%     | 22            | 26         |
| Plaid        | 1%     | 4             | 3          |
| Green        | 8%     | 2             | 2          |
| Reform       | 12%    | 0             | 0          |
| Other        | 2%     | 0             | 0          |

## Scenario 1 - Reform to Conservative
The most common assumption is that Reform voters are on the right and would prefer a Conservative government to Labour. On the simplistic assumption that they would prefer Rishi Sunak to Keir Starmer, this assumes that x% of Reform voters go to the Conservatives, with no other changes.

The percentage in this table is the percentage of votes Reform lose.
Even if *all* Reform voters move to the Conservatives, the poll is bad news. But perhaps not terrible, since 219 seats is better than the Conservatives got in 2005 or Labour got in 2019, and on the upper end of predictions. It also shows how sensitive Conservative performance is to the Reform vote.

It's also interesting that this change also pushes the Lib Dems back.

|Party        | Seats (0%)| Seats (25%)| Seats (50%)| Seats (75%)| Seats (100%)|
|:------------|----------:|-----------:|-----------:|-----------:|------------:|
|Labour       |        492|         460|         421|         391|          364|
|Conservative |         72|         109|         154|         187|          219|
|Lib Dem      |         39|          34|          28|          26|           22|
|SNP          |         22|          22|          22|          22|           22|
|Plaid        |          4|           4|           4|           3|            2|
|Green        |          2|           2|           2|           2|            2|
|Other        |          1|           1|           1|           1|            1|

Here is a graph of how this changes. I was not expecting this to be so linear, but it may be a symptom of MRP making assumptions about constituencies based on national polling.
![img](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-reform-to-con.png?raw=true)

And here for how it affects the smaller parties.

![img](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-reform-to-con-small-parties-only.png?raw=true)


## Scenario 2 - Labour to Greens
There is a lot of anger among the left of the Labour party about Diane Abbott and the obvious place for those voters to go is to the Greens. I don't know how many Labour voters would be tempted by the Greens, but I think it is quite low - I don't think it is plausible that this number will exceed 20% and it is likely to be much lower (20% of Labour voters would give the Greens about 17% of the total vote).

The Greens won't win extra seats this way but it also takes a lot to make a dent in Labour's lead, so unlike disgruntled voters on the Conservative's right, left-leaning Labour voters can stray quite safely. It does increase the Conservative seats, but even at the very upper end, this is worse for the Conservatives than 1997 was.

|Party        | Seats (0%)| Seats (1%)| Seats (5%)| Seats (10%)| Seats (15%)| Seats (20%)|
|:------------|----------:|----------:|----------:|-----------:|-----------:|-----------:|
|Labour       |        492|        486|        474|         446|         413|         384|
|Conservative |         72|         76|         87|         107|         132|         155|
|Lib Dem      |         39|         40|         40|          42|          43|          45|
|SNP          |         22|         23|         24|          29|          36|          39|
|Plaid        |          4|          4|          4|           4|           4|           4|
|Green        |          2|          2|          2|           2|           2|           3|
|Other        |          1|          1|          1|           2|           2|           2|

Here is the graph:
![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-labour-to-green.png?raw=true)

Here is the graph only showing the smaller parties. 
![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-labour-to-green-small-parties-only.png?raw=true)


## Scenario 3 - Labour to the Conservatives
A lot of traditional Conservative voters are leaving the Conservatives at this election. How many does it take for them to switch to the Conservatives to cause trouble for Labour?

For context to this table, 30% of Labour voters going to the Conservatives is similar to 2019 levels of support for Labour, with a similar number of seats all round.
The thing that should worry Conservatives about this table is that by getting 10% of Labour voters (4.6% of the voters), the Conservatives can get upto where they were in 1997. A very large swing here can also help the SNP.

|Party        | Seats (0%)| Seats (1%)| Seats (5%)| Seats (10%)| Seats (15%)| Seats (20%)| Seats (25%)| Seats (30%)|
|:------------|----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|-----------:|
|Labour       |        492|        484|        454|         395|         342|         300|         242|         190|
|Conservative |         72|         79|        111|         165|         217|         258|         316|         367|
|Lib Dem      |         39|         39|         36|          36|          31|          30|          28|          27|
|SNP          |         22|         23|         24|          28|          34|          37|          39|          42|
|Plaid        |          4|          4|          4|           4|           4|           3|           3|           2|
|Green        |          2|          2|          2|           2|           2|           2|           2|           2|
|Other        |          1|          1|          1|           2|           2|           2|           2|           2|

Again, here are the graphs showing the impact overall and to the smaller parties. 
![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-labour-to-conservative.png?raw=true)

![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-labour-to-conservative.png?raw=true)


## Scenario 4 - Hope for the Conservatives
If we add all these together, does this offer some hope to the Conservatives? What do they need to happen, and how plausible is it?

There are four scenarios:

* Base scenario: the original poll
* Scenario A: 10% of Reform go to the Conservatives, 1% of Labour go to the Greens, 5% of Labour go to the Conservatives
* Scenario B: 25% of Reform go to the Conservatives, 1.5% of Labour go to the Greens, 10% of Labour go to the Conservatives
* Scenario C: 50% of Reform go to the Conservatives, 2% of Labour go to the Greens, 15% of Labour go to the Conservatives

I do expect that something a bit more beneficial than A is will happen over the next month or so, which would get the Conservatives back to 1997 levels (to be clear, this is still a disaster for them). Scenario B is definitely achievable, although still on the upper end of the betting markets. Scenario C seems rather optimistic, but would put the Conservatives as the largest party, albeit in opposition. The question is whether anti-Conservative sentiment is stronger than anything else happening in the election.

|Party        | Base|   A|   B|   C|
|:------------|----:|---:|---:|---:|
|Labour       |  492| 430| 356| 273|
|Conservative |   72| 135| 210| 293|
|Lib Dem      |   39|  34|  29|  25|
|SNP          |   22|  25|  29|  35|
|Plaid        |    4|   4|   4|   2|
|Green        |    2|   2|   2|   2|
|Other        |    1|   2|   2|   2|


## Scenario 5 - Conservatives to Labour
The Conservatives are, if anything, falling further in the polls and Sunak is being seen worse by voters than he was before with Starmer being seen more positively.
It does not need many Conservative voters to switch to Labour for the party to be annihilated - another 5% would push them down to the Lib Dems and 15% would give them fewer seats than even some of the parties from Northern Ireland.
Remember, the only beneficiary in terms of votes in this model is Labour.

|Party        | Seats (0%)| Seats (1%)| Seats (5%)| Seats (10%)| Seats (15%)| Seats (20%)|
|:------------|----------:|----------:|----------:|-----------:|-----------:|-----------:|
|Labour       |        492|        501|        520|         547|         561|         568|
|Conservative |         72|         63|         43|          13|           4|           0|
|Lib Dem      |         39|         40|         41|          46|          42|          40|
|SNP          |         22|         21|         21|          20|          19|          18|
|Plaid        |          4|          4|          4|           3|           3|           3|
|Green        |          2|          2|          2|           2|           2|           2|
|Other        |          1|          1|          1|           1|           1|           1|

Here is the graph as before
![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-con-to-labour.png?raw=true)

And here is the graph of small parties, now including the Conservatives.
![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-con-to-labour-small-parties-only.png?raw=true)


## Scenario 6 - Conservative to Lib Dem

What if more Conservative voters move to the Lib Dems, who are not yet gaining in voters but are becoming more efficient?
It hurts the Conservatives much less than going to Labour, but Labour are the main gainers from this, not the Lib Dems.


|Party        | Seats (0%)| Seats (1%)| Seats (5%)| Seats (10%)| Seats (15%)| Seats (20%)|
|:------------|----------:|----------:|----------:|-----------:|-----------:|-----------:|
|Labour       |        492|        494|        507|         516|         527|         535|
|Conservative |         72|         68|         47|          30|          16|           5|
|Lib Dem      |         39|         41|         49|          57|          60|          63|
|SNP          |         22|         22|         22|          22|          22|          22|
|Plaid        |          4|          4|          4|           4|           4|           4|
|Green        |          2|          2|          2|           2|           2|           2|
|Other        |          1|          1|          1|           1|           1|           1|

![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-con-to-lib.png?raw=true)

![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-con-to-lib-small-parties-only.png?raw=true)

## Scenario 7 - Conservative to Reform
Finally, what happens if Reform take more votes from the Conservatives?
This is less damaging to the Conservatives, but gives Labour even more seats, and actually helps the Lib Dems more by splitting the vote. It also doesn't help Reform at all, unless very large numbers of Conservative voters move to them and Reform completely replace the Conservatives.

|Party        | Seats (0%)| Seats (1%)| Seats (5%)| Seats (10%)| Seats (15%)| Seats (20%)| Seats (40%)|
|:------------|----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|
|Labour       |        492|        495|        509|         519|         533|         543|         548|
|Conservative |         72|         68|         53|          37|          19|           7|           0|
|Lib Dem      |         39|         40|         41|          47|          51|          53|          54|
|SNP          |         22|         22|         22|          22|          22|          22|          22|
|Plaid        |          4|          4|          4|           4|           4|           4|           4|
|Green        |          2|          2|          2|           2|           2|           2|           2|
|Other        |          1|          1|          1|           1|           1|           1|           1|
|Reform       |          0|          0|          0|           0|           0|           0|           1|

![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-con-to-reform.png?raw=true)

![GraphCon](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-06-01-electoral-calculus-mrp-poll/2024-06-01-con-to-reform.png?raw=true)


## Summary
This shows a couple of things. Firstly, that the poll outcomes are sensitive to small fluctuations - 5% of Conservative voters on this poll is still around 1% of the total respondents but moving those 5% to Labour will reduce the number of Conservative seats by 25, likewise just 1% of Labour voters are around 0.5% of total respondents but can increase the Conservative seats by 7. Both of these are well within the margin of error (one reason why I would like these polls to come with probability intervals).

The second is how different parties' voters are influencing the election in other ways:

* Reform voters can hit Labour and the Lib Dems by moving to the Conservatives.
* Labour's left wing voters can protest fairly safely by going to the Greens, the difference being a very small number of seats.
* The Conservative's best chance of getting a respectable result is winning over Reform voters, not Labour voters, but both are obviously better (this assumes they keep the other side).
* Conservative voters thinking about going to Reform should think about the impact on parliament -- they probably do not want to help Labour or the Lib Dems, but those are the only beneficiaries.
* Conservative voters thinking about going to Labour or the Lib Dems can do a lot more damage to the Conservatives by going to Labour than the Lib Dems - if they want to protest safely, then the Lib Dems are the party to vote for.
* Labour voters in Scotland who are more interested in hurting the SNP should stay with Labour.
