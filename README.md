# Crime-in-US-Communities
 Can unsupervised learning be used to quantify crime-related differences in US communities?

Slide Type

The dataset includes data taken from the 1990 US Census, 1995 FBI Uniform Crime Report, and 1990 US Law Enforcement Management and Administrative Statistics Survey. Data were normalized within a range of 0-1. Distributions were preserved, except for data that were >3 SD above the mean which were normalized to 1. Relationships within features are preserved while relationships between features are not. One major caveat of this dataset is the relatively small sample size (n=1994).

To avoid cheating...

I am going to avoid using the ViolentCrimePerPop variable in my clustering to ensure that our clustering algorithms do not cluster using this feature. This will replicate a truly 'unsupervised' approach. If these techniques are effective, we should be able to see a difference in this variable between groups at the end.

Tools used- PCA, KMeans, Spectral clustering, Mean shift, Bayesian Gaussian Mixed Models


# Summary and take-aways

The unsupervised clustering we did with PCA and KMeans was effective in grouping our communities into 3 distinct groups. While using the ViolentCrimesPerPop variable to create a supervised model would have likely given us a better understanding of the specific features that predict violent crime, the unsupervised approach was still useful.

One final caveat for those reading is that the features we sorted using the ANOVA do not provide any indication of causuality. For example, PctRecImmig10 was the variable with the greatest F-Statistic from the ANOVA tests, indicating it has the greatest groups differences among the clusters. However, it does not indicate that this variable is having any causual effect on crime in these communities. All we can conclude from these findings is that the KMeans algorithm was able to generate clusters which showed group differences in these features.

Future application of this research should be done with experts in socioeconomic policy to identify how to tackle these issues. 
