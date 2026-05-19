---
title: "Correlation and Linear Regression"
description: "Detailed study notes for the CSSGB exam covering scatter plots, correlation coefficient calculation, hypothesis tests for population correlation, simple linear regression estimation, confidence intervals for the mean response, and slope significance testing. All content drawn from the ASQ CSSGB Handbook, 2nd Edition, and the CSSC Training Manual."
---

## Scatter Plots and Visualizing Relationships

A scatter plot displays the relationship between two numerical variables by placing the independent variable $x$ on the horizontal axis and the dependent variable $ y$ on the vertical axis. Examining the plot reveals the direction, shape, and strength of any association. The convention in Six Sigma projects is to treat the potential cause (input) as $ x$ and the effect (output) as $ y $.

Four fundamental patterns can appear in a scatter plot:

- **Strong positive correlation**: As $x$ increases, $ y$ also tends to increase in a linear fashion. The points cluster tightly around an imaginary line with positive slope.
- **Strong negative correlation**: As $x$ increases, $ y$ tends to decrease linearly. Points are close to a line with negative slope.
- **No correlation**: No discernible linear pattern; the points form a random cloud.
- **Nonlinear relationship**: A clear pattern exists, but it is not a straight line (for example, a curve).

A critical caution: misidentifying which variable is independent and which is dependent can lead to misinterpretation. Always examine the relationship from both directions before deciding.

## Correlation Coefficient $r$

The Pearson correlation coefficient $r$ quantifies both the strength and the direction of the linear relationship between $ x$ and $ y $. Values of $ r$ range from $-1$ to $+1$.

### Formula Using Standardized Scores

The correlation coefficient can be expressed as the average product of standardized scores:

$$
r = \frac{1}{n-1} \sum_{i=1}^{n} \left( \frac{x_i - \bar{x}}{s_x} \right) \left( \frac{y_i - \bar{y}}{s_y} \right)
$$

where  

$n$ = number of paired observations  
$\bar{x}$, $\bar{y}$ = sample means of the $ x$ and $ y$ variables  
$s_x $, $ s_y$ = sample standard deviations of $ x$ and $ y$

### Computational Formula

For hand calculation, the following equivalent formula avoids computing means and standard deviations first:

$$
r = \frac{n \sum xy - (\sum x)(\sum y)}{\sqrt{ \bigl[n \sum x^2 - (\sum x)^2\bigr] \bigl[n \sum y^2 - (\sum y)^2\bigr] }}
$$

### Example 1: Small Dataset

Consider three pairs: $(3,2)$, $(3,3)$, $(6,4)$.

**Step 1: Using the standardized-score formula**  
$\bar{x} = 4$, $\bar{y} = 3$  
Deviations for $x $: $(-1, -1, 2)$; squares sum to $6$, so $ s_x = \sqrt{\frac{6}{3-1}} = \sqrt{3} \approx 1.732$  
Deviations for $y $: $(-1, 0, 1)$; squares sum to $2$, so $ s_y = \sqrt{\frac{2}{2}} = 1.0$  
Products $(x_i-\bar{x})(y_i-\bar{y})$: $(-1)(-1)=1$, $(-1)(0)=0$, $(2)(1)=2$; sum = 3  

$$
r = \frac{1}{3-1} \cdot \frac{3}{(1.732)(1)} = 0.5 \times \frac{3}{1.732} = 0.866
$$

**Step 2: Using the computational formula**  
$\sum x = 12$, $\sum y = 9$, $\sum xy = 3\cdot2+3\cdot3+6\cdot4 = 39$  
$\sum x^2 = 9+9+36 = 54$, $\sum y^2 = 4+9+16 = 29$  
Numerator: $3 \times 39 - 12 \times 9 = 117 - 108 = 9$  
Denominator: $\sqrt{(3 \times 54 - 12^2)(3 \times 29 - 9^2)} = \sqrt{(162-144)(87-81)} = \sqrt{18 \times 6} = \sqrt{108} = 10.392$  

$$
r = \frac{9}{10.392} = 0.866
$$

Interpretation: $r = 0.866$ suggests a strong positive linear association in this tiny sample.

### Example 2: Exercise Time and Weight Loss

Data from six randomly selected individuals (Table 16.6):  
$x$ (hours of exercise per week): 3, 5, 10, 15, 2, 3  
$y$ (weight loss in lbs): 2, 4, 6, 8, 1, 3  

