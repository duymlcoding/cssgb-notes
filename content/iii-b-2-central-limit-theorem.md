---
title: "Central Limit Theorem"
description: "Detailed study notes for the ASQ CSSGB exam covering the Central Limit Theorem, its foundation in standard deviation, the three core statements, the standard error of the mean, and its application to confidence intervals, hypothesis testing, and control charts."
---

## Introduction to the Central Limit Theorem

The central limit theorem (CLT) forms the backbone of many statistical procedures used throughout the Measure phase of a Six Sigma project. It explains why averages behave predictably even when individual observations do not, and it enables practitioners to construct confidence intervals, conduct hypothesis tests, and monitor processes with control charts. To apply the CLT correctly, you must first understand standard deviation, because the theorem describes how the spread of sample means depends on the variation in the original population.

## Standard Deviation: Measuring Variation

Standard deviation quantifies how far individual data values lie from the mean. A large standard deviation indicates wide dispersion; a small standard deviation signals tightly clustered data. Reducing variation is a primary goal in Six Sigma, and standard deviation is the fundamental metric for capturing that variation.

### Population Standard Deviation

When you possess measurements for every item in a population, use the population standard deviation. The formula is:

$$
\sigma = \sqrt{\frac{1}{N}\sum_{i=1}^{N}(x_i - \mu)^2}
$$

Where:
- $\sigma$ (sigma) is the population standard deviation
- $\mu$ is the population mean
- $N$ is the total number of data elements in the population
- $x_i$ represents each individual data element
- $\sum$ directs you to sum the squared deviations for all data points

**Example: Test Scores for an Entire Class**

A teacher records scores for all 15 students on a test. The scores are:

67, 68, 73, 74, 81, 85, 88, 88, 90, 90, 90, 93, 94, 98, 99

Step 1: Compute the mean $\mu $.
$$
\mu = \frac{67 + 68 + 73 + 74 + 81 + 85 + 88 + 88 + 90 + 90 + 90 + 93 + 94 + 98 + 99}{15} = \frac{1278}{15} = 85.2
$$

Step 2: Subtract the mean from each score and square the result. For the first score, \$67 - 85.2 = -18.2$, and $(-18.2)^2 = 331.24$. The full set of squared deviations is:

331.24, 295.84, 148.84, 125.44, 17.64, 0.04, 7.84, 7.84, 23.04, 23.04, 23.04, 60.84, 77.44, 163.84, 190.44

Step 3: Sum the squared deviations and divide by $N = 15$ to obtain the variance.
$$
\frac{331.24 + 295.84 + 148.84 + 125.44 + 17.64 + 0.04 + 7.84 + 7.84 + 23.04 + 23.04 + 23.04 + 60.84 + 77.44 + 163.84 + 190.44}{15} = \frac{1496.4}{15} = 99.76
$$

Step 4: Take the square root to get $\sigma $.
$$
\sigma = \sqrt{99.76} \approx 9.987
$$

The population standard deviation is 9.987 points. This tells the teacher that most scores fall within about ±10 points of the mean. If the result had been much smaller, say 2 points, the teacher would see very consistent performance; a much larger result would signal highly disparate student preparation or test difficulty, pointing to a process-level issue rather than individual differences.

### Sample Standard Deviation

When you work with a sample drawn from a larger population, use the sample standard deviation. The formula compensates for the fact that a sample tends to underestimate population variability:

$$
s = \sqrt{\frac{1}{N-1}\sum_{i=1}^{N}(x_i - \bar{x})^2}
$$

Where:
- $s$ is the sample standard deviation
- $\bar{x}$ is the sample mean
- $N$ is the sample size
- The denominator $N-1$ replaces $ N$ to correct for bias.

**Example: Same Test Scores Treated as a Sample**

Assume the 15 scores are a random sample from all the teacher's classes. The sample mean $\bar{x} = 85.2$ remains the same. The squared deviations are identical. Now divide the total 1496.4 by $ N-1 = 14$:

$$
\text{Variance} = \frac{1496.4}{14} \approx 106.885
$$

$$
s = \sqrt{106.885} \approx 10.338
$$

The sample standard deviation is 10.338, slightly larger than the population value, reflecting the additional uncertainty of working with a sample. If the sample standard deviation had been much larger relative to a comparable population, it would indicate the sample is less representative, prompting a larger sample size or a check for sampling bias.

In practice, you can compute standard deviation quickly using Excel with `=STDEV.S()` for a sample or `=STDEV.P()` for a population, but manual calculation solidifies the understanding that standard deviation is the square root of the average squared distance from the mean.

## The Central Limit Theorem

The central limit theorem describes the behavior of sample means. Even when individual measurements come from a non-normal distribution, the distribution of the sample means approaches a normal shape as the sample size increases. This property makes many inferential statistics robust and allows practitioners to monitor processes effectively without assuming normally distributed output.

The CLT consists of three statements:

1. The mean of the sampling distribution of means equals the population mean $\mu $:
   $$
\mu_{\bar{x}} = \mu
$$

2. The variance of the sampling distribution of means equals the population variance divided by the sample size $n $:
   $$
\sigma^2_{\bar{x}} = \frac{\sigma^2}{n}
$$
   Consequently, the standard deviation of the sample means, called the standard error, is:
   $$
