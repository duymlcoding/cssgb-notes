---
title: "Short-Term vs. Long-Term Capability and Sigma Shift"
description: "Detailed notes on process performance indices, the distinction between short-term and long-term capability, and the 1.5 sigma shift for the CSSGB exam."
---

## Process Performance Indices: Pp, Ppk, and Cpm

Process performance indices quantify how a process behaves over an extended period. Unlike capability indices that rely on within-subgroup variation, performance indices use the overall sample standard deviation, capturing both common and special cause variation. These measures are essential when a process is not in statistical control, or when only population-level standard deviation is available from incoming inspection or supplier data.

### Formulas for Pp and Ppk

The performance indices use the sample standard deviation $s$ of all individual measurements.

$$ Pp = \frac{USL - LSL}{6s} $$

where
$USL$ = upper specification limit,
$LSL$ = lower specification limit,
$s$ = sample standard deviation calculated from $s = \sqrt{\frac{1}{N-1}\sum_{i=1}^{N}(x_i - \bar{x})^2}$,
$\bar{x}$ = sample mean,
$N$ = total number of individual measurements.

$$ Ppk = \min\left( \frac{USL - \bar{x}}{3s},\; \frac{\bar{x} - LSL}{3s} \right) $$

The $Ppk$ index evaluates the distance between the process mean and the nearest specification limit relative to the spread. It is always less than or equal to $Pp$. If $Ppk$ equals $Pp$, the process is centered. A negative $Ppk$ indicates the mean lies outside the specification limit.

### The Cpm Index

When the process has an explicit target value $T$ that may differ from the midpoint of the specification range, the $Cpm$ index measures how well the process both meets specifications and stays on target.

$$ Cpm = \frac{USL - LSL}{6\hat{\sigma}} $$

where
$\hat{\sigma} = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(x_i - T)^2}$,
$T$ = target value,
$n$ = sample size, and $x_i$ are the individual measurements.

Unlike $Pp$, which measures deviation from the mean, $Cpm$ penalizes variation around the target. A $Cpm$ value less than 1 suggests the process has too much dispersion relative to the tolerance zone or is off-target.

### Advantages and Controversies

The AIAG and ANSI recommend using $Pp$ and $Ppk$ when a process is not in statistical control. This position is controversial. Montgomery writes that “the process performance indices $Pp$ and $Ppk$ are actually more than a step backwards. They are a waste of engineering and management effort, they tell you nothing.” Despite this criticism, $Pp$ and $Ppk$ serve a practical role when SPC data are unavailable. Many suppliers do not implement SPC, and those that do may be reluctant to share time-ordered process data. In those cases, a single sample of measurements and its overall standard deviation provide a rough indication of performance, provided the data follow a normal distribution.

## Short-Term vs. Long-Term Capability

Short-term capability studies collect data from a stable process over a brief interval, typically 20 to 30 subgroups. The variability is often small because the study focuses on a single machine, one batch of material, a small set of trained operators, and the same measurement equipment. In such studies, the standard deviation is derived from the average range or from the within-subgroup standard deviation, and the capability indices $Cp$ and $Cpk$ are calculated. These indices represent the inherent common-cause variation only.

Long-term capability reflects performance across a longer period that includes multiple machines, shifts, operators, material lots, and environmental changes. Variation is generally wider than in the short term. The sample standard deviation of all individual values replaces the within-subgroup estimate. The resulting indices are $Pp$ and $Ppk$. Both types of studies assume the data come from a normal distribution. Parameters such as flatness or wait time often require normalization via transformation techniques before capability analysis.

The process mean also shifts over extended periods. The concept of a 1.5-standard-deviation shift, advocated by Bill Smith of Motorola, accounts for this behavior. Figure 15.7 in the handbook illustrates how a short-term centered distribution can drift by about 1.5 standard deviations over time, drastically increasing the defect rate in the long term. The dynamic variation, shown in Figure 15.8, combines changes to both mean and standard deviation across time points.

## The 1.5 Sigma Shift and Sigma Level

The sigma level of a process quantifies its performance by relating the specification limits to the standard deviation. The short-term sigma level (or Z-bench) is

