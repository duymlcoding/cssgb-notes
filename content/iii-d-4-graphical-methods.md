---
title: "Graphical Methods for Data Analysis"
description: "Detailed study notes on graphical methods (stem-and-leaf, box plots, run charts, scatter diagrams, normal probability plots, Weibull plots, Pareto charts) for the ASQ CSSGB exam, grounded exclusively in the official reference books."
---

## Stem-and-Leaf Plot

A stem-and-leaf plot presents numerical data in a way that preserves individual values while showing the shape of the distribution. It acts like a tally column where the last digit of each observation replaces the tally mark. This plot is especially helpful when data are grouped and you need to see both the overall pattern and the exact data points.

**Construction Procedure**

1. Determine the leaf unit: the place value of the last digit you will use as the leaf. For example, if data range from 9.7 to 12.3, set the leaf unit to 0.1 so that the leaf digit is the tenths place.
2. Split each observation into a stem (all digits to the left of the leaf unit) and a leaf (the digit at the leaf unit). With a leaf unit of 0.1, the value 10.3 has stem 10 and leaf 3, and 9.7 has stem 9 and leaf 7.
3. List stems in ascending order from top to bottom.
4. For each observation, write its leaf digit on the same row as its stem.
5. Sort the leaves within each stem row in increasing order.
6. To show cumulative counts, add a left column. Count observations from the top down until you reach the row that contains the median; enclose that row’s count in parentheses. Rows above show cumulative totals from the top; rows below show cumulative totals from the bottom.

**Example**

Weights (grams) of a batch of mixed chemical products:

```
10.3, 11.4, 10.9, 9.7, 10.4, 10.6, 10.0, 10.8, 11.1, 11.9,
10.9, 10.8, 11.7, 12.3, 10.6, 12.2, 11.6, 11.2, 10.7, 11.4
```

Sorted data:

```
9.7
10.0, 10.3, 10.4, 10.6, 10.6, 10.7, 10.8, 10.8, 10.9, 10.9
11.1, 11.2, 11.4, 11.4, 11.6, 11.7, 11.9
12.2, 12.3
```

With leaf unit = 0.1, the stems are 9, 10, 11, 12. Leaves are the tenths digits.

| Count | Stem | Leaves |
|-------|------|--------|
| 1     | 9    | 7      |
| 4     | 10   | 0 3 4 |
| (7)   | 10   | 6 6 7 8 8 9 9 |
| 9     | 11   | 1 2 4 4 |
| 5     | 11   | 6 7 9 |
| 2     | 12   | 2 3 |

The median is 10.9, so the row with stem 10 and leaves `6 6 7 8 8 9 9` receives the parentheses.

**Interpretation**

- The distribution shape is visible. Unusual concentrations or gaps may indicate measurement problems or special causes.
- You can read specific values directly: stem 11, leaf 4 corresponds to 11.4.
- The median is quickly found from the ordered leaves.

## Box Plot (Box-and-Whisker Plot)

The box plot provides a pictorial summary of minimum, first quartile (Q1), median (Q2), third quartile (Q3), and maximum. It displays the interquartile range (IQR) and flags potential outliers.

**Components of a Box Plot**

- **Bottom of the box**: Q1, the 25th percentile. 25% of data values are ≤ Q1.
- **Top of the box**: Q3, the 75th percentile. 75% of data values are ≤ Q3.
- **Line inside the box**: Q2, the median. 50% of data values are ≤ the median.
- **Interquartile range**: IQR = Q3 – Q1.
- **Upper whisker**: Extends to the largest data value within the upper limit. Upper limit = Q3 + 1.5 × IQR.
- **Lower whisker**: Extends to the smallest data value within the lower limit. Lower limit = Q1 – 1.5 × IQR.
- **Outliers**: Any data point beyond the whiskers, plotted as individual markers (often asterisks or dots).

**Constructing a Box Plot from Pull Test Data**

Data: 8.250, 8.085, 8.795, 9.565, 11.880, 9.180, 9.950, 9.630, 8.150.

