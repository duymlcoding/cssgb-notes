---
title: "Sampling and Data Collection Plans and Methods"
description: "Detailed study notes for the ASQ CSSGB Measure phase covering data collection strategies, sampling methods, check sheets, data types, measurement scales, and measurement system analysis including Gage R&R."
---

## Purpose of Data Collection in the Measure Phase
Before a team can analyze a process, it must understand current performance. Creating a baseline metric starts in Define, but the Measure phase delivers the hard numbers. Teams need a process-specific metric and historical data, or they must collect data from scratch. The goal is to capture information that will support root cause analysis and prove that improvements occurred. The choices made about how, what, and when to collect data determine the quality of everything that follows.

## Common Data Collection Errors and How to Minimize Them
Many data problems stem from human and system weaknesses. Typical errors seen in practice include ambiguous terminology, units of measure that are not defined, illegible handwritten characters (confusing a 2 with a Z), inadequate measurement system resolution, rounding off measurements that loses precision, emotional bias such as flinching, guesswork instead of validation, multiple points of data entry that create inconsistency, poor training, and clerical or typographical mistakes.

To minimize these errors, build a rigorous plan. Use the 5W1H structure: what, where, who, when, why, and how. Maintain a calibration schedule for all measurement equipment. Conduct repeatability and reproducibility (R&R) studies on the measurement system. Record auxiliary information including units, time of collection, environmental conditions, measurement tool used, and the name of the data recorder. Apply appropriate statistical tests to remove outliers. For digitally transmitted or stored data, use a redundant error-correction system. Finally, provide clear, complete instruction and training for collection, transformation, analysis, and interpretation.

### Data Coding
When manual entry is unavoidable, coding can reduce fatigue-induced errors. An inspector measuring diameters that fall within a narrow range can assign a single-digit code to each unique measurement value. Later, decoding recovers the actual values. Coding also protects confidentiality and communicates general trends without revealing exact numbers. The table below illustrates a coding scheme.

| Actual measurement | Coded value |
|-------------------|-------------|
| 10.120            | 1           |
| 10.121            | 2           |
| 10.122            | 3           |
| 10.123            | 4           |

## Types of Data: Continuous versus Discrete
Understanding the nature of the data dictates which graphical and analytical tools are appropriate.
- **Discrete data**: Categorical (qualitative) data, sometimes called attribute data. It includes ordinal data (ranked categories such as grades A, B, C), nominal data (named categories such as colors or states), and binary/attribute data (pass/fail, on/off). Discrete data is typically displayed with Pareto charts, pie charts, and bar charts. In some cases, ratios or within-category variation allow conversion to control charts.
- **Continuous data**: Quantitative data measured in units, such as time, temperature, length, or a percentage. Continuous data appears in histograms, box plots, run charts, and control charts.

Whenever possible, teams should choose continuous data. Continuous measurements provide more information, are more precise, and let you remove the variation and errors introduced by estimation and rounding. While continuous data often requires more effort to collect manually, automation can make it efficient. A continuous stream can always be converted to discrete categories later, but the reverse is rarely true.

## Levels of Data (Measurement Scales)
Data classification goes beyond discrete versus continuous. Four levels describe the information carried by numbers.

- **Nominal**: The lowest level. Numbers are labels only, with no order implied. For example, assigning 1 to Texas, 2 to Louisiana, 3 to Arkansas in a survey of birth states. The mode is the only meaningful measure of central tendency.
- **Ordinal**: Numbers represent rank order, but the intervals between ranks are not meaningful. FMEA severity ratings of 1 to 10 are ordinal. You can say a rating of 9 is worse than a 3, but you cannot quantify how much worse. Central tendencies use the mode or median.
- **Interval**: Ordered values with equal intervals that carry meaning. Temperature in degrees Fahrenheit is interval data: the difference between 76 °F and 80 °F is the same 4-degree step as any other. There is no true zero, so ratios are not interpretable.
- **Ratio**: The highest level. Ratio data has an absolute zero, supports all arithmetic operations, and can be discrete or continuous. Examples include defects per million opportunities, voltage, height, and volume. Ratio data provides the greatest flexibility for statistical analysis.

## Sampling Strategies
When studying every unit in a population is impractical, sampling is used. The choice of strategy affects bias and representativeness.

### Random Sampling
Every item in the lot has an equal probability of being selected. This method works only when the lot is homogeneous. If the population contains a mix of outputs from different machines, material lots, or process settings, random sampling can produce a proportion of nonconformities that is larger than expected. In many services, such as call centers or healthcare inventory, random sampling is applied successfully as long as homogeneity is confirmed.

### Stratified Sampling
When the population is not homogeneous, stratify it first. Divide the lot into subgroups based on criteria such as machine, material lot, stream, or process setting. Then draw random samples from each stratum. A shipping company testing delivery time accuracy might stratify by distance (under 200 miles, 201-400 miles, 401-600 miles, over 600 miles) to avoid inadvertently collecting data from only one region. Stratified sampling reduces bias and yields more representative results than random sampling performed on a mixed lot.

