---
title: "Road Maps for Design for Six Sigma (DFSS)"
description: "Study notes covering the DMADV and DMADOV roadmaps, Design for X principles, and the Verify phase drawn from the CSSGB source texts."
---

**BoK:** I-C-1  **Bloom's level:** Understand

## Introduction

Design for Six Sigma (DFSS) provides structured road maps for creating new products, processes, or services that meet customer needs with minimal defects from the start. The most common DFSS road maps are **DMADV** (Define, Measure, Analyze, Design, Verify) and **DMADOV** (Define, Measure, Analyze, Design, Optimize, Validate). These frameworks replace the Improve phase of DMAIC with phases dedicated to designing and validating a new solution. While DMAIC improves an existing process, DFSS focuses on designing something new that is inherently capable.

## DMADV and DMADOV Roadmaps

The first three phases of DMADV and DMADOV (Define, Measure, Analyze) closely parallel their DMAIC counterparts. During these early phases the team identifies customer requirements, establishes baseline measurements of the current state (if any), and analyzes root causes or the design space. The real distinction appears in the Design phase and beyond.

### Design Phase

In the Design phase the team creates the new process, product, or service. Using plans, specifications, and process maps developed in earlier phases, the team builds the solution itself. This work may involve collaborating with internal technical departments, manufacturers, or external vendors; a vendor representative should have been a team member from the start. Testing is integral. The team pilots the solution in a controlled environment, a limited production setting, or through a Beta release to a subset of customers. Feedback from testing is used to troubleshoot and refine the design. In the DMADOV variant this refinement is formally called the Optimize phase, where the team iterates until the best possible solution emerges.

Teams must guard against project fatigue during Design, because the workload often intensifies after weeks or months of prior effort. Realistic timelines are essential; promising an unreasonably fast delivery encourages rushed work and low-quality outcomes.

### Verify Phase

The Verify phase (or Validate in DMADOV) transitions the new design out of project mode and into the hands of the process owner. It serves the same function as the Control phase in DMAIC. The team establishes control plans, control charts, response plans, process maps, and dashboards to monitor ongoing performance. Because the product or process is novel, the team may perform a fresh critical-to-quality (CTQ) analysis at this stage. The new solution may exhibit capabilities the original model did not have, and customers may shift their perception of what matters most. The final deliverable must meet the requirements identified in the Define phase, be free of known defects, and be supported by a documented management plan.

A key tool used during Verify is the traceability matrix, which links each design objective to a corresponding design output and tracks its status.

**Table 3.1 example of a traceability matrix** (conceptual)

| Design Objective            | Design Output                                    | Status                |
|-----------------------------|--------------------------------------------------|-----------------------|
| Extended functionality      | Business user can apply software to operations   | Achieved              |
| Maintainability             | Modular design with minimal coupling             | Replacement eases maintenance |
| Efficiency                  | Transaction completed within five minutes        | Supports customer efficiency |
| Security                    | Password encryption for access                   | Unauthorized use prevented |
| Compliance (emissions)      | Emissions meet Kyoto standards                   | Redesign required     |

This matrix ensures that every objective set during Define has been addressed in the design.

## Design for X (DFX) Considerations in DFSS

A DFSS project does not treat the Design phase as a one-dimensional task. The ASQ handbook describes a suite of "Design for X" considerations that designers must address to embed quality across multiple dimensions. These principles are applied during the Design phase to ensure robust, usable, and sustainable solutions.

### Design for Robustness
Products must withstand life-cycle stresses. Suppliers of purchased parts should document the mean time to failure (MTTF) for nonrepairable items or mean time between failures (MTBF) for repairable items. The fundamental relationship is

$$ \text{MTTF} = \frac{1}{\lambda} \quad \text{or} \quad \text{MTBF} = \frac{1}{\lambda} $$

where $ \lambda $ is the failure rate. Reversing the formula gives

$$ \lambda = \frac{1}{\text{MTTF}} \quad \text{or} \quad \lambda = \frac{1}{\text{MTBF}} $$

*Numerical example*: A component has a constant failure rate of $ \lambda = 0.002 $ failures per hour. The MTTF is

$$ \text{MTTF} = \frac{1}{0.002} = 500 \text{ hours} $$

This means the component can be expected to operate, on average, 500 hours before failure.

### Design for Usability
The product must be validated by having intended users apply it in its specified environment. The quality of the user's experience determines the success of the design, so designers measure and improve how comfortably users obtain value.

### Design for Extended Functionality
Many products initially built for a single purpose can later serve extended functions. Software originally for quick mathematical calculations now supports graphic design, word processing, and database management. Designing with this potential in mind can multiply the product's value.

### Design for Efficiency
The system must consume minimal resources (time, materials, critical components). Although correlated with design for cost, efficiency focuses on resource consumption during operation and directly influences long-term cost and reliability.

### Design for Performance
The design must achieve aggressive benchmarks consistently, delivering "cutting-edge" capabilities. Examples include aircraft that exceed the speed of sound and microchips that continuously increase processing power.

### Design for Security
Security threats such as computer viruses, identity theft, and product misuse must be counteracted. A secure design preserves product integrity and protects the intellectual property and privacy of both users and designers.

### Design for Scalability
Products intended for growth markets must handle rapid adoption without degradation. Without this attribute, quality collapses when usage exceeds design limits. A website that crashes when 100,000 concurrent users access it at month-end is a classic failure.

### Design for Agility
Organizations that compete on customized solutions need nimble development. Agility requires a robust architecture and ready access to components or vendors that can add unique touches. A hot tub manufacturer that seamlessly integrates the tub into a building's architecture exemplifies this principle.

### Design for Compliance
Regulated environments impose requirements that must be met to market the product. Compliance may involve demonstrating specific performance capabilities or proving that appropriate design processes were followed. Noncompliance can bring penalties and opportunity costs, so designing with compliance from the start averts these risks. An example is a process that requires configuration management updates every time the product changes.

## FMEA in DFSS

Failure mode and effects analysis (FMEA) is a front-end risk management tool that fits naturally into DFSS, especially during the Analyze and Design phases. FMEA systematically identifies how a product or process might fail, the effects of each failure, and the actions that can eliminate or reduce the chance of failure. The fundamental purpose is to predict potential failures and prevent them before the design is deployed.

The core metric is the risk priority number (RPN), which combines severity, occurrence, and detection ratings. FMEA is a living document that should be updated throughout the product life cycle. In a disciplined Quality Management System, FMEA links to Quality Function Deployment houses of quality and to production control plans. The methodology applies not only to manufacturing but also to service processes, software, and medical applications.

## Exam Tips

- **Know the phases of DMADV and DMADOV**: The exam may ask which phase replaces Improve in DMAIC or what specific activities occur during Design and Verify. Focus on the transition of the solution and the Verify phase's role in reassessing CTQ factors.
