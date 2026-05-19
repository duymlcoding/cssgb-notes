---
title: "Root Cause Analysis"
description: "Detailed notes on root cause analysis tools and techniques for the Analyze phase of DMAIC, grounded in the ASQ CSSGB Handbook and CSSC Training Manual."
---

## Root Cause Analysis in the Analyze Phase

When a Six Sigma team reaches the Analyze phase without a clear understanding of primary causation, root cause analysis becomes the central activity. The goal is to move from a defined problem or defect to verified root causes that can be addressed in the Improve phase. A variety of structured tools support this process. Some of them, such as the fishbone diagram or Failure Mode and Effects Analysis (FMEA), may also be used in Define or Measure at the discretion of the project leader, but they are especially critical for systematic diagnosis during Analyze. The Black Belt and Green Belt typically lead the analysis, reporting findings to the team, while subject matter experts provide process knowledge. All suspected root causes must be verified through data before solutions are implemented.

## Cause-and-Effect Diagram (Fishbone)

The fishbone diagram is a brainstorming tool that helps a team generate, organize, and visualize possible causes of a problem. The diagram resembles a fish skeleton, with the problem statement at the head and major cause categories branching from a central spine. The collaborative nature of the exercise encourages full team participation and lays the groundwork for a creative, well-grounded solution.

### Creating a Fishbone Diagram

Follow these steps, which couple the fishbone with the 5 Whys method:

1.  Draw the basic fishbone shape on a whiteboard or large flipchart. Write a concise version of the problem at the "fish head." The problem can be the project's original problem statement or a specific defect uncovered during the Define or Measure phase.
2.  Draw a horizontal spine and four category branches. Label them **People**, **Process**, **Materials**, and **Procedure**. Some practitioners also add **Equipment** and **Environment** as separate branches.
3.  Explain each category to the team. Overlap among categories is acceptable; an idea may fit more than one branch.
4.  Starting with the first category, ask, "How could something in this category cause the problem?" Capture every idea on sticky notes and place them on the diagram so they can be moved later.
5.  For each idea on a branch, apply the 5 Whys technique. Ask "Why?" repeatedly to drive to the most granular possible level of detail.
6.  Repeat the brainstorming and 5 Whys drill-down for every remaining category.
7.  Review the completed diagram as a group. Discuss the placement of causes and move items to more appropriate categories or sub-branches to create an organized visual.
8.  Cross out or remove causes that initial discussion shows to be invalid. This keeps the analysis focused on plausible contributors.
9.  Circle the causes the team considers highest priority. These become candidates for verification and further analysis.

After the diagram is built, additional enhancements can support deeper investigation. Teams may annotate causes as controllable or uncontrollable (noise factors) and distinguish factors that are candidates for design of experiments. This labeling sharpens the transition from brainstorming to quantitative analysis.

## 5 Whys

The 5 Whys method asks, "Why does this problem exist?" or "Why did this event occur?" repeatedly. With each answer the team poses another "Why?" The sequence becomes progressively more intensive, peeling away symptoms to reveal systemic root causes. The name reflects the typical observation that five iterations, and sometimes more, expose the true gap that requires resolution. When used together with a fishbone diagram, the 5 Whys form the drill-down mechanism that turns a high-level category into a precise actionable cause.

## Is/Is Not Comparative Analysis

The Is/Is Not technique refines problem diagnosis by precisely delineating the boundaries of a defect. The team constructs a table with the following dimensions:

- **What** – the specific object that has the defect and the specific defect itself.
- **Where** – the geographic location or position on the part where the defect occurs.
- **When** – when the defect was first observed, subsequent occurrences, and where in the product life cycle it appears.
- **Size** – the number of objects affected, defects per object, physical size of the defect, and any trend.

For each dimension, the team populates two columns:

- **Is**: the factual characteristics of the observed defect.
- **Is Not**: similar objects or conditions that could logically exhibit the defect but do not; other plausible defects that are absent; times, locations, or sizes where the defect could have surfaced but did not.

After completing the table, the team identifies differences and changes between the "Is" and "Is Not" entries. This comparison pinpoints the range or batch where the defect source emerged and helps determine whether the defect is related to a special cause such as operator error, shipping damage, or deficient raw material. The method adds rigor to scoping and prevents effort from being squandered on irrelevant variables.

## Cause-and-Effect (X–Y) Relational Matrix

The X–Y relational matrix quantifies and prioritizes the impact of potential causes (inputs, X) on important customer outcomes (effects, Y). It converts subjective judgment into a numerical ranking and is especially useful for prioritizing causes previously identified with a fishbone diagram.

To build the matrix:

