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
