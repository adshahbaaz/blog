---
title: 'Project Euler: Problem 14 - Longest Collatz Sequence'
author: ''
date: '2022-11-14'
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
collatz = function(x) {
  n= 2:x

  trk=c()
  sq = list()
  
  ind = 1
  
  for(v in n){
    cnt = 0
    
    while(v>1){
      
      if(v%%2==0) {
        v =   v/2
      }
      else {
        v = (3*v +1)/2 
      }
      
      #print(v)
      cnt = cnt +1
      
    }
    
    trk[ind] = cnt
    ind = ind +1
  }
  cat("The number with the highest number of terms in the collatz sequence from odd numbers 1 to",x,"is", n[which.max(trk)] ,"with a total of",trk[which.max(trk)],"terms.","The sequence is")
}

system.time(collatz(1e6))
options("scipen" = 400,"digits"=4)
```