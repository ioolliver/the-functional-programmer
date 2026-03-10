---
title: 'Comparing sorting algorithms'
description: 'How much faster is Merge sort compared to Insertion sort? I tested it and compared it.'
pubDate: 'Mar 05 2026'
heroImage: '../../assets/blog-placeholder-3.jpg'
---

Hello, world! This is my first blog post :)

Some weeks ago I was studying the Cormen - Introduction to algorithms and I saw this exercise:

<br />

**Exercise 4.1-3**

*Implement both the brute-force and recursive algorithms for the maximum-subarray problem on your own computer. What problem size n0 gives the crossover point at which the recursive algorithm beats the brute-force algorithm? Then, change the base case of the recursive algorithm to use the brute-force algorithm whenever the problem size is less than n0. Does that change the crossover point?*

<br />

To be honest, i found this exercise fantastic. I like to compare approaches and results. I first answered the exercise, and I found:

For $n >= 40$, the O(n log n) max-sum subarray algorithm works better than the brute-force O(n^2) method. I also made a mixed algorithm and got those results:

<br />

![Terminal screenshot showing benchmark results for max_sum_experiment.c compiled with GCC. The program runs 500,000 iterations per input size and reports average execution time in milliseconds. A table lists sizes from 30 to 50 with three columns: Brute Force, O(n log n), and Mixed. Brute Force starts around 0.00094 ms at size 30 and increases to about 0.00214 ms at size 50. The O(n log n) algorithm ranges from roughly 0.00116 ms to 0.00190 ms. The Mixed approach is generally fastest, ranging from about 0.00090 ms to 0.00145 ms. Execution time gradually increases as the input size grows.](../../assets/blog/comparing-sorting-algorithms/max_sum_experiment.jpeg)

<br />

As you can see, for each n, I run 500,000 iterations for each algorithm with random arrays and calculated the average from it all. We can see that brute force works better for n < 40. The mixed algorithm, however, did better in every n.

# Why the brute-force algorithm beats the O(n logn) algorithm for small n?

