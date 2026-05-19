---
title: "Process Analysis and Documentation"
description: "Tools and techniques for mapping, analyzing, and documenting processes in the Measure phase of a Six Sigma project, including flowcharts, SIPOC, cause-and-effect diagrams, Pareto charts, and relationship matrices."
---

## Process Maps and Flowcharts

ISO 9000 defines a process as a set of interrelated or interacting activities that transforms inputs into outputs. Visualizing a process with flowcharts and process maps makes it easier to understand, communicate, and improve. Practitioners often use the terms interchangeably, but process maps contain additional details beyond the basic sequence of steps. A flowchart shows each step, decision point, input, and output. A process map adds information such as costs, setup time, cycle time, inventory, types of defects that can occur, and the probability of those defects.

Consistent mapping symbols, as defined in international standard ISO 5807:1985, help different people interpret the map in the same way. The most frequently used symbols include:

- A rectangle for a process step.
- An arrow for the direction of flow.
- A diamond for a decision box with multiple outgoing arrows.
- A rounded or elongated shape for start and end points.
- A document shape for an input or output document.
- A trapezoid for manual operation.
- A bullet shape for delay or wait.
- A circle or connector for linking to another page.

Process mapping is often the first step in improving a process. Risk analysis tools such as process failure mode and effects analysis (PFMEA) begin with process mapping. Value stream mapping, used in lean projects, is a form of process mapping that uses different icons.

A swim lane process map arranges process steps into lanes representing departments, functions, or stakeholders. Each process block aligns with the lane of the entity that performs the step. This view makes cross-functional handoffs and responsibilities immediately visible.

### Creating a Flowchart or Process Map

Follow this sequence when building any flowchart or process map:

1. Define the boundaries. Identify the start and end points, key inputs, and key outputs of the process.
2. Collect all process steps. Use team brainstorming or, for an existing process, walk the process to capture what actually occurs. Do not worry about sequence yet; gather every step.
3. Build the sequence. Arrange steps in the proper order. Identify parallel activities and alternative paths. Ensure that decision points branch correctly.
4. Draw the chart using standard mapping symbols.
5. Verify the chart. For a new process, confirm the flowchart represents the intended operation. For an existing process, verify that the chart matches reality. Perform this verification as a team to catch overlaps or gaps between process segments.

Keep flowcharts current when the process changes. Regular audits for safety, quality, or environmental compliance become easier when up-to-date visual standards are readily available.

### Common Process Mapping Mistakes

Avoid these pitfalls:

- Inadequate or inappropriate team representation.
- Unclear scope, leading to redundant flows when multiple teams map overlapping processes.
- Failing to walk the actual process and instead documenting what people assume happens.
- Spending excessive time trying to make the map perfect instead of focusing on the process itself.

The biggest mistake is never attempting to map the process at all.

## Written Procedures and Work Instructions

Written procedures and work instructions drive consistency in business and manufacturing processes, supporting yield improvement, root cause analysis, and traceability. Whether or not an organization pursues ISO 9001 registration, documented procedures provide a repeatable reference.

Procedures describe:

- What is done during the process
- Why it is done (business reason, purpose)
- Where it is done (location or process step)
- When it is done (trigger)

Work instructions add two more dimensions:

- Who does what (personnel with a specific skill set)
- How it is done (step by step)

Where no internal procedure exists and no standard requires one, the activity may be conducted as a method, an unwritten but consistently followed approach. In deciding which processes to document, consider factors such as effect on quality, risk of customer dissatisfaction, statutory or regulatory requirements, economic risk, effectiveness and efficiency, competence of personnel, and complexity of the process.

Work instructions can take many forms: written instructions, checklists, flowcharts, photographs, drawn pictures, videos, electronic screen shots, or electronic software-driven process steps.

## Process Inputs and Outputs

Every process has input variables, output responses, and feedback loops. Examples of inputs include needs, ideas, expectations, requirements, information, data, documents, and resources. Outputs include designs, decisions, results, measurements, products, services, proposals, solutions, authorizations, and actions.

Identifying inputs and outputs is essential before analyzing relationships. A process map provides detailed visibility into these elements, but a detailed map of an entire value stream can become overwhelmingly complex. A SIPOC chart gives a bird’s-eye view at the enterprise level. SIPOC stands for Suppliers, Inputs, Process, Outputs, and Customers. Limit the process portion to four to seven high-level steps to manage complexity. A SIPOC helps a team quickly grasp the project scope and understand how the process fits into the larger organization.