Summary statistics:  
$\sum x = 38$ $\sum y = 24$ $\sum xy = 217$  
$\sum x^2 = 372$ $\sum y^2 = 130$ $ n = 6$

Plug into the computational formula:

$$
r = \frac{6 \times 217 - 38 \times 24}{\sqrt{[6 \times 372 - 38^2][6 \times 130 - 24^2]}}
  = \frac{1302 - 912}{\sqrt{(2232 - 1444)(780 - 576)}}
  = \frac{390}{\sqrt{788 \times 204}}
  = \frac{390}{\sqrt{160752}}
$$

$\sqrt{160752} \approx 401.0$, therefore

$$
r \approx \frac{390}{401.0} = 0.972
$$

The coefficient indicates a very strong positive linear correlation between hours of exercise and weight loss.

## Testing the Significance of the Correlation Coefficient

The sample correlation $r$ is an estimate of the population correlation $\rho $. A hypothesis test determines whether the observed linear association is statistically significant.

### Conditions for the Test

For a given value of $x $, the distribution of $ y$ must be normal, the variances of $ y$ must be equal across $ x $, and the mean of $ y$ must follow the straight-line model $\mu_y = \beta_0 + \beta_1 x $.

### Hypothesis Test Procedure

- **Null hypothesis**: $H_0: \rho = 0$ (no linear relationship)
- **Alternative hypothesis**: $H_1: \rho \neq 0$ (or one-sided: $\rho < 0$ or $\rho > 0$)
- **Test statistic**:

$$
t = r \sqrt{\frac{n-2}{1 - r^2}}
$$

Under $H_0$, $ t$ follows a $ t $-distribution with $ n-2$ degrees of freedom.

- **Critical values** are obtained from the $t $-table using the chosen significance level $\alpha$ and the appropriate tail(s).
- Reject $H_0$ if $|t|$ exceeds the critical value; otherwise, do not reject.

### Confidence Interval for $\rho$

A confidence interval for the population correlation can be constructed as:

$$
r \pm t_{\alpha/2} \, \frac{1 - r^2}{\sqrt{n-2}}
$$

where $t_{\alpha/2}$ is based on $ n-2$ degrees of freedom.

### Example 3: Testing the Exercise Data

From Example 2, $r = 0.972$ and $ n = 6$. Compute the test statistic:

$$
t = 0.972 \sqrt{\frac{6-2}{1 - 0.972^2}}
   = 0.972 \sqrt{\frac{4}{1 - 0.944784}}
   = 0.972 \sqrt{\frac{4}{0.055216}}
   = 0.972 \sqrt{72.44}
   \approx 0.972 \times 8.511 = 8.27
$$

Degrees of freedom = 4. For a one-tailed test with $\alpha = 0.05$, the critical value from Appendix Q is $ t_{c} = 2.132$. Since $8.27 > 2.132$, we reject $ H_0$ and conclude that a positive linear correlation exists between exercise hours and weight loss.

If the test statistic had fallen below the critical value, we would have failed to reject $H_0$, meaning the data would not provide sufficient evidence of a linear relationship.

### Example 4: Testing the Small Dataset

From Example 1, $r = 0.866$, $ n = 3$. Compute:

$$
t = 0.866 \sqrt{\frac{3-2}{1 - 0.866^2}}
   = 0.866 \sqrt{\frac{1}{1 - 0.75}}
   = 0.866 \sqrt{4}
   = 1.732
$$

Degrees of freedom = 1. The two-tailed critical value for $\alpha = 0.05$ is 12.706. Since $1.732 < 12.706$, we fail to reject $ H_0$. Despite the high $ r $, the result is not statistically significant. The Minitab output for this dataset gives a $ p $-value of 0.333, which is greater than 0.05, confirming the conclusion. A practitioner seeing this result would *not* claim a real correlation based on such a small sample.

## Simple Linear Regression

Simple linear regression models the relationship between a single predictor $x$ and a response $ y$ with a straight line. The model is written as:

$$
\hat{y} = a + bx
$$

where $\hat{y}$ is the predicted value of $ y $, $ a$ is the $ y $-intercept, and $ b$ is the slope.

### Least Squares Method

The least squares method finds the line that minimizes the sum of the squared vertical distances (errors) between the observed $y_i$ and the predicted $\hat{y}_i $. The slope and intercept are estimated by:

$$
b = \frac{n \sum xy - (\sum x)(\sum y)}{n \sum x^2 - (\sum x)^2}
$$

