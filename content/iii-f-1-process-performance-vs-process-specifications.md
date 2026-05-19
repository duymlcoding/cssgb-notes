---
title: "Process Performance vs. Process Specifications"
description: "Distinguish natural process limits from specification limits, and calculate process performance metrics from control chart data."
---

## Natural Process Limits and Specification Limits

A process produces output that varies. Six Sigma practitioners quantify this variation with two distinct sets of limits: natural process limits and specification limits. Natural process limits describe the actual spread of the process output when only common-cause variation remains. They are calculated from process data after all special causes have been identified and removed and statistical stability has been achieved. The most common convention sets natural process limits at plus and minus three standard deviations from the process average, that is, $\bar{\bar{X}} \pm 3\hat{\sigma}$.

Specification limits, by contrast, do not come from the process. They are stated expectations from engineering, the customer, or a contract. The specification tells the team what the output must achieve to be acceptable. When the entire natural process spread lies well inside the specification interval (upper specification limit minus lower specification limit), the process is called capable.

### The Four-Quadrant Action Grid

The relationship between statistical control and specification conformance creates four possible states for a process. Figure 15.1 in the ASQ CSSGB Handbook places them on a two-by-two grid and prescribes the Green Belt’s response.

* **Quadrant 1: In statistical control AND meets specification.**  
  The process is predictable and capable. The situation is “good” and no immediate corrective action is required.

* **Quadrant 2: In statistical control but does NOT meet specification.**  
  The process is stable but consistently produces some out-of-specification material. Change the process itself to reduce variation or shift the average, or negotiate a realistic specification change with the customer.

* **Quadrant 3: Not in statistical control but meets specification.**  
  Many engineers in this quadrant argue that nothing needs to be done because the product is within specification. That argument is dangerous. An out-of-control process is unpredictable; the fact that all recent measurements fell inside specification does not guarantee that the next ones will. The Green Belt must investigate and remove the out-of-control conditions.

* **Quadrant 4: Not in statistical control AND does not meet specification.**  
  This is the worst case. Stop the process and immediately investigate assignable causes.

The grid makes clear that statistical control and specification conformance are separate qualities. A process can exhibit one without the other, and the Green Belt must treat each condition differently.

### Stability and the Use of Control Charts

Before natural process limits can be calculated, the process must reach statistical stability. Stability means that no special-cause signals appear on a control chart over a sufficient number of subgroups; commonly 20 or 30 subgroups of points are used. Figure 15.2 in the Handbook shows an $\bar{X}$ and $ R$ chart with plotted subgroups and the corresponding natural process limits. Subgroups that triggered SPC test rule violations are marked as square points. The accompanying test results report which rules failed and at which points. Modern software automates these tests, but interpretation and removal of assignable causes remain human tasks.

A crucial rule: the range chart must be in control before the average chart is examined. Variation must be stable before any adjustment to the process average can be meaningful. After removing special causes, the control limits are recalculated; only then can the team firm up the natural process limits and proceed to capability assessment.

Control charts such as $\bar{X}$ and $ R$ or $\bar{X}$ and $ S$ are robust to non-normality in the original data because of the central limit theorem. Nevertheless, when the final goal is to estimate the proportion of output outside specifications, the underlying distribution of the individual measurements must be normal. If a histogram or a normal probability plot shows severe departure from normality, a transformation such as the Box-Cox or Johnson transformation should be applied before computing capability metrics.

## Estimating Process Performance from Control Chart Data

Once the process is stable, the control chart provides the ingredients for a point estimate of the process standard deviation and, from that, the percentage of product that falls beyond each specification limit.

### Estimating Standard Deviation from the Average Range

For an $\bar{X}$ and $ R$ chart, the within-subgroup variation is captured by the average range $\bar{R}$. Under the assumption that the individual measurements are normally distributed, the process standard deviation $\hat{\sigma}$ is estimated by

$$
\hat{\sigma} = \frac{\bar{R}}{d_2}
$$

where  

