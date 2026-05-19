---
title: "Types of Data and Measurement Scales"
description: "Detailed study notes for the ASQ CSSGB exam covering continuous and discrete data, the four measurement scales (nominal, ordinal, interval, ratio), and their applications in Six Sigma projects."
---

## Continuous and Discrete Data

Six Sigma projects classify quantitative data into two fundamental types: continuous (variables) data and discrete (attributes) data. Continuous data come from measurements on a scale that can take on any value within a range. Length, weight, temperature, and time are typical examples. The scale is called continuous because between any two values an infinite number of other values exist. Between 1.537 inches and 1.538 inches, one can find 1.5372, 1.5373, and 1.53724. Discrete data result from counting the occurrence of events. The number of paint runs per batch, the number of leaking valves, or the number of bubbles in a square foot of floated glass all represent discrete counts.

A project team should distinguish between the two types early in the Measure phase because the choice influences the sensitivity of control charts, the sample sizes required, and the methods available for analysis. Continuous measurements yield richer information. Control charts built on continuous data are more sensitive to process changes than those built on discrete data. When designed experiments are used for process improvement, changes in the continuous response may become visible even before the corresponding discrete attribute changes. Discrete data also demand larger statistically valid sample sizes to achieve the same consumer risk protection (Type II error) as continuous data. For these reasons, a Six Sigma team should, whenever practical, convert discrete measurements into continuous ones. For example, instead of recording whether a temperature is within a range (binary), the team should log the exact temperature in degrees.

A secondary type of data, locational data, identifies where a defect or event occurs. In an automobile assembly line, noting the position of a paint defect on the vehicle body provides essential information that a simple count cannot. Locational data are often displayed with a measles chart, as discussed in Chapter 10 of the *ASQ CSSGB Handbook*. While locational data do not change the fundamental measurement scale of the attribute, they add critical context for troubleshooting.

Discrete data are sometimes grouped into ordinal, nominal, or binary categories. Binary data, pass/fail, on/off, hot/cold, are the simplest form of discrete data to collect. However, even seemingly clear binary judgments can suffer from operator bias when the boundary is ambiguous (for instance, deciding whether a glass is "full" or "empty"). The team can reduce such bias through proper measurement system analysis. Continuous data avoid much of this ambiguity because they record the actual magnitude.

## The Four Measurement Scales

Every measurement falls on one of four scales: nominal, ordinal, interval, or ratio. The scale determines which arithmetic operations and statistical tests are legitimate. A Six Sigma project must match the analytical tool to the scale, otherwise the conclusions may be mathematically unsound or misleading.

### Nominal Scale

Nominal data use numbers or labels purely as identifiers. The numbers carry no quantitative meaning, no order, and no indication of whether one category is "better" or "worse" than another. Color codes for electrical wires, birth states of students in a classroom, or machine numbers in a factory are nominal. Even when a nominal category is assigned a numeric code (Texas=1, Louisiana=2, etc.), that code is just a name.

The only permissible summary statistic for the center of nominal data is the mode, the most frequently occurring category. Valid operations include counting the frequency in each category and performing a chi-square test to compare observed and expected frequencies. Calculating a mean or median on nominal numbers would produce nonsense, because the numbers do not reflect magnitude.

### Ordinal Scale

Ordinal data place items in a meaningful order, but the intervals between successive values are not known or are not equal. Common examples are the defect criticality classification used in an FMEA: critical, major, minor. The team knows that a critical defect is more severe than a major defect and a major more severe than a minor, but cannot say that the difference between critical and major is the same as the difference between major and minor. Movie ratings or pain scales work the same way; a rating of 10 indicates a better experience than a 9, but the scale does not tell how much better.

Because the order is meaningful, teams can use "greater than" and "less than" comparisons with ordinal data. Appropriate location measures are the mode and the median. Dispersion is described by the interquartile range. Nonparametric tests such as the sign test apply to ordinal data. Computing an arithmetic mean or standard deviation on ordinal data is not valid, because those operations assume equal spacing.

### Interval Scale

Interval data possess equal intervals between adjacent values across the entire scale. Temperature measured in degrees Celsius is the classic example: the difference between 20 °C and 40 °C is exactly the same magnitude as the difference between −10 °C and −30 °C. The scale, however, lacks a true zero point; 0 °C does not mean the absence of temperature. This absence of a rational zero prevents ratio statements such as "40 °C is twice as hot as 20 °C."

Because the differences are meaningful, addition and subtraction of interval values are legitimate. The team can calculate an arithmetic mean, a standard deviation, and perform t-tests and F-tests on interval data. Interval data thus support a much wider range of statistical analyses than nominal or ordinal data.

### Ratio Scale

Ratio data exhibit all the properties of interval data and, in addition, possess a true, absolute zero point. Length, weight, force, defects per million opportunities, voltage, units per hour, and volume are ratio measurements. A length of zero means no length, so the ratio of two lengths is meaningful: a board 10 feet long is twice as long as one 5 feet long.

Ratio data allow the full suite of arithmetic and statistical operations. All addition, subtraction, multiplication, and division of scale values are legitimate. Teams can compute geometric means and coefficients of variation. Continuous ratio data support the most powerful parametric tests, including t-tests, Analysis of Variance, and regression analysis. Even discrete ratio data, such as counts of defects, permit many parametric techniques when the underlying distribution is appropriate.

### Relationship Between Data Types and Measurement Scales

A single variable may be classified differently depending on the data type. Continuous data are almost always interval or ratio. Discrete data are typically nominal or ordinal, but they can also be ratio when they represent a true count with an absolute zero (defects per unit, cycle count). The Six Sigma project benefits directly from moving up the scale hierarchy. Higher scales preserve more information and open the door to more sensitive statistical tools. When a team can replace a nominal classification (defective/nondefective) with a continuous measurement (dimension, weight, or time), the resulting analysis is sharper and smaller sample sizes can achieve the same power. This principle drives the frequent advice to convert attribute data into variables data wherever feasible.

## Utility in the Measure Phase

During the Measure phase, identifying the measurement scale and data type is a prerequisite for selecting the correct baseline metrics, control charts, and hypothesis tests. A project that measures customer wait time in minutes (ratio) can assess process capability with standard indices and compare means with a two-sample t-test. A project that only records whether the wait was "short," "medium," or "long" (ordinal) must use nonparametric tests, which have lower power, and may need larger sample sizes to detect improvements. Incorrectly applying interval analysis to ordinal data will produce misleading p-values and erroneous business decisions.

## Exam Tips

- Differentiate between continuous and discrete data by asking: is the value a measurement on an infinitely divisible scale, or is it a count or category?
- For any given variable, identify the measurement scale and list the statistical operations that are mathematically defensible (for example, temperature in Celsius is interval, so you can compute a mean but not a coefficient of variation).
- Explain why a control chart built on continuous data is more sensitive than one built on discrete data: continuous charts track process shifts sooner because they capture subtle variation that attribute charts ignore.
- When presented with an improvement scenario that compares an ordinal rating to a continuous measurement, argue for converting to continuous data to reduce sample size requirements and increase detection power.
- Recognize that binary data (pass/fail) are a limited form of nominal data and that the mode is the only meaningful measure of central tendency for nominal variables.
- Given a dataset of counts with a true zero (defects per unit), classify it as ratio and recall that both parametric tests and control charts for rare events are appropriate.