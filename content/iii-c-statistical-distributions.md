---
title: "Statistical Distributions (BoK III.C)"
description: "Detailed study notes on the six core statistical distributions for the CSSGB Measure phase: Binomial, Poisson, Normal, Chi-Square, t, and F, with formulas, worked examples, and Six Sigma applications."
---

These notes cover the six statistical distributions required for the CSSGB Body of Knowledge III.C. They build on the probability rules and central limit theorem introduced in the Measure phase. Each distribution is presented with its probability function, parameters, mean, variance, and fully worked numerical examples. The goal is to equip you to identify the appropriate distribution for a given quality problem, compute probabilities, and interpret results in the context of a Six Sigma project.

## Binomial Distribution

The binomial distribution models the number of successes in a fixed number of independent trials, where each trial has exactly two possible outcomes (success or failure) and the probability of success is constant. In a quality context, it is used when inspecting a sample of items and classifying each as defective or not defective.

The probability mass function is

$$
P(X = k) = \binom{n}{k}\, p^{\,k} (1-p)^{\,n-k}
$$

where

- $n$ = number of independent trials (sample size)
- $k$ = number of successes (defects, for example) observed
- $p$ = probability of success on a single trial
- $\binom{n}{k} = \frac{n!}{k!\,(n-k)!}$ is the number of combinations of $ n$ items taken $ k$ at a time (see Chapter 11 for the combination formula).

The mean of a binomial random variable is $\mu = np $, and the variance is $\sigma^2 = np(1-p)$.

The binomial distribution relies directly on the special multiplication rule for independent events and the counting rule for combinations covered in Chapter 11. Because each trial is independent, the probability of a specific sequence with $k$ successes is $ p^k (1-p)^{n-k}$, and the combination factor counts all possible sequences.

### Example 1: Defective Medical Claims

A medical billing office audits 15 randomly selected claims each day. Historically, 20% of claims contain at least one error. The office wants to know the probability that exactly 4 claims in the day's sample have errors.

Here $n = 15$, $ p = 0.20$, $ k = 4$. First, compute the combination:

$$
\binom{15}{4} = \frac{15!}{4!\,11!} = \frac{15 \cdot 14 \cdot 13 \cdot 12}{4 \cdot 3 \cdot 2 \cdot 1} = 1365
$$

Then

$$
P(X = 4) = 1365 \times (0.20)^4 \times (0.80)^{11}
$$
$$
(0.20)^4 = 0.0016,\quad (0.80)^{11} \approx 0.0859
$$
$$
P(X = 4) = 1365 \times 0.0016 \times 0.0859 \approx 0.1876
$$

Interpretation: There is about a 18.8% chance of finding exactly 4 erroneous claims in a random sample of 15. If the office observed 4 on a given day, that would be consistent with the historical 20% error rate. Had the probability been extremely small (for example, less than 0.05), the team might suspect a change in the error rate and initiate root cause analysis.

### Example 2: Supplier Lot Acceptance

A receiving inspector draws 20 units from a large supplier lot. The contract allows up to 5% defectives. What is the probability of finding exactly 0 defectives (i.e., accepting the lot without finding any defects)?

Here $n = 20$, $ p = 0.05$, $ k = 0$.

$$
\binom{20}{0} = 1,\quad (0.05)^0 = 1,\quad (0.95)^{20} \approx 0.3585
$$
$$
P(X = 0) = 1 \times 1 \times 0.3585 = 0.3585
$$

There is a 35.85% chance of observing zero defects even when the true defect rate is 5%. If the inspector found a defect, the probability of that event would be \$1 - P(X=0) = 0.6415$, which indicates that with a 5% defect rate, finding at least one defect in 20 is more likely than not. If a zero-defect sample were required for lot acceptance but the supplier's true rate is 5%, the buyer would still accept the lot about 36% of the time purely by chance. This clarifies why sampling plans must consider both producer and consumer risk.

## Poisson Distribution

The Poisson distribution models the number of events occurring in a fixed interval of time, length, area, or volume when events happen independently at a constant average rate. In quality work, it describes defect counts per unit, such as scratches per square meter of sheet metal, or arrivals of customer complaints per day.

The probability mass function is

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

where

