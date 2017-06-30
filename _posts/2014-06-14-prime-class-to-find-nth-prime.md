---
title: Prime class to find nth prime
tags: code
---

Github link: [https://github.com/goutham2027/prime](https://github.com/goutham2027/prime)

{% highlight python %}
class Prime:

    def __init__(self):
        pass

    def nthprime(self,n):
        ''' Find n-th prime '''
        primecount = 1
        prime = 0
        while primecount <= n:
            prime = self.getnextprime(prime)
            primecount+= 1
        return prime

    def isprime(self,num):
        ''' Checks whether given number(n) is prime or not  '''
        squareroot = math.sqrt(num)
        for i in range(2,int(squareroot)+1):
            if num % i == 0:
                return False
        return True

    def getnextprime(self,num=1):
        ''' Get (n+1)th prime '''
        if num < 2:
            return 2
        nextnum = num + 1
        while not self.isprime(nextnum):
            nextnum += 1
        return nextnum

    def getpreviousprime(self,num):
        ''' Get (n-1)th prime '''
        if num <= 2:
            return 2
        previousnum = num - 1
        while not self.isprime(previousnum):
            previousnum -= 1
        return previousnum

    def getallprimes(self,num):

        ''' Get all primes less than the given number '''
        ### implement with a hint argument which gives the list of already existing primes ###
        primes = []
        prime = 2
        while prime <= num:
            primes.append(prime)
            prime = self.getnextprime(prime)
        return primes
{% endhighlight %}
