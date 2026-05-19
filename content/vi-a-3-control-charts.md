---
title: "Control Charts in the Control Phase"
description: "Detailed study notes on variables and attributes control charts, construction, interpretation rules, and the distinction between control and capability, grounded in the ASQ CSSGB Handbook and CSSC Training Manual."
---

## Purpose of Control Charts

Statistical Process Control (SPC) charts serve as the primary tool to monitor process stability during the Control phase of DMAIC. They distinguish between common cause variation, which is intrinsic to the process, and special cause variation, which signals a real change. The control chart minimizes the net economic loss from overadjustment (tampering with a stable process) and underadjustment (failing to act when the process shifts). A process is in statistical control when both its average and variation are stable over time. Every control chart compares new subgroups against control limits derived from baseline data, making small process shifts visible that would otherwise go unnoticed.

## Variables Control Charts

Variables data provide richer insight because they reveal trends and patterns. Always analyze the range (or standard deviation) chart first to assess process variation, then examine the averages chart for shifts in central tendency.

### X-bar and s Chart

When subgroup sizes exceed 10, the X-bar chart for averages and the s chart for standard deviation produce more sensitive signals than the X-bar and R chart.

**Construction steps:**
- Collect at least 25 subgroups of constant size.
- Compute the subgroup mean (X-bar) and sample standard deviation (s) for each.
- Calculate the overall mean of subgroup means (X-double bar) and the average standard deviation (s-bar).
- Select constants A₃, B₃, and B₄ from standard tables based on subgroup size.

**Control limit formulas:**
- For the averages chart: UCL<sub>X-bar</sub> = X-double bar + A₃ × s-bar; LCL<sub>X-bar</sub> = X-double bar – A₃ × s-bar.
- For the standard deviation chart: UCL<sub>s</sub> = B₄ × s-bar; LCL<sub>s</sub> = B₃ × s-bar (B₃ may be zero for small n).

**Example:** With X-double bar = 7.126, s-bar = 0.0020, n = 5, A₃ = 1.628, B₄ = 2.266, B₃ = 0, UCL<sub>X-bar</sub> ≈ 7.129, LCL<sub>X-bar</sub> ≈ 7.123; UCL<sub>s</sub> ≈ 0.005, LCL<sub>s</sub> = 0.

### Individuals and Moving Range (ImR) Chart

Use the ImR chart when the rational subgroup size is one (for example, destructive testing or slow production). The moving range is the absolute difference between consecutive individual measurements.

**Control limit formulas:**
- UCL<sub>X</sub> = X-bar + E₂ × R-bar; LCL<sub>X</sub> = X-bar – E₂ × R-bar
- UCL<sub>MR</sub> = D₄ × R-bar; LCL<sub>MR</sub> = D₃ × R-bar (often zero)
Here, constants E₂, D₃, and D₄ correspond to a sample size of 2 because each moving range compares two successive values.

**Example:** For individual measurements averaging 288.3 with an average moving range of 2.889, E₂ = 2.660 gives UCL<sub>X</sub> ≈ 296 and LCL<sub>X</sub> ≈ 280.6; UCL<sub>MR</sub> ≈ 9.44, LCL<sub>MR</sub> = 0.

### Median Chart

When outliers are a concern, plot the sample median instead of the average. All individual data points appear on the chart, and the user connects the middle point of each sample. A physical range gage, cut to the distance between range control limits, is placed over the plotted points. If the gage cannot cover all points in a subgroup, the range exceeds the control limit. Trends in variation are harder to detect visually with this chart.

**Control limit formulas:**
- UCL<sub>med</sub> = X-tilde' + A'₂ × R-bar; LCL<sub>med</sub> = X-tilde' – A'₂ × R-bar
- UCL<sub>R</sub> = D₄ × R-bar; LCL<sub>R</sub> = D₃ × R-bar (often zero)
A'₂ is a special constant for medians.

## Attributes Control Charts

Attributes charts handle count data: defectives (conforming/nonconforming items) or defects (multiple flaws per unit). They require larger sample sizes (50 to 200) to fit binomial or Poisson distributions. Simplicity is offset by the increased sample volume needed for equivalent sensitivity.

### p-Chart (Proportion Defective, Varying Sample Size)

For binary classification of each item. Plot the fraction defective p = (number of defectives) / n.

**Control limits using average sample size n-bar:**
- p-bar = total defectives / total inspected
- UCL<sub>p</sub> = p-bar + 3 × √[p-bar (1 – p-bar) / n-bar]
- LCL<sub>p</sub> = p-bar – 3 × √[p-bar (1 – p-bar) / n-bar] (set to 0 if negative)

When a sample size deviates more than 25% from n-bar, recalculate limits for that subgroup according to AIAG guidance.

### np-Chart (Number Defective, Fixed Sample Size)

