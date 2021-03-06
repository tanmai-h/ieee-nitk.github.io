---
layout: post
title: "Is Random really Random?"
author_github: subbalakshmi
date: 2017-08-04 03:48:33
image: '/assets/img/'
description: "Random implies indeterminacy (One can't possibly know, what will happen next). At the same time, the result of a computer program is deterministic (If you know the algo, then you know the answer). If that is the case, then is it possible that the random numbers that a computer generates is not truly random?"
tags:
- random
- PRNG
- TRNGs
- cryptography
- Lehmer's RNG
categories:
- Diode
github_username: 'subbalakshmi'
comments: true
---

Random numbers have been used for many thousands of years. 
Roll a dice. 
Flip a coin. 
Pick a card from a deck. 
Whatever the result may be in these three situations, it’s completely random each time and there’s no way of predicting it by looking at the previous outcomes. 
In other words, the end result is left to random chance.

![Dice](/blog/assets/img/random-number-generator/dice.jpg)

Random number generators in a computer are similar: they’re an attempt to achieve an unpredictable, random result. 
From creating random keys for data encryption to random shuffling cards in a poker website, generation of random numbers is vital.

![Gambling](/blog/assets/img/random-number-generator/gamble.jpg)

Now, to generate random numbers we might use the traditional `import random` (python), `randn` (MATLAB) and other packages and functions in other platforms.  
And what do they do? They present to us a randomly picked number.
Simple. 
But have you ever pondered how the computer picks that particular number?

We all know that a computer is good at following instructions. 
It cannot create, or think for itself (until fully functioning Artificial Intelligence becomes a reality). 
If a computer is asked to pick a random number it won’t be able to do so, until and unless it’s told how to do it and this way, the true purpose of randomness is lost.

**Moment of Truth**: Majority of the random number generators used by computers are not truly random. 
The number generated is usually a result of an algorithm.

The random numbers generated by such a way are termed `pseudo-random` i.e it appears random but is actually just a predetermined sequence of numbers. 
The sequence is determined by an initial value known as `seed`.
The Lehmer's Random Number Generation algorithm is one such example of pseudo random generation.

What defines randomness is uncertainty. 
One can never know what will happen next. 
By using algorithms to generate random numbers this property is lost. 
Anyone who gets hold of the algorithm can easily figure out the number.

If random numbers are really generated by a deterministic algorithm, how on earth can we use it for applications as important as cryptography?

In order to generate numbers that are truly random, computers must find a seed that is truly random. 
This is done by measuring a physical occurrence, or reaction, which happens naturally at random.

Most secure random number generators have an `entropy gathering service` continously running on a machine. 
Its job is to harvest entropy from multiple sources over time.
In other words, it  gathers random information from the environment, stores this information, and then returns it when asked to generate a random number. 
For example, the computer can measure white noise, or can measure the timing of various events like keystrokes and packet arrivals, and combine these in a theoretically valid way to generate numbers randomly.

![Comic](/blog/assets/img/random-number-generator/comic.jpg)

At the end of the day, randomness isn’t limited to securing information and gambling. 
It’s so much more. 
Look around you. 
The electronic noise in our devices is random. 
Radioactive Decay is random.
The world is governed by chance. 
Randomness stalks us every day of our lives.Its what keeps us curious, intrigued and excited all along the way! 