Sort: 8.085, 8.150, 8.250, 8.795, 9.180, 9.565, 9.630, 9.950, 11.880.

From the source, the quartiles are:

- Q1 = 8.20
- Q2 (median) = 9.18
- Q3 = 9.79

Compute IQR = 9.79 – 8.20 = 1.59.

Upper limit = 9.79 + 1.5 × 1.59 = 9.79 + 2.385 = 12.175.
Lower limit = 8.20 – 1.5 × 1.59 = 8.20 – 2.385 = 5.815.

All data points (min = 8.085, max = 11.880) lie within these limits, so there are no outliers. Whiskers extend to 8.085 and 11.880.

**Interpretation**

- The median sits at 9.18, roughly centred between Q1 and Q3, suggesting approximate symmetry.
- Unequal whiskers or a median shifted toward one end of the box indicates skewness. If the median is near the centre, the data may follow a normal distribution.
- Outliers, when present, appear as individual points beyond the whiskers; they should be investigated for possible special causes.

**Comparing Groups**

Box plots can compare multiple populations visually. The source gives an example with three process periods. Period 2 shows the largest spread; a Green Belt would probe what differed in that period’s settings (gas flow, temperature) to explain the increased variation.

## Run Chart

A run chart plots individual observations in time sequence with a horizontal reference line at the median. It detects nonrandom patterns that suggest special-cause variation.

**Run Chart Tests and Interpretation**

Statistical software calculates p-values for several patterns. A p-value less than 0.05 indicates a statistically significant nonrandom pattern.

- **Clustering**: Points group tightly in time. May signal measurement issues or lot-to-lot variation.
- **Mixtures**: Points alternate frequently between two extremes. May arise from mixing outputs from different machines or operators.
- **Trends**: A sustained upward or downward movement. Often caused by tool wear, gradual temperature drift, or operator fatigue.
- **Oscillation**: Points bounce above and below the median in a regular fashion, suggesting lack of process steadiness.

**Example from Bond Strength Run Chart**

The source presents a run chart of bond average strength with 120 observations. Software output:

- Number of runs about median: 45
- Expected number of runs: 62.5
- Approx p-value for clustering: 0.00141
- Approx p-value for mixtures: 0.99859
- Approx p-value for trends: 0.21478
- Approx p-value for oscillation: 0.78522

Interpretation: Clustering is highly significant (p = 0.0014), pointing to possible measurement problems or setup-to-setup variability. Trends and oscillation are not significant (p > 0.05).

Run charts differ from control charts: they lack statistical control limits and use only a median line. They are best when subgroup size is one and real-time feedback is needed.

## Scatter Diagram and Correlation

A scatter diagram plots two variables against one another to reveal possible relationships. The independent variable (potential cause) goes on the horizontal axis; the dependent variable (effect) goes on the vertical axis.

### Correlation Coefficient (Pearson r)

The strength and direction of a linear relationship is quantified by the Pearson correlation coefficient r, which always satisfies –1 ≤ r ≤ 1.

**Formulas**

Let \(n\) be the number of data pairs \((x_i, y_i)\).

\[
S_{xx} = \sum x_i^2 - \frac{\left(\sum x_i\right)^2}{n}
\]

\[
S_{xy} = \sum x_i y_i - \frac{\left(\sum x_i\right)\left(\sum y_i\right)}{n}
\]

\[
S_{yy} = \sum y_i^2 - \frac{\left(\sum y_i\right)^2}{n}
\]

\[
r = \frac{S_{xy}}{\sqrt{S_{xx} \; S_{yy}}}
\]

**Interpretation of r**

- r > 0: positive association (upward slope).
- r < 0: negative association (downward slope).
- r ≈ 0: no linear correlation.
- The closer |r| is to 1, the stronger the linear association.

**Coefficient of Determination**

\[
r^2 = r^2
\]

\(r^2\) indicates the proportion of variability in y that can be explained by the linear relationship with x.

### Example 1: Exercise Time and Weight Loss

Data:

| Minutes/day (x) | Weight loss in pounds (y) |
|-----------------|---------------------------|
| 30              | 1.0                       |
| 45              | 2.0                       |
| 60              | 4.0                       |
| 75              | 4.5                       |

