---
title: "Multi-vari Studies"
description: "Detailed study notes on multi-vari studies for the ASQ CSSGB exam, covering types of variation, chart construction, sampling plans, interpretation, and iterative process improvement."
---

## Introduction to Multi-vari Studies

Variation in processes can appear in different ways, especially when products or services are complex. A shaft may have a different diameter at one location than at another, or customer service calls in the first hour of the business day may differ from calls later in the day. A product might fit an assembly at one end but not in the middle, or a manufacturing shift might produce different variation than the other two shifts. Similar patterns occur in service sectors across different centers or periods of the year. As a Green Belt, you analyze these variations, understand their sources, and plan improvements. Multi-vari studies help you accomplish this both analytically and graphically.

Multi-vari studies are the ideal tool for investigating the stability or consistency of a process. They determine where variability originates within a process. The multi-vari chart lets you analyze three fundamental types of variation: cyclical, temporal, and positional. It also guides improvement by highlighting areas of excessive variation to explore further. The chart consists of a series of vertical lines, or other appropriate schematics, placed along a time scale. Each line’s length represents the range of values found in that sample set.

## Types of Variation in Multi-vari Analysis

The three types of variation that a multi-vari study examines are defined by their source relative to the product or process. The table below summarizes them.

| Types of variation | Piece                       | Batch/lot                          |
|--------------------|-----------------------------|------------------------------------|
| Positional         | Within-part                 | Within-batch / within-lot          |
| Cyclical           | Part-to-part                | Batch-to-batch / lot-to-lot        |
| Temporal           | Over time (shift-to-shift)  | Over time (shift-to-shift)         |

Positional variation is often called within-part variation. It refers to variation of a characteristic on the same product, for example the diameter of a shaft measured at different depths or orientations. Cyclical variation is also known as part-to-part or lot-to-lot variation. It captures differences between successive pieces or batches produced under essentially the same conditions. Temporal variation, often called shift-to-shift variation, occurs as changes over time due to tool wear, operator changes, environmental conditions, or other time-related factors. By separating these sources, a multi-vari study reveals which category contributes the most to overall process variation and therefore deserves the first attention.

## The Multi-vari Chart

A multi-vari chart displays sample ranges along a time axis. The measured values appear on the vertical axis, time or sample sequence on the horizontal axis. For each sample, the chart shows the range of the measurements, often as a vertical line connecting the minimum to the maximum. By connecting corresponding measurements with lines, the chart reveals patterns.

Three common patterns that emerge illustrate different variation conditions. Excessive variability within a part may appear as a tapering shape where one end of the part consistently lies near the upper specification limit and the other near the lower limit. Less variability shows a relatively compact grouping where the center is thicker or more consistent. A variability shift over time appears when the entire distribution drifts upward or downward, indicating a temporal change such as tool wear.

## Procedure for Conducting a Multi-vari Study

The Green Belt follows a structured sampling plan that captures within-sample, sample-to-sample, and over-time variation. The procedure consists of these steps.

1. Select the process and the characteristics to be investigated.
2. Select a manageable sample size, typically three to five samples, and decide the frequency and timing of data collection. Begin by understanding the variations within and between samples.
3. Record the time and values from each sample set in a table format.
4. Plot a graph with time on the horizontal scale and the measured values on the vertical scale.
5. Connect the observed values with lines to create the multi-vari chart.
6. Observe and analyze the chart for variation within the sample, sample-to-sample, and over time.
7. Conduct additional studies to concentrate on the area of apparent maximum variation.
8. Make process improvements and repeat the multi-vari study to confirm the results.

When necessary, you may further refine the experiment by calculating statistically valid sample sizes. The initial plan focuses on capturing all three types of variation with a manageable number of samples so that the analysis can proceed without delay.

## Application Example: Stainless Steel Casting

A Six Sigma team addressed a leakage problem in a stainless steel casting with a tight-tolerance inner diameter. A piston moves inside this closed-end cylinder, and a poor seal leads to leaks. Many theories existed: lathe chuck squeezing, tooling issues, and more. Past attempts to fix the problem lacked a structured approach.

A Green Belt conducted a multi-vari study. To capture within-part variation, the inner diameter was measured at three depths: top, middle, and bottom. To capture out-of-round variation, diameters were measured at three angles: 12 o’clock, 2 o’clock, and 4 o’clock. To capture variation over time, five parts were selected at approximately equal intervals during a shift. All measurements used equipment with adequate discrimination and were recorded on a data sheet.

Plotting the data from the first five parts on a multi-vari chart revealed that part-to-part variation dominated. Out-of-round and top-to-bottom variations were present but much smaller. The team therefore focused on reducing part-to-part variation. The investigation traced the cause to the casting process itself. A new precision casting supplier reduced part-to-part variation dramatically.

When the team repeated the study with precision castings, the multi-vari chart showed that part-to-part variation was now minimal, but out-of-round variation had become the dominant source. The team then brainstormed causes for out-of-round conditions. An initial theory pointed to chuck clamping pressure, but careful plotting with orientation numbers showed no consistent pattern: the longest dimension varied randomly across orientations. That evidence eliminated chuck pressure as the cause.

A second-shift operator suggested that machining chips left from the previous operation were being burnished into the surface, causing random diameter differences. The team decided to remove parts from the chuck and pressure-wash them before the burnishing step. Some objected that this had been tried a year earlier with no improvement. The Green Belt pointed out that at that time the large part-to-part variation would have masked any reduction in the minor variation now visible. With the part-to-part variation reduced, the benefit of pressure-washing could be detected. The follow-up multi-vari study confirmed a noticeable reduction in out-of-round variation.

After that improvement, a team member noticed a remaining temporal pattern, likely caused by tool wear. By initiating a tool wear verification and change process, the team reduced variation even further. This iterative use of multi-vari studies illustrates the method’s power: dominant variation sources are reduced, uncovering the next most important source, and the process improves step by step.

## Transactional Process Considerations

Multi-vari studies apply equally to transactional processes such as bank teller transaction times, call center average handle time, or healthcare treatment times. In a transactional process, however, the transaction itself varies by customer need. To obtain a meaningful multi-vari analysis, first stratify the data by transaction type and complexity. Only then can the positional, cyclical, and temporal variation within each stratum be isolated and interpreted correctly.

## Relevance to Six Sigma Projects

Multi-vari studies bring structure to the Analyze phase. Instead of acting on opinions or trying many unverified ideas, the team uses a chart to objectively identify the largest source of variation. The case study shows how this prevents wasted effort: team members with theories about out-of-round were asked to hold those ideas until the dominant part-to-part variation was addressed. Once it was, their energy could be focused on the next real problem. The method provides a visual, data-driven way to communicate variation sources and to prioritize improvement actions. Each improvement is verified by repeating the study, ensuring that the process truly became more consistent and that new variation patterns did not emerge.

## Exam Tips

- Given a process description, design a multi-vari sampling plan that captures positional, cyclical, and temporal variation by specifying where and when to take measurements.
- Interpret a multi-vari chart by visually comparing the ranges and heights of line segments to determine whether within-part, part-to-part, or shift-to-shift variation is dominant.
- Identify the next step in a multi-vari improvement cycle: after reducing the dominant variation source, collect new data and replot to see which source becomes the new primary target.
- Distinguish between the three variation types in a table or list of examples, and correctly label them for a piece (positional, cyclical, temporal) or a batch.
- Apply the multi-vari procedure steps to a simulated case, including stratification for transactional processes, and justify the choice of sample size and frequency.