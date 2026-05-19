---
title: "Design of Experiments Graphs and Plots"
description: "Construct and interpret main effects and interaction plots using full factorial and one-factor experiment data for Six Sigma improve projects."
---

## Dot Plots for One-Factor Experiments

A dot plot places every individual response measurement above the factor level at which it was collected. The horizontal axis carries the factor settings, while the vertical axis shows the measured outcome. Each test result appears as a single dot aligned with its treatment group.

In a completely randomized one-factor experiment, a dot plot quickly reveals the central tendency and spread within each group. For example, a moisture content study ran batches at three temperatures: 180°F, 200°F, and 220°F. Four batches were produced at each temperature, and the moisture percentages were recorded. Plotting all twelve data points as a vertical cluster above each temperature label allows the team to see whether higher temperatures shift the moisture values upward. The visual separation of the clusters suggests a main effect: most readings at 220°F sit noticeably higher than those at 180°F. The dot plot shows that an increase in temperature seems to raise moisture content.

A dot plot alone cannot confirm statistical significance. Experimental error can create apparent differences that are not real. To decide whether the observed effect exceeds random noise, the team must apply analysis of variance (ANOVA). ANOVA compares the variation between the temperature averages with the variation within each temperature group. If the between-treatment variation is large relative to the within-treatment variation, the F-test will produce a small p-value, and the team declares the factor effect significant. The dot plot serves as an exploratory graph, pointing the team toward formal hypothesis testing.

## Main Effects Plots

A main effects plot graphs the average response at each level of a factor. To build one, compute the mean of all observations taken at each factor setting. Mark those averages on a plot where the horizontal axis shows the factor levels and the vertical axis shows the response. Connect the averages with straight line segments.

For the moisture study, the three column averages were 10.6% at 180°F, 11.7% at 200°F, and 13.5% at 220°F. Plotting these three points and joining them creates a line that rises from left to right, capturing the direction and magnitude of the temperature main effect.

The steepness of the line communicates the size of the main effect. A flat line across the levels indicates that the factor has little influence on the response. In a two-level factorial design, the main effect is calculated as the difference between the average response at the high level and the average at the low level. For factor F, the main effect was F(high) minus F(low) equal to zero, so the main effects plot would show two points at the same height. For factor S, the main effect was –2.50, meaning the high-level average was lower than the low-level average; the plot line would slope downward.

Main effects plots are most reliable when interactions are absent. If the effect of one factor depends on the level of another, a main effects plot may mask that dependency. Nevertheless, the plot provides a first-order view of which factors drive the response and helps the team focus on the most influential inputs.

## Interaction Plots

An interaction plot displays how the effect of one input factor changes depending on the level of another factor. To construct an interaction plot for two factors, follow these steps.

1. Obtain the mean response for every combination of the two factors. In a replicated 2² full-factorial experiment with factors A and B, the four cell means were: A low, B low: 28.4; A low, B high: 33.0; A high, B low: 24.7; A high, B high: 37.3.
2. Place factor A on the horizontal axis and mark its low and high levels.
3. Draw a separate line for each level of factor B. Plot the mean response at A low and A high for B low, and connect those two points with a solid line. Then plot the means for B high and connect them with a dashed line.
4. Examine the lines. If they are parallel, the two factors act additively: the effect of moving A from low to high is the same regardless of B’s setting. If the lines are nonparallel or cross, an interaction is present.

In the example, the line for B low drops from 28.4 to 24.7 as A moves from low to high, while the line for B high rises from 33.0 to 37.3. The lines cross, revealing a strong interaction. The calculated interaction effect A×B was 4.0, confirming that the effect of changing A depends on B’s level.

Presence of interactions means that main effects are not additive. A team cannot simply add the separate main effects to predict the combined response. The interaction plot makes this non-additivity visible and guides decisions: when lines cross, the team must control both factors together to optimize the response. In a fractional factorial design, interactions may be confounded with main effects, so the team must verify that confounded interactions are negligible before relying on main effects plots alone.

## Connecting Graphs to Statistical Significance

All design of experiments graphs provide visual hypotheses about which factors matter. Formal confirmation always comes from ANOVA. The ANOVA p-value compares the factor’s effect with experimental error. When the p-value falls below the chosen alpha risk (often 0.05), the team rejects the null hypothesis and declares the factor or interaction significant.

Graphs then become communication tools. A dot plot shows the raw data spread. A main effects plot summarizes the level means and effect magnitude. An interaction plot reveals whether two factors work together. Used alongside ANOVA results, these plots let stakeholders understand which settings deliver the best process performance and why.

## Exam Tips

- Given raw data from a one-factor experiment, sketch a dot plot by placing every observation as a point above its factor level. Use the vertical separation of the dot clusters to form an initial guess about the main effect before running ANOVA.
- From a table of factor-level averages, draw a main effects plot by connecting the mean response at each level with straight lines. A steeper slope signals a larger main effect.
- For a 2² factorial design with replicate runs, compute the four cell means. Plot factor A on the x-axis and draw one line per level of factor B. If the lines are parallel, no interaction exists; if they cross or diverge, interaction is present.
- Interpret an interaction plot numerically: calculate the interaction effect as the difference between the average of cells where the two factors have the same sign and the average where they have opposite signs. A nonzero value indicates non-additivity.
- Remember that all DOE graphs are exploratory. Only the F-test from ANOVA can confirm significance at a chosen alpha level. Use the plots to illustrate the conclusions, not to replace the statistical test.