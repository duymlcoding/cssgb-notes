---
title: "Hypothesis Testing Basics (IV-B-1)"
description: "Detailed study notes for ASQ CSSGB certification covering null and alternative hypotheses, types of errors, one-tail and two-tail tests, required sample size, statistical versus practical significance, power, and test statistics for means using Z-tests and t-tests."
---

## Introduction

Hypothesis testing allows a Six Sigma practitioner to draw conclusions about a population based on sample data. Because conclusions rely on samples rather than the entire population, every test carries risk. This risk is quantified and controlled through significance levels, error types, and power. A Green Belt uses hypothesis testing to validate improvement results, compare process performance, and make data-driven decisions.

## Null and Alternative Hypotheses

The **null hypothesis** ($H_0$) is the statement being tested. It typically asserts that no change or no difference exists, for example $ H_0: \mu = 6.0$.

The **alternative hypothesis** ($H_1$) represents the claim that is accepted if $ H_0$ is rejected. It always states that the population mean is less than, not equal to, or greater than a specific value:

$$
H_1: \mu \neq 6.0,\quad H_1: \mu < 6.0,\quad H_1: \mu > 6.0
$$

A **test statistic** is calculated from sample data and compared with a **critical value** obtained from a probability table (such as the t-distribution table in Appendix Q). The critical value depends on the chosen **level of significance** (1%, 5%, or 10%) and the type of test.

Based on the comparison, a decision is made: reject $H_0$ or fail to reject $ H_0$. Failing to reject does not prove $ H_0$ is true; it simply means the sample evidence is not strong enough to discredit it.

## Types of Errors

Two types of errors can occur when making a decision about the population.

**Type I error ($\alpha$ error)** occurs when the null hypothesis is rejected when it is actually true. This is also called **producer's risk** in acceptance sampling. For example, incoming products that are good are mistakenly labeled defective.

**Type II error ($\beta$ error)** occurs when the null hypothesis is not rejected when it should have been rejected. This is the **consumer's risk**. For example, incoming products that are defective are labeled good.

The error matrix below summarises all possible outcomes.

|                        | Null hypothesis is true | Null hypothesis is false |
|------------------------|-------------------------|--------------------------|
| **Fail to reject $H_0$**  | $ p = 1 - \alpha $, correct outcome | $ p = \beta $, type II error |
| **Reject $H_0$**          | $ p = \alpha $, type I error         | $ p = 1 - \beta $, correct outcome |

The probability $1 - \beta$ is called **power**. Higher power is better in a hypothesis test. Power represents the likelihood that the test correctly rejects a false null hypothesis.

## One-Tail Test

When the null hypothesis is set up to test whether a sample value is smaller or larger than a population value, the entire $\alpha$ risk is placed on one end of the sampling distribution. This is a **one-tail test**.

- Right-tailed test: $H_0: \mu \leq \text{value},\; H_1: \mu > \text{value}$. The rejection region is in the right tail.
- Left-tailed test: $H_0: \mu \geq \text{value},\; H_1: \mu < \text{value}$. The rejection region is in the left tail.

**Example (golf ball).** A company claims a new ball increases driving distance by more than 20 yards.

- $H_0: \mu \leq 20$
- $H_1: \mu > 20$
- Significance level $\alpha = 0.05$ (entire risk in the right tail)

A sample of 10 additional yards is collected: 18, 20, 19, 18, 21, 19, 23, 18, 19, 22. A one-sample t-test yields:

- Mean = 19.673, StDev = 1.775, SE Mean = 0.561
- 95% Lower Bound = 18.644
- $t = -0.58$, $ p = 0.713$

Since $p > 0.05$, we fail to reject $ H_0$. The data do not support the claim that the new ball increases distance by more than 20 yards. If the sample mean had fallen in the rejection region (right tail), the conclusion would have been to reject $ H_0$ and accept the manufacturer's claim.

## Two-Tail Test

A **two-tail test** is used when the alternative hypothesis states that a difference exists in either direction ($\neq $). The allowable $\alpha$ error is split equally into both tails.

For example:

- An economist tests whether unemployment levels have changed significantly from the previous year.
- A study compares salary levels between two companies.

The null hypothesis states equality ($H_0$), and the alternative states no equality ($ H_1$). If the test statistic falls in either tail (extreme high or low values), $ H_0$ is rejected.

## Required Sample Size

The ideal approach is to specify acceptable $\alpha$ and $\beta$ risks and then calculate the sample size needed to detect a meaningful difference with the desired confidence.

The sample size depends on:

- The desired Type I risk ($\alpha $) and Type II risk ($\beta $)
- The minimum difference to detect between population means ($\mu - \mu_0$)
- The variation in the characteristic, measured by the standard deviation $\sigma$ or sample standard deviation $ s$

**Variable data sample size using only $\alpha $:**

$$
n = \frac{Z^2 \sigma^2}{E^2}
$$

where:
- $n$ = required sample size
- $Z$ = Z-value corresponding to the confidence level (for 95% confidence, two-tail, $ Z = 1.96$)
- $\sigma$ = historical standard deviation
- $E$ = the minimum shift in the process mean that must be detected (practical significance limit)