$$ Z_{ST} = \min\left( \frac{USL - \mu_{ST}}{\sigma_{ST}},\; \frac{\mu_{ST} - LSL}{\sigma_{ST}} \right) $$

where $\mu_{ST}$ and $\sigma_{ST}$ come from a short-term study (control chart-derived standard deviation).

Motorola’s convention states that a process will shift and drift by approximately 1.5 standard deviations over the long term. Therefore, the long-term sigma level is estimated as

$$ Z_{LT} = Z_{ST} - 1.5 $$

A process that is 6-sigma in the short term (specification width = ±6σ, centered, giving $Z_{ST}=6$) will exhibit a long-term performance equivalent to a 4.5-sigma process. Using standard normal probabilities, the fraction defective associated with a 4.5-sigma limit is

$$ P(Z < -4.5) \approx 3.4 \times 10^{-6} $$

or 3.4 defective parts per million. This is the origin of the 3.4 ppm defect level that defines Six Sigma quality.

To compute sigma level from long-term data directly, use the overall sample mean $\bar{x}$ and sample standard deviation $s$, and calculate $Z = \min( (USL - \bar{x})/s,\; (\bar{x} - LSL)/s )$. The result is the long-term sigma level; no further shift is applied because the data already incorporate the process drift.

## Numerical Examples

### Example 1: Computing Pp and Ppk from Assembly Line Data

A quality engineer measures a critical parameter on devices from a manufacturing line. The specification limits are $USL = 10.03$ and $LSL = 9.99$. From a sample of many units collected over weeks, the engineer obtains:

- Sample mean $\bar{x} = 10.014$
- Sample standard deviation $s = 0.004$

**Step 1: Calculate Pp**

$$ Pp = \frac{USL - LSL}{6s} = \frac{10.03 - 9.99}{6 \times 0.004} = \frac{0.04}{0.024} = 1.667 $$

A $Pp$ of 1.667 indicates that the overall process spread is narrower than the tolerance zone by a factor of 1.667. This index suggests that if the process were centered, it would meet the specifications with room to spare.

**Step 2: Calculate Ppk**

Compute the distance to each specification limit in units of $3s$:

$$ \text{Upper side} = \frac{USL - \bar{x}}{3s} = \frac{10.03 - 10.014}{0.012} = \frac{0.016}{0.012} = 1.333 $$
$$ \text{Lower side} = \frac{\bar{x} - LSL}{3s} = \frac{10.014 - 9.99}{0.012} = \frac{0.024}{0.012} = 2.0 $$

$$ Ppk = \min(1.333,\; 2.0) = 1.33 $$

**Interpretation:** The $Ppk$ of 1.33 equals the commonly accepted threshold for a capable process. However, the index is not equal to $Pp$, meaning the process is not centered; the mean is shifted toward the upper specification limit. If $Ppk$ had been below 1.0, the process would be producing units outside the engineering specifications. Since the data came from long-term production, the $Ppk$ value directly represents long-term capability. A practitioner seeing $Ppk = 1.33$ would monitor the centering to prevent drift that could push the index below the capability requirement.

### Example 2: Short-Term to Long-Term Shift and Sigma Level Calculation

A shaft machining process has specification limits $USL = 50.10$ mm and $LSL = 49.90$ mm. A short-term study using 25 subgroups yields:

- Short-term mean $\mu_{ST} = 50.02$ mm
- Short-term standard deviation $\sigma_{ST} = 0.02$ mm (estimated from $\bar{R}/d_2$)

**Step 1: Short-term Z-bench**

$$ Z_{USL} = \frac{USL - \mu_{ST}}{\sigma_{ST}} = \frac{50.10 - 50.02}{0.02} = \frac{0.08}{0.02} = 4.0 $$
$$ Z_{LSL} = \frac{\mu_{ST} - LSL}{\sigma_{ST}} = \frac{50.02 - 49.90}{0.02} = \frac{0.12}{0.02} = 6.0 $$

$$ Z_{ST} = \min(4.0, 6.0) = 4.0 $$

The short-term sigma level is 4.

**Step 2: Estimate long-term sigma level via the 1.5σ shift**

