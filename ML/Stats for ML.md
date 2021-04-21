TARGET DECK: STATS ML

when to use T-test, chi square, correlation, and ANOVA  #flashcard 
	 - T-test = 1 numerical(continuous) and 1 column who only has 2 value counts 
	 - chi square - 2 categorical 
	 - correlation (scatterplot) - 2 numerical values
	 - ANOVA - 1 continuous  and 1 or 2 cols with more than 2 values counts 
<!--ID: 1615575406432-->

hypothesis testing #flashcard 
- If you are going to propose a hypothesis, it’s customary to write a statement. Your statement will look like this: “If I…(do this to an independent variable)….then (this will happen to the dependent variable).”
For example: 
 - A good hypothesis statement should:
	- Include an “if” and “then” statement (according to the University of California).
	- Include both the independent and dependent variables.
	-Be testable by experiment, survey or other scientifically sound technique.
	-Be based on information in prior research (either yours or someone else’s).
Have design criteria (for engineering or programming projects).
<!--ID: 1615576351072-->



what is Null Hypothesis  and alternative hypothesis #flashcard 
- If you trace back the history of science, the null hypothesis is always the accepted fact. Simple examples of null hypotheses that are generally accepted as being true are:
	 	- DNA is shaped like a double helix.
		- There are 8 planets in the solar system (excluding Pluto).
		-Taking Vioxx can increase your risk of heart problems (a drug now taken off the market).
# rejecting the null hypothesis
 - Ten or so years ago, we believed that there were 9 planets in the solar system. Pluto was demoted as a planet in 2006. The null hypothesis of “Pluto is a planet” was replaced by “Pluto is not a planet.” Of course, rejecting the null hypothesis isn’t always that easy—the hard part is usually figuring out what your null hypothesis is in the first place.
# alternative hypothesis 
Ten or so years ago, we believed that there were 9 planets in the solar system. Pluto was demoted as a planet in 2006. The null hypothesis of “Pluto is a planet” was replaced by “Pluto is not a planet.” Of course, rejecting the null hypothesis isn’t always that easy—the hard part is usually figuring out what your null hypothesis is in the first place.
![[Pasted image 20210312141153.png]]
<!--ID: 1615576458149-->

measures for central tendency #flashcard 
Mean, mode, and median
<!--ID: 1615576633671-->

quantitative data vs qualitative data #flashcard 
![[Pasted image 20210312141813.png]]
![[Pasted image 20210312141848.png]]
can be an ID or SSN
<!--ID: 1615576768998-->

what is data wrangling #flashcard 
![[Pasted image 20210312142153.png]]
# Goals of data wrangling
	- Reveal a “deeper intelligence” by gathering data from multiple sources
	- Provide accurate, actionable data in the hands of business analysts in a timely matter
	- Reduce the time spent collecting and organizing unruly data before it can be utilized
	- Enable data scientists and analysts to focus on the analysis of data, rather than the wrangling
	- Drive better decision-making skills by senior leaders in an organization
<!--ID: 1615576989335-->


what is KPI #flashcard 
![[Pasted image 20210312143213.png]]
<!--ID: 1615578065431-->


What are common algorithms for predicting a categorical value #flashcard 
Support Vector Machines, ![[Pasted image 20210312143817.png]]
Naive Bayes,  ![[Pasted image 20210312143913.png]]
Logistic Regression, ![[Pasted image 20210312143947.png]]
Decision Trees, ![[Pasted image 20210312144019.png]]
and Neural Networks ![[Pasted image 20210312144101.png]],

Stochastic Gradient Descent ![[Pasted image 20210312144324.png]]
Definition: Stochastic gradient descent is a simple and very efficient approach to fit linear models. It is particularly useful when the number of samples is very large. It supports different loss functions and penalties for classification.

Advantages: Efficiency and ease of implementation.

Disadvantages: Requires a number of hyper-parameters and it is sensitive to feature scaling.,