1.  List the process inputs (causes) as rows.
2.  List the customer requirements or effects (outputs) as columns.
3.  Assign a weighting to each output column that reflects its importance to the customer. A typical scale uses 1–10.
4.  For each input–output cell, rate the strength of the relationship. The rating can be based on objective data or subjective ordinal values.
5.  Multiply each relationship rating by the output's importance weight, and sum the products across all outputs for each input. This produces a total weighted score.
6.  Calculate the percentage of the grand total that each input represents. Sort inputs by total score to reveal which causes carry the greatest aggregate impact.

The resulting prioritization shows exactly which process inputs demand deeper analysis or control, directly linking improvement actions to customer needs.

## Root Cause Tree

The root cause tree combines the structure of a fishbone diagram with the iterative probing of the 5 Whys. It places the failure effect at the top and branches downward into potential root causes, allowing the team to visualize interactions among causes.

A root cause tree can incorporate:

- **"Or" relationships**, where any single cause can produce the effect.
- **"And" relationships**, where multiple causes must occur together.
- **Simultaneous effects**, outcomes that appear together once the causes activate.

Each box in the tree can carry codes that indicate status, weighting, or activity level. A common coding scheme marks two dimensions: **Opportunity** (High, Medium, Low) and **Controllability** (Within control, Have influence, No influence). Color coding draws attention to causes needing action.

The tree begins with a clear statement of the failure effects. The team develops branches that represent different investigative approaches (often labeled A, B, C, etc.) and progressively asks "Why?" to build deeper levels. Once the tree is populated, the team maps priorities and corrective action tasks directly against the boxes. Boxes coded **High opportunity** and **Within control** are the ones the team can address for the greatest immediate impact on problem resolution. This tool ensures a thorough, traceable investigation and makes the link between corrective actions and underlying root causes explicit.

## Failure Mode and Effects Analysis (FMEA)

FMEA is a systematic group of activities designed to:

- Recognize and evaluate potential failure modes of a product or process and the effects of those failures.
- Identify actions that can eliminate or reduce the chance of a potential failure occurring.
- Document the entire analysis.

As a root cause analysis tool, FMEA helps diagnose potential root causes linked to defined failure conditions. Its primary purpose is to understand the opportunity for failure, prioritize risks, and drive actions that eliminate or reduce the impact of those risks.

The team calculates a risk priority number (RPN) by multiplying ratings for **Severity**, **Occurrence**, and **Detection**. Items with higher RPN scores require mitigation plans. A crucial best practice: after mitigations are implemented, the team must revisit and update the FMEA to re-evaluate the residual risk and confirm that all high-risk items have been addressed. This closes the loop, ensuring root causes of failure are actually resolved.

## Root Cause Verification Matrix

Identifying possible root causes is only the start; each candidate must be verified before resources are committed to a solution. The root cause verification matrix documents this critical step.

The matrix contains the following columns:

- **Problem** – the issue under investigation.
- **Possible Root Causes** – the specific causes being tested.
- **Method of Verification** – the technique used to confirm or refute the cause, such as statistical analysis, design of experiments, direct process observation, gathering additional data, graphical analysis, or detailed process mapping.
- **Reason for Verification Method** – a justification for why that method is appropriate for the cause type.
- **Verified?** – a yes/no conclusion.
- **Notes** – any additional findings or context.

For example, if the team suspects inconsistent bake times cause burnt cakes, it might use a box plot of bake times per cake type to visualize variation. The matrix ensures decisions are data-driven, transparent, and traceable, preventing the team from wasting effort on unverified assumptions.

## Using Pareto Charts for Root Cause Analysis

A Pareto chart, grounded in the 80/20 rule, provides a powerful starting point for root cause brainstorming. The chart displays defect categories in descending order of frequency, often with a cumulative percentage line. The team focuses on the few categories that account for the vast majority of the problem. From there, they drill down using a fishbone diagram and the 5 Whys, and may construct additional Pareto charts for subcategories. This approach channels analytical energy toward the causes that, if resolved, will yield the largest performance gains.

---

## Exam Tips

- In an **Is/Is Not analysis**, the "Is Not" column is used to narrow the search area by identifying conditions where the defect could logically appear but does not; the team then analyzes the differences between "Is" and "Is Not" to pinpoint the source.
- When constructing a **Cause-and-Effect (X–Y) Relational Matrix**, the total weighted score for a process input represents the aggregated impact of that input across all customer outputs, enabling data-driven prioritization of causes.
- In a **root cause tree**, a box marked with a high-opportunity code (H) and a controllability code of "within control" (C) signals that the team can address this cause directly to achieve the greatest improvement, making it the top priority.
- After implementing corrective actions identified through an **FMEA**, the team must revisit and update the FMEA to re-evaluate the risk priority numbers and verify that high-risk items have been satisfactorily reduced.
- During a **fishbone diagram** session, any cause that is invalid upon initial team discussion should be crossed out or removed so that the group concentrates on plausible contributors.
- The **root cause verification matrix** requires a documented reason for each chosen verification method to ensure the technique fits the nature of the suspected cause and to maintain an auditable trail of analytical decisions.