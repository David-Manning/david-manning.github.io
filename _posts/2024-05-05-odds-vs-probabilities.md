---
layout: post
title: Odds vs Probabilities
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [primer, probabilities, odds, betting]
comments: true
---

Odds are just another way of writing probabilities, usually for betting purposes. This post explains how to convert between probabilities and the three main types of probabilities.

## Fractional Odds
Fractional odds are most widely used in the UK. They are shown as the profit you make if you win the bet, e.g. 5/1 means your potential profit will be 5 times the stake and 1/5 means your potential profit will be a fifth of your original stake. The stake is returned on top of the odds.

To calculate the probability equivalent to fractional odds, calculate denominator(denominator + numerator). In the odds 31/25, this gives us a probability of 25/31+25 = 0.45.
To go the other way, take the decimal, add one, and turn it into a fraction. To get back to odds from the probability 45%, we get odds of 9/20+1= 29/20 (this is different only due to the error caused by rounding).

## Decimal Odds
Decimal odds are used in mainland Europe, but are also easier to work with on a computer. They represent a multiple of the stake you get back if you win, or your total revenue and can be any number larger than 1.

To calculate the probability equivalent to the decimal odds, calculate the reciprocal of the odds (and vice versa). A probability of 0.45 has decimal odds of $1 / 0.45 = 2.2$.

## Fractional Odds to Decimal Odds

To convert fractional odds into decimal, turn it into a decimal and add one - fractional odds of 31/25 become decimal odds of 31/25 + 1 = 2.24.
To convert decimal odds into fractional, subtract one and turn it into a fraction - decimal odds of 2.2 become 1.2, which expressed as a fraction are 29/20 (as before, this is a rounding error).

## Getting an Implied Probability

Probabilities of events must sum to 1, but betting odds usually sum to more than this to give the bookmaker some profit. To find the probability that the market expects then we rescale the probabilities from the odds. If a football match has given odds of home: 13/10, draw: 9/5, away: 12/5 then we can calculate the priced probabilities as home: 43%, draw: 36%, away: 29%, or a total of 108%. This 8% is the margin taken by the bookmaker and we can calculate the probability of a home win by dividing each of the probabilities by 1.08 to get implied probabilities of home: 40%, draw: 33%, away: 27%.

When betting, you should compare your estimated probability of the event to the priced event and if you want to work out how well the market can predict events or know how likely an event is then you should use the implied probability.
