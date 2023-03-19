---
title: 'Project Euler: Problem 24 - Lexicographic Permutations'
author: ''
date: '2022-11-18'
slug: ''
categories:
  - R
tags:
  - Project-Euler
  - Algorithms
---

## Question




## Solution


```{r}
# /lexicographic permutations */



# //*

f = function(x){
  
  
  
  set = 0:9
  
  
  
  #x=10
  
  
  
  num = c()
  
  j = 0
  
  
  
  
  
  while (length(set)>1) {
    
    
    
    
    n = length(set)
    
    
    
    runs = factorial(n)/n # runs with one number
    
    
    
    
    
    times = ceiling(x/runs)
    
    
    
    
    
    if(runs<x) s_i = times else s_i = 1
    
    
    
    if(s_i==0) s_i==1
    
    
    
    if(s_i > n) s_i = s_i %% n # if index greater than elements in set
    
    
    
    if(x == 0) s_i = 2
    
    
    
    if(runs<x){
      
      
      
      if(times>2) term = runs*(s_i-1) else term = runs
      
      #term =s_i^(times-1)
      
      x = x - term
      
      
      
    }
    
    
    
    
    
    j = j+1
    
    
    
    num[j] = set[s_i]
    
    
    
    set = set[-s_i]
    
  }
  
  return(c(num,set))
  
  
}
```