n = 4.

Compute sums:

\[
\sum x = 210,\quad \sum y = 11.5
\]
\[
\sum x^2 = 900 + 2025 + 3600 + 5625 = 12,150
\]
\[
\sum y^2 = 1 + 4 + 16 + 20.25 = 41.25
\]
\[
\sum xy = 30 \times 1 + 45 \times 2 + 60 \times 4 + 75 \times 4.5 = 697.5
\]

Calculate:

\[
S_{xx} = 12,150 - \frac{210^2}{4} = 12,150 - 11,025 = 1,125
\]
\[
S_{xy} = 697.5 - \frac{210 \times 11.5}{4} = 697.5 - 603.75 = 93.75
\]
\[
S_{yy} = 41.25 - \frac{11.5^2}{4} = 41.25 - 33.0625 = 8.1875
\]

\[
r = \frac{93.75}{\sqrt{1125 \times 8.1875}} = \frac{93.75}{\sqrt{9210.9375}} \approx \frac{93.75}{95.97} \approx 0.9768 \approx 0.977
\]

\[
r^2 \approx 0.954
\]

Thus, 95.4% of the variability in weight loss is explained by exercise time. The strong positive correlation suggests that increasing exercise time is associated with greater weight loss.

If r had been close to zero, the practitioner would look for other factors (diet, metabolism) instead of focusing on exercise time.

### Example 2: Mold Compression Pressure and Part Surface Finish

From the injection-molding data (Table 13.5), take Mold Compression Pressure (x) and Part Surface Finish (y) for the 10 batches.

x: 242, 220, 451, 385, 539, 396, 407, 363, 308, 440  
y: 40.70, 33.00, 44.00, 35.20, 29.70, 38.50, 47.30, 25.30, 35.20, 33.00

n = 10.

\[
\sum x = 3751,\quad \sum y = 361.9
\]
\[
\sum x^2 = 1,491,809
\]
\[
\sum y^2 = 13,490.29
\]
\[
\sum xy = 135,556.3
\]

\[
S_{xx} = 1,491,809 - \frac{3751^2}{10} = 1,491,809 - 1,407,000.1 = 84,808.9
\]
\[
S_{xy} = 135,556.3 - \frac{3751 \times 361.9}{10} = 135,556.3 - 135,748.69 = -192.39
\]
\[
S_{yy} = 13,490.29 - \frac{361.9^2}{10} = 13,490.29 - 13,097.161 = 393.129
\]

\[
r = \frac{-192.39}{\sqrt{84,808.9 \times 393.129}} \approx -0.033
\]

The correlation is effectively zero. There is no linear relationship between mold compression pressure and surface finish in this data. If the result had been strongly negative (for example, r ≈ –0.9), the team would target mold pressure as a root cause for improving surface finish. Since r ≈ –0.033, the team should investigate other variables (coolant temperature, cooling time, hold time) that show stronger correlations.

## Normal Probability Plot

A normal probability plot assesses whether a data set comes from a normal distribution. Several statistical methods assume normality, so this check is critical before proceeding with analyses such as t-tests or ANOVA.

**Construction and Interpretation**

- Data are plotted against the expected values of a normal distribution.
- If the points form an approximately straight line, the data are consistent with a normal distribution.
- Statistical software typically uses the Anderson-Darling (AD) test. Smaller AD values indicate a better fit.
- The associated p-value: if p > 0.05 (common alpha risk), we do not reject the null hypothesis that the data are normal.

**Example: Bond Strength of Assembly Units**

Sample of 19 bond strength measurements: 8.250, 8.085, 8.795, 9.565, 11.880, 9.180, 9.950, 9.630, 8.150, 10.800, 10.800, 11.080, 10.730, 10.520, 10.380, 10.535, 9.600, 10.340, 10.410.

Minitab output:

- Mean = 9.931, StDev = 1.059
- AD = 0.471
- p-value = 0.217

