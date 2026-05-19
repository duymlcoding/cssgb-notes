---
title: "Control Charts in the Control Phase"
description: "Detailed study notes on variables and attributes control charts, construction, interpretation rules, and the distinction between control and capability, grounded in the ASQ CSSGB Handbook and CSSC Training Manual."
---

## Purpose of Control Charts

Statistical Process Control (SPC) charts serve as the primary tool to monitor process stability during the Control phase of DMAIC. They distinguish between common cause variation, which is intrinsic to the process, and special cause variation, which signals a real change. The control chart minimizes the net economic loss from overadjustment (tampering with a stable process) and underadjustment (failing to act when the process shifts). A process is in statistical control when both its average and variation are stable over time. Every control chart compares new subgroups against control limits derived from baseline data, making small process shifts visible that would otherwise go unnoticed.

## Variables Control Charts

Variables data provide richer insight because they reveal trends and patterns. Always analyze the range (or standard deviation) chart first to assess process variation, then examine the averages chart for shifts in central tendency.

### X-bar and R Chart

The most common variables chart pair for subgroup sizes of 2 to 10. The R chart monitors within-subgroup spread; the X-bar chart monitors subgroup averages.

**Construction steps:**
1. Collect at least 25 subgroups of constant size $n$.
2. Compute the subgroup mean $\bar{X}_i$ and range $R_i = X_{\max} - X_{\min}$ for each subgroup.
3. Compute the grand mean $\bar{\bar{X}}$ and average range $\bar{R}$.
4. Look up constants $A_2$, $D_3$, $D_4$ from the standard table for your subgroup size $n$.

**Control limit formulas — R chart (analyze first):**

$$
UCL_R = D_4 \bar{R} \qquad LCL_R = D_3 \bar{R}
$$

**Control limit formulas — X-bar chart:**

$$
UCL_{\bar{X}} = \bar{\bar{X}} + A_2 \bar{R} \qquad LCL_{\bar{X}} = \bar{\bar{X}} - A_2 \bar{R}
$$

> $D_3 = 0$ for $n \leq 6$, so the LCL of the R chart is zero for small subgroups.

### X-bar and s Chart

When subgroup sizes exceed 10, the s chart (using sample standard deviation) is more sensitive than the R chart.

**Construction steps:**
1. Compute the subgroup mean $\bar{X}_i$ and sample standard deviation $s_i$ for each subgroup.
2. Compute $\bar{\bar{X}}$ (grand mean) and $\bar{s}$ (average standard deviation).
3. Look up constants $A_3$, $B_3$, $B_4$ for your subgroup size $n$.

**Control limit formulas — s chart:**

$$
UCL_s = B_4 \bar{s} \qquad LCL_s = B_3 \bar{s}
$$

**Control limit formulas — X-bar chart:**

$$
UCL_{\bar{X}} = \bar{\bar{X}} + A_3 \bar{s} \qquad LCL_{\bar{X}} = \bar{\bar{X}} - A_3 \bar{s}
$$

**Example:** $\bar{\bar{X}} = 7.126$, $\bar{s} = 0.0020$, $n = 5$, $A_3 = 1.628$, $B_4 = 2.266$, $B_3 = 0$:

$$
UCL_{\bar{X}} = 7.126 + 1.628 \times 0.0020 = 7.129 \qquad LCL_{\bar{X}} = 7.126 - 1.628 \times 0.0020 = 7.123
$$

$$
UCL_s = 2.266 \times 0.0020 = 0.005 \qquad LCL_s = 0
$$

### Individuals and Moving Range (ImR) Chart

Use when rational subgroup size is one (destructive testing, slow production, or batch processes). The moving range is the absolute difference between consecutive measurements.

$$
MR_i = |X_i - X_{i-1}|
$$

**Control limit formulas — MR chart:**

$$
UCL_{MR} = D_4 \bar{R} \qquad LCL_{MR} = D_3 \bar{R}
$$

**Control limit formulas — Individuals chart:**

$$
UCL_X = \bar{X} + E_2 \bar{R} \qquad LCL_X = \bar{X} - E_2 \bar{R}
$$

Constants $E_2$, $D_3$, $D_4$ correspond to $n = 2$ because each moving range compares two successive values. Typical values: $E_2 = 2.660$, $D_4 = 3.267$, $D_3 = 0$.

**Example:** $\bar{X} = 288.3$, $\bar{R} = 2.889$, $E_2 = 2.660$, $D_4 = 3.267$:

$$
UCL_X = 288.3 + 2.660 \times 2.889 \approx 296.0 \qquad LCL_X = 288.3 - 2.660 \times 2.889 \approx 280.6
$$

$$
UCL_{MR} = 3.267 \times 2.889 \approx 9.44 \qquad LCL_{MR} = 0
$$

### Median Chart

When outliers are a concern, plot the sample median instead of the average. All individual data points appear on the chart; the user connects the middle point of each sample. A physical range gage cut to the distance between range control limits is placed over the plotted points.

**Control limit formulas:**

$$
UCL_{\tilde{X}} = \tilde{X}' + A'_2 \bar{R} \qquad LCL_{\tilde{X}} = \tilde{X}' - A'_2 \bar{R}
$$

$$
UCL_R = D_4 \bar{R} \qquad LCL_R = D_3 \bar{R}
$$

$A'_2$ is a special constant for medians from the standard table.

---

## Attributes Control Charts

Attributes charts handle count data: defectives (nonconforming items) or defects (multiple flaws per unit). They require larger sample sizes (50 to 200) to fit binomial or Poisson distributions.

