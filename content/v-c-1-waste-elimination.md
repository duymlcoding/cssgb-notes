---
title: "Waste Elimination"
description: "Detailed study notes on waste elimination (muda) and lean tools for the ASQ Certified Six Sigma Green Belt (CSSGB) certification exam, based on the ASQ CSSGB Handbook and CSSC Training Manual."
---

## Waste and Lean Concepts

Waste, known in Japanese as muda, describes any activity that consumes resources without creating value for the customer. Eliminating waste is fundamental to Lean Six Sigma because it reduces costs, shortens lead times, and improves quality. A Six Sigma defect is a failure to meet a requirement, and defects generate waste through rework, scrap, and customer dissatisfaction. Waste also includes unnecessary time, labor, or material that a process uses to produce a satisfactory outcome. By identifying and removing non-value-added tasks, a process becomes more efficient and more capable of meeting customer expectations.

Taiicho Ohno, chief engineer for Toyota, identified seven common forms of muda. Understanding these seven categories allows a Six Sigma project team to spot waste during process analysis and target improvements during the Improve phase.

## The Seven Muda

### Overproduction

Overproduction means producing a product, part, or service too fast, at the wrong time, or in excessive quantity. In a restaurant, cooking hamburger patties before the lunch rush in quantities that sit and degrade is overproduction. Similarly, printing pages faster than a folding machine can process them creates a buildup of work in process. Even preparing equipment trays far in excess of scheduled surgeries constitutes overproduction when the extra trays have no use. In administrative processes, creating reports that no one reads or preparing highly detailed data when a summary would suffice are forms of overproduction. Overproduction drives other wastes, including inventory and waiting, because it pushes more material into the system than it can handle. Eliminating overproduction requires planning based on actual demand and process capability rather than maximum output.

### Correction (Rework)

Correction, or muda of rework, occurs when work is routed back for additional processing because of defects or incomplete information. In an insurance call center, incomplete claim data forces downstream teams to return work to the original queue, requiring another customer contact. In manufacturing, defective parts are culled out and either reworked or scrapped. Rework increases overall process time and consumes extra labor and materials while producing the same output quantity. Moreover, rework can mask root causes of defects. To eliminate adaptation waste, teams must first address the root cause of errors through mistake-proofing or process changes. Second, quality processes should be designed so that correction loops do not add extensive waste; for example, a downstream worker could reroute a claim directly to the correct team rather than send it back to the start.

### Inventory

Inventory waste, similar to overproduction, is the accumulation of materials or inputs before a process step, often called a bottleneck. The printing example shows that if a printer produces 1,000 pages per hour but the folder handles only 800, a 200-page inventory builds every hour. Inventory can hide problems such as unbalanced workstations, unreliable equipment, or poor scheduling. It also ties up capital and space. In service processes, inventory includes work queues, digital data backlogs, or unread emails. Reducing batch sizes lowers work-in-process inventory and shortens lead times because fewer items wait between steps. When batching is unavoidable, inventory levels should be based on historic demand metrics to avoid excessive buildup.

### Motion

Motion waste involves unnecessary movement of people during a process. A data-entry clerk who must click between separate windows to enter related information performs extra hand and eye motions. When aggregated over hundreds of repetitions daily, this small waste multiplies into significant lost time and cost. In a warehouse or library, walking back and forth to transport items one at a time rather than using a sorted cart creates motion waste. A spaghetti diagram, which traces an operator's movement on a floor plan, reveals crossing paths and backtracking. Streamlining the layout or combining digital interfaces eliminates motion waste and reduces fatigue.

### Conveyance (Transportation)

Conveyance, or transportation, waste is the unnecessary movement of outputs, products, or resources. In an office, printing an expense report and routing it physically through multiple approval levels involves conveyance waste when electronic workflows could move information instantly. Extended email chains that relay a data request through several organizational layers represent digital conveyance waste. Physical conveyance often results from poor layout or inventory placement, such as storing glue far from the assembly point where doll eyes are attached. Correcting conveyance waste often involves reorganizing work areas, applying pull systems that stage materials at the point of use, and streamlining digital workflows so information moves directly to the decision maker.

### Over-processing