Since p > 0.05, we conclude the data follow a normal distribution. The plot also shows that roughly 20% of parts fall below the lower specification limit of 9 and about 17% exceed the upper limit of 11, illustrating how the normal probability plot can relate directly to capability.

## Weibull Plot

The Weibull distribution is widely used for reliability analysis when the underlying failure distribution is unknown. Its probability density function is:

\[
P(x) = a\, b\, (x - g)^{\,b-1}\, e^{-a\,(x - g)^{\,b}}
\]

where

- \(a\) = scale parameter
- \(b\) = shape parameter
- \(g\) = location parameter

**Shape Parameter and Life Cycle**

- \(b < 1\): failure rate decreases with time (infant mortality / early life failures).
- \(b = 1\): failure rate is constant (useful life / random failures).
- \(b > 1\): failure rate increases with time (wear-out failures).

**Estimating MTBF and Reliability**

Weibull probability paper plots percent failure against time. The mean time between failures (MTBF) is not the 50th percentile; for the Weibull distribution, MTBF corresponds to the 63.2 percentile on the failure scale (or 36.8 percentile on the reliability scale). To obtain MTBF, draw a horizontal line at 63.2% failure and drop a vertical line to the time axis where it intersects the fitted line.

**Example: Unit Failure Test**

Fifteen units were tested until failure. Failure durations (hours):
4.011, 3.646, 5.226, 4.740, 4.739, 5.833, 4.861, 4.618, 4.012, 3.646, 4.497, 3.646, 4.49, 3.281, 3.889.

Minitab’s Weibull analysis yields:

- Shape parameter b = 6.734
- Scale parameter a = 4.636
- AD p-value > 0.25, indicating a good fit to the Weibull distribution.

From the plot, the 63.2% line intersects the best-fit line at approximately 4.635 hours, so MTBF ≈ 4.635 hours.
To estimate reliability at 3.9 hours: draw a vertical line at 3.9 hours; it crosses the fitted line at about 30% on the percent failure scale. Thus reliability \(R(3.9) \approx 0.70\), meaning about 70% of units survive beyond 3.9 hours.

With b = 6.734 (much greater than 1), the units are failing in the wear-out region, indicating that age-related deterioration is dominant.

## Pareto Chart

A Pareto chart is a bar graph that displays causes or categories in descending order of frequency, overlaid with a cumulative percentage line. It implements the 80/20 rule: roughly 20% of the causes account for 80% of the effect. This chart helps teams focus on the vital few issues.

**Construction and Drill-Down**

1. Collect categorical data (for example, reasons for claims denials).
2. Order categories from highest frequency to lowest.
3. Plot bars for each category and a line for cumulative percent.
4. Concentrate improvement efforts on the categories that make up the bulk of the cumulative percentage.
5. Drill down: for a top category, collect more detailed data and produce a new Pareto chart. For instance, from a “timely filing” denial category, gather data by payer to see which payers contribute most to the problem.

**Example from Medical Claims Denials**

First-level Pareto shows “duplicate claim” and “timely filing” as the top two denial reasons. Drilling into timely filing by payer reveals that payers A and B cause the majority of those denials. The team then investigates whether these payers have shorter filing deadlines or whether staff are unaware of their requirements.

## Exam Tips

- Given a small dataset, construct a box plot: compute Q1, Q2, Q3, IQR, and identify outliers using the 1.5×IQR rule. Interpret skewness and potential normality.
- From a set of paired numeric observations, calculate the Pearson correlation coefficient r using the sums-based formulas, then compute r² and decide if the relationship is strong enough to pursue as a root cause.
- Interpret run chart p-values for clustering, mixtures, trends, and oscillation. A p-value below 0.05 signals a significant nonrandom pattern that requires investigation.
- Use a Weibull plot to estimate MTBF at the 63.2 percentile and determine whether failures fall in the infant mortality, random, or wear-out period based on the shape parameter b.
- Read a stem-and-leaf plot to extract the median and spot data concentrations that may indicate measurement error or process anomalies.
- Apply a Pareto chart with drill-down: identify the top categories and re-stratify data to pinpoint the specific sources contributing most of the effect.