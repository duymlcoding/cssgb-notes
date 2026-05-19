---
title: "Basic Probability Concepts"
description: "Detailed study notes for the ASQ CSSGB Measure phase covering probability definitions, addition and multiplication rules, conditional probability, mutually exclusive and independent events, permutations, standard deviation, and Pareto charts."
---

## Probability Definitions and Simple Events

Probability quantifies the likelihood that a particular event will occur. The value always lies between 0 and 1 inclusive. A probability of 0 means the event cannot happen; a probability of 1 means the event is certain. The sum of the probabilities of all possible outcomes of a random experiment equals exactly 1.

The word "random" indicates that every possible outcome has an equal chance of being selected. For an urn containing 100 marbles, five of which are red, the probability of drawing a red marble at random is

$$P(\text{Red}) = \frac{5}{100} = 0.05$$

If the urn contained no red marbles, the probability would be 0. If every marble were red, the probability would be 1.

### Simple Events

Simple events are single, well-defined outcomes. Classic simple-event probabilities include:

- Probability of obtaining a head in a fair coin toss: \( \frac{1}{2} \)
- Probability of rolling a 2 on a single toss of a fair six-sided die: \( \frac{1}{6} \)

These probabilities form the building blocks for more advanced compound event calculations.

### Why Probability Matters in Six Sigma

A Green Belt uses probability to quantify defect likelihood, predict process yields, and calculate risks associated with process inputs. Mastering probability rules allows the practitioner to model process behavior and assess whether observed effects are due to random chance or to assignable causes that require improvement.

## Compound Events and Venn Diagrams

Compound events are formed by combining two or more simple events. A Venn diagram helps visualize unions (A or B, denoted \(A \cup B\)) and intersections (A and B, denoted \(A \cap B\)). The diagram shows how portions of the sample space overlap.

Relationships among events drive the choice of the correct probability rule.

## Complementation Rule

The probability that an event \(A\) does **not** occur is

$$P(\text{not }A) = 1 - P(A)$$

