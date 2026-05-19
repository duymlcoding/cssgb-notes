---
title: "Team Tools and Decision-Making Concepts"
description: >
  Study notes on team decision-making methods and project planning tools used in the Define phase of a Six Sigma project,
  including weighted multivoting, Critical Path Method, milestone meetings, budgets, and defined measures of success.
---

**BoK:** II-F-3  **Bloom's level:** Apply

## Multivoting (Weighted Approach)

Multivoting allows a team to narrow a list of options and identify the most important items without requiring a ranking scale. Each team member distributes a fixed number of points across the options, reflecting their individual view of relative importance. The option with the highest total point value is considered the team’s top priority.

### Procedure

1. List all options under consideration. In the example from the Handbook, five items labeled A through E are evaluated.
2. Every team member receives the same total number of points to allocate, in the weighted approach, that total is 100 points per member.
3. Working independently, each member assigns all 100 points among the options. The allocation must reflect that member’s perceived relative importance; no ranking scale is used.
4. After all members have allocated their points, sum the points for each option across the entire team.
5. Compare the totals. The option with the largest sum has the highest overall importance, followed by the next largest, and so on.

### Numerical Example

Nine team members evaluate five potential improvement areas (A, B, C, D, E). Each member distributes 100 points. The individual allocations are shown in the source table, and the column totals are:

$$
\begin{aligned}
\text{Total A} &= 30 + 20 + 25 + 35 + 20 + 25 + 25 + 35 + 30 = 245 \\
\text{Total B} &= 15 + 25 + 20 + 20 + 25 + 20 + 20 + 20 + 15 = 180 \\
\text{Total C} &= 10 + 30 + 30 + 25 + 30 + 30 + 30 + 25 + 10 = 220 \\
\text{Total D} &= 20 + 15 + 10 + 15 + 15 + 10 + 10 + 15 + 20 = 130 \\
\text{Total E} &= 25 + 10 + 15 + 5 + 10 + 15 + 15 + 5 + 25 = 125
\end{aligned}
$$

The consolidated result shows that option A, with 245 points, is most important. Option C (220) is second, followed by B (180), D (130), and E (125). The team uses this outcome to focus their next steps on addressing area A.

## Critical Path Method

The Critical Path Method (CPM) is a detailed technique for creating project timelines. It requires more information than a rough phase-based estimate, so the team typically develops a CPM diagram during the Define phase once the project is underway. CPM helps a team make decisions about task sequencing, resource alignment, and realistic completion dates.

### Steps to Create a Critical Path Diagram

1. **Identify the critical activities** needed to complete the project or a phase.  
   For the Define phase of a bad-debt reduction project, the team listed: choose a team, charter the project, define the problem, create a baseline metric.
2. **Put the activities in the necessary order.**  
   The team determined:  
   - Choose a team  
   - Charter the project and define the problem (these can occur simultaneously)  
   - Create a baseline metric
3. **Assign a time estimate to each activity.**  
   The team estimated: choose team – 1 week; charter – 1 week; problem statement – 1 day; baseline metric – 2 weeks.
4. **Create a diagram from left to right,** stacking activities that can be performed in parallel. The leftmost items must finish before the items to the right can begin.
5. **Draw the critical path** through the stacked activities. When steps are stacked, the critical path follows the step with the longest time estimate.  
   Because the project charter (1 week) takes longer than the problem statement (1 day), the critical path goes through the charter step.
6. **Sum the longest times** along the path.  
   - Choose team: 1 week  
   - Charter (longest): 1 week  
   - Baseline metric: 2 weeks  
   Total duration for the Define phase = 1 + 1 + 2 = 4 weeks.

The critical path method shows which tasks directly impact the overall timeline. Experienced practitioners emphasize that the resulting timeline is an estimate that may change as the team learns more.

## Milestone Meetings

Milestones are scheduled checkpoints that keep the team on track and provide formal opportunities to report to the sponsor or champion. In a DMAIC project, the natural milestones fall at the conclusion of each phase: Define, Measure, Analyze, Improve, and Control. A team may also set internal milestones to manage smaller goals within a phase.

### Examples

- A sandwich shop improvement team set these phase-end milestones: Define – January 21, Measure – February 12, Analyze – February 22, Improve – March 15, Control – April 10.
- During the Measure phase, the same team established internal milestones: definitions completed by January 25, temperature data collected by February 5, and time-study data collected by February 10.

Internal milestones break large tasks into manageable pieces, making it easier for the team to maintain momentum and complete work on schedule. External milestones give the sponsor visibility and allow for go/no-go decisions between phases.

## Budgets and Defined Measures of Success

Team decision-making is also shaped by financial constraints and a shared definition of success.

**Budgets**  
Team leaders must understand how the organization calculates and monitors project budgets. Some organizations count only direct expenditures such as equipment, software, or new personnel. Others include the cost of team members’ time and implementation training. When all team members are aware of the budget ceiling, they can make realistic improvement decisions. A solution requiring an 80,000 capital investment cannot be chosen if the project budget is 50,000.

**Defined measures of success**  
A project without a clear, agreed-upon definition of success risks scope creep and stakeholder misalignment. The team must align with the sponsor and customers on exactly what constitutes a successful outcome. A well-defined success measure allows the team to close the project confidently and prevents situations where the team believes the work is finished while leadership considers it a failure.

## Exam Tips

- Given a multivoting table where each member’s points sum to 100, you must be able to calculate column totals and identify which option earned the highest priority. The exam may present a similar table and ask which item should be pursued first.
- You may be shown a critical path diagram with stacked activities. Expect to determine the critical path through the longest-duration tasks and sum those times to find the total duration of a phase.
- Recognize that milestones are most commonly set at the end of each DMAIC phase. The exam could ask why milestones are important, linking them to sponsor communication and phase gate reviews.
- Understand that a defined measure of success and a clear project budget are prerequisite decision-making concepts introduced early in the Define phase. Questions may test recognition that scope creep and stakeholder conflict are avoided by defining success and financial limits up front.