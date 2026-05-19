---
title: "Implementation Planning"
description: "Study notes for ASQ CSSGB covering implementation planning in the Improve phase: solution selection, cost-benefit analysis, piloting, documentation, training, and transition."
---

## Implementation Planning Overview

During the Improve phase of DMAIC, Six Sigma teams move from identifying root causes to planning and executing solutions. Implementation planning translates selected countermeasures into concrete actions that deliver measurable business results. The team first brainstorms potential solutions and uses analytical tools to rank them. Once the top solutions are selected, the team plans a pilot or limited rollout, verifies the solution works with data, and then prepares full-scale deployment. Throughout this planning, the Green Belt ensures that documentation, training, and transition steps are built into the plan so that the gain is sustained.

A project framework drawn from lean practices helps match the right type of improvement activity to the performance gap. Business goals and identified performance gaps can be closed through four types of projects: quick-hit projects (immediate, low-cost changes), kaizen projects (gradual, continuous improvement efforts), value stream mapping projects (eliminating waste across a flow), and Six Sigma projects (complex problem solving with statistical rigor). Savings from process improvements flow from this combination, and implementation planning considers which project mix is appropriate.

Planning also embeds lean thinking at its core. The team specifies value for each specific product or service, identifies the value stream, makes value flow without interruption, lets the customer pull value through the process steps, and pursues perfection by preventing rework. These principles guide the selection and design of solutions so that waste and variation are removed.

## Solutions Selection Matrix

A solutions selection matrix is an analytical tool that lets a team propose, rate, and rank solutions for one validated root cause at a time. The matrix is built collaboratively, often in a spreadsheet, and should include team members, subject matter experts, and stakeholders to ensure realistic solutions. A separate matrix is created for each root cause the team intends to address.

The procedure unfolds in six steps.

1. Enter the final problem statement from the Measure phase (or the refined statement after data gathering).
2. Enter the priority root cause from the Analyze phase.
3. Brainstorm potential solutions. Record every viable idea without evaluation; only solutions that are clearly out of scope or impossible are set aside.
4. Note at a high level the practical methods for implementing each solution (for example, written documentation and training).
5. Rate each solution on three criteria, each on a scale of 1 to 10.
   *Effectiveness* measures how well the solution is expected to eliminate the root cause (1 = not effective, 10 = highly effective).
   *Feasibility* measures the effort and resources needed to implement (1 = not feasible, 10 = highly feasible).
   *Cost-benefit* is a high-level estimation of whether savings outweigh costs. A higher rating means the financial return is strongly favorable.
6. Multiply the three scores for each solution. The product is the overall score used to prioritize solutions.

For example, a team addressing a claims denial problem might evaluate four solutions: requiring front-desk information collection (high feasibility and cost-benefit, moderate effectiveness), creating a patient portal (low feasibility, low effectiveness), requiring clinicians to chart all billing information during visits (moderate effectiveness, low feasibility), and assigning dedicated staff to resolve missing-information claims (high scores across all dimensions). The team may decide to implement the highest-scoring solution and also adopt a low-effort, high-return solution to amplify results.

## Cost-Benefit Analysis

Leadership often requires a more detailed financial picture than the matrix provides. Teams can perform a cost-benefit analysis using the payback method or net present value (NPV). Costs include software, equipment, building changes, added labor, training, supplies, and disruption losses. Benefits include higher product margins, increased revenue, cost savings or avoidance, and intangible gains such as improved morale or customer retention.

### Payback (Pay-Off) Analysis

The payback method estimates how long it takes for a project to pay for itself. Use the formula:

$$
\text{Payback (years)} = \frac{\text{Cost of implementing solution}}{\text{Annual financial benefits} - \text{Annual operating costs}}
$$

If a solution costs 50,000 to implement, generates 15,000 in annual benefits, and carries 2,000 in annual extra labor, the payback is:

$$
\frac{50,000}{15,000 - 2,000} = \frac{50,000}{13,000} \approx 3.84 \text{ years}
$$

Shorter payback periods are preferred, but a longer payback can still be acceptable when the solution solves a critical problem or enables future success.

### Net Present Value (NPV)

NPV adjusts future cash flows for the time value of money using a discount rate (often provided by the finance department). A basic NPV model lists annual benefits and costs over the expected life of the solution, then discounts each net cash flow. A positive NPV indicates that the project’s benefits exceed its costs in present-value terms.

## Piloting a Solution

Before full-scale implementation, the team runs a pilot, a limited trial of the solution in a live environment. Piloting reduces waste if the solution does not work as expected, confirms that the intended results occur, allows troubleshooting at a small scale to minimize disruption, and gathers feedback from employees outside the team. Small or simple changes may not need a pilot, but pilots are essential when changes are large in scope, could cause expensive consequences, would be difficult to reverse, or are costly to deploy fully.