When sample size remains constant, plotting the count of defectives is often more straightforward.

**Formulas:**
- np-bar = total defectives / number of subgroups
- UCL = np-bar + 3 × √[np-bar × (1 – np-bar / n)]
- LCL = np-bar – 3 × √[np-bar × (1 – np-bar / n)] (set to 0 if negative)

### c-Chart (Number of Defects, Constant Sample Size)

Use when the area of opportunity is fixed and each unit can have multiple defects. Count total defects per subgroup.

**Formulas:**
- c-bar = total defects / number of subgroups
- UCL = c-bar + 3 × √c-bar
- LCL = c-bar – 3 × √c-bar (set to 0 if negative)

### u-Chart (Defects per Unit, Varying Sample Size)

For varying subgroup sizes, plot u = defects per unit.

**Control limits using average sample size n-bar:**
- u-bar = total defects / total units inspected
- UCL<sub>u</sub> = u-bar + 3 × √(u-bar / n-bar)
- LCL<sub>u</sub> = u-bar – 3 × √(u-bar / n-bar) (set to 0 if negative)

Recalculate limits when the sample size differs more than 25% from n-bar.

## Interpreting Control Charts

Begin by analyzing the range section for variables charts. A rise in range indicates increased variation within subgroups, possibly from worn bearings, loose fixtures, or inconsistent operator technique. Then examine the averages chart for shifts caused by tool wear, material changes, or altered machine settings.

**Basic out-of-control signals (from the CSSGB Handbook):**
- A point above UCL or below LCL (special).
- Run violation: seven or more consecutive points on one side of the centerline.
- 1-in-20 violation: more than one point in 20 falls in the outer third of the control limits region.
- Trend violation: five or more consecutive points increasing or decreasing, or a drift of seven or more points.

**Minitab's eight rules (consistent with the CSSC training tests):**
1. One point more than 3 standard deviations from the centerline (either side).
2. Nine points in a row on the same side of the centerline.
3. Six points in a row all increasing or all decreasing.
4. Fourteen points in a row alternating up and down.
5. Two out of three points more than 2 standard deviations from the centerline (same side).
6. Four out of five points more than 1 standard deviation from the centerline (same side).
7. Fifteen points in a row within 1 standard deviation of the centerline (either side).
8. Eight points in a row more than 1 standard deviation from the centerline (either side).

These correspond to the zones C (within ±1s), B (between 1s and 2s), and A (between 2s and 3s) on either side of the centerline.

**AIAG's six supplementary rules:**
- Points beyond the control limits.
- Seven consecutive points on one side of the average.
- Seven consecutive points consistently increasing or decreasing.
- Over 90% of plotted points in the middle third of the control limit region (for 25 or more subgroups).
- Fewer than 40% of plotted points in the middle third.
- Obvious nonrandom patterns (cycles, etc.).

Points that violate a rule are circled and investigated. Special causes should be confirmed via the process log or direct observation. Adjusting a stable process based on a single point near the target increases variation and destabilizes the process, a type II error where the hypothesis of a process change is accepted incorrectly. When an out-of-control condition is traced to a special cause, those points are excluded before recalculating tighter control limits. Conversely, a sustained improvement that pulls points close to the centerline without near-limit excursions should be preserved by standardising the change.

## Control Versus Capability

A process in statistical control is stable; its variation is predictable. That does not guarantee it meets customer specifications. Control limits are derived from process data (±3 standard deviations from the process average). Specification limits (USL, LSL) reflect customer requirements. A process can be in control but still produce output outside the specification range. Process capability (Cpk) quantifies this relationship: the sigma level is the number of standard deviations between the process center and the nearest specification limit, and Cpk is that sigma level divided by 3. A Cpk of 1.33 corresponds to 4-sigma performance, a widely accepted minimum. SPC charts must be monitored with both control and specification limits in mind.

## Exam Tips

- Given subgroup data, choose the correct chart type based on data type and sample size (variables with n > 10: X-bar and s; n = 1: ImR; attribute defectives constant n: np; attributes defects constant area: c; varying sample size: p or u).
- Compute control limits from the provided formulas and constants; always set LCL to zero when the calculation yields a negative number.
- Identify out-of-control conditions using the specific run, trend, and zone rules; know the difference between Minitab’s eight rules and AIAG’s additional rules about middle-third percentages.
- Interpret a control chart by examining the variation chart first, then the location chart; link chart signals to possible process causes such as tool wear, material changes, or measurement issues.
- Distinguish between control limits and specification limits; recognize that a controlled process may still be incapable of meeting customer requirements, and calculate sigma level or Cpk when given USL, LSL, and process standard deviation.
- Apply the 25% rule for recalculating p-chart or u-chart limits when a subgroup size differs from the average sample size by more than 25%.