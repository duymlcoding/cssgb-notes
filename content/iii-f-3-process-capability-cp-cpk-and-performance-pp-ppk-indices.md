---
title: "Process Capability (Cp, Cpk) and Process Performance (Pp, Ppk) Indices"
description: "Detailed study notes on process capability and performance indices, including formulas, examples, Cpm, sigma level, and short-term vs long-term capability with sigma shift, grounded in ASQ CSSGB Handbook and CSSC training material."
---

## Overview

Process capability indices quantify how well a process output conforms to engineering specifications. They compare the natural process variation to the specification width and indicate whether the process is centered. Process performance indices serve a similar purpose but use overall sample standard deviation instead of an estimate of common-cause variation from a control chart. Practitioners use capability indices (Cp, Cpk, Cr) when a process is stable and variation is estimated from within-subgroup ranges. They use performance indices (Pp, Ppk, Cpm) when the data include long-term variation and shifts, or when control chart data are unavailable.

## Capability Indices: Cp, Cpk, and Cr

### Cp, Process Capability Index

Cp measures potential capability. It assumes the process is perfectly centred on the nominal value and shows how good Cpk could be if the process were centred.

$$C_p = \frac{\text{Tolerance zone}}{6\sigma}$$

The denominator $6\sigma$ captures the natural process spread (±3σ from the mean). The value $\sigma$ is the short-term standard deviation derived from control charts, typically $\sigma = \bar{R}/d_2$.

A larger Cp indicates less variation relative to the specification width. For example, Cp = 1 means the natural tolerance (±3σ) exactly matches the specification limits. Cp = 2 means the specification width is twice the natural spread, the requirement for a Six Sigma process (σ ≤ 1/12 of the specification).

### Cpk, Process Capability Index

Cpk accounts for both process spread and process centering. It is the smaller of two Z-scores divided by three.

$$C_{pk} = \frac{\min\!\left(Z_U,\;Z_L\right)}{3}$$

with

$$Z_U = \frac{USL - \mu}{\sigma}, \qquad Z_L = \frac{\mu - LSL}{\sigma}$$

- $USL $: upper specification limit
- $LSL $: lower specification limit
- $\mu $: process mean (estimated by $\bar{\bar{X}}$)
- $\sigma $: short-term standard deviation from control chart

Cpk is never larger than Cp. Equality occurs only when the process mean is exactly centered. A negative Cpk signals that the process mean lies outside the specification limits.

### Cr, Capability Ratio

Cr is the inverse of Cp, often expressed as a percentage.

$$C_r = \frac{1}{C_p}$$

Multiplying by 100 gives the percentage of the specification consumed by the process variation. Lower Cr values are better. For instance, Cr = 0.5 means the process uses 50% of the tolerance.

### Example 1: Cp and Cpk for a Stable Process

A shaft diameter has USL = 10.030 mm and LSL = 9.990 mm, tolerance = 0.040 mm. A control chart with subgroups of size 5 gives an average range $\bar{R} = 0.0070$ mm. The appropriate constant $ d_2 = 2.326$, so

$$\sigma = \frac{\bar{R}}{d_2} = \frac{0.0070}{2.326} = 0.00301 \text{ mm}$$

The process mean is $\bar{\bar{X}} = 10.014$ mm.

Compute Cp:

$$C_p = \frac{0.040}{6 \times 0.00301} = \frac{0.040}{0.01806} = 2.214$$

Compute Z-scores and Cpk:

$$Z_U = \frac{10.030 - 10.014}{0.00301} = \frac{0.016}{0.00301} = 5.315$$

$$Z_L = \frac{10.014 - 9.990}{0.00301} = \frac{0.024}{0.00301} = 7.973$$

$$C_{pk} = \frac{\min(5.315, 7.973)}{3} = \frac{5.315}{3} = 1.772$$

Interpretation: Cp = 2.21 indicates the process spread is less than half the tolerance width. Cpk = 1.77 is greater than 1.33, confirming the process is capable and centred reasonably well. If the mean had been far off-target, Cpk would be much smaller than Cp, revealing a centering problem that could be corrected without reducing variation.

### Example 2: Cp and Cpk at Barely Capable

A process fills containers to a target volume of 15.0 mL, with USL = 20.0 mL and LSL = 10.0 mL. Short-term σ = 1.667 mL. The process mean is exactly 15.0 mL.