| Chart | Data type | Sample size | Distribution |
|-------|-----------|-------------|--------------|
| p | Proportion defective | Varying | Binomial |
| np | Count defective | Fixed | Binomial |
| c | Count of defects | Fixed area | Poisson |
| u | Defects per unit | Varying | Poisson |

### p-Chart (Proportion Defective)

Plot the fraction defective $p_i = d_i / n_i$ for each subgroup.

$$
\bar{p} = \frac{\text{total defectives}}{\text{total inspected}}
$$

**Control limits (using average sample size $\bar{n}$):**

$$
UCL_p = \bar{p} + 3\sqrt{\frac{\bar{p}(1 - \bar{p})}{\bar{n}}} \qquad LCL_p = \bar{p} - 3\sqrt{\frac{\bar{p}(1 - \bar{p})}{\bar{n}}}
$$

Set $LCL_p = 0$ if the formula yields a negative number. Recalculate individual limits when a subgroup size deviates more than 25% from $\bar{n}$.

### np-Chart (Number Defective, Fixed Sample Size)

Use when sample size $n$ is constant. Plot the count of defectives directly.

$$
\overline{np} = \frac{\text{total defectives}}{\text{number of subgroups}}
$$

**Control limits:**

$$
UCL_{np} = \overline{np} + 3\sqrt{\overline{np}\left(1 - \frac{\overline{np}}{n}\right)} \qquad LCL_{np} = \overline{np} - 3\sqrt{\overline{np}\left(1 - \frac{\overline{np}}{n}\right)}
$$

### c-Chart (Count of Defects, Fixed Area of Opportunity)

Use when the area of opportunity is fixed and each unit can have multiple defects.

$$
\bar{c} = \frac{\text{total defects}}{\text{number of subgroups}}
$$

**Control limits:**

$$
UCL_c = \bar{c} + 3\sqrt{\bar{c}} \qquad LCL_c = \bar{c} - 3\sqrt{\bar{c}}
$$

### u-Chart (Defects per Unit, Varying Sample Size)

Plot $u_i = c_i / n_i$ (defects per unit) when subgroup sizes vary.

$$
\bar{u} = \frac{\text{total defects}}{\text{total units inspected}}
$$

**Control limits (using average sample size $\bar{n}$):**

$$
UCL_u = \bar{u} + 3\sqrt{\frac{\bar{u}}{\bar{n}}} \qquad LCL_u = \bar{u} - 3\sqrt{\frac{\bar{u}}{\bar{n}}}
$$

Recalculate limits when a subgroup size differs more than 25% from $\bar{n}$.

---

## Interpreting Control Charts

Begin by analyzing the range (or s, or MR) chart. A rise in spread indicates increased within-subgroup variation from worn tooling, loose fixtures, or inconsistent technique. Then examine the averages chart for shifts caused by tool wear, material changes, or machine settings.

**Basic out-of-control signals (ASQ CSSGB Handbook):**
- A point above UCL or below LCL.
- Run violation: seven or more consecutive points on one side of the centerline.
- 1-in-20 violation: more than one point in 20 in the outer third of the control region.
- Trend violation: five or more consecutive points increasing or decreasing.

**Minitab's eight rules (Western Electric rules):**

| Rule | Signal |
|------|--------|
| 1 | 1 point beyond ±3σ (Zone A) |
| 2 | 9 consecutive points on one side of centerline |
| 3 | 6 consecutive points all increasing or all decreasing |
| 4 | 14 consecutive points alternating up and down |
| 5 | 2 of 3 consecutive points beyond ±2σ (Zone B, same side) |
| 6 | 4 of 5 consecutive points beyond ±1σ (Zone C, same side) |
| 7 | 15 consecutive points within ±1σ (Zone C, either side) |
| 8 | 8 consecutive points beyond ±1σ (either side, no points in Zone C) |

Zones: C = within ±1σ, B = between 1σ and 2σ, A = between 2σ and 3σ.

**AIAG supplementary rules:**
- Points beyond control limits.
- Seven consecutive points on one side of the average.
- Seven consecutive points consistently increasing or decreasing.
- Over 90% of points in the middle third of the control region (25+ subgroups).
- Fewer than 40% of points in the middle third.
- Obvious nonrandom patterns (cycles, sawtooth, etc.).

Points violating a rule are circled and investigated via the process log. Adjusting a stable process based on a single point near the target increases variation (tampering). When an out-of-control point is traced to a confirmed special cause, exclude those points and recalculate tighter control limits.

## Control Versus Capability

A process in statistical control is stable but that does not guarantee it meets specifications. Control limits come from the process itself ($\pm 3\sigma$ from the process mean). Specification limits come from customer requirements.

$$
C_{pk} = \min\left(\frac{USL - \bar{X}}{3\hat{\sigma}},\; \frac{\bar{X} - LSL}{3\hat{\sigma}}\right)
$$

A $C_{pk}$ of 1.33 corresponds to 4-sigma performance and is the widely accepted minimum. Monitor SPC charts with both sets of limits in mind: a process can be in control yet still be incapable of meeting customer requirements.

## Exam Tips

- Choose chart type by data type and subgroup size: variables with $n > 10$ use X-bar and s; $n = 1$ uses ImR; attribute defectives with constant $n$ use np; attribute defects with constant area use c; varying sample size uses p or u.
- Always analyze the variation chart (R, s, or MR) before the location chart (X-bar).
- Set LCL to zero whenever the formula yields a negative value.
- Know the 25% rule: recalculate p-chart or u-chart limits individually when a subgroup size deviates more than 25% from $\bar{n}$.
- Distinguish Minitab's 8 rules from AIAG's 6 rules; know the zone definitions (A, B, C).
- Distinguish control limits from specification limits: a controlled process may still be incapable — compute $C_{pk}$ to assess capability.
