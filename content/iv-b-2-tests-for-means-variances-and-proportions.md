---
title: "Tests for Means, Variances, and Proportions"
description: "Detailed study notes on hypothesis tests and confidence intervals for population parameters: means, variances, and proportions. Covers z-tests, t-tests, chi-square tests, F-tests, ANOVA, and related procedures as outlined in the ASQ CSSGB Handbook."
---

In the Analyze phase of a Six Sigma project, teams use hypothesis tests and confidence intervals to draw conclusions about populations from sample data. Because conclusions rest on samples rather than entire populations, every test carries risk. The Council for Six Sigma Certification training manual defines the alpha-risk as the risk of incorrectly rejecting a true null hypothesis and the beta-risk as the risk of failing to reject a false null hypothesis. The p-value quantifies the likelihood that an observed result, or one more extreme, would occur if the null hypothesis were true. A small p-value (typically ≤ 0.05) leads to rejection of the null hypothesis.

This section presents the statistical tools that appear in the ASQ CSSGB Handbook for testing claims about population means, variances, and proportions. Each subsection describes the underlying theory, states the relevant formulas in display math, defines every variable, and works through fully numerical examples directly from the source material. After each example, a brief note explains what a practitioner would do differently if the conclusion had been reversed.

## Confidence Intervals and Hypothesis Tests for a Population Mean (σ Known)

When the population standard deviation σ is known, the sampling distribution of the sample mean is exactly normal for normally distributed populations and approximately normal for large samples regardless of the population shape. A confidence interval for the population mean μ is built around the sample mean $\bar{X}$.

### Confidence Interval Formula

$$
\bar{X} \pm Z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}
$$

Where  
- $\bar{X}$ = sample mean  
- $Z_{\alpha/2}$ = critical value from the standard normal distribution for the desired confidence level (for example, 1.96 for 95% confidence)  
- $\sigma$ = population standard deviation  
- $n$ = sample size

**Margin of error:** $Z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}$

The procedure, as listed in the CSSGB Handbook, is:

1. Determine the confidence level and find the appropriate $Z$ value in the Z-table.  
2. Calculate $\bar{X}$ from the sample data.  
3. Calculate margin of error: multiply $Z$ by $\sigma$ and divide by $\sqrt{n}$.  
4. Obtain the confidence interval as $\bar{X}$ ± margin of error.

### Example 1: Home Shopping Channel – 95% Confidence Interval

From a sample of $n = 32$ customers, the average order is $\bar{X} = 78.25$ dollars, and the population standard deviation is $\sigma = 37.50$ dollars. Compute the 95% confidence interval for the population mean.

$Z_{0.025} = 1.96$ (for a 95% two-sided interval).

Margin of error:

$$
\text{Margin} = 1.96 \times \frac{37.50}{\sqrt{32}} = 1.96 \times \frac{37.50}{5.6569} \approx 1.96 \times 6.63 = 13.00
$$

Confidence interval:

$$
78.25 \pm 13.00 \;\Rightarrow\; (65.25,\; 91.25)
$$

Interpretation: We are 95% confident that the true average order amount falls between 65.25 and 91.25 dollars.

If the calculated interval had not captured the hypothesized value that management was testing, the practitioner would reject the null hypothesis and conclude that the population mean differs from that value.

### Example 2: Same Data – 99% Confidence Interval

To see the effect of a higher confidence level, repeat the interval using $Z_{0.005} = 2.576$.

Margin of error:

$$
2.576 \times \frac{37.50}{\sqrt{32}} = 2.576 \times 6.63 \approx 17.08
$$

Interval:

$$
78.25 \pm 17.08 \;\Rightarrow\; (61.17,\; 95.33)
$$

The wider interval reflects greater certainty at a higher confidence level. If a decision depended on a narrower range, a larger sample would be needed.

## Test for a Single Population Variance (Chi-Square)

The chi-square test evaluates whether the population variance $\sigma^2$ equals a specified value. It also produces confidence intervals for the variance and standard deviation. The test assumes the underlying population is normally distributed.

