---
title: 'Comparing sorting algorithms'
description: 'How much faster is Merge sort compared to Insertion sort? I tested it and compared it.'
pubDate: 'Mar 05 2026'
heroImage: '../../assets/blog-placeholder-3.jpg'
---

Hello, world! This is my first blog post :)

Some weeks ago I was studying the Cormen - Introduction to algorithms and I saw this exercise:

**Exercise 4.1-3**

> Implement both the brute-force and recursive algorithms for the maximum-subarray problem on your own computer. What problem size n0 gives the crossover point at which the recursive algorithm beats the brute-force algorithm? Then, change the base case of the recursive algorithm to use the brute-force algorithm whenever the problem size is less than n0. Does that change the crossover point?

To be honest, i found this exercise fantastic. I like to compare approaches and results. 

I first answered the exercise, and I found:

For n >= 40, the O(n log n) max-sum subarray algorithm works better than the brute-force O(n^2) method. I also made a mixed algorithm and got those results:

[IMAGE HERE]

As you can see, for each n, I run each algorithm with random arrays and calculated the average from it all. We can see that brute force works better for n < 40. The mixed algorithm, however, did better in every n. That happens because we are (as the name suggests) mixing the best of the both worlds: for small n, it is not worth it to divide-and-conquer the array just to find the max sum subarray. This approach have higher constant operations. So in the mixed algorithm we do the divide-and-conquer but, if the current divided array that we are working with is too small, we just apply the brute-force method and it will run faster.