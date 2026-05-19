---
title: "Measurement System Analysis"
description: "Comprehensive study notes for the ASQ Certified Six Sigma Green Belt (CSSGB) on Measurement System Analysis (MSA), covering gage R&R, linearity, bias, stability, and attribute agreement."
---

## Introduction

Measurement system analysis (MSA) examines the variation present in measurement data. Every process measurement passes through a measurement system, so the measurement system must be analyzed early in any improvement effort. Practitioners often discover that measurement error consumes 40 to 50 percent of the process specification. The sources of measurement variation include calibration, stability, repeatability, reproducibility, linearity, bias, accuracy, and precision. Until the 1990s, MSA was mostly confined to metrology laboratories. The advent of QS-9000 (now ISO/TS 16949) brought the practice into widespread industrial use. Even statistical process control experts now place an MSA study at the start of their SPC flow.

## Components of Measurement Error

**Calibration.** Drift in the average measurements of an absolute value over time. Calibration verifies that the gage reads accurately against a known standard.

**Stability.** Drift in absolute value over time. A measurement system is stable if its variation, plotted on a control chart, remains consistent and predictable.

**Accuracy.** Closeness of a measurement to the true value or an accepted reference value. Accuracy reflects the performance of the measurement tool itself, not the operator.

**Precision.** Closeness of repeated readings to one another. Precision is a random error component of the measurement system.

**Bias.** The difference between the measured average and a true (master) value. Bias is evaluated at multiple points across the measurement range.

**Linearity.** The accuracy of the measurement device across its entire operating range. A system may be accurate at one point but biased at another.

**Repeatability.** Variation when a single appraiser measures the same part on the same equipment under the same conditions over a short time. It is the equipment variation, expressed as a standard deviation.

**Reproducibility.** Variation when two or more appraisers measure the same parts multiple times. It captures operator-to-operator variation and is expressed as a standard deviation.

**Discrimination (resolution).** The smallest detectable unit or measurement resolution of the device. A rule of thumb is the 10-bucket rule: the instrument should measure to one-tenth of the tolerance or process spread. Inadequate resolution prevents detection of genuine process changes.

## Steps in a Gage Repeatability and Reproducibility (GR&R) Study

1. **Plan the study.** Confirm that the equipment is calibrated and in good condition, specimens are available and in good condition, and appraisers are trained in the measurement procedure. Use the appraisers who regularly perform the measurements. Anticipate contingencies; some studies take a long time.

2. **Select samples.** Handpick samples that span the full range of the process, including parts near or outside specification limits. Do not pick convenience samples from a production bin. Mark sample identifiers in a location not visible to the appraisers.

3. **Build a randomized experiment.** Create a table that randomizes the order of parts for each appraiser and each trial. Table 14.1 (from the AIAG reference) is an example using 10 parts, 3 appraisers, and 3 trials, with all 90 runs randomized.

4. **Execute measurements.** Call appraisers one by one according to the randomized table. Each appraiser measures every part in the assigned random order. An incomplete study produces imbalances that make calculations unreliable.

5. **Record data.** Enter the measurements into the data collection sheet organized by sample number and trial. The ASQ/AIAG data collection sheet (Figure 14.3) provides the structure.

6. **Compute intermediate statistics.**  
   - Row 16 (Part Average): average the three trials for each appraiser on each part.  
   - Row 17 ($ \overline{\overline{R}} $): average the ranges ($ R_a, R_b, R_c $) across appraisers.  
   - Row 18 ($ \overline{X}_{\text{DIFF}} $): difference between the largest and smallest appraiser average ($ \overline{X} $).  
   - Row 19 ($ \text{UCL}_R $): upper control limit for the ranges using $ \text{UCL}_R = \overline{\overline{R}} \times D_4 $, where $ D_4 = 3.27 $ for two trials and $ 2.58 $ for three trials. Circle any individual $ R $ value that exceeds this limit, investigate the cause, and if necessary repeat those readings.

## GR&R Report and Calculation Formulas