### Hypothesis Test for Variance

Null hypothesis: $\sigma^2 = \sigma_0^2$ (two-tailed). Alternative: $\sigma^2 \neq \sigma_0^2$.

Test statistic:

$$
\chi^2 = \frac{(n-1)s^2}{\sigma_0^2}
$$

Where  
- $n$ = sample size  
- $s^2$ = sample variance  
- $\sigma_0^2$ = hypothesized variance

The degrees of freedom are $n-1$. The critical values come from a chi-square table.

### Example 3: Comparing Process Variances

A sample of $n = 35$ parts yields a variance $ s^2 = 46$ units. The null hypothesis states that the population variance equals $36$ (a target from a different processing method). Use α = 0.05, two-sided.

$$
\chi^2 = \frac{(35-1) \times 46}{36} = \frac{34 \times 46}{36} = \frac{1564}{36} \approx 43.44
$$

Degrees of freedom = 34. The handbook reports a p-value of 0.257. Since p > 0.05, the null hypothesis is not rejected. The two processes do not have detectably different variances.

If the p-value had been ≤ 0.05, the conclusion would be that the variance of the new process is statistically different from 36, and the wider confidence interval for variance would indicate the magnitude of the difference.

### Confidence Interval for Variance

The confidence interval for the population variance is based on the chi-square distribution and is not symmetrical about the point estimate:

$$
\frac{(n-1)s^2}{\chi^2_{\alpha/2,\; n-1}} \le \sigma^2 \le \frac{(n-1)s^2}{\chi^2_{1-\alpha/2,\; n-1}}
$$

Where  
- $\chi^2_{\alpha/2,\; n-1}$ and $\chi^2_{1-\alpha/2,\; n-1}$ are the upper and lower critical values from the chi-square distribution for $ n-1$ degrees of freedom.

### Example 4: 90% Confidence Interval for Variance – Same Data

Use $n = 35$, $ s^2 = 46$, and a 90% confidence level. The chi-square critical values for $ df = 34$ are $\chi^2_{0.95,34} = 21.66$ and $\chi^2_{0.05,34} = 48.60$ (from the handbook).

Lower bound:

$$
\frac{34 \times 46}{48.60} = \frac{1564}{48.60} \approx 32.18
$$

Upper bound:

$$
\frac{34 \times 46}{21.66} = \frac{1564}{21.66} \approx 72.21
$$

The 90% confidence interval for $\sigma^2$ is (32.18, 72.21). Because this interval does not include 36, it would appear that 36 is a plausible variance, but the hypothesis test above showed no significant difference at the 0.05 level because the two-sided chi-square test with α = 0.05 uses different critical values (the 95% CI for the same data is 30.1 to 79.0, which does contain 36). The handbook states: “The new process variance has to be either lower than 30 or higher than 79 to declare a difference.” So a 95% CI would be needed for a conclusion consistent with a 0.05 two-tailed test.

If the computed interval had completely excluded the target, the team would conclude the variances differ and might investigate the new method further.

## Hypothesis Tests and Confidence Intervals for a Proportion

A proportion test compares a sample proportion $p'$ to a hypothesized population proportion $ p_0$. When both $ np_0$ and $ n(1-p_0)$ are at least 5, the normal approximation to the binomial distribution is appropriate.

### Confidence Interval for a Proportion (Large Sample)

$$
p' \pm Z_{\alpha/2} \sqrt{\frac{p'(1-p')}{n}}
$$

Where  
- $p' = x/n$ (sample proportion)  
- $x$ = number of “successes” in the sample  
- $n$ = sample size

The handbook requires $np'$ and $ n(1-p') \ge 5$ (conservatively $ np_0$ and $ n(1-p_0) \ge 5$ for hypothesis test).

### Example 5: Proportion of Female Home Shopping Channel Customers

Out of $n = 175$ random customers, $ x = 110$ were female. Calculate the 90% confidence interval for the true proportion.

$p' = 110/175 = 0.62857$ (rounded to 0.629 in the handbook). $ Z_{0.05} = 1.645$.

