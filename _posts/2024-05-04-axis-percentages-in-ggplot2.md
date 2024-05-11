---
layout: post
title: Axis Percentages in ggplot2
subtitle: A quick code snip
gh-repo: David-Manning/david-manning.github.io
gh-badge: [star, fork, follow]
tags: [code_snip, ggplot2, percentage, formatting, graph, plot, visualisation, R]
comments: true
---

This is a quick post to remind myself how to format ggplot2 axes as percentages. Google can return two ways, one of which is deprecated. This is the current way.

## Generating data
Let's start by generating some test data, `x`, `x2`, and `y` variables are all continuous in the range (0, 1).

```
set.seed(2024)
df_perc <- data.frame(x = runif(n = 100),
                      y = rbeta(n = 100, shape1 = 7, shape2 = 10))
df_perc$x2 <- df_perc$x / 1000
```

## Default behaviour

If we plot this with ggplot2, the axes label markers give numbers like 0.2, 0.4, etc, which is not what we want.
```
ggplot(data = df_perc, mapping = aes(x = x, y = y)) +
    geom_point() +
    labs(title = "Graph with numeric labelling") +
    theme_bw()
```

![Graph1](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-05-04-ggplot2-axes/graph1.png?raw=true)

## Correct behaviour

Adding `scale_x_continuous(labels = scales::percent_format())` will fix this. It has to be done separately for each axis. 

```
ggplot(data = df_perc, mapping = aes(x = x, y = y)) +
    geom_point() +
    labs(title = "Graph with numeric labelling") +
    scale_x_continuous(labels = scales::percent_format()) +
    scale_y_continuous(labels = scales::percent_format()) +
    theme_bw()
```

![Graph2](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-05-04-ggplot2-axes/graph2.png?raw=true)

## Fractions of a percent

It also works out the correct significant figures, so we don't have to spend time getting the formatting right.
```
ggplot(data = df_perc, mapping = aes(x = x2, y = y)) +
    geom_point() +
    labs(title = "Graph with numeric labelling") +
    scale_x_continuous(labels = scales::percent_format()) +
    scale_y_continuous(labels = scales::percent_format()) +
    theme_bw()
```

![Graph3](https://github.com/David-Manning/david-manning.github.io/blob/master/images/2024-05-04-ggplot2-axes/graph3.png?raw=true)
