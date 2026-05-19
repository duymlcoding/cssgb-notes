---
title: "SPC Basics"
description: "Study notes for the ASQ CSSGB exam covering statistical process control, variation classification, control charts, process capability, and sustaining control through control plans and visual management."
---

## Statistical Process Control and the Control Phase

Statistical process control (SPC) applies to any process, whether in manufacturing, an office, a sports team, or a household. A histogram provides a visual picture of variation and center, while the mean and standard deviation give numerical comparisons. Once a process is brought into statistical control, teams can introduce changes to see whether they shift the process average or alter the variation (range). The ultimate goal of process improvement is to reduce the amount of variation present, and SPC provides the framework for monitoring stability and guiding that reduction.

## Process Variation: Common and Special Causes

Walter Shewhart developed control charts in the 1920s to separate assignable (special) variation from the chance (common) variation that exists in every stable process. Every process has variation. That variation can be physical or mechanical (tool, machine, maintenance, equipment, environment) or procedural (operator, accuracy, legibility, workload). The specification limits reflect the voice of the customer; the process variation reflects the voice of the process.

Two categories of variation must be distinguished.

**Common causes** of variation are inherent to the process and generally cannot be controlled by operators. They are also called natural variation and represent the many sources of variation within a system that is in statistical control. Common cause variation can be described by its location (process average), spread (piece-to-piece variability), and shape (distribution), which together make the process predictable.

**Special causes** of variation are unusual events that an operator can usually remove or adjust when properly alerted. They are sometimes called assignable causes. Unless all special causes are identified and mitigated, the process output will be influenced unpredictably, producing random results. The principal purpose of control charts is to recognize the presence of special causes so that appropriate action can be taken.

A process is in statistical control when only common causes remain after special causes have been removed. While statistical techniques can detect both types, common causes are more difficult to isolate and remove than special causes.

### Avoiding Overadjustment and Underadjustment

Confusing the two types of variation leads to costly mistakes. Adjusting a process in response to common cause variation results in more variation, not less, a phenomenon called overadjustment or overcontrol. Failing to respond to a special cause allows that cause to continue producing additional variation, known as underadjustment or undercontrol. A practical exercise from the handbook uses a stopwatch to record daily travel times to work or school, asking the student to identify which sources of variation are common and which are special.

## Data Types and Chart Selection

Selecting the correct SPC method depends on whether the data are discrete or continuous.

**Discrete data**, also called attributes data, produce outcomes limited to a small set of values (pass/fail, true/false, or counts like 0, 1, 2, 3). Probability distributions from such data include the uniform, binomial, and Poisson distributions. Attributes control charts track deficiencies such as units defective, percentage defective, defects per unit, or the total number of defects in a sample. These charts do not require detailed measurements, only simple indicator assignments.

**Continuous data**, or variables data, come from measurements on a continuous scale (length, weight, resistance). The distribution may be normal, lognormal, or some other form. Variables control charts can incorporate measures of central tendency (averages) or variation (range). Averages are more sensitive to change than individual readings.

## Control Charts as Process Behavior Tools

The term "process behavior chart" is used deliberately to emphasize that the focus is on how the process behaves, not on the people operating it. Shewhart laid the foundations, and while over thirty different charts exist, practitioners regularly use only six or seven. Control charts serve three purposes: to attain a state of statistical control, to monitor the process, and to determine process capability. They provide an early warning indicator that something needs to be adjusted or changed to bring the process back into control. A state of statistical control means only random (common) causes are present; it does not guarantee that products meet specifications. Conversely, a process not in statistical control may still produce conforming product.

### Elements of a Control Chart

Every control chart includes a line chart of plotted data points. An x-bar line (the process average) runs through the center. Above and below the x-bar line, lines represent 1, 2, and 3 standard deviations from the center. The Upper Control Limit (UCL) is set at 3 standard deviations above the average, and the Lower Control Limit (LCL) at 3 standard deviations below the average. The areas between the centerline and the control limits are divided into zones, typically labeled from the center outward as Zones C, B, and A (sometimes called Zone 1, Zone 2, Zone 3). These zones form the basis of visual tests for out-of-control conditions.

### Constructing and Setting Up Control Charts

A formal sequence establishes a control chart.

1. **Choose the characteristic to chart.** Select what is defective and also controllable or adjustable by the worker.
2. **Identify the process variables and conditions** that contribute to the product outcomes and characteristics.
3. **Decide between attributes and variables data.** Attributes charts require discrete measurements and are useful when the defective rate is high enough to appear with a reasonable subgroup size. Variables charts require measurements on a continuous scale.
4. **Determine the earliest point in the process** where testing can yield information about assignable causes. Earlier identification allows more effective containment and mitigation.
5. **Choose the specific chart type.** For example, an X-bar and R chart plots both the subgroup average and range.

To attain statistical control, gather data from at least 25 subgroups. Maintain a log of process changes during data collection. Compute trial control limits from the data, chart each subgroup, identify and eliminate assignable causes of excessive variation, and then maintain the control measures. Control limits are placed at ±3 standard deviations from the estimated process mean.

### Operating Characteristic (OC) Curve