Standard error:

$$
\sqrt{\frac{0.629 \times 0.371}{175}} = \sqrt{\frac{0.23336}{175}} \approx \sqrt{0.0013335} \approx 0.03652
$$

Margin of error:

$$
1.645 \times 0.03652 \approx 0.0600
$$

Confidence interval:

$$
0.629 \pm 0.060 \;\Rightarrow\; (0.569,\; 0.689)
$$

We are 90% confident that between 56.9% and 68.9% of all customers are female.

If the interval did not contain the hypothesised proportion, the practitioner would reject the null hypothesis that the true proportion equals that value.

### Example 6: 95% Confidence Interval for the Same Proportion

To see the widening effect, use $Z_{0.025} = 1.96$ for 95% confidence.

Margin of error:

$$
1.96 \times 0.03652 \approx 0.0716
$$

Interval:

$$
0.629 \pm 0.0716 \;\Rightarrow\; (0.557,\; 0.701)
$$

A wider interval offers more confidence but less precision. If a supply decision required a narrow range of female customers, a larger sample would be needed to reduce the margin of error.

### Hypothesis Test for a Proportion (One-Sample p-Test)

$$
Z = \frac{p' - p_0}{\sqrt{\frac{p_0(1-p_0)}{n}}}
$$

Where  
- $p_0$ = hypothesized proportion in the null hypothesis  
- $p' = x/n$  
- $n$ = sample size  

Reject $H_0$ if the computed Z falls in the rejection region determined by the alternative hypothesis and significance level α.

### Example 7: Vendor Defect Rate

A vendor claims at most 2% defectives. Receiving inspection draws a random sample of $n = 500$ and finds $ x = 15$ defectives, so $ p' = 15/500 = 0.03$. Test at α = 0.05 whether the data indicate the vendor is wrong.

Condition check: $np_0 = 500 \times 0.02 = 10 \ge 5$ and $ n(1-p_0) = 500 \times 0.98 = 490 \ge 5$, so normal approximation is valid.

Null hypothesis: $p \le 0.02$; alternative: $ p > 0.02$ (right-tailed). α = 0.05, critical $ Z_{0.05} = 1.645$.

Test statistic:

$$
Z = \frac{0.03 - 0.02}{\sqrt{\frac{0.02 \times 0.98}{500}}} = \frac{0.01}{\sqrt{\frac{0.0196}{500}}} = \frac{0.01}{\sqrt{0.0000392}} = \frac{0.01}{0.006261} \approx 1.597
$$

Since $1.597 < 1.645$, do not reject $H_0$.

Conclusion: At the 0.05 significance level, the data do not provide sufficient evidence that the vendor’s at-most-2% claim is false. The handbook’s Minitab analysis reports a p-value of 0.055, consistent with this conclusion.

If the test statistic had exceeded the critical value, the receiving inspector would reject the shipment and work with the vendor to improve quality.

When $np_0 < 5$ or $ n(1-p_0) < 5$, the binomial distribution must be used directly without the normal approximation. The CSSGB Handbook states that the binomial distribution is applied for hypothesis tests relating to proportion under those small-sample conditions.

## Paired-Comparison Tests: Two-Mean t-Tests and F-Test for Variances

When two groups are compared, the choice of test depends on whether the variances can be assumed equal and whether the observations are independent or paired.

### Two-Mean Equal Variance t-Test

Assumes the two populations have the same unknown variance. The pooled standard deviation $s_p$ is used.

Test statistic:

$$
t = \frac{\bar{X}_1 - \bar{X}_2}{s_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}}
$$

Pooled standard deviation:

$$
s_p = \sqrt{\frac{(n_1-1)s_1^2 + (n_2-1)s_2^2}{n_1 + n_2 - 2}}
$$

Degrees of freedom: $df = n_1 + n_2 - 2$.

Null hypothesis: $\mu_1 = \mu_2$ (two-tailed) vs. $\mu_1 \neq \mu_2$.

### Example 8: Two CNC Machines (Equal Variance Assumed)