The AIAG Gage Repeatability and Reproducibility Report (Figures 14.5 and 14.6) partitions total variation into equipment variation (EV), appraiser variation (AV), part variation (PV), and total variation (TV). Constants $ K_1, K_2, K_3 $ depend on the number of trials, appraisers, and parts.

### Formulas in Display Math

**Equipment Variation (EV)**  
$$
EV = \overline{\overline{R}} \times K_1
$$
$ \overline{\overline{R}} $: average range across all appraisers.  
$ K_1 $: 0.8862 for 2 trials; 0.5908 for 3 trials.

**Appraiser Variation (AV)**  
$$
AV = \sqrt{ \left( \overline{X}_{\text{DIFF}} \times K_2 \right)^2 - \frac{EV^2}{n \times r} }
$$
$ \overline{X}_{\text{DIFF}} $: range of appraiser averages.  
$ K_2 $: 0.7071 for 2 appraisers; 0.5231 for 3 appraisers.  
$ n $: number of parts. $ r $: number of trials.

**Gage R&R (GRR)**  
$$
GRR = \sqrt{ EV^2 + AV^2 }
$$

**Part Variation (PV)**  
$$
PV = R_p \times K_3
$$
$ R_p $: range of part averages.  
$ K_3 $ depends on the number of parts (excerpts):  
- 2 parts: 0.7071  
- 3 parts: 0.5231  
- 4 parts: 0.4467  
- 5 parts: 0.4030  
- 6 parts: 0.3742  
- 7 parts: 0.3534  
- 8 parts: 0.3375  
- 9 parts: 0.3249  
- 10 parts: 0.3146  

**Total Variation (TV)**  
$$
TV = \sqrt{ GRR^2 + PV^2 }
$$

**Percentage of Total Variation**  
$$
\%EV = 100 \times \frac{EV}{TV} \qquad
\%AV = 100 \times \frac{AV}{TV} \qquad
\%GRR = 100 \times \frac{GRR}{TV} \qquad
\%PV = 100 \times \frac{PV}{TV}
$$

**Number of Distinct Categories (ndc)**  
$$
ndc = 1.41 \times \frac{PV}{GRR}
$$

**Precision/Tolerance Ratio (P/T)**  
$$
\%GRR_{\text{tol}} = \frac{100 \times GRR}{\text{Tolerance} / 6}
$$
The denominator covers 99.73% of the process spread (some practitioners use 5.15 for 99%).

### Numerical Example 1: Full GR&R from Figure 14.6

Given data from a completed study with 3 appraisers, 10 parts, 3 trials:  
$ \overline{\overline{R}} = 0.3417 $, $ \overline{X}_{\text{DIFF}} = 0.4446 $, $ R_p = 3.511 $, and $ n=10, r=3 $.

Step 1: EV  
$ EV = 0.3417 \times 0.5908 = 0.20188 $

Step 2: AV  
$ \overline{X}_{\text{DIFF}} \times K_2 = 0.4446 \times 0.5231 = 0.23258 $  
Square: $ 0.23258^2 = 0.05410 $  
$ EV^2 = 0.20188^2 = 0.04076 $  
$ \frac{EV^2}{n r} = \frac{0.04076}{30} = 0.0013587 $  
$ AV = \sqrt{0.05410 - 0.0013587} = \sqrt{0.05274} = 0.22963 $

Step 3: GRR  
$ GRR = \sqrt{0.04076 + 0.05274} = \sqrt{0.09350} = 0.30575 $

Step 4: PV  
$ K_3 $ for 10 parts = 0.3146  
$ PV = 3.511 \times 0.3146 = 1.10456 $

Step 5: TV  
$ TV = \sqrt{0.30575^2 + 1.10456^2} = \sqrt{0.09350 + 1.22005} = \sqrt{1.31355} = 1.14610 $