K-Nearest Neighbours(uses hierarchical clustering) ![[Pasted image 20210312144425.png]] 
<!--ID: 1615578065457-->

Randomized controlled trial design #flashcard 
![[Pasted image 20210312144925.png]]
<!--ID: 1615578568850-->


Explain Standard Deviation Including Normal distribution #flashcard 
- 1 Standard Deviation from the Mean: 68%
- 2 Standard Deviations from the Mean: 95%
- 3 Standard Deviations from the Mean: 99.7%
# Works when the data has a normal distribution 
![[Pasted image 20210417165120.png]]
<!--ID: 1618692683854-->

Cleaning Data with InterQuartile Range Method #flashcard 
#### ==Not all data is normal or normal enough to treat it as being drawn from a Gaussian distribution.==
- A good statistic for summarizing a non-Gaussian distribution sample of data is the Interquartile Range, or IQR for short.
- The IQR is calculated as the difference between the 75th and the 25th percentiles of the data and defines the box in a box and whisker plot.
![[Pasted image 20210417165420.png]]
<!--ID: 1618692862802-->

Automatic Outlier Detection #flashcard 
- In machine learning, an approach to tackling the problem of outlier detection is [One-Class Classification](<https://en.wikipedia.org/wiki/One-class_classification>) , or OCC for short, involves fitting a model on the “normal” data and predicting whether new data is normal or an outlier/anomaly.
- A one-class classifier aims at capturing characteristics of training instances, in order to be able to distinguish between them and potential outliers to appear.
- A simple approach to identifying outliers is to locate those examples that are far from the other examples in the feature space.
- This can work well for feature spaces with low dimensionality (few features), although it can become less reliable as the number of features is increased, referred to as the curse of dimensionality.
![[Pasted image 20210417170438.png]]
![[Pasted image 20210417170448.png]]
[4 Automatic Outlier Detection Algorithms in Python](https://machinelearningmastery.com/model-based-outlier-detection-and-removal-in-python/)
<!--ID: 1618693746934-->

Type 1 error vs type 2 error #flashcard 
![[Pasted image 20210418173352.png]]
# Type 1 error is mistakenly concluding an affect is real when is not
# type 2 error mistakenly concluding something is not real when it is real. An outlier is real Oh No.
<!--ID: 1618781701541-->


alpha meaning in stats #flashcard 
The probability of usual outcomes that surpass significant data
<!--ID: 1618781740947-->


P Value #flashcard 
- A p-value less than 0.05 (typically ≤ 0.05) is statistically significant. It indicates strong evidence against the null hypothesis, as there is less than a 5% probability the null is correct (and the results are random). Therefore, we reject the null hypothesis, and accept the alternative hypothesis.
However, this does not mean that there is a 95% probability that the research hypothesis is true. The p-value is conditional upon the null hypothesis being true is unrelated to the truth or falsity of the research hypothesis.
- A p-value higher than 0.05 (> 0.05) is not statistically significant and indicates strong evidence for the null hypothesis. This means we retain the null hypothesis and reject the alternative hypothesis. You should note that you cannot accept the null hypothesis, we can only reject the null or fail to reject it.
- A statistically significant result cannot prove that a research hypothesis is correct (as this implies 100% certainty).
- Instead, we may state our results “provide support for” or “give evidence for” our research hypothesis (as there is still a slight probability that the results occurred by chance and the null hypothesis was correct – e.g. less than 5%).
<!--ID: 1618781836822-->


exhaustive Permutation #flashcard 
In an exhaustive permutation test, instead of just randomly shuffling and dividing the data, we actually figure out all the possible ways it could be divided. This is practical only for relatively small sample sizes. With a large number of repeated shuffling, the random permutation test results approximate those of the exhaustive permutation test, and approach them in the limit. Exhaustive permutation tests are also sometimes called exact tests, due to their statistical property of guaranteeing that the null model will not test as “significant” more than the alpha level of the test
<!--ID: 1618781942792-->

Permutation test #flashcard 
- combining two samples or more  together and randomly reallocation the observation samples
<!--ID: 1618781958341-->

resampling-  #flashcard 
drawing additional samples from an observed data set
![[Pasted image 20210421134807.png]]
<!--ID: 1618781980245-->


weighted meann  #flashcard 
- A mean where some values contribute more than others
Some values are intrinsically more variable than others, and highly variable observations are given a lower weight. For example, if we are taking the average from multiple sensors and one of the sensors is less accurate, then we might downweight the data from that sensor.
[Math_is_fun](https://www.mathsisfun.com/data/weighted-mean.html)
<!--ID: 1618782155385-->

Spatial data #flashcard 
location/coordinates 
<!--ID: 1618782207387-->

Standard deviation #flashcard 
- Standard Deviationσ=√21704 =147.32... =147 (to the nearest mm)
 -And the good thing about the Standard Deviation is that it is useful. Now we can show which heights are within one Standard Deviation (147mm) of the ==**Mean**==¬  :
- So, using the Standard Deviation we have a "standard" way of knowing what is normal, and what is extra large or extra small.
- Rottweilers are tall dogs. And Dachshunds are a bit short, right?
 ![[Pasted image 20210418174540.png]]
<!--ID: 1618782344210-->

Mean absolute deviation #flashcard 
![[Pasted image 20210418174616.png]]
![[Pasted image 20210418174741.png]]
<!--ID: 1618782578884-->


Median absolute deviation from the median #flashcard 
![[Pasted image 20210418175005.png]]
<!--ID: 1618782617256-->

Interquartile Rangee #flashcard 
![[Pasted image 20210418175110.png]]
<!--ID: 1618782684428-->

Contingency table #flashcard 
![[Pasted image 20210418175312.png]]
<!--ID: 1618782795187-->

Hexagonal vs Contour Plot #flashcard 
![[Pasted image 20210418175354.png]]
[Article on hexagonal binning](https://www.meccanismocomplesso.org/en/hexagonal-binning-a-new-method-of-visualization-for-data-analysis/)
<!--ID: 1618782934075-->

what does it mean to standardize values #flashcard 
subtract the mean and divide by the standard deviation
<!--ID: 1618783136213-->


Exponential distribution #flashcard 
the frequency distribution of the time or distance from one event to the next event
<!--ID: 1618783137531-->

Weibull distribution #flashcard 
A generalized version of the exponential distribution in which the event rate is allowed to shift over time
![[Pasted image 20210419150856.png]]
<!--ID: 1618783161113-->

Stratified sampling #flashcard 
dividing the data into samples
<!--ID: 1618783211708-->

Stratum #flashcard 
a homogeneous subgroups of a population with common characteristics
<!--ID: 1618783227637-->

Regression to mean #flashcard 
	eventually the higher values will fall back down to earth. The rookie of the year will fall back to the pack
<!--ID: 1618783247383-->

sample statistic #flashcard 
	a metric calculated for a sample of data drawn from larger population
<!--ID: 1618783305584-->


Central limit theorem #flashcard 
	the tendency of the sample distribution to take on a normal shape as sample size rises
		all of the samples will eventually represetnt the bell curve provided the sample is large enough 
<!--ID: 1618783305628-->


Bootstrap sample #flashcard 
a sample taken with replacement from an observed data set 
<!--ID: 1618783305669-->


resampling #flashcard 
		the process of taking repeated samples from observed data. includes both boot-stap and permutation (shuffling)  procedures 
		![[Pasted image 20210421134846.png]] 
<!--ID: 1618783305708-->

Basic Bootstrap theory #flashcard 
![[Pasted image 20210418180300.png]]
<!--ID: 1618783383560-->

PMF, PDF, CDF #flashcard 
[study functions](https://medium.com/analytics-vidhya/pdf-pmf-and-cdf-in-machine-learning-225b41242abe)
<!--ID: 1618783533775-->


