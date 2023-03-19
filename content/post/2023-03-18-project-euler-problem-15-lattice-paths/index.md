---
title: 'Project Euler: Problem 15 - Lattice Paths'
author: ''
date: '2023-03-18'
slug: [lattice-paths]
categories: ['R']
tags: ['Project-Euler']
draft: true
---

## Introduction


`$x + 5 = y$`

## Solution

```{r fn}

# // compute sums for horizontals/verticals/diagonals 

Msum = function(type="h"){
  
  k = 0:3
  jlim = 0
  h = 0
  v = 0
  d = 0
  
  while(mlim < ncol(m)){
    
  k = k + 1
  mlim = k[length(k)]      
    
  if(type=="h"){
      
      for(i in 1:ncol(m)){
        h = sum(m[i,k])
        v = sum(m[k,i])
        print(c(h,v))
        print(c(i,mlim))
        
      }
    }
    
  if(type == "d"){
      
      r = 1:4
      lim = ncol(m)/2 +1
       
      for(i in 1:lim){
       #lim = r[length(r)]
       cat("for row",r,",for col",k)
       print(sum(diag(m[r,k])))
       r = r+1
        
      }
    }
  }
}

Msum("d")

```