Over-processing occurs when more work is put into a product or service than the customer values. Verifying insurance benefits for a simple doctor's visit by spending an hour on the phone with the insurer is over-processing; the customer only needs confirmation of coverage. Painting the underside of a shelf that no one sees or ironing table linens to a crisp seam when a wrinkle-free appearance is sufficient are manufacturing and service examples. Building a software application with 100 features when users only need 10 is over-processing and overproduction combined. Every step in a process should contribute to customer-defined value. A value stream map highlights process steps that add cost but not value, enabling the team to eliminate or simplify them.

### Waiting

Waiting waste is idle time for people or equipment when the process cannot proceed because inputs, information, or prior steps are incomplete. In a retail store, a cash register changeover that idles the cashier and customer creates waiting waste. In construction, specialists often wait for prior trades to finish before they can begin. Unreliable processes, long changeovers, and unbalanced workloads all produce waiting. Solutions include standardizing changeover procedures with prepared, interchangeable components, and balancing workloads so that no station starves others. Reducing waiting increases throughput without adding resources.

## Lean Tools That Eliminate Waste

The ASQ CSSGB Handbook describes several lean tools that directly target waste elimination.

**Pull systems** manage scheduling and material flow so that production is triggered only by actual customer demand. Materials are staged at the point of consumption, and restocking is limited to the amount consumed. This avoids the overproduction and excess inventory typical of pushed systems. Pull systems operate consistently with Little's law, which relates lead time, throughput, and work-in-process. By reducing work-in-process levels, lead times shorten and delivery becomes more responsive. Improvements that enhance pull systems include simplification, minimizing setup and changeover times, reducing steps and handoffs, eliminating unnecessary loops, managing constraints and bottlenecks, positioning inventory for rapid deployment, and reducing rework.

**Kaizen** pursues low-cost, incremental improvements continuously. Teams use kaizen events to identify and eliminate non-value-added activities. This ongoing focus on small improvements reduces waste over time and deepens process knowledge among all employees.

**Kanban** is a signal for a specific action such as "obtain inventory," "produce part," or "move material." It also prevents defective pieces from being transferred. By visual signaling, kanban limits overproduction and ensures that only what is needed is produced.

**Poka-yoke** (mistake-proofing) designs the process so that errors are impossible or immediately detected. A fixture that makes it impossible to stack parts with incorrect orientation prevents downstream defects. An electrical plug that only fits one way prevents misconnection. Poka-yoke limits the ways a task can be performed, thereby reducing variation and eliminating the need for inspection or rework.

**5S** is a workplace organization method that reduces waste from poor housekeeping. The five steps are:
- Sort (seiri): Distinguish necessary from unnecessary items and eliminate the latter.
- Straighten (seiton): Arrange tools and materials so that everything has a designated place.
- Shine (seiso): Clean the workplace and remove clutter.
- Standardize (seiketsu): Develop and implement standardized procedures to maintain order.
- Sustain (shitsuke): Reinforce the first four steps with continuous discipline.

**Visual factory** uses visual displays and controls to make problems and operating conditions immediately obvious. Charts showing quality, delivery, downtime, and productivity trends, along with production boards, keep everyone informed. Clear work instructions, lines, signs, and labels ensure that the right components are at the right place and time, reducing variation and waiting.

**Total productive maintenance** manages operations with preventive maintenance, load balancing, and streamlined flow control to prevent unplanned downtime, which is a major source of waiting waste.

**Standard work** uses capacity resource planning to determine the most efficient combination of operations, ensuring consistent cycle times and reducing motion and over-processing.

By applying these tools during the Improve phase, a Six Sigma project systematically removes the seven forms of muda, leading to processes that are faster, more reliable, and more customer-focused.

## Exam Tips

- Given a process scenario, identify which of the seven wastes (overproduction, correction, inventory, motion, conveyance, over-processing, waiting) is present and explain how it consumes resources without adding value.
- Differentiate between pull and push systems: a pull system limits work-in-process based on actual consumption, directly reducing overproduction and inventory waste.
- Describe a poka-yoke solution that would prevent a specific error from reaching the next process step, and explain how that eliminates correction waste.
- Select the correct 5S step (sort, straighten, shine, standardize, sustain) to address a described housekeeping or organization problem.
- Interpret a spaghetti diagram or a value stream map to locate motion, conveyance, or over-processing wastes and propose layout or flow changes to eliminate them.