[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

Yes the distribution is uniform.
Code:


    from __future__ import print_function

    import numpy as np
    import sys

    import nsfg
    import first
    import thinkstats2
    import thinkplot

    sample = np.random.random(1000)

    pmf = thinkstats2.Pmf(sample, label='PMF')
    cdf = thinkstats2.Cdf(sample, label='CDF')

    thinkplot.pmf(pmf)
    thinkplot.Show(xlabel = 'Random Number', ylabel = 'PMF')

    thinkplot.Cdf(cdf)
    thinkplot.Show(xlabel = 'Random Number', ylabel = 'CDF')