\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}
$$

3. If the original population is normally distributed, the sampling distribution of means is exactly normal for any sample size. If the original population is not normally distributed, the sampling distribution becomes increasingly normal as $n$ increases. Statisticians often treat a sample size of 30 or more as sufficiently large for the approximation to hold, though more extreme population shapes demand larger samples.

Figure 11.3 in the source illustrates this behavior: for various population shapes, the distribution of sample means visibly tightens and becomes symmetrical as $n$ moves from 2 to 10 to 30.

### Standard Error of the Mean

The standard error $\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$ measures the typical distance between a sample mean and the true population mean. It shrinks as sample size grows, reflecting the increased precision of larger samples. This quantity is the foundation for margin of error and confidence intervals.

**Example 1: Chemical Filling Process with Known $\sigma $**

A historical analysis shows the standard deviation of a filling process is $\sigma = 0.012$ milligrams. For a sample of $ n = 16$ fillings, the standard error is:

$$
\sigma_{\bar{x}} = \frac{0.012}{\sqrt{16}} = \frac{0.012}{4} = 0.003 \text{ milligrams}
$$

A larger sample of $n = 64$ would yield $\sigma_{\bar{x}} = \frac{0.012}{8} = 0.0015$ milligrams. The sample mean becomes twice as precise. If the standard error were much larger, a practitioner might increase the sample size to reduce the margin of error before making a process adjustment.

**Example 2: Standard Error from Sample Data**

Consider the 15 test scores treated as a sample. The sample standard deviation is $s = 10.338$. The estimated standard error of the mean is:

$$
SE_{\bar{x}} = \frac{s}{\sqrt{n}} = \frac{10.338}{\sqrt{15}} \approx \frac{10.338}{3.873} \approx 2.67 \text{ points}
$$

This value tells us the typical variability of a class average if we repeatedly drew samples of 15 students. With this estimate, the teacher can gauge whether a future average is meaningfully different from 85.2.

## Confidence Intervals Using the CLT

Because the CLT implies the sample mean is approximately normal, we can build confidence intervals for the population mean $\mu$ with known $\sigma $. A 95 percent confidence interval has the form:

$$
\bar{x} - z_{\alpha/2} \frac{\sigma}{\sqrt{n}} \leq \mu \leq \bar{x} + z_{\alpha/2} \frac{\sigma}{\sqrt{n}}
$$

The term $\frac{\sigma}{\sqrt{n}}$ is the standard error, and $ z_{\alpha/2} \frac{\sigma}{\sqrt{n}}$ is the margin of error. For a 95 percent interval, $ z_{0.025} = 1.96$.

**Applying to the Chemical Process**

Given $\bar{x} = 10$ mg, $\sigma = 0.012$ mg, $ n = 16$, and $ z = 1.96$:

Lower limit:
$$
10 - 1.96 \times \frac{0.012}{4} = 10 - 1.96 \times 0.003 = 10 - 0.00588 = 9.99412 \text{ mg}
$$
Upper limit:
$$
10 + 0.00588 = 10.00588 \text{ mg}
$$

The 95 percent confidence interval is (9.9941, 10.0059) mg. We are 95 percent confident that the true process mean lies within this narrow range. If the interval had included values outside a specification limit, the project team would need to investigate and reduce variation or shift the mean.

## Using the CLT in Control Charts

Real-world manufacturing and transactional processes rarely follow a perfect normal distribution. Control charts such as $\bar{X}$ and $ R$ charts or $\bar{X}$ and $ s$ charts plot subgroup averages. The CLT guarantees that those subgroup averages will be approximately normal even when individual measurements are skewed, as long as the subgroup size is adequate. This robustness allows practitioners to set control limits using normal-based constants and to detect special causes accurately. Without the CLT, many SPC procedures would require knowledge of the underlying distribution, making them impractical.

## Using the CLT in Hypothesis Testing

The CLT enables the use of z-tests and t-tests for means. When the sample size is sufficient, the test statistic $z = \frac{\bar{x} - \mu_0}{\sigma/\sqrt{n}}$ follows a normal distribution under the null hypothesis, even if the population is non-normal. The exercise in the source asks for the standard error when $ n = 16$ and $\sigma = 0.012$ mg, yielding 0.003 mg, and then a 95 percent confidence interval around the process average of 10 mg. This same logic extends to hypothesis tests: if a hypothesized mean falls outside the interval, the null hypothesis is rejected.

## Exam Tips

- Memorize the three CLT statements: the mean of the sampling distribution equals the population mean; its variance is $\sigma^2/n $; and normality is achieved for large $ n$ even when the population is not normal.
- Know that the standard error is $\frac{\sigma}{\sqrt{n}}$ and that it decreases as sample size increases.
- For non-normal populations, a sample size of 30 or more is often considered sufficient for the CLT to hold.
- Be able to compute a confidence interval for the mean when $\sigma$ is known, using $\bar{x} \pm z_{\alpha/2} \frac{\sigma}{\sqrt{n}}$, and interpret the result.
- Recognize that control charts plotting subgroup means rely on the CLT to remain valid when individual data are not normally distributed.
- If a problem gives a historical standard deviation and a sample size, immediately compute the standard error; it is the first step to margin of error and confidence intervals.