$$
a = \bar{y} - b \bar{x}
$$

### Example 5: Monthly Complaints

Table 16.7 records the number of complaints received in a manufacturing facility over eight months:

$$
\begin{array}{c|c|c|c|c}
\text{Month }(x_i) & \text{Complaints }(y_i) & x_i^2 & x_i y_i & y_i^2 \\
\hline
1 & 8 & 1 & 8 & 64 \\
2 & 6 & 4 & 12 & 36 \\
3 & 10 & 9 & 30 & 100 \\
4 & 6 & 16 & 24 & 36 \\
5 & 10 & 25 & 50 & 100 \\
6 & 13 & 36 & 78 & 169 \\
7 & 9 & 49 & 63 & 81 \\
8 & 11 & 64 & 88 & 121 \\
\Sigma & 36 & 73 & 204 & 353 & 707 \\
\end{array}
$$

$n = 8$, $\bar{x} = 4.5$, $\bar{y} = 9.125$

Compute the slope:

$$
b = \frac{8 \times 353 - 36 \times 73}{8 \times 204 - 36^2}
  = \frac{2824 - 2628}{1632 - 1296}
  = \frac{196}{336} = 0.5833
$$

Then the intercept:

$$
a = 9.125 - 0.5833 \times 4.5 = 6.50015
$$

The fitted regression line is:

$$
\hat{y} = 6.50015 + 0.5833x
$$

Interpretation: each additional month is associated with an increase of about 0.58 complaints on average. If the process continues at this rate, the predicted number of complaints in month 14 ($x = 14$) is:

$$
\hat{y} = 6.50015 + 0.5833 \times 14 \approx 14.67 \approx 14 \text{ complaints}
$$

## Standard Error of Estimate and Confidence Intervals

The standard error of the estimate $s_e$ measures the typical distance of observed points from the regression line:

$$
s_e = \sqrt{ \frac{ \sum y^2 - a \sum y - b \sum xy }{ n - 2 } }
$$

For the complaints data:

$$
s_e = \sqrt{ \frac{707 - 6.50015 \times 73 - 0.5833 \times 353}{8-2} }
    = \sqrt{ \frac{707 - 474.511 - 205.9}{6} }
    = \sqrt{ \frac{26.589}{6} } = \sqrt{4.4315} = 2.105
$$

A small $s_e$ indicates that the data points lie close to the fitted line.

To construct a confidence interval for the mean of $y$ at a specific value $ x_0$, first compute $ S_{xx}$:

$$
S_{xx} = \sum x^2 - \frac{(\sum x)^2}{n}
$$

For this dataset, $S_{xx} = 204 - \frac{36^2}{8} = 204 - 162 = 42$.

The confidence interval is:

$$
\hat{y} \pm t_c \, s_e \sqrt{ \frac{1}{n} + \frac{ (x_0 - \bar{x})^2 }{ S_{xx} } }
$$

where $t_c$ is the critical value from the $ t $-distribution with $ n-2$ degrees of freedom for the desired confidence level.

**Application to month 8 ($x_0 = 8$):**

$\hat{y} = 6.50015 + 0.5833 \times 8 = 11.1666$  
Inside the square root:

$$
\sqrt{ \frac{1}{8} + \frac{(8 - 4.5)^2}{42} } = \sqrt{ 0.125 + \frac{12.25}{42} } = \sqrt{0.125 + 0.2917} = \sqrt{0.4167} = 0.6455
$$

For a 95% confidence level, $t_c$ with 6 degrees of freedom is 2.447. The margin of error is:

$$
2.447 \times 2.105 \times 0.6455 = 3.326
$$

Thus the 95% confidence interval for the mean complaints in month 8 is:

$$
(11.1666 - 3.326,\; 11.1666 + 3.326) = (7.84,\; 14.49)
$$

We are 95% confident that the true mean number of complaints in month 8 lies between about 8 and 14. If the interval had contained values that indicated no practical increase over earlier months, the business case for intervention would have been weaker.

## Testing the Slope in Simple Regression

Determining whether the independent variable is a useful predictor requires a hypothesis test on the slope $\beta_1$.

**Hypotheses:**  
$H_0: \beta_1 = 0$ (the regression line is horizontal; $ x$ does not help predict $ y $)  
$H_1: \beta_1 \neq 0$ (a linear relationship exists)

**Test statistic:**

