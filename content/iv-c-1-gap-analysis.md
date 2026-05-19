---
title: "Gap Analysis"
description: "Comprehensive study notes on gap analysis in the Analyze phase of DMAIC, covering comparative analysis, fishbone diagrams, 5 whys, X–Y matrix, root cause tree, and FMEA as found in ASQ CSSGB Handbook and CSSC Training Manual."
---

## Understanding Gap Analysis in the Analyze Phase

In the Analyze phase, a Six Sigma team examines the difference between current process performance and the desired target state. This difference defines the performance gap. Gap analysis requires pinpointing exactly where and when defects occur, brainstorming potential causes of the gap, drilling down to root causes, prioritizing those causes, and evaluating the risks associated with failures. The tools described below, drawn directly from the ASQ CSSGB Handbook and the CSSC Training Manual, enable teams to systematically diagnose and close the gap. Each technique brings a distinct form of analysis: comparison, causal brainstorming, layered questioning, quantitative scoring, tree-structured investigation, and risk assessment. Together they provide the precision necessary to link root causes to the observed gap and to select the most impactful improvements.

## Is/Is Not Comparative Analysis

Is/is not comparative analysis sharpens the definition of the problem by contrasting situations where the defect occurs against similar situations where it does not. The method refines the diagnosis and helps pinpoint the ranges, batches, or conditions where the defect source emerged. The team constructs a structured table with four dimensions: What, Where, When, and Size. For each dimension, the team lists exactly what is observed (the "Is" column) and what could have occurred but did not (the "Is Not" column). Finally, the team identifies differences and changes between the Is and Is Not conditions.

### Procedure

1.  Write a concise problem statement at the top of the table.
2.  Under "What," describe the specific object that has the defect and the exact defect observed. In the Is Not column, note similar objects that could have the defect but do not, and other defect types that might be expected but are absent.
3.  Under "Where," specify the geographical or physical location where the defect was first seen. For Is Not, list locations where the defect could have appeared but did not.
4.  Under "When," record the date and time the defect was first observed, any recurrence pattern, and the point in the product life cycle. For Is Not, note times when the defect could have appeared but was not observed.
5.  Under "Size," enter the number of defective objects, the number of defects per object, the defect magnitude, and any trend. For Is Not, state what size or count could have occurred but did not.
6.  Compare the two columns and record the Differences and Changes that distinguish the Is from the Is Not. These differences often point to special causes such as operator error, shipping damage, or deficient raw material.

Why this matters: Is/is not analysis transforms a vague problem into a sharp operational definition. It prevents the team from chasing causes that cannot logically produce the specific pattern of occurrence. The resulting contrast highlights the narrow conditions that must be addressed to close the gap.

## Cause-and-Effect (Fishbone) Diagram

The fishbone diagram organizes brainstorming about potential causes of a problem. The team sketches a fish skeleton, writes the problem at the head, and draws major bones to represent categories. Ideas generated during brainstorming are placed under the appropriate category, creating a visual map of candidate causes that contribute to the performance gap.

### Standard Categories

- Man
- Machine
- Material
- Method
- Maintenance
- Management
- Measurement
- Mother Nature
- Miscellaneous

Service industries often use a variation of the eight P’s:

- Product (service)
- Place
- People
- Process
- Promotion
- Productivity
- Price
- Physical evidence

An alternative structure uses the four S’s:

- Suppliers
- Systems
- Surroundings
- Skills

### Construction Steps (from CSSC Training Manual)

1.  Sketch a basic fishbone shape on a whiteboard or flipchart. Place a summarized problem statement where the head would be.
2.  Draw a spine and four major connectors. Label them People, Process, Materials, and Procedure. Additional connectors Equipment and Environment may be included.
3.  Explain the categories to the team, noting that some ideas may fit under more than one category.
4.  For each category, ask the team how something in that category might cause the problem or defect.
5.  Record ideas on sticky notes and place them on the diagram so they can be repositioned.
6.  Couple the brainstorming with the 5 Whys method. For each branch, ask "Why?" at least five times to drive to granular detail.
7.  Repeat for all categories until the team exhausts ideas.
8.  Review the diagram as a team. Move causes into appropriate categories and subsections to create an organized visual.
9.  Cross out causes that prove invalid after initial discussion.
10. Circle the potential root causes that seem most likely or highest priority for further investigation.

Why this matters: The fishbone diagram captures the collective knowledge of the team, structures it logically, and reveals relationships between ideas. It ensures that causes spanning many dimensions of the process are considered before any data-driven validation begins.

## 5 Whys

