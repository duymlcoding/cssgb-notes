---
title: "Visual Factory – Control Phase"
description: "Detailed study notes on visual controls and SPC chart interpretation for the Certified Six Sigma Green Belt exam, based on the official CSSGB Body of Knowledge."
---

## Visual Management and Visual Controls

Six Sigma teams deploy a visual factory to help business teams sustain a controlled process after improvement projects close. A control plan specifies monitoring and response actions, but visual controls make the plan tangible and immediately usable on the shop floor or in the office. Visual management includes any physical or digital display that conveys process status, standard work, or performance metrics at a glance. Examples of visual controls that teams can implement include the following.

- Signs that direct behaviour or indicate status.
- Posted matrixes and written instructions that simplify decision making.
- Auditing boards that let individuals or groups track performance over time.
- Color coding that classifies materials, areas, or conditions.
- Safety signals that warn of hazards.

These tools build on the 5S discipline, which creates an orderly workplace where abnormalities become instantly visible.

Standard operating procedures can be converted into visual representations on posters. A coffee shop, for example, might display a poster showing the exact ingredients for complex drink flavours, enabling employees to prepare beverages quickly while reducing ingredient errors. In a medical environment, visual reminders for hand washing and short pictorial guides for operating equipment help maintain safe practices. In offices, copy machines use pictures to show how to load paper, and LED screens display animated sequences to guide users through jam clearances. These realistic examples provide a pattern for Six Sigma teams to follow when creating documents that help business staff accept ownership of an improved process and preserve the gains.

Visual controls work because they eliminate the need to rely on memory or to pull out reference manuals during work. They embed process requirements directly into the work environment, making it easy to follow the standard and hard to deviate from it unintentionally.

## SPC Charts as Visual Controls

A control chart is one of the most common visual methods for monitoring a process after the Improve phase. It transforms process data into a time-ordered graph that lets the process owner detect changes quickly. A control chart may be displayed through an automated reporting system or dashboard, where responsible employees can view it as needed. When automated data collection is not available, a business analyst can collect data and present the chart periodically, although periodic analysis is less likely to catch a loss of control in real time.

### Control Chart Elements

A basic control chart contains the following elements.

- A line chart of data with plot points for individual data values.
- An x-bar line that represents the average of the data points.
- Lines above and below the x-bar line marking one, two, and three standard deviations from the centre in each direction.
- An upper control limit (UCL) line drawn at three standard deviations above the average.
- A lower control limit (LCL) line drawn at three standard deviations below the average.

The spaces between these lines are labelled as zones. Moving outward from the centre, the first zone is Zone C (or simply C), followed by Zone B, and finally Zone A, which lies closest to the control limits. These zones, also called Zones 1, 2, and 3, are the foundation for visual tests that reveal whether a process is out of control.

### Interpreting Control Charts: Eight Tests for Out-of-Control Conditions

The source identifies eight visual tests for detecting out-of-control conditions. Five of those tests are detailed below. Each test describes a pattern that, when observed, signals that the process is no longer stable and requires investigation.

**Test One: A single point outside the UCL or LCL.**  
A point beyond the three-sigma limits indicates a major problem. Immediate action is required. The probability of such an extreme value occurring purely by random chance is approximately three in one thousand.

**Test Two: Nine points in a row on the same side of the centre line.**  
This sequence suggests a sustained shift in the process mean. If the process owner knows that a deliberate change caused the shift, no action is needed; the control chart will eventually recalibrate around the new performance level. Otherwise, the process owner must investigate to identify the unexpected change.

**Test Three: Six points in a row that all increase or all decrease.**  
A consistent upward or downward trend over six points indicates that the process is becoming more or less efficient, or is generating fewer or more errors. The process owner should investigate unless a known, intentional reason explains the trend.

**Test Four: Fourteen points in a row that alternate direction, moving up and down.**  
This pattern can point to variation caused by alternating machines, different employees, rotating shifts, or overcorrection by operators. The process owner should search for systematic differences that produce the saw-tooth pattern.

**Test Five: Two out of three consecutive points fall in the upper Zone A or the lower Zone A.**  
When two of three neighbouring points land in the outermost zone on the same side of the centre line, a special cause is likely creating sudden, high variation. The process owner should investigate immediately to isolate the special cause before it affects more output.

Each test supplies a quick, rules-based way to assess process stability. By using these patterns, a process owner or a Green Belt can separate common-cause variation from signals that demand corrective action. When automated dashboards are in place, the system can highlight these violations in real time, enabling rapid response and long-term control of the improved process.

## Exam Tips

- Remember the zone labels: moving away from the centre, Zone C, Zone B, Zone A (or Zones 1, 2, 3). Test five depends on the outermost zone.
- For test two, link “nine points on one side of the centre line” with a process shift; distinguish between intentional, known changes and unknown disturbances.
- Distinguish trend (six points all up or all down) from simple runs above the centre line; trends indicate sustained change in one direction.
- Recognize that a single point beyond a control limit signals an extremely unlikely random event and demands immediate investigation.
- Connect visual factory tools such as auditing boards, colour coding, and SOP posters to the goal of making process standards visible and easy to sustain by the process owner.