$$
t = \frac{b}{s_b}, \qquad s_b = \frac{s_e}{\sqrt{S_{xx}}}
$$

where $s_b$ is the standard error of the slope, $ s_e$ is the standard error of the estimate, and $ S_{xx} = \sum x^2 - n\bar{x}^2$. The statistic $ t$ follows a $ t $-distribution with $ n-2$ degrees of freedom under $ H_0$. Reject $ H_0$ if $|t|$ exceeds the critical value.

### Example 6: Temperature and Viscosity

Data from the source:  
$x$ (Temperature °C): 10, 15, 20, 15  
$y$ (Viscosity, Cp): 2, 3, 5, 4  
$n = 4$

1. Compute sums:  
$\sum x = 60$, $\sum y = 14$, $\sum x^2 = 10^2+15^2+20^2+15^2 = 950$  
$\sum xy = 10\cdot2 + 15\cdot3 + 20\cdot5 + 15\cdot4 = 225$

2. Estimate slope and intercept:

$$
b = \frac{4 \times 225 - 60 \times 14}{4 \times 950 - 60^2}
  = \frac{900 - 840}{3800 - 3600}
  = \frac{60}{200} = 0.3
$$
$$
a = \bar{y} - b\bar{x} = 3.5 - 0.3 \times 15 = -1.0
$$

Regression line: $\hat{y} = -1.0 + 0.3x$

3. Compute $s_e $:  
Predicted values: for $x=10$, $\hat{y}=2.0$; $ x=15$, $\hat{y}=3.5$; $ x=20$, $\hat{y}=5.0$; $ x=15$, $\hat{y}=3.5$  
Residuals: 0, $-0.5$, 0, $+0.5$  
Squared residuals: 0, 0.25, 0, 0.25; SSE = 0.5

$$
s_e = \sqrt{\frac{0.5}{4-2}} = \sqrt{0.25} = 0.5
$$

4. Compute $S_{xx}$:

$$
S_{xx} = 950 - \frac{60^2}{4} = 950 - 900 = 50
$$

5. Compute $s_b$ and $ t $:

$$
s_b = \frac{0.5}{\sqrt{50}} = \frac{0.5}{7.071} = 0.0707
$$
$$
t = \frac{0.3}{0.0707} = 4.24
$$

6. Decision: For a two-tailed test with $\alpha = 0.05$ and $ df = 2$, the critical value is 4.303. Since $4.24 < 4.303$, we fail to reject $ H_0$. There is insufficient evidence to conclude that temperature is a useful predictor of viscosity at the 5% significance level. Had $ t$ exceeded the critical value, we would have concluded a significant linear relationship, permitting use of the regression model for prediction and process control.

## Multiple Linear Regression (Overview)

When a process output depends on several inputs, simple regression is extended to include multiple independent variables:

$$
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_k x_k
$$

Statistical software (such as Minitab) estimates the coefficients $\beta_i$ from sample data. The source notes that multiple regression can explain a higher proportion of the variation in $ y$ than a single-variable model, but the underlying assumptions of normality, equal variance, and linearity must still be verified.

## Correlation, Causation, and Caution

A strong correlation does not, by itself, prove that changes in $x$ cause changes in $ y $. Observational studies show association; establishing cause and effect usually requires designed experiments. Always inspect the scatter plot. A correlation coefficient near zero may hide a strong nonlinear relationship (Figure 16.12d). Choosing an inappropriate independent variable can also produce misleading results; examine the relationship with the roles of the variables swapped to see which orientation makes the most sense in the process context.

## Exam Tips

- Memorize the computational formula for $r$ and practice obtaining it from given sums of $ x, y, xy, x^2, y^2$.
- The test statistic for $H_0: \rho = 0$ is $ t = r \sqrt{(n-2)/(1-r^2)}$ with $ n-2$ degrees of freedom; do not confuse this with a one-sample $ t $-test that uses $ n-1$.
- In simple regression, the same $t$ value tests both $\rho = 0$ and $\beta_1 = 0$; rejecting one is equivalent to rejecting the other.
- The confidence interval for the mean response at $x_0$ is narrowest when $ x_0 = \bar{x}$ and widens as $ x_0$ moves away from the mean, a fact often tested with questions about where predictions are most precise.
- A high sample correlation can occur by chance with very small samples. Always check the $p $-value or conduct the $ t $-test before drawing conclusions.
- The regression line always passes through the point $(\bar{x}, \bar{y})$; you can verify any fitted model quickly with this property.