$$C_p = \frac{20.0 - 10.0}{6 \times 1.667} = \frac{10.0}{10.0} = 1.0$$

$$Z_U = \frac{20.0 - 15.0}{1.667} = 3.0, \quad Z_L = \frac{15.0 - 10.0}{1.667} = 3.0$$

$$C_{pk} = \frac{3.0}{3} = 1.0$$

Interpretation: Cp = Cpk = 1.0 means the process is centred but just meets the specification. The expected defect rate is 0.27% (0.135% in each tail beyond ±3σ). If Cpk had been below 1.0, the process would be producing nonconforming units, and either centering or variation reduction would be required.

## Process Performance Indices: Pp and Ppk

Performance indices use overall sample standard deviation $s $, which captures all sources of variation (common and special causes) present in the data. They are used when the process is not in statistical control, when SPC data are unavailable, or when assessing supplier performance from incoming inspection records.

### Pp

$$P_p = \frac{\text{Tolerance zone}}{6 s}$$

where $s$ is the sample standard deviation:

$$s = \sqrt{\frac{1}{N-1} \sum_{i=1}^{N} (x_i - \bar{x})^2}$$

- $x_i $: individual measurements
- $\bar{x}$: sample mean
- $N $: number of measurements

### Ppk

$$P_{pk} = \min\!\left(\frac{USL - \bar{x}}{3 s},\; \frac{\bar{x} - LSL}{3 s}\right)$$

### Example 3: Pp and Ppk from a Manufacturing Line

A quality engineer measures a critical parameter with USL = 10.030, LSL = 9.990. A random sample of devices yields $\bar{x} = 10.014$, $ s = 0.004$.

Compute Pp:

$$P_p = \frac{0.040}{6 \times 0.004} = \frac{0.040}{0.024} = 1.667$$

Compute Ppk:

$$\frac{USL - \bar{x}}{3 s} = \frac{10.030 - 10.014}{3 \times 0.004} = \frac{0.016}{0.012} = 1.333$$

$$\frac{\bar{x} - LSL}{3 s} = \frac{10.014 - 9.990}{3 \times 0.004} = \frac{0.024}{0.012} = 2.000$$

$$P_{pk} = \min(1.333, 2.000) = 1.333$$

Interpretation: Pp = 1.67 shows that the overall variation could theoretically meet the specification if the process were centred. Ppk = 1.33 indicates the process is shifted toward the upper limit, reducing the margin. Both values meet a common contractual requirement of ≥ 1.33. If Ppk were less than 1.33, the process would need centering or a reduction in long-term variation.

### Example 4: Pp and Ppk from a Wide Sample

A teacher collects test scores from a class: USL = 100, LSL = 60. The sample mean $\bar{x} = 85.2$ and sample standard deviation $ s = 10.338$ (computed from the 15 scores: 67, 68, 73, …, 99).

$$P_p = \frac{100 - 60}{6 \times 10.338} = \frac{40}{62.028} = 0.645$$

$$P_{pk} = \min\!\left(\frac{100 - 85.2}{3 \times 10.338},\; \frac{85.2 - 60}{3 \times 10.338}\right) = \min(0.478, 0.813) = 0.478$$

Interpretation: Pp = 0.645 means the spread of scores far exceeds the specified range. Ppk = 0.478 shows the process mean is closer to the upper limit but still incapable. Substantial improvement is required to reduce variation and centre the performance.

## Cpm, Capability Index for a Target

Cpm is used when a process has a target value $T$ that may not be the midpoint of the specifications. It penalises deviation from $ T$ in addition to variation.

$$C_{pm} = \frac{USL - LSL}{6 \sqrt{s^2 + (\bar{x} - T)^2}}$$

- $s $: sample standard deviation
- $\bar{x}$: sample mean
- $T $: specification target

### Example 5: Cpm from a Mechanical Fit

For a length measurement, USL = 4.566 mm, LSL = 4.540 mm, target $T = 4.553$ mm. The dataset gives $\bar{x} = 4.54289$, $ s = 0.0031118$.

Compute the adjusted spread:

$$s^2 = (0.0031118)^2 = 9.683 \times 10^{-6}$$

$$(\bar{x} - T) = 4.54289 - 4.553 = -0.01011$$

