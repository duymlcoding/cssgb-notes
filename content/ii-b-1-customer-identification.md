---
title: Customer Identification
description: Identify and define customers and their requirements using Quality Function Deployment (QFD) matrices, problem functions, and the 5 Whys to translate the Voice of the Customer into actionable project foundations.
---

**BoK:** II-B-1  **Bloom's level:** Apply

## Translating Customer Needs with QFD

The Voice of the Customer (VOC) becomes actionable when the “what” (customer requirements) is systematically linked to the “how” (technical requirements). Quality Function Deployment (QFD) provides a structured matrix for this translation. The customer requirements populate the rows of the matrix, while the technical requirements form the columns. Every intersection of a customer need and a technical feature receives a relationship indicator, a strong, moderate, or weak link. This relationship key reveals which technical characteristics most directly impact customer satisfaction.

For example, a QFD matrix for an animal trap (see Figure 5.1 in the source) lists customer requirements such as “Animal will be lured,” “Inexpensive refill,” “Won’t attract insects,” “Easily sprung by animal,” “Safe for kids,” and “Rustproof.” The corresponding technical requirements include “Bait attractiveness,” “Bait life,” “Insect attractant #,” “Tab pressure,” “Cage size,” and “Oxidation index.” The matrix shows how strongly each technical feature satisfies each customer need. A strong link between “Animal will be lured” and “Bait attractiveness” tells the project team that bait performance is critical.

The QFD also captures co-relationships among technical features. A positive co-relationship means two characteristics reinforce each other. A negative co-relationship signals a trade-off, a lighter cage might reduce durability, so the team must balance goals. Each technical requirement includes a direction of improvement arrow where “target is best” indicates the ideal is a specific value. The bottom portion of the matrix compares the team’s current product against competitors on each customer requirement, showing where the organization stands and where it must improve to meet customer expectations. By filling out a QFD, a Six Sigma team moves from ambiguous customer desires to measurable, prioritized technical actions.

## Modelling Customer Problems as Functions

Every problem that surfaces through VOC data can be expressed as a function: $y = f(x)$. In this statement, $ y$ is the output metric tied to customer dissatisfaction, and $ x$ represents the inputs or causes that drive that outcome. Often $ y$ results from several $ x$ variables, making the relationship $ y = f(x_1, x_2, \dots)$.

Consider an HVAC service provider where customer feedback shows service calls take 1.75 times longer than company averages. The manager researches by observing reps, interviewing customers, and joining calls. Observations reveal two root causes: too much talking (one rep chats with local homeowners, another gives overly detailed explanations) and inadequate training (one new rep struggles with tasks). The problem can now be stated as:

> The extra service time is a function of too much talking and inappropriate training.

This formulation forces the project to focus on controllable $x$ variables instead of blaming the $ y$ symptom. Other examples directly tie customer satisfaction to specific inputs: “Low customer satisfaction with hamburger taste is a function of an uncalibrated grill” and “Customer wait times are a function of technology distractions for employees.” Defining the $ y=f(x)$ relationship ensures that the team identifies the true customer-impacting causes rather than surface-level complaints.

## Drilling Down with the 5 Whys

The 5 Whys is a brainstorming tool that starts with a broad symptom of customer dissatisfaction and asks successive “why” questions until the team reaches a root cause or a refined problem statement. This method helps distinguish actual customer pain from assumed causes.

A documented example begins with customers rating food quality lower than normal. The team first asks: “Why are customers dissatisfied with the food?” By examining order-level feedback, they discover the low ratings come mostly from hamburger orders. The answer to the first why: customers are dissatisfied with the food because they are dissatisfied with the hamburgers. The next “why” would investigate what specifically about the hamburgers is failing, for example, taste, temperature, or appearance, and so on until the team uncovers the actionable root cause, such as an uncalibrated grill. Each cycle peels away a layer of assumption, replacing it with data-informed insight. When you connect the final cause back to the customer’s voice, you confirm that the project will address what matters most to the customer.

## Exam Tips

- When given a partial QFD matrix, identify which rows represent customer requirements (the “what”) and which columns represent technical requirements (the “how”). The exam often asks you to pick the strongest relationship or interpret co-relationship symbols.
- For $y=f(x)$ scenarios, you must differentiate the customer-facing output ($ y $) from potential causes ($ x $). Practice extracting both from a business narrative.
- The 5 Whys on the exam will appear as a short sequence of statements. Follow the logic: each “why” must build on the previous answer, and you should stop when you reach a root cause that directly links to the original customer complaint.
- Remember that QFD comparisons with competition are used to set strategic improvement targets based on customer importance and gaps.
- A properly defined $y$ is always expressed in terms of a customer metric, not an internal process metric (for example, “customer wait time” not “server idle time”).