- $\lambda$ = average rate of occurrence (mean number of events per interval)
- $k$ = number of events observed (non-negative integer)
- $e \approx 2.71828$

The mean and variance of a Poisson random variable are both equal to $\lambda $.

### Example 1: Surface Defects on Painted Panels

A paint line produces an average of 2.5 dust specks per panel. The team wants the probability that a randomly selected panel has exactly one speck.

$\lambda = 2.5$, $ k = 1$:

$$
P(X = 1) = \frac{2.5^1 e^{-2.5}}{1!} = 2.5 \times e^{-2.5}
$$
$$
e^{-2.5} \approx 0.0821
$$
$$
P(X = 1) \approx 2.5 \times 0.0821 = 0.2053
$$

About 20.5% of panels will show exactly one speck. If the team set an upper specification of zero defects, they would reject roughly 91.8% of panels ($P(X=0)=e^{-2.5}\approx0.082$), pointing to the need for process improvement before tightening the specification.

### Example 2: Call Center Complaints

A customer service center receives an average of 3.0 complaints per hour. The manager wants to know the probability of receiving at least 5 complaints in the next hour.

First, compute the complement $P(X \le 4)$ and subtract from 1:

$$
P(X=0) = \frac{3^0 e^{-3}}{0!} = e^{-3} \approx 0.0498
$$
$$
P(X=1) = \frac{3^1 e^{-3}}{1!} = 3 \times 0.0498 = 0.1494
$$
$$
P(X=2) = \frac{3^2 e^{-3}}{2!} = 9 \times 0.0498 / 2 = 0.2240
$$
$$
P(X=3) = \frac{3^3 e^{-3}}{3!} = 27 \times 0.0498 / 6 = 0.2240
$$
$$
P(X=4) = \frac{3^4 e^{-3}}{4!} = 81 \times 0.0498 / 24 = 0.1680
$$
Sum \\$0.0498 + 0.1494 + 0.2240 + 0.2240 + 0.1680 = 0.8152$

$$
P(X \ge 5) = 1 - 0.8152 = 0.1848
$$

There is an 18.5% chance of 5 or more complaints in the hour. If the center regularly experiences such spikes, the manager might analyze whether the average rate has truly shifted upward or whether this is normal random variation. If a shift is confirmed, the team would investigate root causes and adjust staffing or processes accordingly.

## Normal Distribution

The normal (Gaussian) distribution is the most important continuous distribution in Six Sigma. The central limit theorem (Chapter 11) ensures that sample means become approximately normal as sample size grows, regardless of the shape of the underlying population. This property justifies the use of normal-based confidence intervals, hypothesis tests, and control charts.

The probability density function is

$$
f(x) = \frac{1}{\sigma \sqrt{2\pi}} \exp\!\left[ -\frac{(x - \mu)^2}{2\sigma^2} \right]
$$

where $\mu$ is the population mean and $\sigma$ the population standard deviation.

To find a tail probability, convert $x$ to a standard normal $ Z $-score:

$$
Z = \frac{x - \mu}{\sigma}
$$

Then consult a standard normal table or software to obtain $P(Z > z)$ or $ P(Z < z)$.

### Example 1: Fill Weight Probability

A beverage filling line has a mean fill volume of 355 mL with a standard deviation of 4 mL. The lower specification limit is 345 mL. What proportion of bottles are under-filled?

Compute the $Z $-score:

$$
Z = \frac{345 - 355}{4} = \frac{-10}{4} = -2.50
$$

From the standard normal table, $P(Z < -2.50) \approx 0.0062$. So approximately 0.62% of bottles are under-filled. If the team considers this unacceptable, they might adjust the mean upward or reduce variation to bring the tail further from the limit.

### Example 2: Service Time Capability

A call center aims for a mean handle time of 5.0 minutes with $\sigma = 0.6$ minutes. The service level agreement requires that no more than 2.5% of calls exceed 6.2 minutes. Does the current process meet the requirement?

First, compute the $Z $-score for the threshold 6.2 minutes:

$$
Z = \frac{6.2 - 5.0}{0.6} = \frac{1.2}{0.6} = 2.00
$$