The 5 whys method asks "Why does this problem exist?" or "Why did this event occur?" repeatedly, each time driving to a more detailed level. The process continues until the true root cause, often lying within a system or process, is uncovered. The technique is called 5 whys because five iterations usually expose the root cause, although more may be needed. The sequential questioning becomes increasingly intensive, probing deeper into the contributing factors. By the fifth "why," the real gap requiring resolution typically becomes apparent.

### Procedural Guidance

When using the fishbone diagram, for each candidate cause the team asks "Why?" and appends the answer as a sub-branch. The next "Why?" targets that answer. This chain continues until the team reaches a cause that is actionable and systemic. The fifth iteration often reveals a process or system deficiency rather than a human error.

Why this matters: Without structured depth, teams may stop at superficial symptoms. The 5 whys forces the analysis past immediate explanations, uncovering the systemic issues that create the performance gap.

## Cause-and-Effect (X–Y) Relational Matrix

The X–Y relational matrix quantifies and prioritizes the impacts of various causes (X) on effects (Y) using numerical ranking. Teams assign impact scores based on objective data or subjective ordinal values. Additional weights can reflect customer importance, making it possible to focus on process inputs that have the greatest effect on the gap.

### Construction

A matrix is built with process inputs listed in rows and effects (or customer requirements) in columns. For each intersection, the team rates the strength of the relationship on a scale (commonly 1, 3, 5, or 9). A row total and percentage contribution are computed. The matrix in the Handbook example shows inputs such as customer input, equipment specs, bill of materials, and approval cycles, and scores them against efficiency, commonality, yield, and change implementation. The results allow formal prioritization of the causes that appeared on a fishbone diagram.

Why this matters: The matrix converts qualitative causal knowledge into a structured, prioritised list. It reveals which inputs account for the largest share of the gap, guiding resource allocation during the Improve phase.

## Root Cause Tree

A root cause tree visually connects the failure effect at the top to potential root causes and core problems. It combines the fishbone structure with the 5 whys, showing branching pathways that lead from the observed gap down through layers of causation. The tree can reflect different logical relationships.

- "Or" relationships: only one of several causes can lead to the effect.
- "And" relationships: multiple causes must occur together for the effect to materialize.
- Simultaneous effects: effects that appear at the same time once the causes are activated.

The tree uses codes to indicate status, weight, or activity. In the example from the Handbook, each box is marked with an opportunity level (High, Medium, Low) and a controllability rating (Within control, Have influence, No influence). Color coding draws attention to areas requiring more action.

### Application

The team begins with a failure statement at the top. They identify major branches (A, B, C, D…) representing different investigative approaches. Each branch breaks down into contributing causes, with deeper layers revealing more fundamental drivers. Boxes marked with high opportunity and within control are those the corrective action team can directly address to achieve the greatest impact. The tree becomes a traceable investigation map; tasks can be assigned against specific boxes.

Why this matters: The root cause tree captures complex causal interactions that a flat list cannot. It makes visible the logical gate conditions (AND/OR) that determine whether a root cause will trigger the failure, ensuring that the team does not waste effort on causes that cannot independently close the gap.

## Failure Mode and Effects Analysis (FMEA)

FMEA is a systematic activity set intended to recognize and evaluate potential failure modes of a product or process, assess the effects of those failures, and identify actions that could eliminate or reduce the chance of occurrence. It documents the entire process and provides a structured way to prioritize risks. Risk Priority Scores are calculated by multiplying severity, occurrence, and detection ratings. Mitigations must be determined and implemented for high-risk items. Once mitigations are completed, the FMEA is revisited and updated to re-evaluate the risk and verify that all high-risk items have been addressed. The root causes of failure are addressed and resolved through these mitigations.

Why this matters: FMEA serves as a forward-looking gap analysis, identifying where failures could occur in the design before they create an actual performance gap. In the Analyze phase, it can also be applied as a diagnostic tool to examine existing processes and uncover root causes associated with known defects.

## Exam Tips

- Differentiate Is/Is Not analysis from a simple check sheet. For the exam, expect to identify which dimension (What, Where, When, Size) clarifies the defect boundary and reveals differences that suggest special causes.
- Given a fishbone diagram with categories and cause branches, be prepared to select which category a new candidate cause belongs to, and identify which branch would be circled as a potential root cause requiring verification.
- For the 5 Whys, recognize that the drill-down should always push past human error toward a systemic or process-related root cause. If a "why" chain stops at a person, the analysis is incomplete.
- Interpret a partial X–Y relational matrix by calculating row totals and percentage contributions, then determine which input would be prioritized for the Improve phase.
- On a root cause tree, identify whether a cause-and-effect relationship is an "And" gate (all causes needed) or an "Or" gate (any single cause sufficient), and understand how controllability ratings guide corrective action assignment.