Some texts write the complement as \(\sim A\), \(A'\), or \(\overline{A}\).

### Example: Car Starting

If the probability that a car starts on a rainy day is 0.4, then the complement, the probability it does **not** start, is

$$P(\text{not start}) = 1 - 0.4 = 0.6$$

**Interpretation:** On rainy days, the car fails to start 60% of the time. If a fleet manager observed a higher-than-expected no-start rate, the complement rule would help quantify the performance gap and trigger root-cause analysis.

## Conditional Probability

Conditional probability measures the chance that event \(B\) occurs given that event \(A\) has already occurred. The formal definition is

$$P(B|A) = \frac{P(A \cap B)}{P(A)}$$

where \(P(A \cap B)\) is the probability that both \(A\) and \(B\) happen.

### Example 1: Drawing Marbles Without Replacement

An urn holds three white and two black marbles. The probability that the first marble drawn is black is

$$P(\text{Black}_1) = \frac{2}{2+3} = \frac{2}{5}$$

If the first marble is black and is **not** replaced, the urn now contains one black and three white marbles. The probability that the second marble is black, given the first was black, is

$$P(\text{Black}_2 \mid \text{Black}_1) = \frac{1}{1+3} = \frac{1}{4}$$

Using the general multiplication rule (derived below), the probability that **both** draws are black is

$$P(\text{Black}_1 \cap \text{Black}_2) = P(\text{Black}_1) \times P(\text{Black}_2 \mid \text{Black}_1) = \frac{2}{5} \times \frac{1}{4} = \frac{2}{20} = 0.10$$

**Interpretation:** There is a 10% chance of drawing two black marbles consecutively without replacement. This matters in quality audits that involve destructive testing, where sampling without replacement changes the probabilities of subsequent draws.

### Example 2: Die and Conditional

Consider a fair die. Let \(A\) be "the outcome is an even number" and \(B\) be "the outcome is a 6". Then \(P(A) = 3/6 = 0.5\), \(P(A \cap B) = 1/6\). The conditional probability

$$P(B|A) = \frac{P(A \cap B)}{P(A)} = \frac{1/6}{3/6} = \frac{1}{3}$$

**Interpretation:** Given that the roll produced an even number, the probability it is a 6 is one-third. Conditional probability underlies reliability block diagrams and Bayesian reasoning in process control.

## Mutually Exclusive Events

Two events are mutually exclusive (disjoint) if they cannot occur at the same time. Formally, \(A\) and \(B\) are mutually exclusive when

$$P(A \cap B) = 0$$

Equivalently, the addition rule collapses to the special form.

### Special Addition Rule

For mutually exclusive events \(A\) and \(B\),

$$P(A \cup B) = P(A) + P(B)$$

### Example 3: Rolling a Die

Event \(A\): rolling a 4 (\(P = 1/6\))
Event \(B\): rolling a 6 (\(P = 1/6\))

Since a single die cannot show both 4 and 6, the events are mutually exclusive.

$$P(A \cup B) = \frac{1}{6} + \frac{1}{6} = \frac{2}{6} = \frac{1}{3}$$

**Interpretation:** The chance of rolling either a 4 or a 6 is 33.3%. If a process step had only two mutually exclusive failure modes each with known probability, the special addition rule gives the total failure probability directly.

### Example 4: Supplier Boards

An assembly uses an electronic board supplied by three vendors. The probability that a board from Supplier A works is 0.2, from B is 0.3, and from C is 0.5. Because the assembly can use only one board, only one supplier’s board can be the one that works. The events "board from B works" and "board from C works" are mutually exclusive. Therefore,

$$P(B \cup C) = 0.3 + 0.5 = 0.8$$

**Interpretation:** There is an 80% chance the assembly will work when using either the B or C board. If that probability were unacceptably low, the Green Belt would investigate alternative suppliers or improve reliability of the existing boards.

## General Addition Rule

When events are not mutually exclusive, the possibility of double-counting the intersection must be removed. The always-true rule is

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

### Example 5: Injection Molding Machines

An organization has two injection molding machines. Each machine has a probability of 0.8 of working. The machines operate independently, so both can work simultaneously. The probability that the organization meets weekly production (i.e., at least one machine works) is

$$P(\text{Machine1} \cup \text{Machine2}) = 0.8 + 0.8 - (0.8 \times 0.8)$$

Compute:

- \(P(\text{Machine1 and Machine2}) = 0.8 \times 0.8 = 0.64\)
- Then \(0.8 + 0.8 - 0.64 = 1.6 - 0.64 = 0.96\)

**Interpretation:** The redundancy yields a 96% chance of at least one machine working. This is a reliability calculation common in process design. If the probability were 0.80 without redundancy, adding a second identical machine raises the probability substantially.

### Example 6: Overlapping Customer Issues (Pizza Caterer – Relationship Matrix Context)

Take "pizza delivered late" and "pizza not hot enough" from a catering process. They are not mutually exclusive because a late delivery often also leaves the pizza cold. Suppose from data: \(P(\text{late}) = 0.25\), \(P(\text{not hot}) = 0.20\), and \(P(\text{late and not hot}) = 0.12\). Then the probability of either a late delivery or a cold pizza (or both) is

$$P(\text{late} \cup \text{not hot}) = 0.25 + 0.20 - 0.12 = 0.33$$

**Interpretation:** About 33% of orders experience at least one of these two quality problems. A team would use a relationship matrix to see which causes affect both issues and prioritize corrective actions that address the root cause driving the overlap.

## Independence and Multiplication Rules

Two events are independent if the occurrence of one does not change the probability of the other occurring. Statistically, \(A\) and \(B\) are independent when

$$P(B|A) = P(B)$$

or, equivalently,

$$P(A \cap B) = P(A) \times P(B)$$

### Special Multiplication Rule (Independent Events)

For independent events, use:

$$P(A \cap B) = P(A) \times P(B)$$

### Example 7: Electronic Board Assembly

An assembly has two major components, A and B. The probability that component A works is 0.7, and the probability that component B works is 0.8, with independent operation.

$$P(\text{Assembly works}) = P(A \cap B) = 0.7 \times 0.8 = 0.56$$

**Interpretation:** The assembly has a 56% chance of functioning. If this is a critical subsystem, the design team might introduce redundancy (see Example 5) or improve component reliability to raise overall yield.

### General Multiplication Rule (Always True)

For any two events (whether independent or dependent), the probability of both occurring is

$$P(A \cap B) = P(A) \times P(B|A)$$

### Example 8: Production Lot Sampling Without Replacement

A production lot of 50 units has 10 defective units. Three units are sampled at random without replacement. The probability that all three are defective is a chain of conditional probabilities:

- \(P(\text{1st defective}) = \frac{10}{50}\)
- \(P(\text{2nd defective} \mid \text{1st defective}) = \frac{9}{49}\)
- \(P(\text{3rd defective} \mid \text{first two defective}) = \frac{8}{48}\)

Multiply them:

$$P(\text{all three defective}) = \frac{10}{50} \times \frac{9}{49} \times \frac{8}{48} = \frac{720}{117,600} = 0.0061 \text{ or } 0.61\%$$

**Interpretation:** The chance of drawing three defectives in a row without replacement is only 0.61%. This low probability indicates that finding three defectives in a random sample of three would be strong evidence that the lot is far worse than the nominal 20% defective rate, prompting containment action. If the lot had been larger, the changes after each draw would be smaller, but the principle remains the same.

## Permutations

A permutation is an ordered arrangement of \(n\) distinct objects taken \(r\) at a time. The number of permutations, denoted \(_n P_r\), is

$$_n P_r = n \times (n-1) \times (n-2) \times \cdots \times (n - r + 1) = \frac{n!}{(n - r)!}$$

Important factorial values needed for hand calculations:

$$0! = 1, \quad 1! = 1, \quad n! = n \times (n-1) \times \cdots \times 2 \times 1$$

Also note: \(_n P_n = n!\)

### Example 9: Seating Arrangement

When arranging two people, A and B, in airline seats, AB (window then aisle) differs from BA (aisle then window). The number of permutations of 2 persons taken 2 at a time is

$$_2 P_2 = \frac{2!}{(2-2)!} = 2! = 2$$

**Interpretation:** There are two distinct seating orders. This matters in layout design where operator access or ergonomics depends on sequence.

### Example 10: Arranging Letters of "sigma"

How many arrangements can be formed using all the letters of the word "sigma"? The word has 5 unique letters, so \(n = r = 5\).

$$_5 P_5 = 5! = 5 \times 4 \times 3 \times 2 \times 1 = 120$$

**Interpretation:** 120 different orderings exist. In experimental design, the number of possible run orders for five unique treatments is 120, which underlies randomization strategies.

Why permutations matter: Many Six Sigma statistical tests rely on counting principles to calculate probabilities under randomization or to enumerate possible sample orders.

## Standard Deviation

Standard deviation is the fundamental measure of variation in a process. It is denoted by the Greek letter \(\sigma\) for population data and by \(s\) for sample data. Standard deviation measures the typical distance between individual data points and the mean; a large standard deviation indicates wide spread, while a small standard deviation indicates tightly clustered points.

Six Sigma uses standard deviation as the yardstick for process capability and control limit calculations. Higher variation means more defect opportunities. Therefore, understanding and reducing standard deviation is a central goal of improvement projects.

### Population Standard Deviation Formula

When every member of the population is measured, the population standard deviation is

$$\sigma = \sqrt{\frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2}$$

where:
- \(\sigma\) = population standard deviation
- \(N\) = number of data elements in the population
- \(x_i\) = each individual data value
- \(\mu\) = population mean
- \(\sum_{i=1}^{N}\) indicates summation over all \(N\) data points

### Population Example: Test Scores

A teacher records scores for all 15 students in a class: 67, 68, 73, 74, 81, 85, 88, 88, 90, 90, 90, 93, 94, 98, 99.

**Step 1 – Compute the mean:**

$$ \mu = \frac{67+68+73+74+81+85+88+88+90+90+90+93+94+98+99}{15} = \frac{1278}{15} = 85.2 $$

**Step 2 – Compute squared deviations \((x_i - \mu)^2\) for each score:**

- 67: \((67 - 85.2)^2 = (-18.2)^2 = 331.24\)
- 68: \((-17.2)^2 = 295.84\)
- 73: \(( -12.2)^2 = 148.84\)
- 74: \((-11.2)^2 = 125.44\)
- 81: \((-4.2)^2 = 17.64\)
- 85: \((-0.2)^2 = 0.04\)
- 88: \( (2.8)^2 = 7.84\) (two values)
- 90: \( (4.8)^2 = 23.04\) (three values)
- 93: \( (7.8)^2 = 60.84\)
- 94: \( (8.8)^2 = 77.44\)
- 98: \( (12.8)^2 = 163.84\)
- 99: \( (13.8)^2 = 190.44\)

**Step 3 – Sum the squared deviations:**

$$ \sum (x_i - \mu)^2 = 331.24 + 295.84 + 148.84 + 125.44 + 17.64 + 0.04 + 2 \times 7.84 + 3 \times 23.04 + 60.84 + 77.44 + 163.84 + 190.44 = 1496.4 $$

**Step 4 – Divide by \(N = 15\) to get the variance:**

$$ \text{Variance} = \frac{1496.4}{15} = 99.76 $$

**Step 5 – Take the square root:**

$$ \sigma = \sqrt{99.76} \approx 9.987 $$

**Interpretation:** The standard deviation of about 10 points indicates that individual test scores typically lie within roughly 10 points of the class mean. In a process context, this spread quantifies the consistency of student performance. Compare this to a process with a smaller standard deviation (for example, 3 points), which would indicate far less variation.

### Sample Standard Deviation Formula

When only a sample of the population is available, the formula uses \(n-1\) in the denominator to correct for bias:

$$ s = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2} $$

