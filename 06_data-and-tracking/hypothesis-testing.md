# Hypothesis Testing 

### Central Limit Theorem 
The Central Limit Theorem (CLT) states that, irrespective of the shape of the underlying population, the sampling distribution of the mean will approximate a normal distribution as the sample size grows larger (n > 30), assuming if all samples are identical in size and randomly sampled. 
- **Large Sample Size & Individual Data Points:** Even with a large sample, the distribution of individual data points could still ne non-normal. For example, a dataset with millions of data points could exhibit significant skweness or extreme kurtosis. 
- **Large Sample Size & Averages of samplles:** if you are taking multiple samples from a population and calculating their averages, the distribution of those averages tends to be normal due to the CLT - even if the underlying population is not normal.
- **Practical Implications:** While the CLT is powerful, it's also important to remember that many statistical tests and methods assume that the individual data points (not their means) follow a normal distribution. Therefore, having a large dataset doesn't alllow you to bypass these assumptions

### Hypothesis Testing 
- The first step in hypothesis testing is formulating a hypothesis, which is a premise or claim that we want to test about a population parameter. The objective of a hypothesis is to decide, based on a sample from the population, which of the complementary hypothesis is true: 

1. Null Hypothesis H₀ - This would be the currently "accepted" value for a parameter. 
2. Alternative Hypothesis H₁ - The alternative hypothesis is a statement asserting an alternative condition or outcome compared to the null hypothesis. 

In a hyptothesis problem, after observing the sample experimenter must decide either to accept the H₀ as true or to reject it, and decide H₁ to be true. 

Example: 
- If 𝜇 denotes a population parameter, let’s say the change in a patient’s blood pressure after taking a drug, we write:

        H₀ =  0   versus     H₁ ≠     0

- The null hypothesis states, on average the drug has no effect on blood pressure, and the alternative hypothesis states that there is some effect. 

- Statistical hypothesis testing operates on the principle that while establishing universal truth is challenging, it is possible to demonstrate falsity through the presentation of counter examples. 
    - The null hypothesis should assert the absence of an effect and explicitly state equalities ( =, > or < ). 


So after formulating the NUll and Alternative Hypothesis: 

**Step by step:**
1. Choose significance level
2. Collect the data 
3. Calculate Test Statistic 
4. Determine the P-value 
5. Decision Making 

Note: The significance level, denoted by 𝛼, is the probability of incorrectly rejecting the null hypothesis when it is actually true. In other words,  how likely is our test findings to yield a wrong conclusion (so how likely is our test to produce a false positive result)? 
    - Common choices for 𝛼 are 1%, 5% or 10%. This will heavily depends on the nature of the problem studied/context of the study. 

**Step 3. Calculate Test Statistic**
The formula for the t-statistic is $t = \frac{\bar{x} - \mu_0}{s / \sqrt{n}}$.
- \bar{x} = sample mean
- \mu_0 = hypothesised population mean
- s = sample standard deviation
- n = sample size
- \sqrt{n} = square root of 𝑛

The test statistic quantifies how many standard deviations the sample mean is from the hypothesized population mean, aiding in the determination of whether to reject the null hypothesis based on the observed sample data.

Options: 

1. When 𝜎 is known, the appropriate test statistic is the z-score. This statistic conforms to a normal distribution.

$$
z = \frac{\bar{x} - \mu_0}{\sigma / \sqrt{n}}
$$

Where:
- $\bar{x}$ is the sample mean  
- $\mu_0$ is the hypothesised population mean  
- $\sigma$ is the known population standard deviation  
- $n$ is the sample size  

2. When $\sigma$ is unknown or the number of samples is less than 30, the appropriate test statistic is the $t$-statistic. This statistic conforms to a $t$-distribution. The formula is:

$$
t = \frac{\bar{x} - \mu_0}{s / \sqrt{n}}
$$

Where:
- $\bar{x}$ is the sample mean  
- $\mu_0$ is the hypothesised population mean  
- $s$ is the sample standard deviation  
- $n$ is the sample size

**Step 4: Determine P-value**
- Having obtained a test statistic and considered the distribution of our samples (whether normal or T), now we can evaluate the probability of getting a sample mean as extreme as the one we have observed. This probability is known as the p-value. 

- If the p-value is low, this means that the likehoof of obtaining the observed results, or more extreme results, under H0 is unlikely. This also often leads to rejecting the null hypothesis in favor of an alternative hypothesis. 

**Step 5: Decision-making** 
- We need to decide in this step whether to reject H₀ or H₁. 
    - in two-tailed tests (when test for equalities):
        - If p_value < 𝛼 we reject the null hypothesis.
        - If p_value > 𝛼 we fail to reject the null hypothesis.

    - in one-tialed tests (when we test for inequalities): 
        - If p_value < 𝛼  and the test statistic is in the same direction as       we reject the null hypothesis.
        - If p_value > 𝛼 or the test statistic is in opposite direction as       we fail to reject the null hypothesis.

**Different Types of Tests**

one Sample T-test:
- in python: ttest_1samp(sample, k, alternative = “two-sided”)
- in python: ttest_1samp(sample, k, alternative = “greater”)
- in python: ttest_1samp(sample, k, alternative = “less”)

Two Sample T-test(compares the means of two independent samples)
- in python: ttest_ind(sample1, sample2, alternative = “two-sided”)
- in python: ttest_ind(sample1, sample2, alternative = “greater”)
- in python: ttest_ind(sample1, sample2, alternative = “less”)

Paired Sample T-test (compares the means of two dependent samples)
- in python: ttest_rel(sample1, sample2, alternative = “two-sided”)
- in python: ttest_rel(sample1, sample2, alternative = “greater”)
- in python: ttest_rel(sample1, sample2, alternative = “less”)

Paired Sample T-test (compares the means of two dependent samples)
- in python: ttest_rel(sample1, sample2, alternative = “two-sided”)
- in python: ttest_rel(sample1, sample2, alternative = “greater”)
- in python: ttest_rel(sample1, sample2, alternative = “less”)

ANOVA (compares the means of multiple independent samples)
in python: f_oneway(sample_1, sample_2, sample_3, …, sample_n)