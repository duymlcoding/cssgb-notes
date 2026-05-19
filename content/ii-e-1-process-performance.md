---
title: "Process Performance"
description: "How to quantify and analyze process performance gaps using problem statements and the 5 Whys tool in the Define phase of a Six Sigma project."
---

**BoK:** II-E-1  **Bloom's level:** Analyze

## Problem Statement as a Performance Baseline

A Six Sigma improvement project begins by defining the current performance of the process under study. The problem statement transforms a vague dissatisfaction into a measurable performance baseline. A strong problem statement answers specific questions that let any reviewer understand the process deficiency without additional explanation. According to the CSSC training material, a problem statement must include the following elements.

- Where the problem occurred (facility, department, geography)
- When the problem occurred (specific months, quarters, or dates)
- What process the problem involved
- How the problem is measured (the metric used)
- The magnitude of the problem, preferably tied to cost

For example, a call center in Jacksonville, Florida handled 36,000 calls in February 2015. Of those calls, 8,000 had an average speed of answer (ASA) over the contract-required 15 seconds. Those 8,000 service-level-agreement violations cost the operation $200,000. This single sentence supplies location, time period, process (answering calls), metric (ASA), and financial impact. It establishes a clear performance gap: 8,000 out of 36,000 calls failed to meet the ASA target.

Quantifying performance this way matters because it justifies the investment a Six Sigma project requires. A $1.4 million annualized cost, as seen in the distribution center example that reported a 13.8 percent return rate instead of 7 percent, gives leadership a concrete reason to support the initiative. The problem statement also sets the baseline against which the team will measure improvement. Without numbers, the team cannot determine whether the process has moved.

## Using 5 Whys to Analyze Performance Gaps

Once a problem statement reveals what the performance gap looks like, the team must understand why the gap exists. The 5 Whys is a rapid root-cause analysis tool used in the Define phase when processes involve human interactions or when the team needs to move from a high-level performance symptom to an actionable cause. The method costs little time and facilitates communication among subject-matter experts.

The procedure follows a strict iterative questioning pattern.

1. Write a general problem statement that states something about defects or dissatisfaction. The statement can be broad, such as “Customers are dissatisfied with hamburgers.”
2. Ask the highest-level “Why?” question possible. “Why are customers dissatisfied with hamburgers?”
3. Write the answer directly under the question. Example: “The meat is undercooked.”
4. Form the next “Why?” question about that answer. “Why is the meat undercooked?”
5. Repeat until the team identifies a root cause that, if addressed, would prevent recurrence.

In the hamburger example, four questions moved the team from “undercooked meat” to “the grill is not properly calibrated” to “the new grill cook was not trained to calibrate the grill.” At that point the team had a specific cause-and-effect relationship: the untrained cook (x) produced undercooked meat (y). A fifth question, “Why was the grill cook not properly trained?”, pointed toward a control solution (a consistent training policy). In Six Sigma terms, the team built the y = f(x) relationship that connects process performance to its drivers.

Teams use 5 Whys when no one has been able to define what is actually wrong, when a supervisor notices a recurring problem, or when a general feeling of poor performance exists. Because the technique is conversation-based, a moderator should keep the session on task. The method works best for problems rooted in human action, but it also serves as an effective brainstorming start for any process.

## Quantifying Process Performance from Problem Statement Data

A strong problem statement provides enough data to calculate key performance metrics. Using the call center example, the team extracts these numbers.

- Total calls handled: 36,000
- Calls exceeding the ASA target: 8,000
- Cost of violations: $200,000 for the month

The defect rate is the ratio of defective calls to total calls. The team computes it as:

$$
\text{Defect rate} = \frac{\text{Number of calls with ASA} > 15 \text{ seconds}}{\text{Total calls}} = \frac{8,000}{36,000} \approx 0.2222
$$

Expressed as a percentage, 22.2 percent of calls failed the service level agreement in February 2015. The cost of poor performance that month was $200,000. If the process remains unchanged, the annualized cost exceeds $2.4 million. This numerical analysis turns the problem statement into a precise performance baseline that the project can target for improvement.

A second example reinforces the analytical step. A Canton, Ohio bakery produced 300,000 loaves of bread in November and December 2014 and received 50,000 complaints about undercooked bread. The complaint rate is:

$$
\text{Complaint rate} = \frac{50,000}{300,000} \approx 0.1667
$$

The bakery operated with a 16.7 percent quality failure rate, and the linked costs were estimated at $125,000 per month. In both scenarios, the team moves beyond anecdotal claims and anchors the project in reproducible numbers.

## Constructing a Problem Statement from Process Observations

When writing a problem statement, approach the task as a journalist would. Use a checklist to avoid leaving out critical information.

- Where did the problem occur?
- When did the problem occur?
- What process did the problem involve?
- How is the problem measured?
- How much is the problem costing (in money, time, customer satisfaction, or another critical metric)?

Draft the statement and then test it by asking a coworker who is not close to the issue to answer those same questions using only the statement. A weak statement, such as “The Ohio call center has a service-level-agreement issue costing about $9,000 per day,” fails because it does not specify when, what process, or the metric. Conversely, the Jacksonville call center statement passes every checklist question. A complete problem statement directly yields an objective statement for the project team.

## Exam Tips

- The CSSGB exam expects you to identify a strong problem statement by checking for location, time, process, metric, and quantified impact. Weak statements often omit the metric or lack a clear magnitude.
- Be ready to compute defect rates or proportionate failure levels from the numbers embedded in a problem statement. The Analyze level often tests the ability to calculate a percentage and interpret its meaning.
- Know that the 5 Whys is a Define-phase tool used when human factors dominate a process. The exam may present a scenario and ask which tool is most appropriate for quickly drilling to a root cause.
- Understand the relationship between the 5 Whys output and the y = f(x) thinking. The chain of questions moves from the performance problem (y) to the actionable causes (x), which is fundamental to process performance analysis.