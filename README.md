## Chapter 1
#### Plus Four confidence interval

is a method for computing confidence intervals for a process from a sample proportion. We add 4 more observation to the total number of observation among which 2 are successes and 2 are failures. The plus four method has a high coverage-rate compared to other methods.

$\tilde{p}\pm z^{*} \sqrt{\tilde{p}(1-\tilde{p}/n+4)}$

#### Parameter and Statistic:

A parameter is a metric that describes the whole population, we denote the population mean and proportion by $\mu$ and $\pi$. A statistic is the same metric but calculated for sample, we denote the sample mean and proportion by $\bar{x}$ and $\hat{p}$.

#### Biased and Unbiased samples

The statistic values of a biased sample are systematically different from the parameter values of the population. An unbiased sample's statistic values are much more closer to the parameter values.


#### Simple random sample

Is a technique that gives every observational entities in the population an equal chance of being sampled. 

#### Sampling from a finite population

When sampling from a finite population without replacement, trials are no longer considered independent. The probability of successive events is not constant throughout events anymore. 

The central limit theorem also applies when sampling from large finite population with a large sampling size. It states that the distribution of sample proportions will be modeled by a normal distribution with mean=$\pi$. The sample is considered large enough if there are at least 10 successes and 10 failures, the population is considered large enough if it's more than 20 times the sample size.

Note the two desirable properties of sample means when we using random samples from a
large population:
    • The distribution of sample means centers at the population mean (so the sampling method is
unbiased).
    • The distribution of sample means has less sample to sample variability when we increase the sample
size (producing increased precision).

Notice that sample proportion variability is dependent on the sample size. Large samples have less variability than small ones.

#### Non-sampling errors:

Are errors associated with sources of bias after the sample has been selected. It's anything that suggests  to the participants that a certain answer is preferred over the others.

#### Hypergeometric Random Variable

Are random variable used when:
    1. trials are no longer independent
    2. there are two distinct types of objects in the population.
    
An hypergeometric random variable is similar to a binomial rand var in that both variables require that there are 2 types of distinct object in the population. An hypergeometric var is used when the population is finite and trials are no longer considered independent of each other.

## Chapter 2:

#### Numerical and graphical summaries

When visualizing quantitative data, the total number of observations matter. Large data sets are best visualized using an histogram where has dotplot are preferred for small data sets. 

Once the data is in graphically presented we look at 3 specific features:
    + its shape: is the distribution symmetrical or is skewed, what pattern does it follow? how many clusters of data are there? how spaced are they? are there any outliers? i.e of the all the distribution model which one does this one most resembles to?
    + its center: Where is the center of the distribution? where are most of the values clustered? what's a typical value? ie where is the mean and mode.
    + its variability: how spread out are the values? this should give us an indication of the sd.
    
#### Assessing model fit

When assessing a model for our distribution we are looking to choose among the model fit which one fits our distribution the most. This allows us to come up with a mathematical expression that approximates our distribution the most. Another method is to calculate a probability plot for the data we have. The probability plot is a graphical technique for assessing whether or not a data set follows a given distribution such as the normal or Weibull. The data are plotted against a theoretical distribution in such a way that the points should form approximately a straight line.


#### Modeling non normal data

non normal data is generally skewed either to the right or left. We describe non normal data using a 5 number summary that includes the minimum, 1/4 quartile, the median, the 3/4 quartile and the maximum of the data set. The interquartile range is equal to the 3/4 quartile minus the 1/4 quartile, it expresses the range of values that represent the 50% middle observations. We use a boxplot to graphically represent the 5 number summary of a non normal data set. 

We define an outlier using the 1.5IQR criterion. Values larger than median + 1.5IQR or smaller than median - 1.5IQR are then considered outliers.

We often apply data transformation to non normal data to make it have more of a normal distribution's shape. A data transformation is involves applying a mathematical function on every elements of a data set.


#### Non normal population

When samples are selected from a large population, regardless of its properties, with mean $\mu$ and sd $\sigma$ then the distribution of the sample means will have the following properties:
    + the mean will be approximately equal to $\mu$
    + and the sd will be $\sigma /\sqrt(n)$
An extension to the central limit theorem states that the distribution of sample means will be normal for a large  sample size regardless of the distribution of the population.


#### Approximation of standard deviation

Most of the time the standard deviation of a population is not known, we have to approximate using the standard deviation of the sample by calculating the standard error of $\bar{x}$. The standard error is given by the following formula $s/\sqrt{n}$ where s is the sd of the sample. 

#### t-distribution

a t-distribution is a statistical model fit that has heavier tails than a normal distribution would. The higher the degree of freedom the closer the shape of the t-distribution to a normal one. the degree of freedom is defined as $n-1$. 

