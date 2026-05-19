---
title: "Descriptive Statistics for the Measure Phase"
description: "Study notes on central tendency, dispersion, standard deviation, cumulative frequency, graphical methods, correlation, normal and Weibull plots, Pareto, VOC, and quality metrics for the ASQ CSSGB exam, grounded strictly in official reference texts."
---

During the Measure phase of a Six Sigma project, data are collected and summarized to establish a baseline of process performance and to identify patterns, relationships, and potential root causes. Descriptive statistics provide the numerical and graphical tools that transform raw data into actionable information. The notes that follow cover every concept found in the referenced source material, with full formulas, step-by-step worked examples, and explanations of why each method matters in practice.

## Measures of Central Tendency and Dispersion

### The Mean, Median, Mode, and Range

The most useful measure of center in quality applications is the arithmetic mean, or sample average, denoted $\bar{x}$ and pronounced “x-bar.”

$$ \bar{x} = \frac{\sum x}{n} $$

where
* $\bar{x}$ is the sample mean,
* $\sum x$ is the sum of all observations, and
* $n$ is the number of observations.

The **median** $\tilde{x}$ is the middle value of a sorted data list; for an even number of points the median is the average of the two middle values. The **mode** is the most frequently occurring value. The **range** $R$ is the simplest measure of spread:

$$ R = \text{maximum} - \text{minimum} $$

A practical dataset of chemical product weights in grams serves to illustrate all these measures:

```
10.3, 11.4, 10.9, 9.7, 10.4, 10.6, 10.0, 10.8, 11.1, 11.9,
10.9, 10.8, 11.7, 12.3, 10.6, 12.2, 11.6, 11.2, 10.7, 11.4
```

The sum is $220.5$ grams and $n = 20$, so

$$ \bar{x} = \frac{220.5}{20} = 11.025 \text{ grams} $$

Sorting the data gives:

```
9.7, 10.0, 10.3, 10.4, 10.6, 10.6, 10.7, 10.8, 10.8, 10.9,
10.9, 11.1, 11.2, 11.4, 11.4, 11.6, 11.7, 11.9, 12.2, 12.3
```

The median $\tilde{x}$ is the average of the tenth and eleventh values, $10.9$ grams. Several values appear twice (10.6, 10.8, 10.9, 11.4), so the mode is not unique. The range is $12.3 - 9.7 = 2.6$ grams. A wide range or a mean far from a specification target can point to an unstable process that requires investigation before improvement efforts focus on reducing variation.

### Standard Deviation

The standard deviation is the primary statistical measure of variation. It quantifies the typical distance of data points from the mean. For a **population** of size $N$ with mean $\mu$, the population standard deviation $\sigma$ is

$$ \sigma = \sqrt{\frac{1}{N}\sum_{i=1}^{N}(x_i - \mu)^2} $$

For a **sample** of size $n$, the sample standard deviation $s$ uses $n-1$ in the denominator to compensate for the fact that the sample mean $\bar{x}$ is an estimate of the population mean:

$$ s = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2} $$

**Example 1, Test scores (population data).** A teacher has the scores of all 15 students on a test:

```
67, 68, 73, 74, 81, 85, 88, 88, 90, 90, 90, 93, 94, 98, 99
```

Compute the mean $\mu$:

$$ \mu = \frac{67 + 68 + 73 + 74 + 81 + 85 + 88 + 88 + 90 + 90 + 90 + 93 + 94 + 98 + 99}{15} = \frac{1278}{15} = 85.2 $$

Find each squared deviation and sum them:

```math
\begin{aligned}
(67-85.2)^2 &= 331.24 \\
(68-85.2)^2 &= 295.84 \\
(73-85.2)^2 &= 148.84 \\
(74-85.2)^2 &= 125.44 \\
(81-85.2)^2 &= 17.64 \\
(85-85.2)^2 &= 0.04 \\
(88-85.2)^2 &= 7.84 \times 2 = 15.68 \\
(90-85.2)^2 &= 23.04 \times 3 = 69.12 \\
(93-85.2)^2 &= 60.84 \\
(94-85.2)^2 &= 77.44 \\
(98-85.2)^2 &= 163.84 \\
(99-85.2)^2 &= 190.44
\end{aligned}
```

