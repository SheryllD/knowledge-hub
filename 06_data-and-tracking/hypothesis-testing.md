# Hypothesis Testing 

### Central Limit Theorem 
The Central Limit Theorem (CLT) states that, irrespective of the shape of the underlying population, the sampling distribution of the mean will approximate a normal distribution as the sample size grows larger (n > 30), assuming if all samples are identical in size and randomly sampled. 
- Large Sample Size & Individual Data Points: Even with a large sample, the distribution of individual data points could still ne non-normal. For example, a dataset with millions of data points could exhibit significant skweness or extreme kurtosis. 
- Large Sample Size & Averages of samplles: if you are taking multiple samples from a population and calculating their averages, the distribution of those averages tends to be normal due to the CLT - even if the underlying population is not normal.
- Practical Implications: While the CLT is powerful, it's also important to remember that many statistical tests and methods assume that the individual data points (not their means) follow a normal distribution. Therefore, having a large dataset doesn't alllow you to bypass these assumptions

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


Step by step: 
So after formulating the NUll and Alternative Hypothesis: 
1. Choose significance level
2. Collect the data 
3. Calculate Test Statistic 
4. Determine the P-value 
5. Decision Making 

Note: The significance level, denoted by 𝛼, is the probability of incorrectly rejecting the null hypothesis when it is actually true. In other words,  how likely is our test findings to yield a wrong conclusion (so how likely is our test to produce a false positive result)? 
    - Common choices for 𝛼 are 1%, 5% or 10%. This will heavily depends on the nature of the problem studied/context of the study. 

The formula for the t-statistic is $t = \frac{\bar{x} - \mu_0}{s / \sqrt{n}}$.
- \bar{x} = sample mean
- \mu_0 = hypothesised population mean
- s = sample standard deviation
- n = sample size
- \sqrt{n} = square root of 𝑛