Two operators machining parts on two CNCs. Data from the handbook:

Machine 1: $\bar{X}_1 = 5.2334$, $ s_1 = 0.0143$, $ n_1 = 5$  
Machine 2: $\bar{X}_2 = 5.2208$, $ s_2 = 0.0179$, $ n_2 = 5$

Compute pooled standard deviation:

$$
s_p = \sqrt{\frac{(4) \times (0.0143^2) + (4) \times (0.0179^2)}{5+5-2}} = \sqrt{\frac{4 \times 0.00020449 + 4 \times 0.00032041}{8}} = \sqrt{\frac{0.00081796 + 0.00128164}{8}} = \sqrt{\frac{0.0020996}{8}} \approx \sqrt{0.00026245} \approx 0.0162
$$

Test statistic:

$$
t = \frac{5.2334 - 5.2208}{0.0162 \sqrt{\frac{1}{5} + \frac{1}{5}}} = \frac{0.0126}{0.0162 \sqrt{0.4}} = \frac{0.0126}{0.0162 \times 0.6325} = \frac{0.0126}{0.01024} \approx 1.23
$$

Degrees of freedom = 8. Critical value $t_{0.025,8} = 2.306$ (two-tailed α = 0.05). Since $1.23 < 2.306$, fail to reject $ H_0$. The data do not show a significant difference between the machine means. The handbook’s Minitab output yields a p-value of 0.255.

Had the t-statistic exceeded the critical value, the team would conclude the machines produce parts with different average dimensions and investigate the differences.

### Two-Mean Unequal Variance t-Test (Welch’s t-Test)

When the population variances cannot be assumed equal, a separate variance estimate is used, and the degrees of freedom are approximated (Satterthwaite).

Test statistic:

$$
t = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}
$$

Degrees of freedom:

$$
df = \frac{\left( \frac{s_1^2}{n_1} + \frac{s_2^2}{n_2} \right)^2}{\frac{\left( \frac{s_1^2}{n_1} \right)^2}{n_1-1} + \frac{\left( \frac{s_2^2}{n_2} \right)^2}{n_2-1}}
$$

The CSSGB Handbook rounds the computed df down to increase the confidence level.

### Example 9: Same CNC Data – Unequal Variances

Using the same numbers:

$$
t = \frac{0.0126}{\sqrt{\frac{0.0143^2}{5} + \frac{0.0179^2}{5}}} = \frac{0.0126}{\sqrt{\frac{0.0002045}{5} + \frac{0.0003204}{5}}} = \frac{0.0126}{\sqrt{0.0000409 + 0.0000641}} = \frac{0.0126}{\sqrt{0.0001050}} = \frac{0.0126}{0.01025} \approx 1.23
$$

Compute df:

Numerator of df formula: $(0.0001050)^2 = 1.1025 \times 10^{-8}$  
Denominator: $\frac{(0.0000409)^2}{4} + \frac{(0.0000641)^2}{4} = \frac{1.6728 \times 10^{-9}}{4} + \frac{4.1088 \times 10^{-9}}{4} = (4.182 + 10.272) \times 10^{-10} \approx 1.4454 \times 10^{-9}$

$df \approx \frac{1.1025 \times 10^{-8}}{1.4454 \times 10^{-9}} \approx 7.63$, rounded down to 7. Critical value $ t_{0.025,7} \approx 2.365$. The test statistic remains 1.23, so we fail to reject $ H_0$. The conclusion is the same as the equal variance case.

If the variances had been shown to be different (via an F-test), the unequal variance test would be the appropriate choice. The handbook notes that Green Belts should first test for equality of variances and then select the appropriate t-test.

### Paired t-Test

When measurements come in natural pairs (before-after, left-right, matched subjects), the paired t-test analyzes the differences.

Test statistic:

$$
t = \frac{\bar{d}}{s_d / \sqrt{n}}
$$

Where  
- $\bar{d}$ = mean of the paired differences  
- $s_d$ = standard deviation of the differences  
- $n$ = number of pairs (differences), $ df = n-1$

