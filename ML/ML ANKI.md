TARGET DECK: machine learning 

  when should you use PCA #flashcard
1. Do you want to reduce the number of variables, but aren’t able to identify variables to completely remove from consideration?
2. Do you want to ensure your variables are independent of one another?
3. Are you comfortable making your independent variables less interpretable?
- only use if you answer yes to all of them
<!--ID: 1615570734529-->

What is dimension reduction? #flashcard 
	removing variables/columns from the Dataframe. Two techniques are feature elimination and feature extraction. features extaction grabs independent variables
<!--ID: 1615570907473-->

what are the 4 types of data analytics #flashcard 
![[4-types-of-data-analytics-principa 1.png]]
<!--ID: 1615570987172-->

what is factor analysis? #flashcard 
It's different types of analysis. ![[1rvJypl8A2okj41pLRfXWfQ.jpg]]
<!--ID: 1615571099443-->

time-series-analyst #flashcard 
![[ts-pp-yellowstone-1.jpg]]
https://towardsdatascience.com/the-complete-guide-to-time-series-analysis-and-forecasting-70d476bfe775 
forecasting the future. continuous and no endpoint unless the world comes to an end. 
<!--ID: 1615571168290-->

what is gg plot and what language uses it ? #flashcard 
ggplot2 is a data visualization package for the statistical programming language R. Created by Hadley Wickham in 2005, 
<!--ID: 1615571216637-->

GDPR Law of Data #flashcard 
hen the processing is based on consent the data subject has the right to revoke it at any time.![[GDPR-processor-half.png]]
<!--ID: 1615571292312-->

Descriptive vs prescriptive modeling #flashcard 
![[cover.png]]
![[4-types-of-data-analytics-principa 1.png]]
<!--ID: 1615571379016-->

How Does PCA work? #flashcard 
is case, the “red direction” is the more important one. We’ll get into why this is the case later, but given how the dots are arranged, can you see why the “red direction” looks more important than the “green direction?” (Hint: What would fitting a line of best fit to this data look like?)
![[1P8_C9uk3ewpRDtevf9wVxg.png]]
![[1wsezmnzg-0N_RP3meYNXlQ.png]]
https://towardsdatascience.com/a-one-stop-shop-for-principal-component-analysis-5582fb7e0a9c
<!--ID: 1615571447591-->

central limit theorem #flashcard 
![[1DfBsmbGDS72leAVaV37uKg.png]]
<!--ID: 1615571520862-->


Quick overview on data engineer #flashcard 
![[GTQN2JFwrvv-dMxKRdJggkkSNYk4HouxoLGwQFZLSSHnl1uOhC7nFKZPKR-FieYHDKgziVDO8bELCLEIaaEjZaDzNAIRRCAh6Gna4MVsUpELF6h-sKa.png]]
<!--ID: 1615571575735-->

What is the mode? #flashcard 
![[0wHMvuwRa_YF9SFwY.png]]
<!--ID: 1615571953348-->



what is descriptive statistics? #flashcard 
![[areas_of_interest_for_descriptive_statistics.jpg]]
<!--ID: 1615571953388-->



when to use column charts, or line charts, or bar charts, or area charts, or pie charts #flashcard 
![[paste-7a8c93eb0d64a66126015244906e54a2a056f6f5.jpg]]
<!--ID: 1615571953414-->



What is prescriptive analytics? #flashcard 
- prescriptive analytics aims to find the best solution given a variety of choices. Additionally, the field also empowers companies to make decisions based on optimizing the result of future events or risks, and provides a model to study them.
- Prescriptive analytics gathers data from a variety of both descriptive and predictive sources for its models and applies them to the process of decision-making. This includes combining existing conditions and considering the consequences of each decision to determine how the future would be impacted.
- In healthcare business intelligence, prescriptive analytics is applied across the industry, both in patient care and healthcare administration. For practitioners and care providers, prescriptive analytics helps improve clinical care and provide more satisfactory service to patients.
- 
<!--ID: 1615571953433-->