* $\bar{R}$ is the average of the subgroup ranges,  
* $d_2$ is a statistical constant that depends on the subgroup size $ n $.  

Common values of $d_2$ are 2.059 for $ n=4$ and 2.326 for $ n=5$. The estimate becomes more precise as the number of subgroups increases.

### Computing Z Values

The distance from the process average to a specification limit is expressed in multiples of the estimated standard deviation. Two Z values are computed.

$$
Z_U = \frac{USL - \bar{\bar{X}}}{\hat{\sigma}}
$$

$$
Z_L = \frac{\bar{\bar{X}} - LSL}{\hat{\sigma}}
$$

where  

* $USL$ is the upper specification limit,  
* $LSL$ is the lower specification limit,  
* $\bar{\bar{X}}$ is the grand average of the subgroup means,  
* $\hat{\sigma}$ is the estimated process standard deviation.

A large positive $Z$ indicates that the specification limit is far from the average in standard deviation units, which means a small fraction of output falls outside that limit.

### Converting Z to Proportion Outside Specification

The standard normal probability density function is

$$
\phi(z) = \frac{1}{\sqrt{2\pi}} e^{-z^2/2}
$$

and the cumulative distribution function $\Phi(z)$ gives the area to the left of $ z $. The area beyond $ Z_U$ is \$1 - \Phi(Z_U)$, and the area beyond $ Z_L$ (lower tail) is $\Phi(-Z_L) = 1 - \Phi(Z_L)$. In practice, a standard normal table supplies these areas. The total proportion nonconforming is the sum of the two tail areas.

### Natural Process Limits

The natural process limits, using the $\pm 3\sigma$ convention, are

$$
L_{NPL} = \bar{\bar{X}} - 3\hat{\sigma}, \quad U_{NPL} = \bar{\bar{X}} + 3\hat{\sigma}.
$$

If these limits fall outside the $[LSL, USL]$ interval, the process is not capable of meeting the specification even when it is perfectly stable.

### Worked Example 1: Package Weight

A packing line is specified to produce packages weighing between 1.00 and 1.10 lbs. Data collected over 30 days, with a subgroup size of four every two hours, give a grand average $\bar{\bar{X}} = 1.065 \text{ lbs}$ and an average range $\bar{R} = 0.05 \text{ lbs}$. The control chart shows no special causes.

**Step 1: Estimate standard deviation.**  
For $n=4$, $ d_2 = 2.059$.

$$
\hat{\sigma} = \frac{0.05}{2.059} \approx 0.024 \text{ lbs}.
$$

**Step 2: Compute Z values.**  
$USL = 1.10$, $ LSL = 1.00$.

$$
Z_U = \frac{1.10 - 1.065}{0.024} = \frac{0.035}{0.024} \approx 1.46
$$

$$
Z_L = \frac{1.065 - 1.00}{0.024} = \frac{0.065}{0.024} \approx 2.70
$$

**Step 3: Obtain tail areas from a standard normal table.**  
The area beyond $Z_U = 1.46$ is \$0.0721$ (or 7.21%).  
The area beyond $Z_L = 2.70$ is \$0.0035$ (or 0.35%).

**Interpretation:** Approximately 7.21% of shipped packages are expected to be overweight, and 0.35% to be underweight. The total predicted nonconformance is \$7.21\% + 0.35\% = 7.56\%$.

**Step 4: Compute natural process limits.**

$$
L_{NPL} = 1.065 - 3 \times 0.024 = 0.993 \text{ lbs}, \quad U_{NPL} = 1.065 + 3 \times 0.024 = 1.137 \text{ lbs}.
$$

The natural limits 0.993 to 1.137 lbs fall outside the specification limits 1.00 to 1.10 lbs. This process is not capable. The Green Belt should first attempt to centre the process closer to the midpoint of the specification (1.05 lbs). If centring alone is insufficient, reducing variation becomes the priority.

If the $Z$ values had been larger, say $ Z_U = 4.0$ and $ Z_L = 4.5$, the predicted nonconformance would be negligible. A practitioner seeing such numbers would conclude the process is highly capable and might shift effort to other characteristics or consider whether the specifications could be tightened.