The relationship between inputs and outputs is expressed as y = f(x). Controlling variation in the input variables (x) reduces variation in the output response (y). Tools for exploring these relationships include cause-and-effect diagrams, relationship matrices, scatter diagrams, and design of experiments.

## Cause-and-Effect Analysis

The cause-and-effect diagram, also called the Ishikawa or fishbone diagram, organizes potential causes of a problem into categories. Traditional manufacturing categories are personnel, machines, materials, methods, measurement, and environment. Adapt the categories to the context. A software development team might use people, processes, products, resources, and miscellaneous.

Begin by drawing a large empty diagram with the effect (problem statement) at the head of the fish. Use brainstorming to populate the diagram. Brainstorming encourages divergent thinking where quantity of ideas takes priority. A trained facilitator enforces ground rules and prevents participants from criticizing or discarding ideas during the session, which would inhibit contributions. A typical session generates 25 to 40 ideas.

After collecting ideas, convergence tools condense the list and identify priorities. Nominal group technique (NGT) is especially useful when the topic is sensitive or team members span several organizational levels. To apply NGT

- The team generates ideas silently.
- The ideas are displayed, and duplicate or redundant items are removed.
- Members silently rank the remaining items.
- The ranks are tallied to produce a prioritized list.

Because ranking happens individually, dominant members do not sway the outcome. Multivoting is an alternative in which participants distribute 100 points among the choices based on relative importance.

The affinity diagram organizes a large number of ideas into natural groupings. Use it when the team faces an overwhelming set of facts or when group consensus is needed. It is particularly helpful for analyzing qualitative customer feedback.

CEDAC, the cause-and-effect diagram with addition of cards, displays a large fishbone on a wall. Employees add causes directly on the diagram using sticky notes. Success depends on the organization’s culture and communication climate.

Once potential causes are identified, collect data to verify their impact. The various causes are then prioritized on a Pareto chart.

## Pareto Charts

A true Pareto chart arranges categories in descending order of frequency (or other measures such as cost or weighted criticality). It includes a secondary axis showing cumulative percentage and a cumulative percentage line. The chart visually separates the “vital few” from the “trivial many,” reflecting the 80:20 principle popularized in quality improvement by Dr. Joseph Juran based on Vilfredo Pareto’s work.

Constructing a Pareto chart correctly requires aggregating data at the right level of detail. Overly specific defect descriptions, such as “scratch on the display screen,” “scratch on the nameplate,” and “scratch on the body,” scatter occurrences across too many categories. The resulting chart shows vital many and trivial few, defeating the purpose. Generalize such items into a single “Scratches” category to surface systemic issues that warrant root cause resolution. Once the top systemic category is selected, the team can drill down using the specific data for that category.

Weighted Pareto charts assign criticality weights or costs to each occurrence. Multiply the frequency by the weight and create the chart using the weighted score. This approach directs resources toward problems that have the greatest impact on the customer or the business.

## Measles Charts

When a product is large and defect opportunities are numerous, a measles chart saves time and clarifies location information. It is a pictorial check sheet, often a drawing of the product, on which inspectors mark the type and location of each defect. Car rental contracts, for example, use a measles chart of the vehicle to circle preexisting damage during checkout.

## Relationship Diagrams

A relationship diagram displays the strength of relationships between variables, such as process inputs and outputs, or causes and effects. Teams assign symbols to represent strong (● or 9), medium (○ or 3), and weak (△ or 1) relationships. They then sum the scores across rows and columns. Adding a weight column or row refines the prioritization by incorporating the relative importance of each output or effect. The resulting weighted scores guide the focus of improvement efforts.

## Exam Tips

- You are given a list of process activities from a warranty replacement scenario. Draw a swim lane flowchart that separates customer, customer support, and warehouse actions. Use standard symbols and align each step in the correct lane.
- A colleague presents a Pareto chart based on 30 distinct defect codes, each with two or three occurrences. Recommend generalizing the codes into broader categories before redrawing the chart, and explain why this reveals the vital few.
- Describe the steps you would take to create a SIPOC for an order-to-cash process, making sure to limit the process block to a maximum of seven high-level steps.
- Plan a cause-and-effect brainstorming session for a machining surface-defect problem. State which categories you would use, how you would enforce the no-criticism rule, and how you would then use NGT to converge on the top three causes.
- Prepare a weighted Pareto when defect occurrences are accompanied by a cost-of-rework field. Show the calculation of the weighted score and the construction of the chart with cumulative percentage.
- For an inspection process that records detailed scratch locations on large panels, propose a measles chart as the primary data-collection tool and justify it over a text-based log.