**Example (shipyard).** An operational adjustment may alter the process hourly mean. Determine the minimum sample size at 95% confidence to confirm a mean shift greater than 10 metric tons per hour. Historical standard deviation is 35 tons.

- $Z = 1.96$, $\sigma = 35$, $ E = 10$
- $n = \frac{(1.96)^2 \times (35)^2}{(10)^2} = \frac{3.8416 \times 1225}{100} = \frac{4705.96}{100} = 47.0596 \approx 471$

Collect 471 hourly yield values and compute the average. If this average deviates from the previous hourly average by more than 10 tons, a significant change at the 95% confidence level has occurred. If the deviation is less than 10 tons, the shift can be explained by chance.

**Power-based sample size.** When both $\alpha$ and $\beta$ are considered, power and sample size calculations use software. For example, a one-sample Z-test with $\sigma = 0.03$, difference to detect = 0.04, $\alpha = 0.05$, and desired power = 0.9 yields a required sample size of 6, giving an actual power of 0.904. This means with 6 samples, the test has a 90% chance of detecting a true difference of 0.04.

If the experimenter had used a smaller sample, power would drop below 0.9, increasing the risk of a Type II error and possibly missing a real effect. Conversely, if a larger sample had been feasible, power would increase beyond 0.9.

## Statistical and Practical Significance

**Statistical significance** is evaluated by the **p-value**. The p-value is the probability of obtaining a test statistic result at least as extreme as the observed value, assuming the null hypothesis is true. If the p-value is greater than the chosen significance level (often 0.05 or 0.01), the evidence is insufficient to reject $H_0$. A small p-value (less than $\alpha $) leads to rejection.

**Practical significance** asks whether a detected difference is large enough to matter in the real world. A difference may be statistically significant but not practically important.

For example, two processes may show a statistically significant difference in defect levels of 0.5%. However, the customer allows a defect level of 3% for this non-critical step. The 0.5% difference, though real, does not justify process changes. Another example: a measurement difference of up to 50 microns between two pieces of test equipment may be acceptable practically, while a statistical test might declare a significant difference at 20 microns.

To evaluate practical significance, sample size must be adequate. Low power from an insufficient sample size can lead to incorrect decisions. Calculating power helps inform stakeholders of the risk involved in a decision.

**Desired power** is typically 0.8 or higher. In situations with high organisational risk, 0.9 or more may be required. A power of 0.8 means an experiment with the current sample size has an 80% likelihood to correctly identify a significant difference when one truly exists, and a 20% chance of a Type II error.

## Tests for Means: Z-Test and t-Test

Hypothesis tests on population means use the Z-test when the population standard deviation is known or the sample size is large ($n \ge 30$), and the t-test when the population standard deviation is unknown and the sample size is small.

### Z-Test

The test statistic for a mean is:

$$
Z = \frac{\bar{X} - \mu_0}{\sigma / \sqrt{n}}
$$

where:
- $\bar{X}$ = sample mean
- $\mu_0$ = hypothesized population mean
- $\sigma$ = population standard deviation (assumed known)
- $n$ = sample size

The alternative hypothesis determines the type of test:
- $H_1: \mu \neq \mu_0$ → two-tail test
- $H_1: \mu > \mu_0$ → right one-tail test
- $H_1: \mu < \mu_0$ → left one-tail test

**Procedure for testing the mean (Z-test):**

1. Verify conditions: normal population or large sample ($n \ge 30$), and $\sigma$ known.
2. State $H_0$ and $ H_1$.
3. Choose significance level $\alpha $.
4. Determine critical value(s) from the Z-table.
   - Two-tail: find $Z_{\alpha/2}$ such that the area to its right is $\alpha/2$. Critical values are $\pm Z_{\alpha/2}$.
   - Right-tail: find $Z_\alpha$ such that area to its right is $\alpha $. Critical value is $ Z_\alpha $.
   - Left-tail: find $Z_\alpha$ as for right-tail; critical value is $-Z_\alpha $.
5. Compute the test statistic $Z $.
6. If the test statistic falls in the rejection region, reject $H_0$; otherwise, do not reject.
7. State the conclusion in context.

**Example 1 (two-tail Z-test).** A vendor claims the average weight of a shipment is 1.84. A customer randomly selects 64 parts and finds an average of 1.88. The population standard deviation is known to be 0.03. Test at $\alpha = 0.05$ whether the claim is incorrect.

- Condition satisfied: large sample, $\sigma$ known.
- $H_0: \mu = 1.84$, $ H_1: \mu \neq 1.84$ (two-tail test).
- $\alpha = 0.05$, so $\alpha/2 = 0.025$.
- Critical values: $\pm 1.96$.
- Compute $Z $: $\bar{X} = 1.88$, $\mu_0 = 1.84$, $\sigma = 0.03$, $ n = 64$
  $$Z = \frac{1.88 - 1.84}{0.03 / \sqrt{64}} = \frac{0.04}{0.03 / 8} = \frac{0.04}{0.00375} \approx 10.67$$