where:
- \(s\) = sample standard deviation
- \(n\) = sample size
- \(\bar{x}\) = sample mean

Using the same 15 scores as a sample (rather than the entire population), the only difference occurs in the variance step:

$$ \text{Sample variance} = \frac{1496.4}{14} \approx 106.885 $$

Thus,

$$ s = \sqrt{106.885} \approx 10.338 $$

**Interpretation:** The sample standard deviation is slightly larger (10.34 vs. 9.99) because dividing by \(n-1\) compensates for the additional uncertainty inherent in estimating the population standard deviation from a sample. Green Belts use sample statistics when process data are collected over time or when measuring every unit is impractical.

### Standard Deviation in Excel

Excel computes sample standard deviation with the function `STDEV()`. To use it:

1. Enter data in a column.
2. In a new cell, type `=STDEV(`
3. Select the cell range containing the data.
4. Press Enter.

The formula applies the \(n-1\) correction automatically, so it works for sample data. For population data, use `STDEV.P()`.

### Why Calculate Standard Deviation

Standard deviation pinpoints how much variation actually exists and provides a benchmark for improvement. When a process average is on target but standard deviation is large, the process is not capable even though it is centered. For example, test scores with a mean of 85 and standard deviation of 10 suggest a wide performance spread; a mean of 90 with standard deviation of 3 indicates consistent mastery. A low mean with a tiny standard deviation would point to a systemic problem in instruction. In Six Sigma, standard deviation feeds directly into capability indices (Cp, Cpk), control chart limits, and sample size calculations.

