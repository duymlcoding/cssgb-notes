---
title: "Project Risk Analysis and Management"
description: "Techniques for identifying, quantifying, and mitigating project risks using AQP, viability matrices, team design, and auditing."
---

**BoK:** II-C-7  **Bloom's level:** Understand

## Fundamentals of Risk in the Define Phase

Advanced quality planning (AQP) establishes that solid planning prevents surprises and saves resources. In a Six Sigma project, every unanswered question about materials, people, tools, or methods is a potential risk. The cause-and-effect diagram forces the team to list all inputs that could produce the desired output. Each input that is missing, uncontrolled, or misunderstood represents a risk to project goals. Thinking through these causes before work starts aligns with the first step of the plan–do–study–act cycle and reduces the chance of costly rework later.

## Quantifying Project Viability with the Selection Matrix

A structured way to assess project risk is the 15-point weighted viability matrix. This tool evaluates how well a proposed project fits the DMAIC structure by scoring 15 criteria, each carrying a weight that reflects its importance. The criteria include presence of a sponsor, alignment with corporate goals, data availability, defect definition, process stability, customer benefits, company benefits, completion within six months, unknown solution, likelihood of implementation, low cost, team member availability, input controllability, ability to improve without a full redesign, and maintenance of quality across the value chain.

For each criterion the team assigns a rating from 1 (No) to 5 (Yes). The weight is multiplied by the rating to produce a weighted score. All weighted scores that fall into the same rating column are summed to obtain five column totals.

### Full Numerical Example

Using the same weights and ratings shown in the table on page 105 of the CSSC Training Manual, the computation proceeds as follows.

| Criterion | Weight | No (1) | Mostly No (2) | Possibly (3) | Mostly Yes (4) | Yes (5) |
|---|---|---|---|---|---|---|
| Sponsor or champion | 3 | 1 | | | | |
| Goals align with corporate goals | 4 | | | | | 1.3 |
| Data available or accessible | 3 | | | 1 | | |
| Defects well defined | 3 | | | | | 1 |
| Process stable | 1 | | | | 0.3 | |
| Customer benefits | 5 | | | | | 1.7 |
| Company benefits | 5 | | | 1.7 | | |
| Complete within 6 months | 3 | | 1 | | | |
| Solution unknown | 4 | | | | 1.3 | |
| Discovered solution will be implemented | 3 | | 1 | | | |
| New solution costs little to no cash | 5 | | | 1.7 | | |
| Six Sigma team members available | 3 | | 1.3 | | | |
| Inputs can be controlled | 5 | | | 1.7 | | |
| Improve without full redesign | 2 | | | | | 0.4 |
| Quality maintained across value chain | 5 | | | 1.7 | | |
| **Column totals** | | **1.3** | **4.4** | **4.7** | **3.3** | **4.4** |

**Step 1:** Multiply each column total by the rating number at the top of that column.

- No column: $1.3 \times 1 = 1.3$
- Mostly No column: $4.4 \times 2 = 8.8$
- Possibly column: $4.7 \times 3 = 14.1$
- Mostly Yes column: $3.3 \times 4 = 13.2$
- Yes column: $4.4 \times 5 = 22.0$

**Step 2:** Sum the five results:

$$1.3 + 8.8 + 14.1 + 13.2 + 22.0 = 59.4$$

**Step 3:** Sum the original (un-multiplied) column totals:

$$1.3 + 4.4 + 4.7 + 3.3 + 4.4 = 18.1$$

**Step 4:** Divide the sum from Step 2 by the sum from Step 3 to obtain the project score:

$$\frac{59.4}{18.1} = 3.28$$

### Interpreting the Score as a Risk Indicator

The resulting score is interpreted against fixed thresholds that define the level of risk a project carries for DMAIC execution.

| Score | DMAIC Viability | Risk Implication |
|---|---|---|
| Below 2.0 | Not viable for DMAIC | High risk; the project lacks essential enablers such as sponsorship, data, or stability. |
| 2.0 to 3.0 | Possibly viable | Moderate risk; further validation must confirm that the weak criteria can be strengthened. |
| Above 3.0 | Viable DMAIC project | Acceptable risk level; the project has the structural supports needed for success. |

A process that does not fit DMAIC may still need improvement, but the approach may shift to DMADV when a redesign is required. Using the matrix at the project selection stage prevents teams from investing resources in efforts that are almost certain to stall or fail because of fundamental risks.

## Mitigating People-Related Risks Through Team Management

Even a well-scored project can derail if the team is not built to handle the work. The team structure described in the Define phase directly counteracts several common risks.

**Team member types** help balance workload and expertise risk. Regular members attend all activities and keep momentum. Ad hoc members provide process insight only when needed, avoiding production capacity risk. Resource members from ancillary departments supply specialized knowledge without creating full-time commitments. Keeping the core team around five people reduces communication breakdown and burnout, both of which are major project risks.

Selection criteria further lower risk. The guidelines call for employees who know the customer, product, or process, who have demonstrated teamwork and access to the necessary data, and who can contribute at least five hours per week. Matching skills to the project’s likely technical needs prevents delays from missing competencies. Including a person who might otherwise resist the change can neutralize political obstacles early.

**Roles and responsibilities** build accountability. The sponsor or champion secures funding, removes political barriers, and coaches the team on the charter, directly reducing resource and political risk. The process owner, who will receive the final solution, maintains focus on long-term control; this prevents the risk that improvements will degrade after the project closes. The Black Belt leader coordinates scheduling, decision making, and documentation, ensuring the project stays on plan. When these roles are clearly assigned, the team can address risks proactively instead of reacting to crises.

## Auditing as a Risk Discovery Mechanism

Auditing is an independent assessment of processes against established standards. In a Six Sigma context, project teams can use audits to surface risks that are embedded in the current process. A process audit examines standard operating procedures and actual practice; any deviation becomes a finding that signals a risk to quality or safety. The audit cycle itself is a risk management loop.

- **Audit planning:** the auditor studies the criteria and documentation, reducing the risk of missing key evidence.
- **Audit performance:** evidence is gathered through interviews and observation. Any potential noncompliance is reconciled for validity, ensuring risks are factual, not assumed.
- **Audit reporting:** findings and opportunities for improvement are documented along with corrective or preventive actions. This step creates a record of known risks and their assigned responses.
- **Audit closure:** follow-up confirms that action plans eliminated the root causes, closing the risk.

Internal auditors who follow the guidelines, remaining pleasant, factual, and thorough, build trust while uncovering risks that might otherwise stay hidden. Viewing an audit as a risk identification tool helps Green Belts appreciate why auditors must record observations and verify document revision before the audit conduct.

## Exam Tips

- Know how to apply the weighted viability matrix step by step and interpret the score thresholds as risk levels: below 2.0 is high risk, 2.0–3.0 is moderate risk, and above 3.0 is low risk.
- Associate the cause-and-effect diagram from advanced quality planning with the early identification of project risks, particularly around missing inputs.
- Recall the specific team member types and selection criteria that reduce people-related risks; the exam