- $10.67 > 1.96$, so reject $ H_0$.
- Conclusion: At the 0.05 significance level, the data indicate the vendor's claim of average weight 1.84 is false.

If the test statistic had fallen between -1.96 and 1.96, we would have failed to reject $H_0$ and concluded there was not enough evidence to contradict the vendor's claim.

**Example 2 (one-tail Z-test).** Using the same data, test whether the mean is less than 1.84 (left-tail test). $H_0: \mu \geq 1.84$, $ H_1: \mu < 1.84$.
- $\alpha = 0.05$, left tail: critical value = $-1.645$ (since $ Z_{0.05}=1.645$).
- Test statistic: $Z = 10.67$ (same calculation).
- $10.67$ is not less than -1.645, so fail to reject $ H_0$.
- Conclusion: There is insufficient evidence to conclude the mean weight is less than 1.84.

For a right-tailed test $H_1: \mu > 1.84$, critical value would be 1.645, and $ Z = 10.67$ would fall in the rejection region, leading to rejection of $ H_0$ and support for the claim that the mean exceeds 1.84.

### Student's t-Test

The t-test is used when the population standard deviation is unknown and the sample size is small ($n < 30$), although it is valid for any sample size. The data must come from a normally distributed population, confirmed by a histogram or normal probability plot.

The test statistic is:

$$
t = \frac{\bar{X} - \mu_0}{s / \sqrt{n}}
$$

where:
- $\bar{X}$ = sample mean
- $\mu_0$ = hypothesized population mean
- $s$ = sample standard deviation
- $n$ = sample size

Degrees of freedom: $df = n - 1$. The critical value $ t_{\alpha}$ or $ t_{\alpha/2}$ is found from the t-distribution table using $\alpha$ and $ df $.

**Procedure for t-test:**

1. Calculate sample mean $\bar{X}$ and sample standard deviation $ s $.
2. Compute the difference $\bar{X} - \mu_0$.
3. Compute the standard error $s / \sqrt{n}$.
4. Divide the difference by the standard error to obtain $t $.
5. Compare the absolute value of $t$ with the critical value $ t_c$ from the t-table.
6. Reject $H_0$ if $|t|$ exceeds $ t_c$ (for two-tail) or if $ t$ falls in the rejection tail; otherwise fail to reject.
7. State the conclusion.

**Example 3 (one-sample t-test, cutoff saw).** A cutoff saw historically produced parts with a mean length of 4.125. After installing a new blade, a random sample of 20 parts gives $\bar{X} = 4.123$ and $ s = 0.008$. Use $\alpha = 0.10$ to test whether the mean has decreased.

- Population standard deviation unknown, sample size 20 → t-test.
- $H_0: \mu = 4.125$, $ H_1: \mu < 4.125$ (left-tailed test).
- $\alpha = 0.10$, $ df = 19$. From t-table, one-tail critical value $ t_{0.10,19} = 1.328$. For left tail, critical value = $-1.328$.
- Compute $t $:
  $$t = \frac{4.123 - 4.125}{0.008 / \sqrt{20}} = \frac{-0.002}{0.00178885} \approx -1.118$$
- $-1.118$ lies to the right of $-1.328$ (not in the rejection region), so fail to reject $ H_0$.
- Conclusion: At the 0.10 significance level, the data do not indicate that the average length has decreased.

If the sample mean had been lower, producing a t-statistic less than -1.328, the conclusion would have been to reject $H_0$ and accept that the mean had decreased after the blade change. The practitioner would then investigate the blade's effect.

**Example 4 (one-sample t-test, golf ball).** As seen in the one-tail section, the golf ball data gave $t = -0.58$ with $ p = 0.713$, leading to failure to reject $ H_0$ at $\alpha = 0.05$. That example used a right-tailed test, but since $ H_1: \mu > 20$, a negative t-statistic would never fall in the right rejection region. The large p-value confirms there is no evidence to support the claim.

## Exam Tips

1. When a hypothesis test yields a p-value greater than $\alpha $, state "fail to reject $ H_0$", never "accept $ H_0$". If the problem gives a critical value, compare the absolute test statistic to the critical value for two-tailed tests, or check the sign for one-tailed tests.
2. To determine the correct hypothesis setup, identify the research claim and place it in $H_1$. Directional claims (greater than, less than) produce one-tailed tests; a claim of difference produces a two-tailed test.
3. For sample size calculation using the formula $n = Z^2 \sigma^2 / E^2$, ensure all units are the same and $ E$ represents the smallest shift you must detect. If $ n$ is not an integer, always round up.
4. Distinguish Type I and Type II errors by cost context: Type I error (producer's risk) is rejecting good product, Type II error (consumer's risk) is accepting bad product. Given a scenario, identify which error is more costly to the organization.
5. Power is the probability of correctly rejecting a false null hypothesis ($1 - \beta $). If a problem asks you to evaluate risk of missing a real effect, think about low power and the need for a larger sample size.