$P(Z > 2.00) \approx 0.0228$, or 2.28%. This is just below 2.5%, so the process currently meets the requirement marginally. If the $ Z $-score were 1.96, the upper tail would be 2.5% exactly; any mean shift or increase in $\sigma$ could push the defect rate above the allowable limit. The team should monitor the process closely and consider reducing variation to create a safety margin.

## Chi-Square Distribution

If $Z_1, Z_2, \dots, Z_\nu$ are independent standard normal random variables, then the sum of their squares follows a chi-square distribution with $\nu$ degrees of freedom:

$$
\chi^2 = \sum_{i=1}^{\nu} Z_i^2
$$

The distribution is continuous, right-skewed, and becomes more symmetric as $\nu$ increases. Its mean equals $\nu$ and its variance equals \$2\nu $.

In Six Sigma projects, the chi-square distribution is used for hypothesis tests on categorical data (goodness-of-fit, contingency tables) and for constructing confidence intervals on the variance of a normal population.

### Example: Chi-Square Test for Independence

A team classifies product defects by two shifts over one week, obtaining observed frequencies:

| Shift | Defect A | Defect B | Defect C | Total |
|-------|----------|----------|----------|-------|
| Day   | 30       | 20       | 10       | 60    |
| Night | 20       | 30       | 10       | 60    |
| Total | 50       | 50       | 20       | 120   |

To test whether defect type is independent of shift, compute expected frequencies under independence: for example, Day-Defect A expected = (60×50)/120 = 25. The full expected table:

| Shift | Defect A | Defect B | Defect C |
|-------|----------|----------|----------|
| Day   | 25       | 25       | 10       |
| Night | 25       | 25       | 10       |

The chi-square test statistic is

$$
\chi^2 = \sum \frac{(O - E)^2}{E}
$$

Compute each cell:

- Day-A: $(30-25)^2/25 = 25/25 = 1.0$
- Day-B: $(20-25)^2/25 = 25/25 = 1.0$
- Day-C: $(10-10)^2/10 = 0$
- Night-A: $(20-25)^2/25 = 1.0$
- Night-B: $(30-25)^2/25 = 1.0$
- Night-C: $(10-10)^2/10 = 0$

Total $\chi^2 = 4.0$.

Degrees of freedom = (rows - 1)×(columns - 1) = (2-1)×(3-1) = 2. At $\alpha = 0.05$, the critical value from a chi-square table with $\nu = 2$ is approximately 5.991. Since \$4.0 < 5.991$, we fail to reject the null hypothesis of independence. The team would conclude that defect type does not significantly depend on shift. If the statistic had exceeded the critical value, the team would investigate shift-specific procedures that might cause certain defects.

## Student's t-Distribution

When the population standard deviation $\sigma$ is unknown and must be estimated from a small sample, the normal $ Z$ procedure overstates confidence. The $ t $-distribution accounts for the additional uncertainty. Its shape is symmetric and bell-shaped but with heavier tails than the normal; as degrees of freedom increase, it converges to the normal.

The $t $-statistic is

$$
t = \frac{\bar{x} - \mu_0}{s / \sqrt{n}}
$$

where

- $\bar{x}$ = sample mean
- $\mu_0$ = hypothesized population mean
- $s$ = sample standard deviation (using $ n-1$ denominator, see Chapter 5)
- $n$ = sample size

Degrees of freedom = $n - 1$.

### Example: Paint Thickness Audit

A supplier claims the mean thickness of a coating is 30 microns. An inspector measures 8 randomly selected spots: 28, 29, 31, 32, 30, 27, 29, 31. Test whether the true mean differs from 30 at $\alpha = 0.05$.

First, compute sample mean and standard deviation:

$$
\bar{x} = \frac{28+29+31+32+30+27+29+31}{8} = \frac{237}{8} = 29.625
$$
Deviations: -1.625, -0.625, 1.375, 2.375, 0.375, -2.625, -0.625, 1.375. Squared: 2.6406, 0.3906, 1.8906, 5.6406, 0.1406, 6.8906, 0.3906, 1.8906. Sum = 19.875.

$$
s^2 = \frac{19.875}{7} \approx 2.8393,\quad s \approx 1.685
$$

Now compute $t $:

$$
t = \frac{29.625 - 30}{1.685 / \sqrt{8}} = \frac{-0.375}{0.5958} \approx -0.629
$$