Step 6: Percentages  
$ \%EV = 100 \times (0.20188 / 1.14610) = 17.62\% $  
$ \%AV = 100 \times (0.22963 / 1.14610) = 20.04\% $  
$ \%GRR = 100 \times (0.30575 / 1.14610) = 26.68\% $  
$ \%PV = 100 \times (1.10456 / 1.14610) = 96.38\% $

Step 7: ndc  
$ ndc = 1.41 \times (1.10456 / 0.30575) = 1.41 \times 3.6124 = 5.094 \approx 5 $

Interpretation: The %GRR of 26.68% falls in the cautious zone (10–30%). The measurement system is acceptable depending on application, cost, and risk. With an ndc of 5, the system can distinguish enough categories for control charts and capability studies. If the result had been above 30%, the practitioner would need to improve the measurement system before using it for process control.

### Numerical Example 2: Precision/Tolerance Ratio

Assume the specification width (USL – LSL) for this dimension is 10 units.  
$ \text{Tolerance} / 6 = 10 / 6 = 1.6667 $  
$ \%GRR_{\text{tol}} = 100 \times 0.30575 / 1.6667 = 18.34\% $

Interpretation: With a 18.34% P/T ratio, the measurement system is in the caution zone (10–30%). If the ratio had been below 10%, the system would be fully acceptable; above 30% would demand corrective action.

## Interpreting GR&R Results

The AIAG guidelines divide results into zones. For % Study Variation:
- Less than 10%: acceptable.
- 10% to 30%: acceptable depending on application, cost, and repair factors.
- Greater than 30%: unacceptable; improvement required.

For % Contribution (of variance):
- Less than 1%: acceptable.
- 1% to 9%: conditionally acceptable.
- Greater than 9%: unacceptable.

Number of distinct categories:
- 1: can only detect conformance vs. nonconformance.
- 2–4: insensitive; coarse estimates of process parameters.
- 5 or more: suitable for control charts, process parameters, and capability indices.

The CSSC training manual provides a concise pass/caution/fail table for variable MSA:
| Element | Pass | Caution | Fail |
|-------------------------------|------------|------------|------------|
| % Study Variation | 0–10 | 10–30 | 30+ |
| % Tolerance | 0–10 | 10–30 | 30+ |
| % Contribution | 0–1 | 1–9 | 10+ |
| # Distinct Categories | 10+ | 6–10 | 1–5 |

## Effect of R&R on Capability

As GR&R increases, the observed capability ($ C_p $) becomes inflated relative to the actual process capability. For example, with an observed $ C_p $ of 1.0 and a GR&R of 50%, the actual $ C_p $ is 1.23. Reducing GR&R to 10% brings the observed $ C_p $ much closer to the true value, at 1.01. This relationship is shown graphically in Figure 14.10 of the ASQ Handbook. A poor measurement system masks process problems and can lead to mistaken conclusions about process capability.

## Linearity and Bias Study

Linearity studies assess whether the measurement bias changes across the operating range. Bias is evaluated by comparing measurements against master values. The ASQ Handbook provides an example (Table 14.2) where appraiser A measurements are compared to master values for 10 parts across a range.

From Minitab analysis:
- $ R^2 = 0.0\% $, indicating a severe nonlinearity problem. The relationship between bias and reference value is not linear, so the reported percent linearity is not valid.
- Average percent bias has a $ p $-value of zero, indicating statistically significant bias overall. The report also provides the percent bias at each reference point.

Causes of nonlinearity include improper calibration at the extremes, errors in master part measurements, worn instrument components, or inherent instrument design flaws. When nonlinearity is present, the practitioner must correct the gage or restrict its use to a range where linearity holds. After correction, the study should be repeated across a broader range.

## Common Errors in Performing GR&R

