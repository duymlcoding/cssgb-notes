---
title: "Audits"
description: "Study notes on audits in the Control phase of DMAIC, grounded in the ASQ CSSGB Handbook and the CSSC Training Manual."
---

## Overview of Audits in the Control Phase

During the Control phase, the Six Sigma team ensures the improved process continues to perform as intended after the project closes. Audits in this phase take the form of structured reviews and ongoing checks that verify changes are sustained and that corrective actions are taken when needed. The source material describes several audit-oriented activities: revisiting the Failure Modes and Effect Analysis to confirm improvements, deploying a control plan that specifies how to monitor performance, using statistical process control charts with defined visual tests, and conducting a final tollgate review. Each of these activities serves as an audit of the process, its controls, or the project deliverables.

## Revising the FMEA as an Audit of Risk

At the end of the Improve phase or the beginning of the Control phase, teams should revisit the FMEA originally used to identify potential failures. This reexamination acts as an audit of the risk landscape after solutions have been implemented.

The team follows a clear procedure. First, they note which recommended actions were completed. Next, they recalculate the risk priority numbers for the improved process. The updated FMEA then reveals whether the interventions reduced the likelihood or severity of failures, providing evidence that positive changes occurred. Because Six Sigma is a continuous improvement initiative, the revised FMEA also helps the team identify the next problem or root cause that could be addressed in a future project. In this way, the FMEA audit both validates past work and uncovers new risks.

## Control Plan: A Living Audit Tool

To maintain improvements, the team creates a written control plan and hands it to the process owner. The control plan functions as an ongoing audit mechanism: it tells the business team what to monitor, how to monitor, what range of data is acceptable, and how to respond with corrective action when measurements fall outside that range.

A complete control plan includes the following elements:

- Company, division, or department name
- Name of the person who created the plan
- Date the plan was created
- Name of the person who last edited the plan
- Date the plan was last edited
- Project and/or process name or identifier
- Process owner
- List of process steps where control action is required
- CTQ or metric associated with each action required
- Limit specifications, including lower and upper specification limits (LSL and USL)
- The unit of measurement
- The method of measurement
- The necessary sample size
- The frequency of measurement
- The person responsible for measurement
- Where the information is recorded
- Correction actions
- Associated policy and procedure documents

By specifying exactly how to measure, who does it, how often, and what to do when limits are broken, the control plan ensures a consistent audit of process performance. For example, the source presents a chocolate bar production case where a control plan defines how operators measure sugar addition and batch temperature, including corrective steps such as recalibrating the sugar disbursement machine per a standard operating procedure. The plan keeps the audit at the operator level whenever possible, minimizing downtime and reinforcing employee involvement.

## Statistical Process Control Charts for Continuous Auditing

One of the most common audit methods is the control chart. When data collection can be automated, the chart becomes a live dashboard that lets process owners and employees audit process stability at a glance.

A basic control chart contains:

- A line chart of data with plotted points
- An x-bar line representing the average of the data points
- Lines above and below the x-bar line that mark 1, 2, and 3 standard deviations from the center
- An upper control limit (UCL) line at 3 standard deviations above the center
- A lower control limit (LCL) line at 3 standard deviations below the center

The zones between the center line and the control limits are labeled C (nearest the center), B, and A, going outward in both directions. These zones support eight visual tests that allow quick detection of an out-of-control process.

The eight tests are as follows.

- Test one: A single point outside the UCL or LCL. This signals a major problem and requires immediate action. The probability of a random point falling beyond three standard deviations is about 3 in 1,000.
- Test two: Nine points in a row on one side of the center line. This indicates a sustained shift. If the shift was an intentional change, the chart will re-stabilize with the new data; otherwise, investigate.
- Test three: Six points in a row increasing or decreasing. This trend implies the process is drifting, becoming more or less efficient, or producing more or fewer errors.
- Test four: Fourteen points in a row alternating up and down. This pattern may point to variation from machines, employees, shifts, or overcorrection.
- Test five: Two out of three consecutive points in the upper A section (or in the lower A section). This suggests a special cause creating sudden high variation.
- Test six: Four out of five consecutive points in the upper B section or beyond, or in the lower B section or beyond. This can indicate a major causation or a shift similar to test four.
- Test seven: Fifteen consecutive points within the C section above or below the center line. This often means the control limits need recalculation because variation has decreased, or short-term variation is unusually tight.
- Test eight: Eight points in a row on either side of the center line with none in the C section. This pattern points to mixed processes (for example, two different sub-processes being charted together) or stark differences between operators.

These tests provide a straightforward audit routine. Process owners do not need deep statistical knowledge to learn the patterns, and they can focus on production or corrective actions rather than manual data documentation.

## Verifying Process Capability as Part of the Audit

Audits must also confirm that a process is not only stable but capable of meeting customer requirements. Control limits describe the voice of the process; specification limits describe the voice of the customer. A process can be in control yet produce off-spec output.

To audit capability, teams calculate the sigma level and the process capability index Cpk.

The sigma level is the smaller of the two calculations:

`(USL − x̄) / σ`  or  `(LSL − x̄) / σ`

where x̄ is the process median, σ is the standard deviation, USL is the upper specification limit, and LSL is the lower specification limit.

Process capability Cpk is the sigma level divided by 3. A Cpk of 1.33 corresponds to a sigma level of 4, which many experts consider the minimum for satisfying most customers. Organizations often target a Cpk of 2.0, with a minimally acceptable value of 1.5. Including capability calculations in the audit verifies that the improved process is truly delivering to customer expectations, not merely operating within its natural control limits.

## Control Tollgate Review as Final Audit

The final project-level audit occurs during the tollgate review with the sponsor or champion. The team uses a checklist to confirm that all control elements are in place:

- The new process’s performance and capability have been calculated.
- A written control plan has been communicated to the process owner.
- A monitor for the process has been created, either through manual data collection procedures or automated generation of control charts.
- The process owner and business team have received all tools and information needed to maintain the improvements.
- The sponsor, champion, or executive leadership has been informed about the state of the improvements.
- The team has met to reflect on the project and generate a list of ideas for future improvements.

This review ensures that the audit mechanisms are embedded in daily operations and that accountability for process control has been fully transferred.

## Exam Tips

- Remember that revisiting the FMEA serves as an audit: teams note completed actions and recalculate RPNs to confirm risk reduction.
- Know the list of common control plan elements; the exam may ask you to identify items that belong in a control plan.
- Learn the eight SPC visual tests for out-of-control signals by pattern and meaning, especially tests one (outside limits), two (run of nine on one side), and three (trend of six).
- Distinguish between control limits (process voice) and specification limits (customer voice), and recall that audits verify both control and capability.
- Associate the tollgate checklist with the final audit of project deliverables and handoff to the process owner.