With $df = 7$, the two-tailed critical value at $\alpha = 0.05$ is approximately 2.365. Since $|t| = 0.629 < 2.365$, we fail to reject $ H_0$: the data do not provide sufficient evidence that the mean thickness differs from 30 microns. If the $ t $-statistic had exceeded the critical value, the team would work with the supplier to adjust the process or revise the specification.

## F-Distribution

The $F $-distribution arises as the ratio of two independent chi-square variables, each divided by its degrees of freedom:

$$
F = \frac{\chi^2_1 / \nu_1}{\chi^2_2 / \nu_2}
$$

It is continuous, right-skewed, and non-negative. Its shape is governed by two degrees of freedom, $\nu_1$ (numerator) and $\nu_2$ (denominator).

In quality improvement, the $F $-distribution is used primarily to compare variances of two populations (ANOVA and equality-of-variance tests). If an improvement is expected to reduce variation, an $ F $-test can formally determine whether the new process variance is significantly smaller than the old one.

### Example: Comparing Two Filling Machine Variances

Machine A (current) and Machine B (trial) fill containers. A team samples 10 containers from Machine A (sample variance $s_A^2 = 5.2$) and 12 from Machine B ($ s_B^2 = 2.8$). They want to test whether Machine B has a smaller variance (one-tailed test).

Hypotheses: $H_0: \sigma_A^2 = \sigma_B^2$ versus $ H_a: \sigma_A^2 > \sigma_B^2$.

The $F $-ratio is

$$
F = \frac{s_A^2}{s_B^2} = \frac{5.2}{2.8} \approx 1.857
$$

Degrees of freedom: numerator $\nu_1 = n_A - 1 = 9$, denominator $\nu_2 = n_B - 1 = 11$.

Using an $F $-table at $\alpha = 0.05$, the critical value $ F_{0.05, 9, 11}$ is approximately 2.90. Since \\$1.857 < 2.90$, we fail to reject $ H_0$: the evidence is not strong enough to conclude that Machine B's variance is smaller. If the $ F $-ratio had exceeded the critical value, the team would have statistical justification to adopt Machine B for its lower variability.

## Comparison Table

| Distribution | Type        | Mean        | Variance            | Primary Six Sigma Use Case                              |
|--------------|-------------|-------------|---------------------|---------------------------------------------------------|
| Binomial     | Discrete    | $np$        | $ np(1-p)$           | Proportion defective in a fixed sample size             |
| Poisson      | Discrete    | $\Lambda$   | $\Lambda$           | Defect counts per unit of area, time, or volume         |
| Normal       | Continuous  | $\mu$       | $\sigma^2$          | Modeling sample means, capability analysis, control charts |
| Chi-Square   | Continuous  | $\nu$       | \$2\nu$              | Tests on categorical data, variance confidence intervals|
| t            | Continuous  | 0 (for $df>1$) | $\frac{\nu}{\nu-2}$ (for $\nu>2$) | Hypothesis tests for means when $\sigma$ is unknown |
| F            | Continuous  | $\frac{\nu_2}{\nu_2-2}$ (for $\nu_2>2$) | complex formula | Comparing two variances, ANOVA |

## Exam Tips

1. When a question describes a fixed number of independent trials with a constant defect probability and asks for the chance of exactly $k$ defects, apply the binomial PMF with the combination formula.
2. For defect counts per unit of opportunity (scratches per panel, calls per hour) where no natural upper limit exists, choose the Poisson distribution and verify that the mean and variance are approximately equal to confirm fit.
3. Always standardize a normal raw value to a $Z $-score before looking up tail probabilities; recall that $ Z = (x - \mu)/\sigma$ and that the standard normal table gives cumulative area to the left of $ Z $.
4. Use the $t $-distribution instead of the normal when the sample size is small ($ n < 30$) and the population standard deviation is estimated from the sample; the degrees of freedom are $ n-1$.
5. The chi-square test statistic sums $(O - E)^2/E $; if the calculated value exceeds the critical chi-square limit for the appropriate degrees of freedom, reject the hypothesis of independence or good fit.
6. In an $F $-test for equal variances, always place the larger sample variance in the numerator to obtain an $ F $-ratio $\ge 1$, and compare against the upper-tail critical value.