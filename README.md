# matplotlib-challenge

One note: I generated 2 summary statistics table: one creating series and combining them together and one using groupby.aggregate feature. All numbers match except for the variance and standard deviation columns, which differ slightly. This is because the method combining series uses ddof=0 for variance and std dev. Meanwhile, the aggregate feature has a default ddof = 1. I plan to do a little more research to determine how to update the ddof in the groupby.aggregate function.
