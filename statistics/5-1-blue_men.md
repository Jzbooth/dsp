[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

It was discovered that 34.2746837631% of the U.S. male population falls in the range of 5'10" and 6'1".
code:


    import scipy.stats

    mu = 178
    sigma = 7.7

    dist = scipy.stats.norm(loc = mu, scale = sigma)

    low = dist.cdf(177.8)
    high = dist.cdf(185.42)
    print(high - low)