quasi experiments are? #flashcard 
Like a true experiment, a quasi-experimental design aims to establish a cause-and-effect relationship between an independent and dependent variable.
However, unlike a true experiment, a quasi-experiment does not rely on random assignment. Instead, subjects are assigned to groups based on non-random criteria.
Quasi-experimental design is a useful tool in situations where true experiments cannot be used for ethical or practical reasons.
![[Evaluation-Final_Fotor-678x381 1.jpg]]
<!--ID: 1615571953450-->


PCA Principal component analysis #flashcard 
is a feature extraction technique. so it combines our input variables in a specific way, then we can drop the “least important” variables while still retaining the most valuable parts of all of the variables! As an added benefit, each of the “new” variables after PCA are all independent of one another. 
<!--ID: 1615571953465-->

explain what feature scaling is #flashcard 
- It refers to putting the values in the same range or same scale so that no variable is dominated by the other
- machine learning algorithms use euclidean distance between two data points
	- for example 5kg and 500 mg high distance will weight a lot more than small/ low magnitude
<!--ID: 1615574919682-->




what algorithms benefit more feature scaling and what algorithms does it not affect #flashcard 
# scaling matters for 
- K-nearest neighbors - euclidean distance measures is sensitive to magnitude and hence should be scaled for all features to weight equally 
- Principal component analysis (PCA)- PCA tries to get the features with maximum variance and the variance is high for high magnitude features. This skews the PCA towards high magnitude features.
# scaling does not matter for 
-   **Tree based models** are not distance based models and can handle varying ranges of features. Hence, Scaling is not required while modelling trees.
-   Algorithms like **Linear Discriminant Analysis(LDA), Naive Bayes** are by design equipped to handle this and gives weights to the features accordingly. Performing a features scaling in these algorithms may not have much effect.
<!--ID: 1615574919748-->

The flow for creating a ML Model #flashcard 
1. Problem definition — What business problem are we trying to solve? How can it be phrased as a machine learning problem?
2. Data — If machine learning is getting insights out of data, what data we have? How does it match the problem definition? Is our data structured or unstructured? Static or streaming?
3. Evaluation — What defines success? Is a 95% accurate machine learning model good enough?
4. Features — What parts of our data are we going to use for our model? How can what we already know influence this?
5. Modeling — Which model should you choose? How can you improve it? How do you compare it with other models?
6. Experimentation — What else could we try? Does our deployed model do as we expected? How do the other steps change based on what we’ve found?
<!--ID: 1615575015418-->




 methods to normalization (feature scaling) #flashcard 
 - Normal distribution aka bell curve
1. min-max scaling
	- It can be easily seen that when x=min, then y=0, and When x=max, then y=1.
2. mean normalization- 
	- ==You need to normalize our data if you’re going use a machine learning or statistics technique that assumes that data is normally distributed e.g. t-tests, ANOVAs, linear regression, linear discriminant analysis (LDA) and Gaussian Naive Bayes.==
3. standardization _also called_ **_z-score normalization_**_)_
	- ![[Pasted image 20210221085253.png]]
	- ==**a mean of 0 and a standard deviation of 1.**=
<!--ID: 1615574919830-->




