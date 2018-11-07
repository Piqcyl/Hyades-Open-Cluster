# The Hyades

Below is a qualitative summary of the method used to analyze the Hyades. My advisor intends for me to test the limits of this method going forward.

- Note: My other repository "Pleiades-Open-Cluster" is a refined version of this method applied to a more distant star cluster.

# Process

“Hyades1” - (Data with spectroscopic observations) 

1. Import data without radial velocity
2. Assume data is normally distributed and biased towards cluster parameters. Use this to filter extreme observations.
3. Extend proper motions to identify moving cluster point of convergence. 
4. Calculate lambda using relationship between parallax, radial velocity, and proper motion. Work backwards to test if formula for radial velocity is correct.
5. Inspect outliers in lambda, lambda error, rv, and rv error.  (3d plot as well as moving cluster point of convergence)
6. Print relevant statistics and plots regarding rv, and lambda which will be useful when analyzing Hyades2
7. Finalized dataset, “final”

“Hyades2” - (Data with spectroscopic observations)

1. Similarly as in step (2), preform hypothesis testing with normal distribution by testing against “final”, a more representative distribution of Hyades cluster.
2. Using filtered lambda data, calculate the average and run it through moving cluster relation to calculate radial velocities for stars with out spectroscopic observations. 
3. Extend proper motions to identify moving cluster point of convergence. 
4. Investigate outliers for proper motion, proper motion error, calculated radial velocity, and calculated radial velocity error.
5. Use personal judgement to decide on what constitutes an “extreme value” and filter accordingly. 
6. Finalized dataset, “final1”.

# Conclusion

1. Plot color magnitude diagram of “final” + “final1”
2. Implement parametric bootstrap to create confidence interval for distance (parsecs.
3. Show 3d plot of cluster and print calculated statistics of interest (all of which have propagated errors) as well as previous estimates in astrophysical literature. 

Previously, I concluded that are around 330 stars in the Hyades cluster. In my most recent revision I decided to tighten my definition of membership via point of convergence and filtering of extremities uncharacteristic of the core population of stars. For most of these extremes, they tended to miss the point of convergence or converge with another extreme outside of the interval. I assume these stars are on the fringe of being considered “core members” and are possibly being stripped due to some nearby gravitational. Interestingly they all tend to appear in the same area, further supporting this idea. 

# Concerns

- Despite making the criterion for membership stricter, I believe that my application of statistics is weak and a few non-members go un-detected. One of these stars that looks suspicious is the one just below the middle of the main sequence on the final color magnitude diagram. My first thought is that this is one of the stars mentioned above but another guess is that it’s a stray star that was born from a different protostellar cloud and wandered into the gravitational pull of the Hyades.  
- In order to effectively generalize this method to other moving groups I intend to systematize my determination of point of convergence. Another region that needs to be systemetized is determining what constitutes an extreme observation. Possible application of extreme value theory to quantify this. 

# References
1. http://articles.adsabs.harvard.edu/cgi-bin/nph-iarticle_query?1998A%26A...331...81P&amp;data_type=PDF_HIGH&amp;whole_paper=YES&amp;type=PRINTER&amp;filetype=.pdf

2. https://arxiv.org/pdf/1804.00759.pdf

3. http://cds.cern.ch/record/524614/files/0110617.pdf

4. https://arxiv.org/pdf/1410.0192.pdf

5. http://www.geol.lsu.edu/jlorenzo/geophysics/uncertainties/Uncertaintiespart2.html