$$(\bar{x} - T)^2 = 0.0001022$$

$$s^2 + (\bar{x} - T)^2 = 0.0001119$$

$$\sqrt{0.0001119} = 0.01058$$

$$C_{pm} = \frac{0.026}{6 \times 0.01058} = \frac{0.026}{0.06348} = 0.410$$

Interpretation: Cpm = 0.41 is low because both the variation and the offset from target are large relative to the tolerance. The process needs centering and variation reduction. If Cpm were close to Cp, the process would be on target.

When the process is perfectly centred on the target, $C_{pm} = C_p $. Using the Example 2 data (centred, $ s = 1.667$, tolerance = 10, $ T = 15$) gives $ C_{pm} = 10/(6 \times 1.667) = 1.0$.

## Sigma Level of a Process

The sigma level expresses the capability in terms of the number of standard deviations that fit between the process mean and the nearest specification limit, incorporating a 1.5σ shift to account for long-term dynamic variation.

A Six Sigma process satisfies $Cp \ge 2$, meaning the specification width is at least 12σ. When the process mean drifts by up to 1.5σ over time, the effective distance to the specification limit becomes $6\sigma - 1.5\sigma = 4.5\sigma $. The fraction defective then corresponds to a $ Z$ value of 4.5, which yields 3.4 defects per million opportunities total.

To calculate the sigma level from capability indices:

1. Obtain the short-term capability index Cpk.
2. Compute the short-term Z-score: $Z_{\text{ST}} = 3 \times Cpk $.
3. Add 1.5 to obtain the long-term sigma level: $\text{Sigma Level} = Z_{\text{ST}} + 1.5$.

Example: For the capable process in Example 1, Cpk = 1.772, so $Z_{\text{ST}} = 3 \times 1.772 = 5.316$. Sigma level $= 5.316 + 1.5 = 6.816$. This process exceeds six-sigma capability. If Cpk had been 1.33, sigma level would be $3 \times 1.33 + 1.5 = 5.49$, still a high level but leaving more defects.

## Short-Term vs. Long-Term Capability and the Sigma Shift

Short-term capability is calculated from data collected over a brief period (20–30 subgroups) under tightly controlled conditions. The variation is small because the data involve a single machine, homogeneous material, trained operators, and the same measuring equipment. The standard deviation used for Cp and Cpk comes from the within-subgroup variation (average range method).

Long-term capability reflects variation from many sources: different machines, spindles, cavities, operators, shifts, material lots, and environmental changes. The standard deviation used for Pp and Ppk is the overall sample standard deviation of individual measurements, which is generally larger.

The AIAG manual recommends comparing Cp/Cpk with Pp/Ppk to prioritise improvement. A large gap between Cp and Pp indicates that a substantial amount of variation comes from long-term sources; reducing these common-cause or special-cause sources will bring the long-term performance closer to the short-term potential.

The mean also shifts over time. The widely-used 1.5-sigma shift (advocated by Motorola) captures the typical drift of a process mean from the short-term setting. Figure 15.7 in the Handbook illustrates how a process centred at 3σ short-term produces 1350 ppm defective on each side, but after a 1.5σ shift, the same 6σ design yields only 3.4 ppm total defective. Figure 15.8 shows how short-term capability at different time points combines into a wider long-term distribution.

## Exam Tips

- Distinguish when to use Cp/Cpk (stable process, within-subgroup σ from $\bar{R}/d_2$) versus Pp/Ppk (overall sample s, non-stable or no control chart). The formulas share the same structure but employ different estimates of spread.
- Compute Cp and Cpk separately and interpret their relationship: Cpk ≤ Cp always. If Cpk is much smaller than Cp, centre the process first. If both are low, reduce variation.
- For a one-sided specification, calculate only the relevant side (upper or lower Cpk). The same logic applies to Pp and Ppk.
- Use Cpm when a target value drives function (for example, interference fits). The denominator adds squared offset from target to the variance, so Cpm penalises off-target condition more than Ppk.
- Convert Cpk to sigma level: multiply Cpk by 3 to get the short-term Z-score, then add 1.5 to estimate long-term sigma level. A true Six Sigma process has Cpk ≥ 2.0 short-term and yields 3.4 DPMO long-term after the 1.5σ shift.