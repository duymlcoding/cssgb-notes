---
title: "Kaizen and Kaizen Blitz"
description: "Core Lean tools and waste elimination methods that underpin continuous improvement and rapid improvement events, drawn from process design, SIPOC, standard work, and the seven muda."
---

## Lean Foundation for Continuous Improvement

Kaizen, continuous improvement, is built on a mindset that processes are never developed in isolation. Process design requires active involvement from suppliers and representatives across all affected areas. The focus throughout is meeting customer needs without adding activities or costs that do not add value. Engaging employees, communicating the benefits of standard work, and addressing employee concerns are essential to achieving sustained improvement. By involving the right people and making improvement a daily practice, teams can target waste, stability gaps, and capacity mismatches.

### Process Design and SIPOC

Suppliers-Inputs-Process-Outputs-Customers (SIPOC) charting anchors process development on customer needs. SIPOC highlights how internal customers must be served to satisfy external customers. The methodology identifies who receives or is affected by every output. Then it defines the inputs connected to those customer requirements and communicates them to suppliers, both internal and external. Driving the process from customer requirements creates traceability from each process step to a fulfilled customer requirement. After analyzing the suppliers, inputs, outputs, and customers, the team maps the steps that convert inputs to outputs in an efficient, customer-focused manner. SIPOC simplifies complex systems by showing interrelationships and interdependencies between processes, and that structured view of who serves whom improves process design.

### Process Stability

Stable processes yield predictable costs, quality, and cycle times. Without stability, outcomes cannot be determined accurately and planning becomes difficult. Five elements must be controlled to achieve stability.

- Method: Process steps are clearly defined and consistently followed.
- People: Minimum levels of training and qualification are established.
- Machinery: Equipment is designed and maintained in a consistent manner.
- Measurement: Instruments are properly used, maintained, and regularly calibrated.
- Materials: Input quality is consistent.

Process design minimizes variation from each of these elements. Once a process is stable, the expected variation becomes predictable within limits set by the process average and standard deviation. Predictable performance is a prerequisite for sustained quality, cost, and delivery performance.

### Process Capability and Capacity

Process capability compares the voice of the customer (VOC) with the voice of the process (VOP). The higher the result, the more capable the process is of meeting customer needs.

Process capacity is calculated using a lean capacity sheet that examines equipment and manual time in a work area. The required inputs are machine time per piece, manual time per piece (operator activity while the machine is not producing), total cycle time per piece (machine plus manual time), number of pieces before a tool change is needed, time to perform a tool change, tool change time per piece (tool change time divided by pieces between changes), and available time per shift.

The capacity formula is:

Capacity = Available time per shift / (Total cycle time per piece + Tool change time per piece)

A step that cannot produce to its theoretical capacity pinpoints where problem-solving efforts should focus. Additionally, understanding capacity helps relate output to takt time.

## Identifying and Eliminating Waste (Muda)

Waste, or muda, is a non-value-added task within a process. Eliminating muda is a driving concept of Lean and the Toyota Production System. Seven common types of waste must be recognized and removed.

**Overproduction**
Producing a part, product, or service too fast, at the wrong time, or in excessive quantity. Example: printing 1,000 pages per hour when a downstream folding machine can handle only 800 pages creates inventory and potential errors. In service environments, creating reports nobody reads or preparing equipment that will never be used is overproduction. The key countermeasure is planning based on known demand and process capability. Producing to takt and matching output to the slowest constraint prevents this waste.

**Correction (Rework)**
Work that is rerouted back for correction because of defects or incomplete information. Rework increases total process time and consumes extra labor and materials. In a call center, a poorly completed claim form sent back to the original queue causes re-handling and delays. Two actions are required: address the root cause of errors through mistake-proofing (poka-yoke), proper training, or process redesign, and design quality steps that minimize rework loops. For example, empower downstream workers to reroute work correctly instead of returning it to the original queue, while holding accountability through metrics.

**Inventory**
Materials, work-in-process, or information stacking up before a process step, often called a bottleneck. It can be caused by overproduction, batch processing, or purchasing inputs before they are needed. Digital queues, email inboxes, and paper stacks are inventory waste. Reducing batch sizes lowers lead time and inventory. Base inventory decisions on historic demand. A shipping center should not order 300,000 boxes if the weekly need ranges from 50,000 to 100,000.

**Motion**
Unnecessary movement of people during a process. Clicking between screens to enter data, walking back and forth to retrieve tools or documents, and poor workspace layout all create motion waste. A spaghetti diagram, a bird’s-eye drawing of the workspace with a line tracing actual movement, reveals inefficient travel paths. The resulting diagram looks like tangled spaghetti and highlights where movements cross or extend unnecessarily. Simplifying layout and integrating information on a single screen eliminates this muda.

**Conveyance (Transportation)**
Movement of outputs, products, or resources. In manufacturing, carrying glue from a distant inventory room to the assembly line is conveyance waste. In administrative processes, routing an expense report through multiple physical stops or forwarding an email through four levels of hierarchy before information reaches the requester are conveyance wastes. A spaghetti diagram or process map locates these movements. Often conveyance waste is a symptom of correction loops, so addressing root-cause defects reduces both.

**Over-processing**
Putting more work or resources into a product or service than the customer values. In a healthcare office, spending an hour to verify insurance benefits for a routine visit is over-processing. Painting the underside of an inside cabinet shelf where nobody sees it, ironing restaurant table linens to crisp seams that will never be visible, or building an app with 100 features when 99 percent of users only use 10 are all over-processing. A value stream map identifies process steps that add no value. Every step should do just enough useful work to meet customer expectations, balancing quality with speed.

**Waiting**
Idle time of people or equipment caused by uncoordinated steps, unreliable processes, large batches, rework, or long changeovers. A cashier waiting while a register drawer is counted can be eliminated by preparing interchangeable drawers in advance and swapping them in seconds. Construction crews standing idle while a predecessor task finishes illustrate waiting. In digital workflows, waiting occurs when approvals or information are delayed. Reducing batch sizes, leveling workloads, and coordinating handoffs eliminates waiting.

## Applying Lean Tools in Improvement Events

SIPOC helps a team clarify the process and link every step to customer requirements. The process capacity calculation quickly identifies a bottleneck step that cannot meet demand. A spaghetti diagram visualizes motion and conveyance waste in a physical workspace, while a value stream map reveals over-processing and unnecessary transportation in both physical and digital flows. For each waste identified, teams address root causes through mistake-proofing, layout changes, standard work, and demand-based scheduling.

Engaging employees throughout these activities is critical. Communicating the benefits of standard work, understanding concerns, and involving the right people from all affected areas makes success easier to obtain. Teams use data, average order patterns, capacity numbers, motion time measurements, to plan improvements and sustain them with standard work.

## Exam Tips

- When given a scenario with a printer running faster than a folder, classify the extra printed pages as **overproduction** and identify the resulting pile-up as **inventory** waste.
- Given a spaghetti diagram tracing a worker’s path, calculate whether rearranging equipment can reduce **motion** waste and explain the impact on cycle time.
- Use the process capacity formula: Capacity = Available time / (Total cycle time + Tool change time). Compute capacity for a shift and identify the step that falls short of takt time as the **bottleneck requiring focused improvement**.
- In a service example where a claim is repeatedly sent back to the original queue for missing information, identify **correction (rework)** as the primary waste, and propose mistake-proofing the form or training to eliminate the root cause.
- To eliminate **over-processing**, map the process and ask whether each step’s output is something the customer is willing to pay for. Remove steps that add no value from the customer’s perspective.