#### One sample t-test

In testing a sample mean against a population mean when the sd of the population is unknown, we use the standard error of the sample and compare the standardized statistic $t_{0}=\bar{x}-\mu/(s/\sqrt{n})$. This formula requires the sample size to be large.
It also allows us to find the hypothetical p-value for a given mean value. 

#### One sample t-interval

When he sample size is large enough a confidence interval for $\mu$ is given by $\bar{x}\pm t_{n-1}(s/\sqrt{n})$ where $t_{n-1}$ is the t-value for the t-distribution of degree n-1.

## Chapter 3-4 
#### Binary variable

 The simplest statistic for comparing a binary variable between two groups is the difference in the proportion of “successes” for each group.
To compare the two groups we also need a conditional proportions.
A conditional proportion is when you calculat separately proportions for each group rather than computing the overall proportion.

eg:
  Comparing success rate on penalties for soccer player to determine most likely to score in a competition.
  
#### Two sample z-test

is used to compare the means of two samples to see if it is feasible that they come from the same population. This test requires that we both population have normal distribution and that the variance be known for both population. It is preferred to the t-test when the variance is known. In R  we use iscamtwopropztest which takes the following inputs: 

  observed1 (either the number of successes or sample proportion for first group), n1 (sample size for first group, observed2 (count or proportion), and n2

  Optional: hypothesized difference and alternative (“less”, “greater”, or “two.sided”) Optional: confidence level
  
  example:
  Given 2 samples of shot scored on free kicks. We can use this test to determine if both samples come from the same player. 
  
#### types of study
##### observational study
Observational study is one in which the researchers passively observe and record information about the observational units.
eg:
What side of the bed do partners usually like when sleeping?
This involve observing and recording which side does each partner in a couple likes to sleep on.
##### experimental study
In an experimental study, the researchers actively impose the explanatory variable on the observational units.
eg:
How does different caffeine levels affects focus level in students?
This involves giving the students various level of caffeine and assess their level of focus as a result of ingesting the caffeine.

#### Two population means
How do you compare two population means?
As with comparing two population proportions, when we compare two population means from independent populations, the interest is in the difference of the two means. In other words, if is the population mean from population 1 and is the population mean from population 2, then the difference is μ 1 − μ 2. We usually hypothised on that value is the difference is 0 then there is no difference else there is a difference between the two means.

eg: We would use this procedure to compare the means of two group as a result of altering a parameter for the group.

## Chapter 5

#### Chi-square statistic

Chi-square statistic is used to compare the observed and expected counts, allowing for more than two categories for the response variable. A Chi Square distribution is skewed to the right and provides a reasonables model for large sample sizes.

When comparing several population proportions, the chi-square degrees of freedom are equal to the number of explanatory variable categories minus 1 , c-1.

In R: The iscamchisqprob function takes the following inputs 
• xval = the observed value of the test statistic 
• df = degrees of freedom for the chi-square distribution

#### Scatter plot

A scatter plot shows the direction of a relationship between the variables. A clear direction happens when there is either: High values of one variable occurring with high values of the other variable or low values of one variable occurring with low values of the other variable.

![Scatter plot example](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/data-analysis-in-tableau-desktop/compare-measures-using-a-scatter-plot/images/15f83f48a4bd1701727b368bce219fca_1-eaa-6-efe-e-360-4554-957-d-d-76-c-227-a-111-f.png)

#### Correlation

Correlation is a statistical measure that expresses the extent to which two variables are linearly related (meaning they change together at a constant rate). It's a common tool for describing simple relationships without making a statement about cause and effect.
You find The correlation by:
Finding the mean of all the x-values
then finding the standard deviation of all the x-values(sx) and the standard deviation of all the y-values(sy)

![Types of correlation](https://sphweb.bumc.bu.edu/otlt/MPH-Modules/PH717-QuantCore/PH717-Module9-Correlation-Regression/Correlation%20Coefficient%20examples.png)

#### Best fit line

Line of best fit refers to a line through a scatter plot of data points that best expresses the relationship between those points.
The line of best fit is described by the equation ŷ = bX + a, where b is the slope of the line and a is the intercept (i.e., the value of Y when X = 0). This calculator will determine the values of b and a for a set of data comprising two variables, and estimate the value of Y for any specified value of X.
Divide the sum by sx*sy

#### Residual

A residual is a measure of how well a line fits an individual data point. This vertical distance is known as a residual.

The residual for each observation is the difference between predicted values of y (dependent variable) and observed values of y . Residual=actual y value−predicted y value,ri=yi−^yi.