### Worked Example 2: Bearing Diameter

A machine shop produces bearings with a diameter specification of 10.00 mm to 10.40 mm. An $\bar{X}$ and $ R$ chart with subgroups of size five is maintained. After 25 subgroups, no special causes are present. The grand average is $\bar{\bar{X}} = 10.22 \text{ mm}$ and the average range is $\bar{R} = 0.12 \text{ mm}$. For $ n=5$, $ d_2 = 2.326$.

**Step 1: Estimate standard deviation.**

$$
\hat{\sigma} = \frac{0.12}{2.326} \approx 0.0516 \text{ mm}.
$$

**Step 2: Compute Z values.**

$$
Z_U = \frac{10.40 - 10.22}{0.0516} \approx \frac{0.18}{0.0516} \approx 3.49
$$

$$
Z_L = \frac{10.22 - 10.00}{0.0516} \approx \frac{0.22}{0.0516} \approx 4.26
$$

**Step 3: Tail areas.**  
From a standard normal table, the area beyond $Z_U = 3.49$ is about \$0.00024$ (0.024%). The area beyond $ Z_L = 4.26$ is approximately \$0.00001$ (0.001%). Total predicted nonconformance is roughly \$0.025\%$.

**Step 4: Natural process limits.**

$$
L_{NPL} = 10.22 - 3 \times 0.0516 = 10.065 \text{ mm}, \quad U_{NPL} = 10.22 + 3 \times 0.0516 = 10.375 \text{ mm}.
$$

Both natural limits lie inside 10.00–10.40 mm. The process is capable. Even a 1.5σ shift, as assumed in long-term sigma calculations, would leave substantial safety margin.

If the $Z_U$ had fallen below 1.5, the upper tail area would have been large, perhaps 7% or more, signaling an urgent need to reduce variation or shift the mean downward. The practitioner would then launch a root-cause investigation focused on the factors that push diameters toward the upper limit.

## Process Performance Metrics and Their Meaning

The Z-score approach gives a direct picture of process performance in the language of specification conformance. It answers the question “What percentage of output currently falls outside the customer’s limits?” without requiring the more formal capability indices (Cp, Cpk, Pp, Ppk) that are covered elsewhere in the Body of Knowledge. By working directly with the control chart’s $\bar{R}$ and $\bar{\bar{X}}$, the Green Belt ties performance assessment to the same data that monitors stability, reinforcing the principle that capability measurement is invalid unless the process is stable.

Organisations sometimes set internal specifications that are tighter than the customer’s specifications to provide an additional safety buffer. The same Z-score method applies: the internal limits serve as USL and LSL, and the resulting tail areas indicate the risk of violating the customer limits.

## Exam Tips

* Always verify that the range chart is in control before interpreting the $\bar{X}$ chart or computing capability metrics. A violation on $ R$ means the variation itself is unstable, making any $\hat{\sigma}$ unreliable.
* Memorise the formula $\hat{\sigma} = \bar{R} / d_2$. On the exam you may be given a table of $ d_2$ values corresponding to different subgroup sizes. Be ready to select the correct constant.
* When a process is out of control but still meeting specification (Quadrant 3), resist the temptation to do nothing. The correct answer is to investigate the out-of-control condition, because the process is unpredictable and may later produce defects without warning.
* If the total percent nonconforming from Z-table tail areas exceeds what the organisation tolerates, immediate actions are centring the process (shift the mean toward the centre of the specification) and then reducing variation. The exam may ask which action to take first.
* Be able to interpret the relationship between natural process limits and specification limits in plain language. If natural limits are wider than the specification, the process is not capable. If they are narrower, it is capable. This simple comparison often appears in multiple-choice questions.
* A high Z value (for example $Z \geq 3$) corresponds to a very small tail area; a low Z value (for example $ Z \leq 1.5$) indicates a substantial fraction of output outside the specification. Know how to use the standard normal table to convert between Z and tail areas quickly.