---
title: 'Coins and Factors'
date: 2017-12-29
permalink: /posts/2017/12/blog-post-001/
tags:
---

I love Fivethirtyeight's Riddler column.  Every Friday morning, I wake up, have myself a coffee, and try to solve the latest puzzle.

[Here](https://fivethirtyeight.com/features/can-you-survive-this-deadly-board-game/) is the first puzzle I ever solved.  It is a simple puzzle, yet it has an elegant computational and analytic solution.  Let's take a look.

The puzzle says:

>You place 100 coins heads up in a row and number them by position, with the coin all the way on the left No. 1 >and the one on the rightmost edge No. 100. Next, for every number N, from 1 to 100, you flip over every coin >whose position is a multiple of N. For example, first you?ll flip over all the coins, because every number is a >multiple of 1. Then you?ll flip over all the even-numbered coins, because they?re multiples of 2. Then you?ll flip >coins No. 3, 6, 9, 12 ? And so on.
>
> What do the coins look like when you?re done? Specifically, which coins are heads down?


##Computing the Solution

This is really easy to program.  Here is a little python script to compute the solution:

```python

import numpy as np
import matplotlib.pyplot as plt


# Array of 100 True.  True is Heads up
coins = np.ones(100,dtype = bool)

#Go through the coins
for i in range(100):
    
    N = i+1
    factors = np.array([j for j in range(N,101) if j%N==0]) #Find all numbers which are have N as a factor
    
    coins[factors-1] = ~coins[factors-1]  #Flip the coin
  
```


When we take a look at the `coins` variable, we see that those coins in positions which are perfect squares pop out.  That is an interesting result, but what is more interesting is reasoning out the solution without doing any computation at all!


![][/images/blog/coins.png)

#Reasoning Out the Solution.