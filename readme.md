# 0. What is this?
This is summary of the basic concepts of college statistics.  The information was taken from [Khan Academy's Statistics Series](https://www.youtube.com/watch?v=uhxtUt_-GyM&list=PL1328115D3D8A2566)

# 1. Descriptive Statistics vs Inferential Statistics
- __Descriptive:__ finding indicative numbers that describe a dataset without having to go through all the data set.
- __Inferential:__ finding conclusions about a population through studying a random sample of that population.


# 2. Measures of central tendency
There are many ways to represent a dataset's central tendency. Some of the most used indicators of central tendency are:

- __Arithmetic Mean:__ The well known mean.
- __Median:__ Sort all numbers in order and find the number that is in the middle. If the dataset is even, the median is the arithmetic mean of the two middle numbers.
- __Mode:__ The number that repeats the most. If there are 2 numbers that repeat equally, any could be chosen as the mode of the dataset.


# 3. Population vs Sample
This is better explained through an example.  Imagine you want to know the average height of women in the US.

- __Population:__ The 150 million women that live in the US. (You typically can't survey the whole population.)
    - Population size is noted with the letter `N` (e.g `N = 150 million women`) 
- __Sample:__ A __random__ subset of the women in the population (e.g 2000 randomly chosen women.)
    - Sample size is noted with the letter `n` (e.g `n = 2000 randomly chosen women`)


# 4. Population mean vs Sample mean
Population mean and sample mean are calculated in the same way. However there are some differences in the notation.

<img src="/equations/4_population_mean_vs_sample_mean/population_vs_sample_mean.png"/>


# 5. Measures of dispersion
How spread out is the data relative to its mean. There are 2 classic measures of dispersion: __variance__ and __standard deviation__.

- __Variance:__ is measured the units of `x^2` (e.g `cm^2` if x is the height of women in cm).
- __Standard deviation:__ measured in the same units as `x` (e.g `cm`).


# 6. Population Dispersion vs Sample Dispersion
## 6.1 Population Dispersion

<img src="/equations/6_population_dispersion_vs_sample_dispersion/population_variance_and_sd.png"/>

## 6.2 Sample Dispersion

<img src="/equations/6_population_dispersion_vs_sample_dispersion/sample_variance_and_sd_v2.png"/>

- __Biased estimator:__  The expeceted value of the estimator is __not__ equal to the expected value of of the parameter being estimated.
- __Unbiased estimator:__ The expected values of the estimator and the parameter being estimated are the same. (If you actually knew the population's mean, you wouldn't neet to use the unbiased estimator.)
- __Unbiased estimator of a population's standard deviation:__ Unlike the mean and the variance, there is no general formula for an __unbiased estimator__ of standard deviation that works across all distribuitions. In practice, finding an unbiased estimator is of [little relevance since its need is avoided by standard procedures, such as the use of significance tests and confidence intervals, or by using Bayesian analysis.](https://en.wikipedia.org/wiki/Unbiased_estimation_of_standard_deviation)


# 7. Probability density functions
- Continuous version of discrete probability distributions.
- The probability of something happening is the area under the curve of the probability density function f(x).
    - Ranges are used for probability density functions. (e.g `P(|X-2| < 0.1) = P(1.9<X<2.1) = integral of f(x) between 1.9 and 2.1`).
    - This means that `P(X = Anything) = 0` as the area of a line is 0. 
    - The whole area under the curve must be equal to 1.

<img src="/equations/7_probability_density_functions/probability_density_function.gif"/>


# 8. Binomial Distribution
The binomial distribution is the basis of the significance test in statistical hypothesis testing. That is why it is so important.

- It is the discrete version of the normal distribution. As the number of trials increase (`n`), the binomial distributions starts to approximate the normal distribution.

## 8.1 Building the Binomial Distribuition.

__The binomial distribution is the distribution resulting from these conditions:__

- Outcome of the experiment is boolean (yes/success or no/failure)
- `n` independent experiments are done
    - When `n=1` the binomial distribuition is known as the Bernoulli distribution.
- `p` is the probability of yes/success on each experiment independently
- `q = 1-p` is the probability of no/failure
- `k` number of yes/success (`k` any integer between `0 and n`)
- `X` = number of successes when doing `n` experiments

The probability of having `k` successes on `n` independent experiments, each with `p` probability of success is (i.e `P(X=k)`):

<img src="/equations/8_binomial_distribution/binomial_probability.png"/>

If you calculate `P` for every single `k` (from `0 to n`) and graph it, you will get a binomial distribution. For example, for `n=6` and `p=0.5`:

<img src="/equations/8_binomial_distribution/binomial_distribution_graph.png" height="200px" />


## 8.2 Bionomial distribution through an example
Example
X = #number of baskets I make when throwing a basketball n times.
p = there is a 30% chance that I make a basket any shot I make
q = there is 70% chance (1-p) that I don't make a basket on any shot I make
n = I am going to do 6 shots (experiments)


__Sample mean__

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{bmatrix}&space;2&3&space;&&space;4&space;\\&space;5&6&7&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{bmatrix}&space;2&3&space;&&space;4&space;\\&space;5&6&7&space;\end{bmatrix}" title="\begin{bmatrix} 2&3 & 4 \\ 5&6&7 \end{bmatrix}" /></a>

<img src="/images/ch3_likelihood_of_change_vs_dependents.png" width="600"/>
[Wrong Code Example](code_examples/chapter_2.rb#L61-L71) / [Right Code Example](code_examples/chapter_2.rb#L73-L102)
