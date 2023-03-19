---
title: Find the Factors of a Given Number
author: ''
date: '2022-11-12'
slug: ''
categories:
  - R
tags:
  - Algorithms
---

## Introduction




## Proposed Algorithm

```{r}
# find factors 

n=1e3

factors = function(n){
  
  n_l =2 : ceiling(sqrt(n))
  
  f_b = n_l[n %% n_l == 0]
  
 # if prime 
  if(!length(f_b)) return(c(1,n))
  
  f_a = c()
  
  for(i in 1: length(f_b)){
    
    upr = ceiling(sqrt(n)+1):ceiling((n/f_b[i]))
    
    f_a[i] =  upr[upr * f_b[i] == n]
    
  }
  
  
  return(sort(c(1,f_b,f_a)))
}
```