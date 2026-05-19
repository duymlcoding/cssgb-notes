---
title: "Customer Requirements"
description: "Translating the voice of the customer into actionable technical specifications using Quality Function Deployment and classifying requirements by type."
---

**BoK:** II-B-3  **Bloom's level:** Apply

## Voice of the Customer and Quality Function Deployment

Quality Function Deployment (QFD) is a structured method for converting customer desires into technical design parameters. It ensures that customer requirements, often expressed in everyday language, are systematically linked to measurable engineering specifications and process controls. QFD reinforces the robustness of the design and defines the terms of product development, delivery, maintenance, and fulfillment.

### The Input–Output Matrix

At the core of QFD is an input–output matrix that organizes two categories of information:

* **“Whats”** – Customer requirements. These can be classified as required (must have), necessary (expected to have), or optional (nice to have).
* **“Hows”** – Technical details that address, at a minimum, the specific requirements of the customer.

The complete matrix provides a database for product development, serves as a basis for planning improvements, and suggests opportunities for new or revised products or processes.

#### Building a QFD Matrix – Step by Step

1. List the customer requirements (“Whats”) in the left column of the matrix. These are gathered from surveys, interviews, complaints, and other VOC sources.
2. Assign an importance rating to each requirement, typically on a scale such as 1 to 5, reflecting the customer’s priority.
3. Record the customer’s competitive assessment for your product and for competitors, using a numeric scale (for example, 1 = worse to 5 = better).
4. List the design requirements (“Hows”) across the top columns. These are the technical characteristics that the organization can control and measure.
5. Populate the relationship matrix in the body of the chart. Rate the strength of the link between each “What” and each “How” (for example, 9 = strong, 3 = medium, 1 = weak).
6. Compute the technical importance for each design requirement by multiplying the importance rating of each customer requirement by the relationship value and summing down the column. This reveals which design features deserve the most focus.
7. Complete the correlation roof matrix to show how the design requirements influence each other positively or negatively. Mark strong positive, positive, negative, or strong negative correlations.
8. Set objective target values for each design requirement, aligned with competitive benchmarking and technical importance.
9. Perform an engineering competitive assessment to compare your product’s technical performance against competitors.

The completed matrix creates an objective, traceable link between customer expectations and acceptance criteria. Teams use it to prioritize improvement actions and allocate resources effectively.

### Staged Application of QFD

QFD extends beyond a single matrix. In a staged environment, the outputs of one phase become the inputs of the next. The typical flow cascades as follows:

Design requirements (first house) → Parts requirements → Process requirements → Production requirements.

This cascade entrenches customer requirements into the earliest stages of product development and pushes them without gaps through manufacturing and delivery. Every subsequent stage answers, “How will we fulfill the customer requirements defined in the prior stage?” The process closes the loop on customer satisfaction while managing cost.

### Customer Value Characteristics

Customers evaluate products and services along multiple dimensions. Table 5.1 from the *CSSGB Handbook* lists the following product value characteristics:

* Performance
* Benefit relative to cost
* Durability
* Safety
* Serviceability
* Usability / ease of use
* Simplicity of design
* Functionality
* Availability
* Performance

Service value characteristics include:

* Responsiveness
* Reliability
* Competence
* Access
* Communication
* Credibility / image
* Confidentiality / security
* Understanding the customer
* Accuracy / completeness
* Timeliness

Understanding these characteristics helps the team collect the right voice-of-the-customer data and translate it into the structure of a QFD matrix. For instance, if customers mention “fast support,” the team might map that to Responsiveness and Competence among service characteristics, then link it to technical details such as call-answer time or staff training hours.

## Identifying Customer Requirements Through Root Cause Analysis

Another approach to clarifying customer requirements uses the y = f(x) mental model. A customer-facing problem (Y) exists because of one or more causes or inputs (X). Stated as a function, the dissatisfaction is driven by some unmet requirement. The 5 Whys technique systematically drills down from a general complaint to a specific, measurable requirement.

Consider a restaurant experiencing low customer satisfaction with food quality. The 5 Whys investigation might unfold as follows:

* Why are customers dissatisfied with the food? They are dissatisfied with hamburgers.
* Why are customers dissatisfied with hamburgers? The meat is undercooked.
* Why is the meat undercooked? The grill is not properly calibrated.
* Why is the grill not properly calibrated? The morning cook responsible for calibration was not trained.

At this point, the team has identified that a customer requirement, hamburgers cooked to a safe and expected temperature, was not being met. The gap can now be expressed in a strong problem statement that quantifies its magnitude: “In November and December, 50,000 complaints of undercooked bread were received from the Canton facility, costing an estimated \\$125,000 per month.” The problem statement defines the requirement (proper bake), the current failure rate, and the financial impact, giving leadership a clear justification for the improvement project.

When crafting a problem statement that captures a customer requirement gap, answer these questions:

* Where did the problem occur?
* When did the problem occur?
* What process did the problem involve?
* How is the problem measured?
* How much is the problem costing in money, time, or customer satisfaction?

A well-structured problem statement makes the unmet customer requirement visible and actionable, aligning the team on what success looks like.

## Exam Tips

* When the exam presents a customer complaint, classify it as a required, necessary, or optional requirement. For example, an airline passenger who expects a seatbelt is stating a required feature; a passenger who hopes for a free meal is expressing an optional “nice to have.”
* Given a