### Example 10: Equipment Calibration — Before and After

An operator measured the same five parts before and after calibration. Differences (After minus Before):

| Part | 1 | 2 | 3 | 4 | 5 |
|------|-------|-------|-------|-------|-------|
| Difference | 0.014 | 0.027 | 0.010 | 0.010 | 0.002 |

**Step 1 — Mean difference:**

$$
\bar{d} = \frac{0.014 + 0.027 + 0.010 + 0.010 + 0.002}{5} = \frac{0.063}{5} = 0.0126
$$

**Step 2 — Standard deviation of differences:**

Each deviation $(d_i - \bar{d})$ and its square:

| $d_i$ | $d_i - \bar{d}$ | $(d_i - \bar{d})^2$ |
|--------|-----------------|----------------------|
| 0.014 | -0.0014 | $1.96 \times 10^{-6}$ |
| 0.027 | +0.0144 | $2.0736 \times 10^{-4}$ |
| 0.010 | -0.0026 | $6.76 \times 10^{-6}$ |
| 0.010 | -0.0026 | $6.76 \times 10^{-6}$ |
| 0.002 | -0.0106 | $1.1236 \times 10^{-4}$ |

$$
s_d^2 = \frac{3.3784 \times 10^{-4}}{4} = 8.446 \times 10^{-5} \qquad s_d = 0.00919
$$

**Step 3 — Test statistic** ($df = n - 1 = 4$):

$$
t = \frac{\bar{d}}{s_d / \sqrt{n}} = \frac{0.0126}{0.00919 / \sqrt{5}} = \frac{0.0126}{0.00411} \approx 3.08
$$

**Step 4 — Decision:** For a two-tailed test at $\alpha = 0.05$ with $df = 4$, the critical value is $t_{0.025,\,4} = 2.776$. Since $3.08 > 2.776$, reject $H_0: \mu_d = 0$.

**Conclusion:** Calibration produced a statistically significant shift in measurements. The 95% confidence interval for the mean difference is (0.00123, 0.02397), which does not include 0, confirming the result. If the t-statistic had been below the critical value, the team would conclude that calibration produced no detectable change and would investigate measurement system adequacy further.

### F-Test for Equality of Two Variances

The F-test compares the variances of two independent normal populations.

Test statistic:

$$
F = \frac{s_1^2}{s_2^2}
$$

Where the larger sample variance is usually placed in the numerator to obtain a right-tailed test. Degrees of freedom for numerator = $n_1 - 1$, for denominator = $ n_2 - 1$.

Null hypothesis: $\sigma_1^2 = \sigma_2^2$ (or $\sigma_1^2 \le \sigma_2^2$ for a one-tailed test of improvement).

### Example 11: Pickle Crispness After Aging

A pickle factory wants to know whether aging for one month improves consistency (reduces variance). Assume a 95% confidence level.

Initial: $n_1 = 8$, $ s_1 = 1800$  
After one month: $n_2 = 6$, $ s_2 = 600$

The concern is improvement, so a one-tailed test with $H_0: \sigma_1^2 \le \sigma_2^2$ versus $ H_a: \sigma_1^2 > \sigma_2^2$.

$$
F = \frac{1800^2}{600^2} = \frac{3,240,000}{360,000} = 9
$$

Numerator df = 7, denominator df = 5. From the F-table, the critical value $F_{0.05,7,5} = 4.88$. Since $9 > 4.88$, reject $H_0$.

There is evidence that the variance has decreased, meaning crispness is more consistent after aging one month.

If the computed F had fallen below the critical value, the factory would conclude that aging did not improve consistency and might test a different aging duration.

## Single-Factor Analysis of Variance (One-Way ANOVA)

One-way ANOVA tests whether the means of several populations are all equal. The method assumes normally distributed populations, independent samples, and equal population variances. The test partitions total variation (SST) into variation between treatments (SSB) and variation within treatments (SSW).

### ANOVA Calculation Procedure

Collect data from $k$ treatments, each with $ n$ observations (balanced design). Let $ N = k \times n $, $ T$ be the grand total, $ T_i$ be the sum of observations in treatment $ i $, $ y_{ij}$ the individual measurements.

