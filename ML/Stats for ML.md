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
