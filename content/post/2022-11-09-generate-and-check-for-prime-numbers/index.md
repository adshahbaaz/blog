---
title: Generate and Check for Prime Numbers
author: ''
date: '2022-11-09'
slug: ''
categories:
  - R
tags:
  - Project-Euler
  - algorithms
draft: true
---


#/* Prime numbers */ #
p=1523



v

isprime = function(p){
  
  if(p <0) return(F)
  
  fct = 2
  sieve = 2:floor(sqrt(p))
  isprime = T
  
  while(!is.na(fct)) {
    
    if(p%%fct==0) {isprime=F ; break}
    
      sieve = sieve[sieve%%fct!=0]
    
  #  if(!p %in% sieve){ isprime= F; return(FALSE)}
    
    fct = sieve[1]
  }
  
  return(isprime)
  
}

system.time(sapply(seq(1e6,2e6,10),isprime))
system.time(sapply(seq(1e6,2e6,10),ISprime))

sapply(seq(1e6,2e6,10),ISprime)

#///

  prime_gen = function(n){
  
  
  range = 2:n
  p =2
  sum=0
  primes = 0
  i = 1
  
  while(p<sqrt(n)){
    
    p = range[1]
    primes[i] = p
    sum = sum + p
    range = range[range%%p!=0]
    i = length(primes) + 1
  }
return(c(primes,range))
}

isprime(10)
isprime(2e6)

n=10
range
system.time(isprime(1e5))

PrimeSieve <- function(n) {
  if (n <= 1) {
    primes <- numeric(0)
  }
  if (n == 2 | n == 3) {
    primes <- 2:n
  }
  else {
    numbers <- 2:n
    sieve <- rep(TRUE, times = n - 1)  # let all flags to be TRUE
    cross.limit <- floor(sqrt(n))
    count <- 1   
    p <- numbers[sieve][count]  # let p be the first sieve number
    while (p <= cross.limit) {
      sieve[p * (2:floor(n / p)) - 1] <- FALSE
      count <- count + 1
      p <- numbers[sieve][count]
    }   
    primes <- numbers[sieve]
  }
  return(primes)
}
result <- sum(as.numeric(PrimeSieve(2e6)))
cat("The result is:", result, "\n")

system.time(PrimeSieve(2e6))
system.time(isprime(2e6))

system.time(PrimeSieve(1e5))
isprime(10)