Correction factor:

$$
C = \frac{T^2}{N}
$$

Sum of squares total:

$$
SST = \sum y_{ij}^2 - C
$$

Sum of squares between treatments:

$$
SSB = \sum \frac{T_i^2}{n} - C
$$

Sum of squares within treatments:

$$
SSW = SST - SSB
$$

Degrees of freedom: between = $k-1$, within = $ N - k $, total = $ N - 1$.

Mean squares: $MSB = SSB/(k-1)$, $ MSW = SSW/(N-k)$.

F-statistic:

$$
F = \frac{MSB}{MSW}
$$

Reject $H_0: \mu_1 = \mu_2 = \dots = \mu_k$ (all means equal) if $ F$ exceeds the critical value $ F_{\alpha, k-1, N-k}$. This is a right-tailed test.

### Example 12: Effect of Temperature on Moisture Content

A polyurethane casting process can be run at 200°F, 220°F, or 240°F. Four batches were run at each temperature, for a total of 12 runs in random order. The moisture content (percent H₂O) is recorded.

Data table (each column a temperature):

| 240°F | 220°F | 200°F |
|-------|-------|-------|
| 10.8  | 11.4  | 14.3  |
| 10.4  | 11.9  | 12.6  |
| 11.2  | 11.6  | 13.0  |
| 9.9   | 12.0  | 14.2  |

Column totals: $T_{240} = 42.3$, $ T_{220} = 46.9$, $ T_{200} = 54.1$. Grand total $ T = 42.3 + 46.9 + 54.1 = 143.3$.

$N = 12$, $ n = 4$, $ k = 3$.

Sum of squared observations:

$$
\sum y_{ij}^2 = 10.8^2 + 10.4^2 + 11.2^2 + 9.9^2 + 11.4^2 + 11.9^2 + 11.6^2 + 12.0^2 + 14.3^2 + 12.6^2 + 13.0^2 + 14.2^2 = 1732.27
$$

Correction factor:

$$
C = \frac{143.3^2}{12} = \frac{20534.89}{12} = 1711.24
$$

SST:

$$
SST = 1732.27 - 1711.24 = 21.03
$$

SSB:

$$
SSB = \frac{42.3^2}{4} + \frac{46.9^2}{4} + \frac{54.1^2}{4} - 1711.24 = \frac{1789.29}{4} + \frac{2199.61}{4} + \frac{2926.81}{4} - 1711.24 = 447.3225 + 549.9025 + 731.7025 - 1711.24 = 1728.9275 - 1711.24 = 17.6875 \approx 17.69
$$

SSW:

$$
SSW = 21.03 - 17.69 = 3.34
$$

Degrees of freedom: between = 2, within = 9, total = 11.

Mean squares:

$$
MSB = 17.69 / 2 = 8.845, \quad MSW = 3.34 / 9 = 0.3711
$$

F-statistic:

$$
F = \frac{8.845}{0.3711} \approx 23.84 \text{ (handbook reports 23.92 with slightly different rounding, or 23.81 in Minitab)}
$$

Critical value from F-table: $F_{0.05,2,9} = 4.26$. Since the computed F far exceeds the critical value, reject $ H_0$. At the 0.05 significance level, temperature does affect moisture content. The Minitab output yields a p-value of 0.000.

If the F-statistic had been below the critical value, the conclusion would be that there is no evidence of a temperature effect, and the team would search for other factors.

The CSSGB Handbook also demonstrates the use of Excel’s `FINV(probability, deg_freedom1, deg_freedom2)` to obtain critical F-values and the Data Analysis Toolpak to perform one-way ANOVA directly.

## Chi-Square Goodness-of-Fit Test

The chi-square goodness-of-fit test determines whether an observed frequency distribution matches a hypothesized (expected) distribution.

Conditions: all expected frequencies must be at least 1, and no more than 20% may be less than 5.

Test statistic:

$$
\chi^2 = \sum \frac{(O - E)^2}{E}
$$