Pilots can be conducted on a limited scale (a specific region, team, or machine) or for a limited time (temporary change with a decision point at the end). Process pilots might test locations, customers, employees, or dry runs. Product pilots use test markets, product models, or alpha and beta testing with subsets of customers.

To create a pilot, the team selects the audience without biasing results. Avoid using only top performers or loyal customers. Often, an alpha test with a very small, trusted group provides early feedback, followed by a beta test with a larger, more diverse group. After each pilot cycle, the team analyzes results using hypothesis testing and graphical analysis to verify statistically significant improvements.

## Implementation Action Plan

Once the solution is verified, the team creates an action plan detailing tasks, responsibilities, and deadlines. The plan is maintained in a shared location. Typical tasks include documentation, training, and transition.

**Documentation.** All work from the DMAIC phases, data tables, statistical analyses, and brainstorming outputs must be accessible. New or changed processes are recorded in standard operating procedures (SOPs). The team may also draft general communications, cheat sheets, and FAQs.

**Training.** The Six Sigma team trains designated trainers or subject matter experts from the affected department. Those individuals then train the broader workforce. Over time, the training is integrated into the organization’s standard training systems.

**Transition.** During Improve, the team begins considering how the process will be handed back to the process owner. Strong documentation and training lay the foundation for a smooth Control phase.

## Improve Tollgate Checklist

Before moving to Control, the team verifies that:

- Solutions were reviewed and prioritized.
- One or two top solutions were selected for action.
- Solutions were implemented on a limited basis (pilot).
- Data from the limited trials was analyzed and solutions appear to work as expected.
- A cost-benefit analysis was performed.
- The sponsor, champion, or executive steering committee signed off on full implementation.
- All team members agree the solution should be implemented.
- The solution is fully documented through SOPs and training materials.
- Critical staff received training and are prepared to train others.

## Lean Principles in Implementation Planning

Implementation planning also considers the organizational shifts that make improvement sustainable. Lean thinking transforms several aspects of operations.

- **Product and service design**: standardize and make incremental changes to gain continuity.
- **Capacity**: increase flexibility and overall utilization to smooth demand spikes.
- **System layout**: emphasize work flow with multiple work cells instead of large isolated areas.
- **Workforce**: build team-based cooperation, empower practitioners, cross-train for diverse skills, and drive change through consensus.
- **Scheduling**: reduce setup times and enable concurrent production of different models.
- **Inventories**: reduce work-in-process to lower carrying costs and eliminate large segregated storage areas.
- **Suppliers**: foster partnership and interdependency, reduce vendor counts, and deliver directly to the point of application.
- **Operations**: use visual indicators, preventive quality and maintenance approaches, and work at the logical pace of progress to become more anticipatory.

Specific lean tools are often planned into the implementation to sustain control.

- **5S** creates order through sort (seiri), straighten (seiton), shine (seiso), standardize (seiketsu), and sustain (shitsuke).
- **Visual factory** uses displays and controls so anyone can promptly see process status and operating conditions.
- **Kaizen** pursues low-cost gradual improvement, either continuously or through dedicated blitz events.
- **Kanban** signals when to obtain inventory, produce a part, or move material; it also prevents defective pieces from passing downstream.
- **Poka-yoke** (mistake-proofing) designs the work so errors are impossible. For example, an electric plug can only be inserted one way. By limiting how a task can be performed or making mistakes visible, variation is reduced and nonconformances prevented.
- **Total productive maintenance** uses preventive maintenance, load balancing, and streamlined flow control.
- **Standard work** applies capacity resource planning to find the most efficient combination of operations.
- **Pull systems** schedule production so materials are staged at the point of consumption and restocking is limited to what has been consumed, eliminating overproduction and excess inventory. Pull systems operate consistently with Little’s law (the relationship between lead time, throughput, and work-in-process). Reducing WIP reduces lead times and speeds customer delivery. Efficiencies that enhance pull systems include simplification, setup time reduction, fewer handoffs, elimination of rework loops, bottleneck management, and positioning inventory for rapid deployment.

## Exam Tips

- Given a root cause and a set of candidate solutions, you must be able to construct a solutions selection matrix: enter the problem statement, brainstorm solutions, assign effectiveness/feasibility/cost-benefit ratings on 1–10, multiply for overall score, and justify which solution(s) to pursue.
- Calculate payback period using the formula and interpret a longer vs. shorter payback in the context of organizational priorities.
- Identify when a pilot is necessary: apply the criteria of solution scope, reversibility, cost, and potential for large-scale disruption.
- Describe the purpose and sequence of alpha and beta testing, and explain why pilot audiences should not be limited to top performers.
- List the items on the Improve tollgate checklist and, given a scenario, determine whether a project is ready to exit the Improve phase.
- Select the appropriate lean tool (for example, poka-yoke, 5S, pull system) for a given process control need described in a case study.