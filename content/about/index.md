---
title: About
author: ''
date: ''
slug: []
---
<p class="drop"><span class="newthought">This blog records my solutions to mathematical/programming problems using R, Python and/or C++.</span></p>

It also documents interesting implementations of data science techniques, primarily in R.  The site is primarily intended to be a repository for self-study but it is hoped that some of the algorithms developed are of interest to the curious reader. 

Problems have been collated from a variety of websites, but the majority have been taken from the excellent [Project Euler](https://projecteuler.net/). Where appropriate, multiple methods to solve the problem are presented - with a focus on the most elegant solution found. 

The aim is not to write production level code and thus  NOT ALL edge cases will be covered. Therefore, programs may have undefined behaviour for certain user inputs. Similarly, error handling is avoided where not absolutely necessary.

**PROGRAMMING PHILOSOPHY**

A short note about the programming philosophy underpinning the code on this blog:

- The logic of the program must be straightforward.[^1]
- The code must not rely on external libraries for calculations.[^2]
- Brute force methods are only preferable to optimised solutions when the computation time is  `$ <1s $`.
- Every program must use the fewest lines of code without compromising understandability for abstraction.

Due to a frightening lack of natural talent, the code will not obey these rules at all times; but it will serve admirably as a guide.


**POSTS**

Below are a list of posts:

- [The `outer()` Function, Double Sums and a Grumpy Customer](/post/some-lesser-known)



**NOTE ON TAGS**

Posts are tagged [*referred*] if the logic of the code was obtained by referral to other sources. If, for the solution, there is an overdependence on a non-derived mathematical formula - which cannot be found in a GCSE math textbook, for example - the post is tagged [*math.referred*]. Every effort is made to credit the source. Where the solution is developed independent of any consultation, the post is tagged [*independent*]. Given a problem was independently solved, the time it took to come up with a solution is also published.  


There will no doubt be errors and countless refinements possible to the code published -- if found it would be of great benefit to me if you could e-mail me at :   adshahbaaz@gmail.com 


[^1]: What is meant by this is that the control flow of the program must be uncluttered, avoiding nested conditions and loops as much as possible.

[^2]:  All solutions are written using only the 'standard' library of the language being used. This makes the code (more) language agnostic and its intent clearer.