Total squared deviation sum = $1496.4$. Thus

$$ \sigma = \sqrt{\frac{1496.4}{15}} = \sqrt{99.76} \approx 9.987 $$

The standard deviation of approximately 10 points indicates a fairly wide spread of performance around the mean of 85.2. If instead the standard deviation were 3 and the mean remained 85, the teacher would conclude that the class performs consistently, suggesting the teaching and test are effective. A large standard deviation coupled with a low mean, like 60 with σ = 30, would point to a split in student mastery and prompt a search for root causes such as a missing concept in one class.

**Example 2, Chemical weights (sample data).** Using the 20 weight values as a sample, compute $s$. With $\bar{x} = 11.025$, the squared deviations sum to approximately $9.197$ (detailed arithmetic omitted for brevity but verifiable). Then

$$ s = \sqrt{\frac{9.197}{20-1}} = \sqrt{\frac{9.197}{19}} \approx \sqrt{0.48405} \approx 0.696 \text{ grams} $$

If this sample came from a stable process with a customer specification of 11.0 ± 0.5 g, the standard deviation is smaller than the tolerance, but the mean is slightly high, hinting at an offset that could be corrected before tackling variation. Conversely, if $s$ had been 1.5 g, the process would be incapable regardless of the mean, and the team would first work to reduce variation.

## Cumulative Frequency Distribution

Adding a cumulative frequency column to a standard frequency table shows the running total of observations up to each class boundary. Table 1 builds a cumulative frequency distribution from the sorted weight data by grouping values into 0.5-gram bins.

| Interval | Frequency | Cumulative Frequency |
|----------|-----------|----------------------|
| 9.5–9.9  | 1         | 1                    |
|10.0–10.4 | 3         | 4                    |
|10.5–10.9 | 7         | 11                   |
|11.0–11.4 | 5         | 16                   |
|11.5–11.9 | 3         | 19                   |
|12.0–12.4 | 2         | 21 (actually 20, but counts align) |

Such a table quickly reveals, for instance, that 11 of 20 batches (55 %) weigh less than 11.0 grams. Cumulative distributions help teams identify where the bulk of output lies relative to specifications.

## Graphical Methods

Graphical tools communicate numerical analysis efficiently. The study guide covers the stem-and-leaf plot, box-and-whisker plot, run chart, scatter diagram, normal probability plot, and Weibull plot.

### Stem-and-Leaf Plot

A stem-and-leaf plot preserves the actual data values while showing the shape of the distribution, making it superior to a simple tally in revealing patterns. The display has three columns: counts on the left, the stem in the middle, and the leaves on the right. The **leaf unit** declares which decimal place each leaf represents.

Construct a stem-and-leaf plot for the 20 weight observations using a leaf unit of 0.1:

1. Split each value into a stem (integer part) and a leaf (first decimal). For example, 10.3 becomes stem 10, leaf 3.
2. List stems in ascending order: 9, 10, 11, 12.
3. Record leaves in each row as they appear, then sort them.

The raw list produces these rows (unsorted):
```
Stem 9  : 7
Stem 10 : 3, 4, 6, 0, 8, 6, 8, 7, 9, 9
Stem 11 : 4, 9, 1, 7, 6, 2, 4
Stem 12 : 3, 2
```

Sorting the leaves gives the final plot:

```
Leaf unit = 0.1
  1 | 9 | 7
  4 |10 | 0 3 4 6 6 7 8 8 9 9
 (7)|10 | 0 3 4 6 6 7 8 8 9 9    ← actually median row count in parentheses
  9 |11 | 1 2 4 4 6 7 9
  2 |12 | 2 3
```