Where  
- $O$ = observed frequency in each category  
- $E$ = expected frequency (calculated from the hypothesized proportions)

Degrees of freedom = $k - 1$, with $ k$ = number of categories. The test is always right-tailed.

### Example 13: Defect Type Distribution

Historical distribution of four defect types:

| Defect Type      | Proportion |
|------------------|------------|
| Paint run        | 0.16       |
| Paint blister    | 0.28       |
| Decal crooked    | 0.42       |
| Door cracked     | 0.14       |

A random week’s sample of 208 rejected parts yields:

Observed: Paint run 27, Paint blister 60, Decal crooked 100, Door cracked 21.

Total = 27+60+100+21 = 208.

Compute expected frequencies by multiplying each proportion by 208:

- Paint run: $0.16 \times 208 = 33.28$
- Paint blister: $0.28 \times 208 = 58.24$
- Decal crooked: $0.42 \times 208 = 87.36$
- Door cracked: $0.14 \times 208 = 29.12$

Now compute the chi-square sum:

$$
\chi^2 = \frac{(27-33.28)^2}{33.28} + \frac{(60-58.24)^2}{58.24} + \frac{(100-87.36)^2}{87.36} + \frac{(21-29.12)^2}{29.12}
$$

- Paint run: $\frac{(-6.28)^2}{33.28} = \frac{39.4384}{33.28} = 1.185$
- Paint blister: $\frac{(1.76)^2}{58.24} = \frac{3.0976}{58.24} = 0.053$
- Decal crooked: $\frac{(12.64)^2}{87.36} = \frac{159.7696}{87.36} = 1.829$
- Door cracked: $\frac{(-8.12)^2}{29.12} = \frac{65.9344}{29.12} = 2.264$

Total $\chi^2 = 1.185 + 0.053 + 1.829 + 2.264 = 5.331$

Degrees of freedom = $4 - 1 = 3$. For α = 0.05, the critical value from the chi-square table is 7.815.

Since $5.331 < 7.815$, do not reject $ H_0$. The data do not indicate a change in the defect distribution. The Minitab analysis confirms a p-value of 0.149.

If the test statistic had exceeded 7.815, the conclusion would be that the distribution has shifted, prompting a root-cause analysis of the defect categories that contributed most to the discrepancy.

## Parametric and Nonparametric Tests

The CSSGB Handbook distinguishes between parametric and nonparametric tests. A parametric test assumes the data follow a specific distribution, most commonly the normal distribution. All the previous tests (z, t, chi-square for variance, F, ANOVA) are parametric.

A nonparametric test makes no assumption about the population distribution. These distribution-free methods are useful when data are only ranks or when the normality assumption is untenable. The handbook mentions three powerful nonparametric techniques that are outside the Green Belt BoK: Kendall coefficient of concordance, Spearman rank correlation coefficient, and Kruskal-Wallis one-way analysis of variance. Understanding that nonparametric alternatives exist is important for a Green Belt when data do not meet parametric assumptions.

## Exam Tips

- For a confidence interval on the mean with known σ, the margin of error halves when sample size quadruples because of the $\sqrt{n}$ denominator. This relationship is often tested.
- When the sample size is small and σ unknown, a t-distribution must be used. Know when to apply a pooled variance t-test versus a paired t-test based on the structure of the data (independent groups versus matched pairs).
- In a chi-square goodness-of-fit test, always check that all expected frequencies are at least 1 and that fewer than 20% are below 5; failure to meet these conditions invalidates the approximation.
- The F-statistic in ANOVA is the ratio of between-treatment variability to within-treatment variability. A larger F indicates that the treatment effect dominates the random error, leading to rejection of equal means.
- When testing a proportion with a very small expected count (np₀ < 5), the normal approximation is not valid; be prepared to identify scenarios where the binomial distribution should be used directly.
- The paired t-test is always a two-tailed test by default in the CSSGB context, but the hypotheses can be directional if the problem specifies one-sided improvement; always verify the alternative hypothesis stated in the exam question.