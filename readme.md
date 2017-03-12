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

__Sample mean__

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{bmatrix}&space;2&3&space;&&space;4&space;\\&space;5&6&7&space;\end{bmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{bmatrix}&space;2&3&space;&&space;4&space;\\&space;5&6&7&space;\end{bmatrix}" title="\begin{bmatrix} 2&3 & 4 \\ 5&6&7 \end{bmatrix}" /></a>

<img src="/images/ch3_likelihood_of_change_vs_dependents.png" width="600"/>
[Wrong Code Example](code_examples/chapter_2.rb#L61-L71) / [Right Code Example](code_examples/chapter_2.rb#L73-L102)