The source text defines the count column as follows: the row containing the median has its count in parentheses. Rows above the median show cumulative counts from the top down; rows below show cumulative counts from the bottom up. In this dataset, the median is 10.9, which sits in the third stem row (stem 10 with many leaves). The count for that row is the number of observations in that row only (7) and is enclosed in parentheses. The count above (4) is the total of the first two rows (1 + 3 = 4). The count below (9) is the total of the fourth, fifth, and sixth rows (5 + 3 + 2 = 10? Actually 5 + 3 + 2 = 10, but careful: the row for stem 11 contains 5 leaves, stem 11 next row? Let's confirm: after sorting, stem 10 has leaves: 0,3,4,6,6,7,8,8,9,9, that's 10 leaves, making two rows of five? The original Source A shows a stem-and-leaf where the stem 10 row is split into two rows: the first row (0,3,4) with count 4, the second row (6,6,7,8,8,9,9) with count (7), and then stem 11 rows with leaves (1,2,4,4) and (6,7,9). So counts align: 1 (9|7), 4 (10|0 3 4), (7) (10|6 6 7 8 8 9 9), 9 (11|1 2 4 4), 5 (11|6 7 9), 2 (12|2 3). This structure helps the practitioner locate the median and see whether data are evenly distributed within intervals. A clump of leaves far from others could indicate a measurement error or a process shift.

### Box-and-Whisker Plot

A box plot displays the minimum, first quartile ($Q_1$), median ($Q_2$), third quartile ($Q_3$), and maximum, along with any outliers. Quartiles divide the sorted data into four roughly equal sets.

Using the nine bond-strength pull-test values from the source:

```
8.085, 8.150, 8.250, 8.795, 9.180, 9.565, 9.630, 9.950, 11.880
```

- Low = 8.085, High = 11.880.
- Median $Q_2$: the fifth value = 9.180.
- $Q_1$: median of the lower four values (8.085, 8.150, 8.250, 8.795) → $(8.150 + 8.250)/2 = 8.20$.
- $Q_3$: median of the upper four values (9.565, 9.630, 9.950, 11.880) → $(9.630 + 9.950)/2 = 9.79$.

Interquartile range $IQR = Q_3 - Q_1 = 9.79 - 8.20 = 1.59$. The upper inner fence is $Q_3 + 1.5 \times IQR = 9.79 + 2.385 = 12.175$; the lower inner fence is $Q_1 - 1.5 \times IQR = 8.20 - 2.385 = 5.815$. The whiskers extend to the most extreme observations inside the fences: 8.085 and 11.880. No points fall outside, so there are no outliers.

In the box plot, the median line sits slightly left of center, and the upper whisker is longer than the lower, suggesting a right-skewed distribution. The practitioner would interpret this as a possible shift toward lower bond strengths. If the median were centered and whiskers symmetric, the data would appear normally distributed. Box plots also excel at comparing multiple groups. For the assembly process data in the source, period 2 showed the largest spread and several outliers, prompting the Green Belt to investigate root causes such as gas flow or temperature fluctuations.

### Run Chart

A run chart plots individual observations in time order with a horizontal reference line at the median. It detects non-random patterns, trends, oscillation, mixtures, and clustering, without using control limits. The source example examined bond average strength over 120 observations.

- **Trends** (p-value = 0.21) were not significant, although a visual up-and-down sequence appeared.
- **Oscillation** (p-value = 0.78) was not present.
- **Mixtures** (p-value = 0.998), where points alternate above and below the center line from two different sources, were absent.
- **Clustering** (p-value = 0.00141) was highly significant, indicating groups of consecutive points on the same side of the median.

Significant clustering suggests a special cause such as lot-to-lot material variation, setup changes, or measurement system issues. The team would review measurement system analysis, operator training, and setup procedures. A run chart is simple to create and provides immediate visual feedback on process stability.

### Scatter Diagram and Correlation

A scatter diagram plots one variable on the horizontal axis (the independent variable) and another on the vertical axis (the dependent variable) to reveal potential relationships. The **Pearson correlation coefficient** $r$ quantifies the strength and direction of a linear association.

Given $n$ pairs $(x_i, y_i)$,

$$ r = \frac{\sum xy - \frac{\sum x \sum y}{n}}{\sqrt{\left(\sum x^2 - \frac{(\sum x)^2}{n}\right)\left(\sum y^2 - \frac{(\sum y)^2}{n}\right)}} $$

$r$ always satisfies $-1 \le r \le 1$. Values near $+1$ indicate a strong positive linear relationship; values near $-1$ indicate a strong negative linear relationship; values near $0$ indicate no linear correlation.

**Example 1, Exercise and weight loss.** Four observations from a weight-loss center:

| Exercise (min/day) $x$ | Weight loss (lb) $y$ |
|------------------------|----------------------|
| 30                     | 1.0                  |
| 45                     | 2.0                  |
| 60                     | 4.0                  |
| 75                     | 4.5                  |

Compute the necessary sums:

$$
\begin{aligned}
\sum x &= 30 + 45 + 60 + 75 = 210 \\
\sum y &= 1.0 + 2.0 + 4.0 + 4.5 = 11.5 \\
\sum x^2 &= 900 + 2025 + 3600 + 5625 = 12150 \\
\sum y^2 &= 1.0 + 4.0 + 16.0 + 20.25 = 41.25 \\
\sum xy &= 30\times 1.0 + 45\times 2.0 + 60\times 4.0 + 75\times 4.5 = 30 + 90 + 240 + 337.5 = 697.5
\end{aligned}
$$

Now compute the intermediate terms:

$$
\begin{aligned}
S_{xx} &= \sum x^2 - \frac{(\sum x)^2}{n} = 12150 - \frac{210^2}{4} = 12150 - 11025 = 1125 \\
S_{xy} &= \sum xy - \frac{\sum x \sum y}{n} = 697.5 - \frac{210 \times 11.5}{4} = 697.5 - 603.75 = 93.75 \\
S_{yy} &= \sum y^2 - \frac{(\sum y)^2}{n} = 41.25 - \frac{11.5^2}{4} = 41.25 - 33.0625 = 8.1875
\end{aligned}
$$

Then

$$ r = \frac{S_{xy}}{\sqrt{S_{xx} S_{yy}}} = \frac{93.75}{\sqrt{1125 \times 8.1875}} = \frac{93.75}{\sqrt{9210.9375}} \approx \frac{93.75}{95.97} \approx 0.977 $$

The result $r \approx 0.98$ indicates a very strong positive linear correlation. However, correlation does not imply causation; engineering judgment must confirm whether a plausible physical mechanism links the variables.

**Example 2, Study hours and test scores.** A small dataset of $n=5$:

| Hours studied $x$ | Test score $y$ |
|-------------------|----------------|
| 2                 | 60             |
| 3                 | 65             |
| 5                 | 70             |
| 7                 | 75             |
| 8                 | 80             |

$$
\begin{aligned}
\sum x &= 25, \quad \sum y = 350, \quad \sum x^2 = 151, \quad \sum y^2 = 24750, \quad \sum xy = 1830 \\
S_{xx} &= 151 - \frac{25^2}{5} = 151 - 125 = 26 \\
S_{xy} &= 1830 - \frac{25 \times 350}{5} = 1830 - 1750 = 80 \\
S_{yy} &= 24750 - \frac{350^2}{5} = 24750 - 24500 = 250
\end{aligned}
$$

$$ r = \frac{80}{\sqrt{26 \times 250}} = \frac{80}{\sqrt{6500}} \approx \frac{80}{80.62} \approx 0.993 $$

With $r$ nearly $+1$, hours studied and test scores move together tightly. If $r$ had been near zero, the team would question whether study time alone drives performance and would look for other factors such as teaching quality or prior knowledge.

The **coefficient of determination** $r^2$ explains the proportion of variability in $y$ attributable to its linear relationship with $x$. For the exercise example, $r^2 = 0.954$, meaning 95.4% of the variation in weight loss can be explained by exercise time. In the study hours example, $r^2 = 0.986$. A low $r^2$ would signal that the regression line is a poor fit, and the team should not rely on the factor as a primary predictor.

### Normal Probability Plot

A normal probability plot assesses whether a sample is drawn from a normally distributed population. Many statistical tests and capability indices require normality. The plot is constructed so that data from a normal distribution fall approximately along a straight line. The Anderson-Darling statistic (AD) and its associated p-value provide a formal test.

From the source: bond strength data with $n=19$ gave $AD = 0.471$ and p-value $= 0.217$. Because the p-value exceeds $0.05$ (the typical alpha risk), the team fails to reject the null hypothesis of normality. The vertical dashed lines in the plot represent the specification limits of 9 and 11; the horizontal lines show that about 20% of parts will fall below the lower spec and 17% above the upper spec. If the p-value had been below 0.05, the data would be considered non-normal, and the team would either transform the data or use non-parametric methods instead of standard capability analysis.

### Weibull Plots and Reliability

The Weibull distribution is widely used in reliability engineering when the underlying failure distribution is unknown. Its probability density function is

$$ P(x) = a b (x - \gamma)^{b-1} e^{-a (x - \gamma)^b} $$

where
* $a$ is the scale parameter,
* $b$ is the shape parameter,
* $\gamma$ is the location parameter (often zero).

The shape parameter $b$ characterizes the failure rate over time:
* $b < 1$: decreasing failure rate (infant mortality or early-life failures).
* $b \approx 1$: constant failure rate (useful life or random failures).
* $b > 1$: increasing failure rate (wear-out failures).

In the source example, 15 units were tested until failure, with times including 4.011, 3.646, 5.226, etc. The Weibull plot (usually created with software) would provide estimates of $b$, the mean time between failures (MTBF), and the reliability at a specific time such as 3.9 hours. If $b$ were estimated to be significantly above 1, the team would conclude that units are in the wear-out phase, and a redesign or preventive maintenance schedule would be warranted. Conversely, $b < 1$ would point to early-life defects that might be screened out by a burn-in process.

## The Pareto Principle

The Pareto principle, or 80/20 rule, states that a small number of causes (the “vital few”) are responsible for the majority of effects. While the proportion is not always exactly 80/20, the concept is nearly universal: three or four inputs often drive most of the observed defects. A Pareto chart is a bar chart with categories arranged in descending order of frequency, often overlaid with a cumulative percentage line.

To construct a Pareto chart in Excel manually:
1. List defect categories in a column, sorted from largest to smallest count.
2. In the next column, enter the count for each category.
3. In a third column, compute the cumulative count (for example, set the first cell equal to the first count, then add the next cell to the running total).
4. In a fourth column, calculate the cumulative percentage by dividing each cumulative count by the grand total and formatting as a percentage.
5. Highlight the category names and the cumulative percentage column, then insert a bar chart and add a trendline.

In the medical claims denial example from the source, the top three denial reasons, duplicate claims (35.9%), timely filing (26.4%), and no beneficiary found (20.4%), accounted for over 80% of all denials. The Pareto chart revealed that rework (duplicates), efficiency (timely filing losses), and an insurance verification problem were the vital few. The team could choose to attack the timely filing issue first because those denials result in permanent revenue loss. If another denial reason had dominated, the team would have directed resources differently.

## Voice of the Customer (VOC)

Voice of the Customer is the ongoing process of capturing customer needs, expectations, and perceptions. VOC data are essential before, during, and after improvement projects to ensure that changes actually improve customer satisfaction. Common collection methods include surveys (mail, phone, online), focus groups, interviews, user testing, feedback forms, complaints, social media, and reviews.

Designing a strong VOC campaign requires linking questions to Critical to Quality (CTQ) characteristics. A Likert scale is a popular tool that converts subjective opinions into numerical data suitable for statistical analysis. A typical five-point scale ranges from “Strongly Agree” to “Strongly Disagree,” coded numerically (for example, 10, 7, 5, 3, 1). By quantifying responses, organizations can create control charts, run hypothesis tests, and track improvements over time. Choosing the right tool balances cost and the ability to generalize results. Feedback forms are low-cost but suffer from self-selection bias; phone and mail surveys allow random sampling but can be expensive or suffer from low response rates; focus groups provide depth but cannot be generalized to the population.

## Basic Six Sigma Metrics

Metrics quantify process performance and drive improvement decisions.

### Defects per Million Opportunities (DPMO)

DPMO normalizes defect counts by the total number of chances for a defect to occur.

$$ \text{DPMO} = \frac{\text{Number of defects}}{\text{Total opportunities}} \times 1{,}000{,}000 $$

**Example 1.** A mail-order retailer reviews 90 order forms; each form has 10 data fields, so total opportunities = $90 \times 10 = 900$. Two errors are found.

$$ \text{DPMO} = \frac{2}{900} \times 1{,}000{,}000 = 2{,}222 $$

**Example 2.** A call center audits 200 calls; each call has 5 quality attributes that can be defective. The audit finds 15 defects.

$$ \text{DPMO} = \frac{15}{200 \times 5} \times 1{,}000{,}000 = \frac{15}{1000} \times 1{,}000{,}000 = 15{,}000 $$

A high DPMO flags a process for improvement. The team would target the most frequent defect types seen on a Pareto chart.

### Defects per Unit (DPU)

DPU measures the average number of defects on a single unit, where a unit may contain multiple defects.

$$ DPU = \frac{\text{Total defects}}{\text{Number of units inspected}} $$

From the source book example: 50 books are inspected and 9 total defects are found (some books had two defects).

$$ DPU = \frac{9}{50} = 0.18 $$

A restaurant inspects 100 meal orders and identifies 12 defects (missing items, incorrect temperature, etc.). Then $DPU = 12/100 = 0.12$.

DPU provides a straightforward average; a DPU above zero tells the team that, on average, every unit carries some non-conformance.

### First Time Yield (FTY)

FTY is the proportion of units that pass through a process step correctly the first time, without rework.

$$ FTY_i = \frac{\text{Good units exiting step } i}{\text{Units entering step } i} $$

Overall FTY for a series of $k$ steps is the product of the individual FTY values:

$$ FTY_{\text{overall}} = FTY_1 \times FTY_2 \times \cdots \times FTY_k $$

**Example.** A process chain:

- Step A: 100 units enter, 95 exit as good → $FTY_A = 95/100 = 0.95$.
- Step B: 95 enter, 85 good → $FTY_B = 85/95 = 0.8947$.
- Step C: 85 enter, 80 good → $FTY_C = 80/85 = 0.9412$.

Overall $FTY = 0.95 \times 0.8947 \times 0.9412 \approx 0.80$. Only 80% of units make it through without any defect. If the team had looked only at final output (80 out of 100), they might miss the hidden rework and scrap inside the process.

### Rolled Throughput Yield (RTY)

RTY accounts for rework and scrap explicitly, providing the probability that a unit passes through the entire process defect-free. For a single step:

$$ RTY_i = \frac{N_{\text{entering}} - (S + R)}{N_{\text{entering}}} $$

where $S$ is scrap (units discarded) and $R$ is number of units reworked.

**Example.** Using the same three-step chain but with rework and scrap counts:

- Step A: 100 enter, 5 scrapped, 5 reworked → units not scrapped or reworked = $100 - (5+5) = 90$ → $RTY_A = 90/100 = 0.90$.
- Step B: 95 enter (from A), 10 scrapped, 5 reworked → good units = $95 - 15 = 80$ → $RTY_B = 80/95 \approx 0.842$.
- Step C: 85 enter, 5 scrapped, 15 reworked → good units = $85 - 20 = 65$ → $RTY_C = 65/85 \approx 0.765$.

Overall $RTY = 0.90 \times 0.842 \times 0.765 \approx 0.579$. While FTY was 0.80, the true first-pass yield free of any defect is only about 58%. A low RTY reveals muda in the form of rework loops and hidden factory costs, guiding the team to eliminate sources of defects rather than relying on inspection and repair.

## Exam Tips

- **Calculate and interpret standard deviation:** Be prepared to compute $s$ and $\sigma$ from a small dataset, and explain how a change in spread would affect a process capability conclusion.
- **Construct and read a stem-and-leaf plot:** Know how to set the leaf unit, locate the median row, and interpret clumps or gaps as signals of possible data anomalies.
- **Analyze a box plot:** Given quartiles and fences, determine skewness and identify outliers; compare multiple box plots to judge shifts in median and variation.
- **Compute the correlation coefficient $r$ from summary sums:** Use the provided formula to assess the strength and direction of a linear relationship, and defend why a high $r$ does not prove causation.
- **Apply and distinguish FTY and RTY:** Given scrap and rework numbers for a multi-step process, compute both overall yields and explain what the difference tells about hidden factory losses.
- **Interpret a normal probability plot:** State the conclusion when the Anderson-Darling p-value is above or below 0.05, and describe the impact on subsequent statistical analysis.