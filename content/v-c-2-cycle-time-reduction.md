---
title: "Cycle-Time Reduction"
description: "Detailed study notes for CSSGB BoK V-C-2 covering lean techniques such as standard work, kanban, total productive maintenance, and the seven muda to analyze and reduce cycle time."
---

## Introduction to Cycle-Time Reduction

Cycle time measures the total elapsed time from the start of a process to its completion, including both value-added and non-value-added activities. In a Six Sigma Improve phase project, reducing cycle time eliminates delays, reduces work-in-process inventory, and improves delivery speed to customers. Lean tools systematically expose and remove waste while establishing predictable, repeatable workflows. This section covers three practical tools drawn directly from the ASQ CSSGB Handbook and the CSSC Training Manual: kanban, total productive maintenance, and standard work. It also details the seven forms of waste (muda) that directly extend cycle time and must be eliminated.

## Kanban

A properly administered kanban system controls the movement of materials and information so that they flow into and out of each process step exactly when needed. Inputs that arrive too early create confusion, excess inventory, and unnecessary costs. Outputs that are not synchronised with downstream steps cause delays and customer dissatisfaction. Kanban improves cycle time by enforcing a pull-based flow: a downstream process signals an upstream process to produce or deliver only what has been consumed. This timely movement eliminates the overproduction and waiting that inflate cycle time.

## Total Productive Maintenance

Total productive maintenance (TPM) addresses equipment-related sources of delay and variation. When machines degrade even subtly, process output can shift in unsuspected ways, increasing rework and downtime. TPM integrates engineering, operations, and maintenance so that some maintenance tasks shift to operators during normal work. TPM pursues five concrete objectives.

- Avoid reduced, idled, or stopped performance caused by breakdowns.
- Reduce time spent on setup and changeover, which otherwise idles machines and creates bottlenecks.
- Prevent stoppages from the discovery or processing of unacceptable products.
- Ensure equipment runs at its designed speed; investigate and rectify any slowdown.
- Increase the yield of acceptable material to cut scrap, rework, and material reviews.

Cycle time drops when machines stay up, setups shorten, and processes run at expected speeds without defect-induced interruptions. TPM extends beyond preventive maintenance to include management of people, processes, systems, and the environment.

## Standard Work

Standard work is the lean method for establishing a repeatable baseline against which cycle-time improvements can be measured. It defines every work activity with precision: the required cycle time, takt time, the exact sequence of tasks, and the minimum in-process inventory needed. All jobs are organised around human motion to create an efficient, waste-free sequence. The baseline captures the current best-known way to perform the work and becomes the foundation for kaizen and poka-yoke.

### Purpose and Benefits

Standard work provides process stability, clear definition, organisational learning, employee involvement, and a baseline that supports other lean practices. Process stability means repeatability, which reduces variation in output and cycle time. Employees closest to the work are involved because they understand it best. However, resistance may arise; the following nine-step engagement sequence helps build acceptance.

1. Communicate the change.
2. Identify the benefits.
3. Identify the barriers.
4. Identify how to capitalise on the benefits.
5. Identify methods to mitigate the barriers.
6. Obtain buy-in and agreement on steps 4 and 5.
7. Implement the change.
8. Communicate the results.
9. Celebrate success.

### Three Charts That Create Standard Work

Three analytical charts are used to study the current state, design improvements, and document the new standard.

#### Production Capacity Chart

This chart determines the capacity of machines and humans in a process. It relies on several factors: process time, interval, setup time, and operational time per shift. By calculating capacity for each step, the team identifies bottlenecks. A bottleneck dictates the maximum throughput of the entire line, so its elimination or decoupling reduces overall cycle time.

#### Standardized Work Combination Table

This table lists every work element in sequence and records the time each element takes for both operator and machine. It also displays the interactions between the operator and the machine or between multiple operators and machines. The table helps distinguish value-added time from non-value-added time. It often reveals operator idle time that can be filled with another value-added task. Removing idle periods and non-value-added steps shortens cycle time directly.

#### Standardized Work Analysis Chart

This chart provides a visual rationalisation of the process layout. It includes the work cell layout, the physical placement of equipment, and the sequential process steps. It serves as a training aid for employees because it clearly shows motion paths. By examining the chart, the team can spot unnecessary movement, conveyance, and wasted space that lengthen cycle time.

