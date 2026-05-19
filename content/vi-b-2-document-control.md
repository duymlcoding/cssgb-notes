---
title: "Document Control"
description: "Study notes on document control within the Control phase of DMAIC, covering standardization, standard operating procedures, control plans, and visual management."
---

## Standardization and the Document Control Framework

Standardization locks in the gains achieved during the improvement process. The standardize–do–check–adjust (SDCA) cycle drives this activity: after a process change yields a new, stable level of performance, the team updates all process documentation and creates controls to sustain that level. Standard operating procedures (SOPs) form the backbone of that documentation. Organizations may call them work instructions, job aids, standard job practices, or level-three ISO 9001 documentation, but they all serve the same function.

Every SOP must address these details:
- What is the job?
- Where does the SOP apply?
- When does the SOP apply?
- Who is responsible?

Operators hold the responsibility to follow SOPs exactly as written. When a deviation becomes unavoidable, the operator must document what was done and why. That record becomes critical if a problem surfaces later and an investigation ensues.

An SOP exists as a living document. If a process change produces a new desirable level, the operator updates the SOP and all related documents immediately. Those updates then pass through a review by other affected functional areas and by technical experts, engineering, purchasing, shipping and receiving, and similar groups. That review validates the changes and builds support for deployment.

The plan–do–study–act (PDSA) cycle and the SDCA cycle work together to create a complete system for identifying processes, improving them, and applying lessons learned. When operators use both cycles, they sustain improvements with a constant eye on customer satisfaction.

## Control Plan Documentation

To sustain the improved process, Six Sigma teams produce a written control plan and hand it to the process owner. The control plan serves as a concise, easy-to-reference document that tells the business team when to monitor, how to monitor, what measurement range is acceptable, and what corrective action to take when the measurement falls outside that range.

Common elements of a control plan include:
- Company, division, or department name
- Name of the person who created the plan
- Date the plan was created
- Name of the person who last edited the plan
- Date the plan was last edited
- Project or process identifier
- Process owner
- List of process steps where control action is required
- CTQ or metric associated with each step
- Limit specifications (lower specification limit, LSL, and upper specification limit, USL) defining the acceptable range
- Unit of measurement
- Method of measurement
- Necessary sample size
- Frequency of measurement
- Person responsible for measurement
- Where the information is recorded
- Correction actions
- Associated policy and procedure documents

A control plan typically appears as a spreadsheet, a specialized digital document, or a hard-copy posting at a workstation. The chocolate bar example illustrates its use. For the step "Addition of sugar to batch," the plan specifies the CTQ as total amount added, an LSL of 4.90 cups and USL of 5.10 cups, a special six-cup sugar test bowl as method, a sample size of one batch, a frequency of every two hours, the mixer operator as responsible employee, a mix operation log spreadsheet as recording location, and corrective action that includes manual correction, machine calibration per SOP 100.54, testing the first batch after calibration, and reporting to the supervisor.

Specification limits (LSL and USL) are not the same as control limits. The LSL and USL represent the voice of the customer and define the acceptable product range. Control limits, in contrast, describe the natural variation of the process. A control plan focuses on specification limits so the operator can judge whether the output meets customer requirements.

When possible, teams automate measurement and data collection. Automation removes detailed measurement instructions from the control plan but does not eliminate the need for the plan itself. The document shifts its guidance toward reviewing automated data or control charts and taking action when signals appear.

## Visual Management as Document Control

Visual controls extend documentation to the physical workspace. Teams may install signs, posted matrixes and instructions, auditing boards that display individual or group performance over time, color coding, and safety signals. SOPs frequently become visual guides: a coffee shop might post a pictorial guide of ingredients for complex drinks, a medical unit might display hand-washing reminders, and an office copy machine shows pictorial instructions for loading paper or clearing jams. These visual documents reduce errors and help staff accept ownership of the improved process by making standardized procedures instantly accessible without consulting a written manual.

## Documenting Process Capability and Performance

Control charts add a powerful layer to documentation by providing ongoing evidence of process stability. A basic control chart contains:
- A line of plotted data points
- An x-bar line representing the average
- Lines at 1, 2, and 3 standard deviations above and below the average, creating zones C, B, and A (also called Zones 1, 2, 3)
- An upper control limit (UCL) at +3 standard deviations
- A lower control limit (LCL) at –3 standard deviations

Eight documented rules signal an out-of-control condition and trigger investigation or corrective action:

1. A single point falls outside the UCL or LCL. Likelihood of random occurrence is only 3 in 1,000.
2. Nine consecutive points lie on one side of the center line. A sustained shift has occurred.
3. Six points trend steadily upward or downward. The process is growing more or less efficient.
4. Fourteen points alternate up and down. This suggests variation across machines, shifts, or overcorrection.
5. Two out of three consecutive points land in the upper A section or the lower A section. Special causes create high variation.
6. Four out of five consecutive points appear in the upper B section (or beyond) or the lower B section (or beyond). A shift or major cause is likely.
7. Fifteen consecutive points fall within the C section above or below the centerline. Control limits may need recalculation.
8. Eight consecutive points lie on both sides of the center line but none in the C section. Mixed processes or resources may be present.

When a process is both in control and capable, teams also document sigma level and process capability (Cpk). Sigma level is the smaller of:

\[
\frac{USL - \bar{x}}{\sigma} \quad\text{or}\quad \frac{LSL - \bar{x}}{\sigma}
\]

Process capability equals sigma level divided by 3. A Cpk of 1.0 corresponds to a sigma level of 3; a Cpk of 1.33 corresponds to a sigma level of 4, the minimum many experts consider acceptable for customer satisfaction.

## Continual Improvement and Document Updates

Document control fits within the larger framework of continual improvement. W. Edwards Deming deliberately changed the term from "continuous" to "continual" to acknowledge that real processes sometimes step back or level off before advancing again. His system of profound knowledge, appreciation for a system, knowledge about variation, theory of knowledge, and psychology, guides how organizations maintain and improve quality through documentation.

Process improvement targets three components of variability: instability (lack of a stable operating process, with unchecked common and special cause variation), variation (the spread around a target), and off-target (the distance between the process center and the customer’s ideal). Process behavior charts help operators monitor stability. When processes are redesigned, operators must supply current information to engineers so that improved targets appear in updated SOPs and control plans. In this way, document control is not a single event but a recurring loop: standardize, do, check, adjust, and then standardize again.

## Exam Tips

- Recall the four questions an SOP must answer: what, where, when, and who.
- State that operators must follow SOPs as written and document any deviations with the reason.
- Identify common elements of a control plan, including LSL/USL, method, frequency, and corrective actions, and recognize a missing element in a sample.
- Distinguish between specification limits (LSL/USL) and control limits (UCL/LCL) in documentation; the control plan uses specification limits to assess acceptability for the customer.
- Describe the eight out-of-control tests for a control chart, because they often appear in control plans as triggers for corrective action.
- Explain that SOPs are living documents that must be updated immediately after the process reaches a new desirable level and reviewed by affected functional areas and technical experts.