$$ Z_{LT} = Z_{ST} - 1.5 = 4.0 - 1.5 = 2.5 $$

A long-term sigma level of 2.5 corresponds to roughly 6,210 defects per million opportunities (from a standard normal table). This warns that the process will likely experience many defects over time due to drift.

**Step 3: Collect long-term data to verify**

After several weeks, the engineer gathers 100 individual measurements. The sample mean rises to $\bar{x} = 50.04$ mm and the sample standard deviation becomes $s = 0.03$ mm. The actual long-term Z-bench is

$$ Z_{USL} = \frac{50.10 - 50.04}{0.03} = \frac{0.06}{0.03} = 2.0 $$
$$ Z_{LSL} = \frac{50.04 - 49.90}{0.03} = \frac{0.14}{0.03} = 4.667 $$

$$ Z_{LT} = \min(2.0, 4.667) = 2.0 $$

The observed long-term sigma level of 2.0 is even worse than the 1.5-shift estimate, because the mean shifted more and the variation increased beyond the short-term study.

**Step 4: Compute Pp and Ppk from long-term data**

$$ Pp = \frac{50.10 - 49.90}{6 \times 0.03} = \frac{0.20}{0.18} = 1.111 $$

$$ \text{Upper side} = \frac{50.10 - 50.04}{3 \times 0.03} = \frac{0.06}{0.09} = 0.667 $$
$$ \text{Lower side} = \frac{50.04 - 49.90}{3 \times 0.03} = \frac{0.14}{0.09} = 1.556 $$

$$ Ppk = \min(0.667, 1.556) = 0.667 $$

A $Ppk$ less than 1.0 confirms the process is producing shafts outside the upper specification. The team must improve the mean centering and reduce variation. If the long-term $Ppk$ had instead remained above 1.33, the engineer would conclude the process retains adequate long-term capability despite the expected shift.

### Example 3: Cpm Calculation for a Targeted Process

A cylindrical part requires a target diameter of $T = 50.0$ mm, with $USL = 50.5$ mm and $LSL = 49.5$ mm. Five parts are measured: 49.9, 50.1, 50.0, 50.2, 49.8 mm.

**Step 1: Compute the target-centered standard deviation**

$$ \hat{\sigma} = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(x_i - T)^2} $$

Compute deviations from target $(x_i - 50)$:

- 49.9 → -0.1 → squared 0.01
- 50.1 → 0.1 → 0.01
- 50.0 → 0 → 0
- 50.2 → 0.2 → 0.04
- 49.8 → -0.2 → 0.04

Sum of squares = $0.01 + 0.01 + 0 + 0.04 + 0.04 = 0.10$

$$ \hat{\sigma} = \sqrt{\frac{0.10}{5-1}} = \sqrt{0.025} = 0.1581 $$

**Step 2: Compute Cpm**

$$ Cpm = \frac{USL - LSL}{6\hat{\sigma}} = \frac{50.5 - 49.5}{6 \times 0.1581} = \frac{1.0}{0.9486} = 1.054 $$

A $Cpm$ of 1.054 indicates the process variation around the target just meets the capability threshold. If the target is critical, such as for a specific mechanical fit, the team should reduce variation or better center the process. A $Cpm$ below 1.0 would require immediate corrective action.

## Exam Tips

- Distinguish the source of standard deviation: $Cp$, $Cpk$ use within-subgroup variation; $Pp$, $Ppk$ use overall sample standard deviation. If the problem describes SPC subgroups, calculate capability indices; if data come from a single large sample or inspection, calculate performance indices.
- When a process has a specific target different from the specification midpoint, compute $Cpm$ using deviations from the target, not from the mean.
- Remember the relationship: $Ppk \leq Pp$ always. If $Ppk$ is negative, the process mean has moved outside a specification limit.
- For the sigma shift, the long-term sigma level equals the short-term Z-bench minus 1.5. If a question states a process is 6 sigma, it implies a short-term Z of 6, yielding 3.4 ppm long-term defects.
- Interpret numerical results in context: a $Pp$ of 2.0 but $Ppk$ of 0.8 tells you the process potential is excellent but the mean is mis-centered and defects are being produced. In such a case, center the process before attempting to reduce variation.