## The Seven Muda (Wastes) and Cycle Time

Muda means waste: any activity that consumes resources without adding value. Each of the seven classic wastes increases cycle time by introducing non-value-added time, rework, delays, or unnecessary movement. The CSSC Training Manual, referencing Taiicho Ohno’s classification, describes them as follows.

### Overproduction

Producing too much, too early, or too fast relative to downstream demand creates inventory, hides defects, and ties up resources. For example, printing pages faster than a folding machine can process them creates stacks of paper that wait. The extra waiting is pure non-value-added time in the cycle. Overproduction also includes generating reports no one reads or preparing equipment that will not be used. Reducing batch sizes and aligning production pace to takt time eliminate this waste.

### Correction (Rework)

Defective outputs that must be rerouted for correction extend total process time because they consume extra labour, material, and transportation. In a call center, a claim sent back to the original queue for missing information requires another complete cycle. While some inspection might be necessary, the root cause of errors must be addressed. Mistake-proofing (poka-yoke) and designing quality steps that avoid backward loops reduce rework time and prevent compounding of cycle time.

### Inventory

Inventory is any material, work-in-process, or digital queue that accumulates before a step. The folding-machine example shows inventory building up at 200 pages per hour. Inventory delay is a direct addition to cycle time. Batch processing tends to create inventory; reducing batch size lowers lead times. In service processes, inventory appears as unread emails or pending work in a queue, each item waiting for attention.

### Motion

Unnecessary human movement during a task wastes time. Examples include a data-entry clerk clicking back and forth between two screens or a worker walking repeatedly across a poorly laid-out workspace. A spaghetti diagram captures movement paths; analysing the diagram reveals motions that can be eliminated or simplified. Cycle time contracts when operators move less and remain focused on value-adding tasks.

### Conveyance (Transportation)

Conveyance is the movement of materials, outputs, or data between process steps. Physically carrying a report through multiple approval stations or routing an email through a long chain adds time. Even if movement seems minor, it contributes to the overall flow time. A value stream map or process map exposes conveyance waste. Reducing it often means rearranging equipment, combining steps, or using digital tools to transmit information without physical handoffs.

### Over-processing

Putting more work into a product or service than the customer values extends cycle time without increasing satisfaction. Painting the underside of a shelf that nobody sees or verifying insurance benefits to an extreme level during every visit are examples. Every over-processing step is a non-value-added step in the cycle. Value stream mapping helps teams identify where value stops being added; those steps become candidates for removal or simplification.

### Waiting

Idle time for people or machines occurs when upstream steps are not synchronised, setups are long, batches are large, or rework disrupts flow. A cashier waiting for a register-drawer swap, construction crew waiting for a preceding trade to finish, or a machine waiting for material all represent waiting waste. Reducing setup time (Single-Minute Exchange of Die concepts) and balancing line loads through standard work directly attacks waiting and shortens cycle time.

Each form of waste lengthens the time a process takes. Cycle-time reduction therefore demands systematic identification and elimination of muda. Tools such as value stream mapping, spaghetti diagrams, and the three standard-work charts provide visibility, while lean principles such as continuous flow, pull, and setup reduction offer the corrective actions.

## Exam Tips

- Given a process with idle operators and variable task times, select the standardized work combination table as the tool that will expose value-added versus non-value-added time and highlight idle periods.
- When a production line suffers from frequent machine stoppages and slow cycles, identify TPM as the appropriate approach and connect it to the specific objective of operating equipment at designed speed and increasing acceptable yield.
- Analyse a scenario where rework loops cause double handling of a claim; classify the waste as muda of correction, and propose mistake-proofing or quality-at-the-source to shorten cycle time.
- If exam question describes stockpiling of materials between process steps, recognise the waste as inventory, and predict that reducing batch size or moving to a pull system will lower lead time.
- In a case with excessive report preparation that customers never use, name the waste as over-processing and explain its removal will eliminate non-value-added cycle time.
- When the question asks which chart helps identify a bottleneck, reference the production capacity chart, recalling it integrates process time, setup time, interval, and operational time per shift to compute step capacity.