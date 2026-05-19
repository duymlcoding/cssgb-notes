---
title: "Project Methodology in Six Sigma"
description: "Study notes covering the DMAIC framework, with emphasis on the Define phase and project planning tools such as timelines, budgets, and success measures."
---

**BoK:** II-C-1  **Bloom's level:** Apply

## The DMAIC Methodology

Six Sigma projects follow a structured road map to reduce variation and improve existing processes. The most common methodology is **DMAIC**, which stands for **Define, Measure, Analyze, Improve, and Control**. Each phase guides the team through a logical sequence: identify the problem and customer requirements, baseline current performance, isolate root causes, implement solutions, and sustain the gains. When a process must be completely redesigned or replaced, organizations may use the **DMADV** methodology (Define, Measure, Analyze, Design, Verify). DMADV is suited for launching new products, aligning processes with future goals, or when the team discovers that incremental improvement will not deliver the required success. Many organizations still use DMAIC terminology even during redesign efforts to simplify training and communication. The material that follows focuses on the DMAIC project methodology, particularly the activities and outputs of the **Define phase**.

## The Define Phase in DMAIC

During the Define phase, the team clarifies the problem, establishes the project scope, and sets measurable goals. The key output is the **project charter**, a document usually limited to one or two pages that provides a top-level, quick overview of the project. The charter includes the problem statement, business case, scope, high-level timeline, team members, and expected benefits. In addition to the charter, the team may create a **project management plan** that expands on the activities, milestones, and resource allocations.

A visual companion to the charter is the **storyboard**. Storyboards convey changes that are easier to show than to describe in words. A common application is a set of *current state* and *future state* images that depict a facility or product redesign. Six Sigma storyboards are often organized into five sections labelled Define, Measure, Analyze, Improve, and Control, with charts, figures, and documents illustrating the activity in each phase. Storyboards help the team and stakeholders quickly understand the project's direction.

All project planning in the Define phase must account for **project budgets** and **defined measures of success**. Team leaders must understand how the organization tracks costs, whether they consider only direct expenditures (equipment, software, new personnel) or also include the loaded cost of team members' time. Moreover, every participant must agree on what "success" means. Without a clear, shared definition, the team risks scope creep and conflicting perceptions of the project's outcome. A well-written project charter resolves these ambiguities early.

## Creating a Project Timeline

A timeline gives the team and sponsor a realistic schedule. Two approaches are common.

### Phase-Based Raw Estimate

An experienced Black Belt or Six Sigma leader starts with a total allowed duration, often set by leadership. For a four-month project, the leader assigns a rough number of weeks to each DMAIC phase. A simple example:

| Phase     | Estimated duration |
|-----------|-------------------|
| Define    | 3 weeks           |
| Measure   | 5 weeks           |
| Analyze   | 4 weeks           |
| Improve   | 3 weeks           |
| Control   | 1 week            |

The phases overlap, especially Measure with Define and Analyze. The estimate is quick to produce but can create unrealistic expectations if stakeholders treat it as a hard deadline. The team must communicate that the timeline is a rough estimate that will evolve.

### Critical Path Method

When more information is available, the team can build a detailed critical path diagram. This method identifies the longest sequence of dependent tasks and yields a precise total duration. The steps are:

1. **List the critical activities** needed to complete the phase or the project.
2. **Put the activities in order**, noting which tasks can occur in parallel.
3. **Assign a duration to each task.**
4. **Draw the diagram** from left to right. Stack simultaneous tasks vertically.
5. **Draw the critical path** through the diagram. When tasks are stacked, the critical path passes through the task with the longest duration.
6. **Sum the durations along the critical path** to obtain the total time.

#### Worked Example: Define Phase Timeline

A medical billing team uses the critical path method for the Define phase of a project to reduce bad debt. They identify these tasks and their order:

- Choose a team: 1 week
- Develop a project charter (1 week) and write a problem statement (1 day), which can be done simultaneously.
- Create a baseline metric: 2 weeks

The diagram would show "Choose a team" (1 week) on the left. After that, two tasks are stacked: "Create charter" (5 days) and "Create problem statement" (1 day). The critical path goes through "Create charter" because it takes longer. Finally, "Create baseline metric" (2 weeks) follows.

The total duration is:

$\$1 \text{ week} + 1 \text{ week} + 2 \text{ weeks} = 4 \text{ weeks}$$

Even for complex projects, the critical path method provides a logical, defensible schedule.

### Milestone Meetings

Once the timeline exists, the team sets milestone dates. In DMAIC, natural milestones fall at the end of each phase. The team presents findings to the sponsor at these gate reviews. Dates also create accountability. For example:

- Define: January 21
- Measure: February 12
- Analyze: February 22
- Improve: March 15
- Control: April 10

Internal milestones can be added within a phase. In the Measure phase, the team might set goals such as: definitions created by January 25, temperature data collected by February 5, and time data collected by February 10. Breaking work into smaller, manageable pieces increases the likelihood that tasks are completed on schedule.

## Managing Budgets and Measures of Success

All team members should understand the financial drivers of the project. In some organizations, salary data is restricted, so a Black Belt may need to perform certain cost analyses alone. Still, teams that know the budget can make realistic decisions. An improvement project with a \\$50,000 budget cannot pursue a solution requiring an \\$80,000 capital investment. Leaders must have frank discussions with the sponsor about how budgets are calculated, what expenses are tracked, and whether the sponsor can secure additional funding.

Success must be defined in measurable terms and agreed upon by the team, sponsor, and customer. A well-defined measure of success prevents the project from drifting and ensures all parties evaluate the outcome the same way. Without it, a team might declare victory while leadership considers the effort a failure.

## Exam Tips

- **Differentiate DMAIC and DMADV.** The exam expects you to recognize that DMADV replaces "Improve and Control" with "Design and Verify" for new process creation or when incremental improvement is insufficient.
- **Construct a timeline from given task data.** You may see a table of tasks, durations, and dependencies. Be prepared to identify the critical path and calculate the total project length by adding only the longest durations in each parallel group.
- **Know the content and purpose of a project charter.** It is a concise, one-to-two-page document that communicates the problem, scope, goals, team, and high-level plan. The charter is the primary output of the Define phase.
- **Recognize milestone placement.** Milestones are typically aligned with the end of each DMAIC phase, but the team can define internal milestones for finer control.
- **Apply the concept of defined measures of success.** Exam questions may ask why a shared definition of success matters: to prevent scope creep, align stakeholders, and ensure consistent project closure.