### Sequential Sampling
Two distinct practices carry this name.
- In destructive and reliability testing, samples are tested one-by-one sequentially until the desired outcome (pass, fail, or a decision) is reached. This approach minimizes the number of expensive units destroyed.
- Some teams use sequential sampling to mean selecting every X-th item on a production line or recording a measurement every fixed time interval. While convenient, this method carries a risk: if the sequence aligns with an underlying process cycle, the sample may be skewed.

## Check Sheets
A check sheet is a structured, pre-categorized form used to collect data during process execution. It can use words, tally marks, or graphics. The tool makes data collection easy and reveals patterns and trends immediately. Completed check sheets often become the basis for Pareto charts or attribute control charts, and simply using one can spur improvement.

### Steps to Create a Check Sheet
1. Identify and agree on the causes, conditions, or categories to be collected.
2. Decide who will collect the data, the time period, and the method of collection.
3. Design a check sheet that fits naturally into the operation where it will be used.
4. Collect data consistently and accurately according to the design.

## Measurement Systems Analysis (MSA)
Measurement systems analysis applies scientific principles to evaluate the variation contributed by the measurement system itself. The goal is to quantify errors of accuracy so they can be reduced or accounted for. Teams investigate six elements.

- **Accuracy**: The closeness of a measurement to a true value. Verify gauges by calibrating them against known standards. Instruct operators to record raw data without rounding. Capture auxiliary information that helps identify unusual conditions.
- **Resolution**: The smallest change a measurement system can detect. Use the 10-bucket rule: if a pipe must fit within a 5 mm tolerance, measure to at least 0.5 mm resolution. For time-based data, sample frequently enough to catch process shifts.
- **Linearity**: The consistency of accuracy across the entire measurement range. A scale may be accurate at 5 kg but drift by 0.25 kg per additional kilogram. Teams compare measurements at multiple points against a trusted standard and develop correction equations or avoid the unreliable ends of the range.
- **Stability**: The consistency of measurements over time. A stable measurement system, when mapped on a control chart, shows no out-of-control signals. If instability appears, rule out measurement system issues before concluding the process has changed.
- **Repeatability**: The ability of a single operator, using the same tool, to obtain the same result when measuring the same item multiple times.
- **Reproducibility**: The ability of multiple operators, using the same tool, to obtain matching results on the same item.

## Gage Repeatability and Reproducibility (Gage R&R)
Gage R&R studies isolate operator and equipment variation. Two types exist: attribute and variable.

### Attribute Gage R&R
Used for pass/fail, go/no-go, yes/no measurements. The procedure:
1. Select at least two appraisers.
2. Obtain a set of samples. Label them so that the appraiser cannot identify individual items.
3. Determine the true attribute for each sample using the best available reference.
4. Have each appraiser evaluate every sample (Trial 1). Record the results.
5. Randomize the sample order and have each appraiser evaluate the same samples again (Trial 2).
6. Compare each trial against the true value and against the other appraiser.

Compute agreement percentages for repeatability (how often an appraiser agrees with themselves) and reproducibility (how often appraisers agree with each other). Systems with low agreement percentages indicate unclear standards, poor training, or defective tools. Strive for at least 20 samples to strengthen the study.

### Variable Gage R&R
Used when measurements are continuous. The setup is similar:
- Use two to three appraisers and at least five to ten parts.
- Each appraiser measures each part two to three times, in randomized order.
- Record all data in a Gage R&R template.

Statistical software calculates four key metrics. Safe, caution, and failure zones are given below.

| Metric                  | Pass        | Caution     | Fail         |
|-------------------------|-------------|-------------|--------------|
| % Study Variation       | 0 to 10     | 10 to 30    | 30 and above |
| % Tolerance             | 0 to 10     | 10 to 30    | 30 and above |
| % Contribution          | 0 to 1      | 1 to 9      | 10 and above |
| Number of Distinct Categories | 10 or more | 6 to 10     | 1 to 5       |

A measurement system with one or more metrics in the failure zone should be repaired or replaced. Caution zone values may be acceptable if improving the system is too costly, but the team must document the risk.

## Collecting Data Samples in Practice
Once the measurement system is validated, collect data according to the chosen sampling plan. Whenever feasible, automate data capture or pull from existing databases to approach population-level analysis. Manual collection relies on random or stratified sampling to represent the population within time and cost limits. Always record context details: the person collecting, the time, the machine, and any environmental anomalies. Review data for misplaced decimals, duplicates, and missing points before advancing to the Analyze phase.

## Exam Tips
- When a question describes a mixed population with different machines or material lots, immediately think **stratified sampling**, not simple random sampling.
- Memorize the four levels of data (nominal, ordinal, interval, ratio) and their properties. A common exam item asks which level an example represents, or which measure of central tendency is appropriate.
- For any scenario where human operators take measurements, recall the difference between repeatability (same operator, same part) and reproducibility (different operators, same part). Gage R&R studies test both.
- The check sheet creation steps are often tested as a sequencing question. Know them in order: agree on causes, decide who/when/how, design the sheet, then collect data.
- When continuous data is possible but discrete data is proposed, choose continuous. It provides more information and can always be converted to discrete later.