The OC curve plots the true value of a process parameter against the probability that a single sample will fall within the control limits. It illustrates the chart’s ability to detect process changes and shows the probability of accepting the original hypothesis as reflecting the population's true value. The curve highlights the risk of a type II (β) error for one- or two-tail tests.

## Detecting Out-of-Control Conditions: The Eight Tests

When a control chart is displayed, eight visual tests quickly indicate whether a process has gone out of control. These tests rely on the zones around the centerline.

- **Test 1:** A single point falls outside the UCL or LCL. This signals a major problem requiring immediate action; the chance of a random point beyond 3 standard deviations is only 3 in 1,000.
- **Test 2:** Nine points in a row appear on one side of the centerline. This indicates a sustained shift in the process. If the shift was intentional, the chart will eventually restabilize; otherwise, investigation is needed.
- **Test 3:** Six points in a row steadily increase or decrease. This trend suggests the process is becoming systematically more or less efficient or generating progressively more errors.
- **Test 4:** Fourteen points in a row alternate up and down. This pattern often points to variation in machines, operators, shifts, or overcorrection.
- **Test 5:** Two out of three consecutive points lie in the upper Zone A or the lower Zone A (within 1 standard deviation of the control limit). This reflects a sudden high variation due to a special cause.
- **Test 6:** Four out of five consecutive points lie in the upper Zone B or beyond, or the lower Zone B or beyond. This indicates a major causation problem or a shift similar to Test 4.
- **Test 7:** Fifteen points in a row fall within Zone C (the inner third) on either side of the centerline. This suggests the control limits are no longer relevant. If variation has been reduced, limits should be recalculated. It can also occur temporarily when short-term variation is unusually small.
- **Test 8:** Eight points in a row lie on either side of the centerline, but none fall in Zone C. This may indicate mixed processes or a major difference in performance between two operators or teams.

These tests can be taught to process owners and operators without requiring deep SPC expertise, making control charts practical for daily monitoring.

## Control Versus Capability

A process can be in statistical control (stable, with only common cause variation) yet fail to meet customer requirements. A capable process has not only low variation but also outputs centered around the customer’s target. Specification limits define the acceptable range; control limits define process stability. Both are necessary.

### Sigma Level and Process Capability (Cpk)

Sigma level is the number of standard deviations between the process center (the median) and the nearest specification limit. It is calculated as the smaller of:

(USL − x̄) / σ   or   (x̄ − LSL) / σ

Process capability, denoted Cpk, equals the sigma level divided by 3. A Cpk of 1.33 corresponds to a sigma level of 4, which many experts consider the minimum level for customer satisfaction. Organizations often aim for a Cpk of 2.0, with a minimum acceptable value of 1.5.

## Sustaining Improvements: Control Plans, Visual Management, and FMEA Revision

During the Control phase, the Six Sigma team must transfer the improved process back to the process owner. A written control plan provides concise, easy-to-reference instructions for ongoing monitoring. Common elements include the company name, the plan creator and date, the process owner, process steps requiring control action, the CTQ or metric, specification limits (LSL and USL), unit of measurement, measurement method, sample size, frequency, responsible employee, data recording location, corrective actions, and references to associated policies and procedures.

A control plan example for a chocolate bar process specifies that for the step "Addition of sugar to batch," the total amount added must lie between 4.90 and 5.10 cups, measured with a 6-cup sugar test bowl every two hours. Corrective actions include manual measurement and machine calibration. Whenever possible, corrective actions should be built at the process level to minimize downtime and empower operators. Automated data collection and generation of control charts are preferred, but when not feasible, a manual collection and charting procedure is defined.

Visual management complements control plans. Tools include signs, posted matrices, auditing boards, color coding, safety signals, and pictorial standard operating procedures. Examples range from ingredient posters in a coffee shop to hand-washing reminders and equipment-loading diagrams on copy machines.

The team should also revisit the FMEA originally developed in earlier phases. Recalculating risk priority numbers after implemented actions shows the positive changes achieved and helps identify the next root causes that might be addressed in future improvement cycles.

## Team Closure and Tollgate Review

When the process is deemed capable and in control and the transfer to the business team is complete, the team holds a celebration and reflection meeting. This meeting closes loose ends, recognizes contributions, and captures lessons learned. Team members brainstorm ideas for future improvement projects while the details are still fresh. A control tollgate checklist confirms that the process capability has been calculated, a control plan has been written and communicated, a monitor (manual or automated) has been established, the process owner and business team have all required tools and information, the sponsor has been informed, and the team has met to reflect and generate future improvement ideas.

## Exam Tips

- Differentiate special and common causes by their controllability and effect on predictability, and recognize examples such as overadjustment (tampering with a stable process) versus underadjustment (ignoring a shift).
- Given a scenario with data types, determine whether an attributes chart or a variables chart is appropriate based on whether measurements are continuous or discrete.
- Memorize the eight out-of-control tests by linking each pattern (for example, one point beyond limits, nine points on one side, six-point trend) to its interpretation so you can diagnose a chart on the exam.
- Calculate sigma level and Cpk from provided values of USL, LSL, x̄, and σ, and relate Cpk values to sigma levels (for example, Cpk 1.33 equals 4 sigma).
- Identify the required elements of a control plan and explain how a well-structured plan ensures a monitored, sustainable handoff to the process owner.