scaling to unit of length for feature scaling #flashcard 
This usually means dividing each component by the [Euclidean length](https://en.wikipedia.org/wiki/Euclidean_length) of the vector:
<!--ID: 1615574919924-->

Types of Machine learning Problems #flashcard 
1. supervised learning - predicting a label
2.  unsurpervised learning - no labels then adding labels after organizing
3 . transfer learning - building a ml algorithm in top of another ml algorithm
<!--ID: 1615575397222-->


Types of Data for ML #flashcard 
-   **Structured data** — Think a table of rows and columns, an Excel spreadsheet of customer transactions, a database of patient records. Columns can be numerical, such as average heart rate, categorical, such as sex, or ordinal, such as chest pain intensity.
-   **Unstructured data** — Anything not immediately able to be put into row and column format, images, audio files, natural language text.
-   **Static data** — Existing historical data which is unlikely to change. Your companies customer purchase history is a good example.
-   **Streaming data** — Data which is constantly updated, older records may be changed, newer records are constantly being added.
<!--ID: 1615575397315-->




Evaluation #flashcard
-   **False negatives** — Model predicts negative, actually positive. In some cases, like email spam prediction, false negatives aren’t too much to worry about. But if a self-driving cars computer vision system predicts no pedestrian when there was one, this is not good. <iframe src="https://giphy.com/embed/aqCcKVAnFt85MSqh1j" width="480" height="379" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/cbsnews-election-2020-cbs-news-second-presidential-debate-aqCcKVAnFt85MSqh1j"></a></p>
-   **False positives** — Model predicts positive, actually negative. Predicting someone has heart disease when they don’t, might seem okay. Better to be safe right? Not if it negatively affects the person’s lifestyle or sets them on a treatment plan they don’t need.<iframe src="https://giphy.com/embed/ZNKllWJ4aUBTknvD0h" width="480" height="320" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/boomerangtoons-courage-the-cowardly-dog-ZNKllWJ4aUBTknvD0h"></a></p>
-   **True negatives** — Model predicts negative, actually negative. This is good.
-   **True positives** — Model predicts positive, actually positive. This is good.
-   [**Precision**](https://en.wikipedia.org/wiki/Precision_and_recall) — What proportion of positive predictions were actually correct? A model that produces no false positives has a precision of 1.0. <iframe src="https://giphy.com/embed/kfFhknV3Ztpq8" width="480" height="282" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/cartoon-kfFhknV3Ztpq8"></a></p>
-   [**Recall**](https://en.wikipedia.org/wiki/Precision_and_recall) — What proportion of actual positives were predicted correctly? A model that produces no false negatives has a recall of 1.0. <iframe src="https://giphy.com/embed/l0Iy0sxvaOjQltnoI" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/l0Iy0sxvaOjQltnoI">via GIPHY</a></p>
-   [**F1 score**](https://en.wikipedia.org/wiki/F1_score) — A combination of precision and recall. The closer to 1.0, the better.
-   [**Receiver operating characteristic (ROC) curve & Area under the curve (AUC)**](https://towardsdatascience.com/understanding-auc-roc-curve-68b2303cc9c5) — The ROC curve is a plot comparing true positive and false positive rate. The AUC metric is the area under the ROC curve. A model whose predictions are 100% wrong has an AUC of 0.0, one whose predictions are 100% right has an AUC of 1.0.
<!--ID: 1615575397404-->


Name the 3 different data sets and explain there purpose #flashcard 
-   **Training data set** — Use this set for model training, 70–80% of your data is the standard.
-   **Validation/development data set** — Use this set for model tuning, 10–15% of your data is the standard.
-   **Test data set** — Use this set for model testing and comparison, 10–15% of your data is the standard
 
<!--ID: 1615575397496-->


hypothesis testing #flashcard 
- If you are going to propose a hypothesis, it’s customary to write a statement. Your statement will look like this: “If I…(do this to an independent variable)….then (this will happen to the dependent variable).”
+ For example: A good hypothesis statement should:
* Include an “if” and “then” statement (according to the University of California).
+ Include both the independent and dependent variables.
+ Be testable by experiment, survey or other scientifically sound technique.
+ Be based on information in prior research (either yours or someone else’s).
+ Have design criteria (for engineering or programming projects).




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
<!--ID: 1615576351162-->


# what is winsorizing #flashcard 
The distribution of many statistics can be heavily influenced by outliers. A typical strategy is to set all outliers to a specified percentile of the data; for example, a 90% winsorization would see all data below the 5th percentile set to the 5th percentile, and data above the 95th percentile set to the 95th percentile. Winsorized estimators are usually more robust to outliers than their more standard forms, although there are alternatives, such as trimming, that will achieve a similar effect.
____
==from scipy.stats.mstats import winsorize==
winsorize([92, 19, 101, 58, 1053, 91, 26, 78, 10, 13, -40, 101, 86, 85, 15, 89, 89, 28, -5, 41], limits=[0.05, 0.05])
<!--ID: 1618356872110-->

feature extraction #flashcard 
Feature Extraction aims to reduce the number of features in a dataset by creating new features from the existing ones (and then discarding the original features). These new reduced set of features should then be able to summarize most of the information contained in the original set of features. In this way, a summarised version of the original features can be created from a combination of the original set. (PCA, )
<!--ID: 1626286123510-->

Feature selection #flashcard 
feature selection aims instead to rank the importance of the existing features in the dataset and discard less important ones (no new features are created). 
![[Pasted image 20210714141144.png]]
<!--ID: 1626286425527-->
