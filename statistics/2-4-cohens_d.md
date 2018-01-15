[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

cohens D for the weight differences between first babies and others is -0.088672927072602 
cohen's D for the pregnancy length differences between first babies and others is 0.029 
These numbers are very small and therefore there is little difference between the weight or pregnancy length of a first born child versus another child.
It is interesting to note that first born children are typically carried for longer than other babies but on average weigh less than other babies.  Again, this difference is very small, 13 hours on average for pregnancy length and 2 oz for difference in weight.  

code:

     
    def WeightDifference(live, firsts, others):
        """Explore the difference in weight between first babies and others.
        live: DataFrame of all live births
        firsts: DataFrame of first babies
        others: DataFrame of others
        """
    
        mean0 = live.totalwgt_lb.mean()
        mean1 = firsts.totalwgt_lb.mean()
        mean2 = others.totalwgt_lb.mean()

        var1 = firsts.totalwgt_lb.var()
        var2 = others.totalwgt_lb.var()

        print('Mean')
        print('First babies', mean1)
        print('Others', mean2)

        print('Variance')
        print('First babies', var1)
        print('Others', var2)

        print('Difference in lbs', mean1 - mean2)
        print('Difference in oz', (mean1 - mean2) * 16)

        print('Difference relative to mean (%age points)',
              (mean1 - mean2) / mean0 * 100)

        d = thinkstats2.CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
        print('Cohen d', d)