1. Selecting samples that do not cover the full tolerance spread. For process control applications, samples must span the entire range, including parts outside specification.
2. Failing to randomize the measurement sequence. This introduces knowledge bias, as appraisers may recall previous readings.
3. Using untrained appraisers or personnel who do not normally perform the measurement. This inflates reproducibility error.
4. Altering or damaging samples during the study (for example, accidental drops).
5. The experimenter is absent during the human-interaction portions, such as loading or alignment. Mistakes that occur may invalidate the entire study.
6. Publishing results with appraisers’ real names. This can create unhealthy comparisons and reduce future cooperation. Present results as Appraiser A, B, C.
7. Assuming GR&R results remain valid forever. Changes in methods, appraisers, settings, or firmware require periodic revalidation.
8. Assuming a GR&R study on one gage applies to all gages of the same type. Different usage conditions, environment, or appraiser pools can produce different results.

## Attribute Gage R&R

When the measurement system produces binary or categorical decisions (pass/fail, go/no-go), an attribute Gage R&R evaluates repeatability, reproducibility, and accuracy.

**Procedure from the CSSC Training Manual:**
1. Select at least two appraisers.
2. Select a set of samples with known reference attributes (from a master, best-available measurement). Label them discreetly.
3. Have each appraiser evaluate each sample in random order.
4. Record the judgment (for example, Pass or Fail).
5. Repeat the trial with the same samples in a newly randomized order.
6. Enter data into a table and compute agreements.

**Example (CSSC, 10 samples, 2 appraisers, 2 trials):**

| Sample | Actual | Appraiser 1 T1 | T2 | Appraiser 2 T1 | T2 | Overall Agreement? |
|--------|--------|---------------|----|---------------|----|-------------------|
| 1      | P      | P             | P  | F             | P  | No |
| 2      | P      | P             | P  | P             | P  | Yes |
| 3      | P      | P             | P  | P             | P  | Yes |
| 4      | F      | P             | F  | F             | F  | No |
| 5      | P      | P             | P  | P             | P  | Yes |
| 6      | F      | F             | F  | F             | P  | No |
| 7      | F      | P             | P  | F             | F  | No |
| 8      | P      | P             | P  | F             | F  | No |
| 9      | F      | F             | F  | F             | F  | Yes |
| 10     | P      | P             | P  | P             | P  | Yes |

Overall, the two appraisers agreed with each other and with the reference on only 5 of 10 samples, giving a reproducibility (agreement) of 50%. Appraiser 1 repeated his own judgments 90% of the time; Appraiser 2, 80% of the time. Accuracy against the master was 80% for Appraiser 1 and 70% for Appraiser 2. Such results indicate a measurement system that needs better operational definitions, training, or a different measurement method. A more reliable attribute study uses at least 20 samples.

## Additional MSA Considerations

**Resolution and the 10-Bucket Rule.** The measurement unit should be one-tenth of the tolerance or one-tenth of the process spread. If pipes must be within 5 mm, the gage should resolve to 0.5 mm. For time-based measurements, sampling frequency should be high enough to capture process changes.

**Stability Monitoring.** A measurement system is stable if its readings show no trends, shifts, or out-of-control signals on a control chart over time. If instability appears, investigate whether the gage or the process is the source.

**Accuracy and Calibration.** Before any GR&R study, verify the gage against a known standard. If a digital scale is used, calibrate with certified weights; if templates are used, compare them against verified rulers. Accuracy assessment focuses on the tool, while precision (R&R) also involves operators.

## Exam Tips

- Memorize the formulas for EV, AV, GRR, TV, and the appropriate K constants. Be able to compute them from a summarized data set like the one in Figure 14.6 without referring to software.
- Distinguish clearly between repeatability (within-appraiser, equipment variation) and reproducibility (between-appraiser variation). Be able to identify which part of the GR&R report each belongs to.
- Know the pass, caution, and fail criteria for %Study Variation, %Contribution, and ndc. Expect questions that provide a %GRR and ask whether the measurement system is acceptable.
- Understand how high GR&R inflates observed capability (Cp). Given an observed Cp and GRR percentage, you might be asked to infer the direction of the true capability.
- Recognize common GR&R execution errors and their consequences. For example, failing to cover the full specification spread yields an understated PV and an overstated %GRR.
- For attribute MSA, compute percent agreement and interpret whether an operational definition or training issue exists when agreement is low.