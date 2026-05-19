---
title: "DOE Basic Terms"
description: "Foundational concepts for Design of Experiments including assumptions, application, SDCA, simulation studies, and main effects analysis."
---

## Overview of Design of Experiments
Design of Experiments (DOE) is a systematic method for moving through stages of experimentation to understand and optimize a process. Each experiment provides a different answer, so the experimenter can logically progress toward the final optimal settings. DOE is more suitable for optimizing a process than for solving problems. In practice, the operator works with engineering, supervisors, and Six Sigma practitioners to look for variation. Because operators know the machines best, they give valuable insights about what might happen when different settings are used.

## Key Assumptions for a Valid DOE
Three conditions must be in place for a DOE to be valid and successful.

### Measurement System Capability
Confirm that the measurement system is capable before the experiment begins. Continue to confirm its capability throughout the life of the experiment. If the measurement system cannot produce consistent, accurate data, the experimental results become unreliable.

### Process Stability
Start and end the experiment at standard process set points under identifiable operating conditions. Establish a baseline to reveal whether the process drifted during experimentation. Without stability and a baseline, shifts in the process could mask or distort the true effects of the factors being tested.

### Residuals
Residuals are the estimates of experimental error, defined as the observed response minus the predicted response. For the experiment to be valid, residuals should be normally and independently distributed, with a mean of zero and constant variance. This assumption ensures that the model correctly captures the systematic effects and that the error behaves randomly.

## How DOE Is Applied
The experiment designer creates a list of exact settings for each trial. Typically, eight or more test runs are made for each DOE. The operator runs the machine at the designed settings and takes random parts for testing. After the sample parts are tested and measurements recorded, a computer calculates the optimal settings based on the response data.

A confirmation test follows. Using the new settings, the team runs the process to verify that the experiment identified a better working condition. If the confirmation test proves successful, the new settings become part of the operation. The operator then updates the documentation in the work area to reflect the new process settings and parameters. This confirmation step prevents adopting changes based on chance results.

## SDCA Cycle – Standardize, Do, Check, Act
Once a process has been improved, the SDCA cycle locks in the gains. SDCA is most commonly used after a DOE-driven improvement. Teams update control plans and process sheets, then standardize the changes throughout the organization. SDCA is the outcome of applying sound recommendations based on a correct interpretation of valid effects from a properly designed experiment.

## Simulation Studies in DOE
When simulation software is used, or for any DOE initiative whether directly performed or simulated, apply a consistent set of steps:

1. **Specify** the problem, questions, business needs, and expected outcomes or answers.
2. **Prepare a plan** that includes the test data, data collection approach, alternative scenarios, milestones, and timelines.
3. **Collect the data**, identifying and addressing any potential or existing gaps.
4. **Build a model or framework** that connects inputs, process variables, and outputs.
5. **Design and run the scenarios**, clearly distinguishing between fixed and variable parameters and ensuring the reproducibility of results.
6. **Analyze and interpret the data**, verifying statistical significance for meaningful effects.
7. **Map outcomes back** to the original problems, questions, business needs, and expected outcomes to determine whether the experiment fulfilled its intent.

## Main Effects Analysis
A main effect is the estimated effect of a factor independent of any other factor. To calculate main effects, average the response values for all runs where the factor was set at a given level. This is sometimes called the average main effect.

Consider a small experiment with three factors: Feed (F), Speed (S), and Coolant temperature (C). Feed has a low level of 0.01 in/rev and a high level of 0.04 in/rev. Speed has levels 1300 and 1800 rev/min, and Coolant has levels 100 °F and 140 °F. The response is a surface finish score where a lower number is better. Table 1 shows the run structure (F = – for low, + for high) and response values from the source example.

| Run | F   | Response |
|-----|-----|----------|
| 1   | –   | 10       |
| 2   | –   | 4        |
| 3   | –   | 6        |
| 4   | –   | 2        |
| 5   | +   | 7        |
| 6   | +   | 6        |
| 7   | +   | 6        |
| 8   | +   | 3        |

The runs with Speed at 1300 rev/min are 1, 2, 5, and 6; those at 1800 are 3, 4, 7, and 8. Coolant at 100 °F appears in runs 1, 3, 5, and 7; at 140 °F in runs 2, 4, 6, and 8. Using these groupings:

- F.01 = (10 + 4 + 6 + 2) ÷ 4 = 5.5  
- F.04 = (7 + 6 + 6 + 3) ÷ 4 = 5.5  
- S1300 = (10 + 4 + 7 + 6) ÷ 4 = 6.75  
- S1800 = (6 + 2 + 6 + 3) ÷ 4 = 4.25  
- C100 = (10 + 6 + 7 + 6) ÷ 4 = 7.25  
- C140 = (4 + 2 + 6 + 3) ÷ 4 = 3.75  

These averages form the main effects.

## Interpreting Main Effects Graphs
Plot each factor’s level on the horizontal axis and the average response on the vertical axis. The main effects graphs reveal:

- A flat line (as for Feed, both 5.5) indicates the factor does not impact the response in the tested range. The team would choose the level that improves efficiency, here the higher feed rate of 0.04 in/rev because it makes the operation faster without harming surface finish.
- A steep slope downward from the low to high level (Speed from 1300 to 1800, and Coolant from 100 to 140) shows a strong effect. Since a lower response is better, the team selects the higher speed (1800 rev/min) and the higher coolant temperature (140 °F).

Factors with the greatest difference between their high and low average responses have the greatest impact on the quality characteristic of interest. The graph isolates each factor’s independent contribution, allowing the team to choose the combination that minimizes the response.

## Exam Tips
- State the three assumptions required for a valid DOE: capable measurement system confirmed before and during the experiment, process stability with a baseline, and residuals that are normally and independently distributed with zero mean and constant variance.
- Recognize that a confirmation test verifies the optimal settings identified by DOE, and successful confirmation leads to updating process documentation.
- Know that DOE is better suited to process optimization than to problem solving.
- Given a table of runs and responses, calculate a main effect by averaging the responses for all runs where the factor was at a particular level.
- Understand that the SDCA cycle (Standardize, Do, Check, Act) locks in improvements after DOE by updating control plans and standardizing changes.
- List the seven steps of a simulation-based DOE initiative, from specifying the problem through mapping outcomes back to business needs.