## The Pareto Principle and Pareto Chart

The Pareto principle states that roughly 20% of causes drive 80% of effects. This "law of the vital few" means a small number of inputs create the majority of output variation or defects. In Six Sigma, teams use the Pareto principle to focus improvement efforts on the few critical causes that will deliver the largest impact.

A Pareto chart is a bar graph where causes are ordered from the highest frequency (or cost) on the left to the lowest on the right. Often a cumulative percentage line is overlaid.

### Pareto Chart Creation in Excel

The following steps create a Pareto chart for denial reasons of medical claims. The data:

| Reason                  | Count  |
|-------------------------|--------|
| Duplicate claim         | 18012  |
| Timely Filing           | 13245  |
| No beneficiary found    | 10215  |
| Claim lacks information | 4548   |
| Service not covered     | 2154   |
| Medical necessity       | 1423   |
| Date of service issue   | 526    |

1. Sort the reasons from largest count to smallest.
2. Add a cumulative count column. The first cell equals the first count. Each subsequent cumulative cell equals the previous cumulative cell plus the current count.
3. Add a percent column: divide each individual count by the grand total (50123). Use absolute cell reference (`$C$9` for the total) to drag the formula. Format as percentages.
4. The resulting table:

| Reason                  | Count  | Cumulative Percent |
|-------------------------|--------|--------------------|
| Duplicate claim         | 18012  | 35.9%              |
| Timely Filing           | 13245  | 26.4%              |
| No beneficiary found    | 10215  | 20.4%              |
| Claim lacks information | 4548   | 9.1%               |
| Service not covered     | 2154   | 4.3%               |
| Medical necessity       | 1423   | 2.8%               |
| Date of service issue   | 526    | 1.0%               |

5. Highlight the Reason and Percent columns and insert a bar chart. Format the bars and add data labels if desired.

**Interpretation of the Pareto chart:** The top three denial reasons (duplicate claims, timely filing, no beneficiary found) account for approximately 80% of total denials. This signals where process improvements will yield the greatest reduction in rework and lost revenue. A Green Belt would then drill down into root causes for these vital few, applying the probability concepts and statistical tools from earlier sections.

If the Pareto chart showed a flat distribution with many small causes, the team would recognize that no vital few exist and would instead search for systemic issues or reduce overall process complexity.

## Exam Tips

- Memorize the exact statements: Mutually exclusive means \(P(A \cap B) = 0\); independent means \(P(B|A) = P(B)\). Do not confuse the two concepts.
- When a problem describes events that “cannot happen at the same time,” apply the special addition rule \(P(A \cup B) = P(A) + P(B)\).
- When events do not affect each other’s probabilities, use the special multiplication rule \(P(A \cap B) = P(A) \times P(B)\). If the scenario involves replacement, you have independence.
- The general addition rule \(P(A \cup B) = P(A) + P(B) - P(A \cap B)\) is always correct; use it whenever the events are not mutually exclusive.
- For sampling without replacement, probabilities change after each draw. Calculate dependent events with the general multiplication rule \(P(A \cap B) = P(A) \times P(B|A)\).
- Standard deviation: the denominator is \(N\) for population data and \(n-1\) for sample data. This distinction appears in capability studies and control chart calculations.
- The Pareto chart ranks causes by frequency. Use it to separate the vital few from the trivial many before deploying detailed statistical analyses.