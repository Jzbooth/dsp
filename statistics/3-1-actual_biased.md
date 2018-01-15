[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

The mean of the unbiased distributions was found to be 1.02420515504 and the mean of the biased distribution was found to be 2.40367910066.  
Code:

    from __future__ import print_function

    import numpy as np
    import sys

    import nsfg
    import first
    import thinkstats2
    import thinkplot

    resp = nsfg.ReadFemResp()

    pmf = thinkstats2.Pmf(resp.numkdhh, label = 'NUMKDHH')


    def BiasPmf(pmf, label):
        new_pmf = pmf.Copy(label = label)

        for x, p in pmf.Items():
           new_pmf.Mult(x, x)

        new_pmf.Normalize()
        return new_pmf
    biased_pmf = BiasPmf(pmf, label = 'observed')
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf, biased_pmf])
    thinkplot.Show(xlabel = 'Number of children', ylabel = 'PMF')

    print(pmf.Mean())
    print(biased_pmf.Mean())

