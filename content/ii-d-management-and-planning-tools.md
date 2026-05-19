---
title: "Management and Planning Tools"
description: "Detailed study notes on the management and planning tools used in the Define phase of a Six Sigma project, including benchmarking, cause-and-effect diagrams, check sheets, FMEA, flowcharts, force-field analysis, Gantt charts, and others."
---

**BoK:** II-D  **Bloom's level:** Apply

## Introduction

Management and planning tools help a Six Sigma team define the problem, understand current processes, gather and organize information, and plan improvements. In the Define phase, these tools set the stage for effective measurement and root cause analysis. This section covers benchmarking, brainstorming, cause-and-effect diagrams, check sheets, customer feedback, failure mode and effects analysis (FMEA), flowcharts, focus groups, force-field analysis, Gantt charts, and an overview of graphical and statistical tools. Each tool is presented with its purpose, step-by-step procedure, and practical significance.

## Benchmarking

Benchmarking compares one system's processes to another's to identify ideas for improvement. It can be done internally (across departments) or externally (within or across industries). External benchmarking is often easier when performed against organizations outside the same industry because competitive barriers are reduced. All information obtained must be treated as confidential and for internal use only.

The benchmarking process follows eight steps:

1. Flowchart the current process.
2. Identify the areas to be improved.
3. Brainstorm ideas.
4. Investigate how others (internal and external) perform similar processes.
5. Develop plans for applying the ideas.
6. Pilot test the ideas.
7. Initiate the new process.
8. Evaluate the new process.

Before starting, the team must document the current process in detail. Flowcharting often reveals disagreements about the exact steps or their order, making it an essential first step. After researching how others operate, the team creates a change plan that includes required materials, timing, training, and other transition details. A pilot test is critical because even well-laid plans can have hidden problems.

## Cause-and-Effect Diagram (Fishbone, Ishikawa Diagram)

The cause-and-effect diagram, developed by Kaoru Ishikawa, graphically displays the factors (causes, *x*) that influence an outcome (effect, *y*). The relationship is expressed as $y = f(x)$. The tool works equally well for analyzing positive and undesirable effects. It organizes potential causes to help teams and management see the structure of a problem.

**Construction procedure:**

1. Define the effect to be studied and place it at the far right of the diagram.
2. Draw a central spine and add major cause categories. The six Ms are a common starting set: Man (people/operator), Machine (equipment), Methods (operating procedures), Materials, Measurement, and Mother Nature (environment). Management and Money are optional additions.
3. For each category, use brainstorming or the five Ws and one H (what, why, when, where, who, how) to generate detailed causes. Add them as branches off the main ribs.
4. Continue branching until all plausible causes are recorded, ensuring thorough exploration of potential root causes.

Figure 7.3 in the *ASQ CSSGB Handbook* shows a manufacturing team analyzing iron contamination in a product. Under “Machines,” the team identified specific reactor and pump numbers; “Calibration” appeared under both “Methods” and “Measurement,” illustrating that some causes interact across categories.

## Check Sheets

A check sheet is a simple data collection tool that pre-categorizes potential outcomes so an observer can tally occurrences quickly. It helps identify patterns and trends during process execution. The resulting data can feed attribute control charts and other analyses.

**Steps to create a check sheet:**

1. Identify and agree on the causes or conditions to collect.
2. Decide who will collect data, over what period, and by what method.
3. Design a check sheet that works within the operation.
4. Collect data consistently to ensure accuracy.

For example, a paint mixing process check sheet might list defect causes (operator misread instructions, wrong pigment, wrong color code, outdated base paint) with tally columns for each day of the week. Weekly and daily totals reveal where problems concentrate.

## Failure Mode and Effects Analysis (FMEA)

FMEA is a systematic tool for identifying potential failures in a process, assessing their impact, and prioritizing risks. Teams can begin an FMEA in the Measure phase or even late in Define, provided they have enough process knowledge. The FMEA produces a risk priority number (RPN) that guides improvement efforts.

**Procedure for building an FMEA spreadsheet:**

1. List all process steps or inputs in the first column.
2. For each step, identify what could go wrong (potential failure) and the effect on the customer.
3. Assign a Severity (SEV) rating from 1 (no effect) to 10 (endangers a process or person).
4. Identify the potential cause(s) of the failure and assign an Occurrence (OCC) rating from 1 (very unlikely) to 10 (almost inevitable).
5. Describe current controls that monitor or prevent the failure, then assign a Detection (DET) rating from 1 (automated detection that rarely fails) to 10 (no detection at all).
6. Calculate the RPN for each failure:

$$RPN = SEV \times OCC \times DET$$

**Worked example:**

A Six Sigma team improving refund processing creates two FMEA rows:

- **Row 1**: Process step: "Refund request is entered in system." Potential failure: "Incorrect amount is entered." SEV = 8. Potential cause: "Data-entry employee transposes numbers." OCC = 10. Current control: "Supervisor randomly reviews a sample." DET = 7.  
  $RPN = 8 \times 10 \times 7 = 560$

- **Row 2**: Process step: "Refund check is printed." Potential failure: "Printed check has defects." SEV = 9. Cause: "Printer misaligned or out of ink." OCC = 1. Control: "Signer reviews checks." DET = 2.  
  $RPN = 9 \times 1 \times 2 = 18$

The first failure has a much higher RPN (560 versus 18) and therefore receives priority during the Analyze and Improve phases. After changes are implemented, the team rescore SEV, OCC, and DET; if the new RPN is equal to or higher than the original, the change was ineffective.

Columns 10 through 15 (recommended actions, responsibility, action completed, rescored SEV, DET, RPN) are typically completed during the Improve phase.

## Flowchart

A flowchart depicts the separate steps of a process in sequential order, showing inputs, outputs, decision points, involved personnel, time per step, and process measurements.

**Basic flowchart development procedure:**

1. Define the process to be diagrammed and write its title.
2. Decide on boundaries: where the process starts and ends, and the required level of detail.
3. Brainstorm activities and write each on a card or sticky note without worrying about sequence.
4. Arrange the activities in proper sequence.
5. When everyone agrees on the sequence, draw arrows to show flow.
6. Review the flowchart with process participants (workers, supervisors, suppliers, customers) to verify accuracy.

Flowcharts can be high-level (as in Figure 7.5) or detailed (Figure 7.6), which includes decision diamonds and branches for credit checks, inventory status, and quality inspections.

## Force-Field Analysis

Force-field analysis examines the forces that drive toward a desired future state and those that restrain it. A team lists the goal as the future state, then brainstorms two columns: driving forces (help achieve the goal) and restraining forces (block achievement). The team ranks the items using a technique such as nominal group technique (NGT). Often, reducing or removing restraining forces yields more improvement than simply strengthening driving forces.

**Example:** Goal: "Number of errors is less than three per hundred documents."  
Driving forces include "Pressure from customer A," "Group incentive system," and "Use of control charts." Restraining forces include "Lack of training," "Inertia," and "Poor input data."

## Gantt Chart

A Gantt chart graphically displays a project's key activities, their durations, and their sequence over a calendar. It shows task milestones and dependencies between predecessor and successor tasks. A Gantt chart provides a quick visual assessment of the project's schedule, resource alignment, and performance against the plan. Delays or pull-ins on a single task immediately reveal the impact on the overall timeline.

## Graphical Charts, Control Charts, and Statistical Tools

Control charts study how a process changes over time by comparing current data to historical control limits. Data types determine chart selection:

- **Variables data** are measured on a continuous scale (time, weight, temperature) and use charts such as X– and R, X– and s, individuals (IX-MR), CUSUM, EWMA, and multivariate charts.
- **Attributes data** are counted and represent presence-or-absence criteria (errors count). Charts include p, np, c, u, D, and U charts.

Simple graphical tools such as bar charts and pie charts help convey customer feedback, defect data, and process performance. Caution: customer data usually comes from observational studies, where high correlation does not imply cause-and-effect relationships.

## Exam Tips

1. **Apply the FMEA RPN formula** straightforwardly. Expect a question that provides SEV, OCC, and DET for two failures and asks which gets priority.
2. **Identify the correct sequence** for benchmarking or flowcharting. The exam may list steps out of order; know exactly what comes first (flowcharting the current process, defining boundaries, etc.).
3. **Recognize force-field analysis** as a tool that categorizes driving and restraining forces, with an emphasis on reducing restraining forces rather than only boosting drivers.
4. **Distinguish between variables and attributes data** when selecting a control chart, and remember that continuous data provides more information and is preferred when feasible.
5. **Use check sheets for attribute data collection** and understand how they feed directly into Pareto charts and attribute control charts.