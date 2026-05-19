---
title: "Plan-Do-Check-Act (PDCA) in the Control Phase"
description: "Applying the PDCA cycle to sustain process improvements using control plans, SPC charts, OEE, and corrective actions."
---

## The PDCA Mindset in the Control Phase

Sustaining process improvements requires a continuous cycle of planning, doing, checking, and acting. The Control phase tools described in the source texts form an operational Plan-Do-Check-Act (PDCA) loop. The control plan provides the plan. Daily operation follows standard procedures and data collection. SPC charts and overall equipment effectiveness (OEE) supply the check. Corrective actions, FMEA revision, and team reflection drive the act step, feeding into the next cycle of improvement.

## Plan: Building the Control Plan

A written control plan tells process owners exactly how to monitor the process and what to do when measurements fall outside acceptable ranges. According to the source material, common elements of a control plan include:

- Company, division, or department name  
- Name of the person who created the plan, the creation date, the last editor, and the last edit date  
- Project or process name and the process owner  
- Process steps where control action is required  
- CTQ or metric associated with each action  
- Specification limits (lower and upper), unit of measurement, method of measurement  
- Sample size and frequency of measurement  
- Person responsible for measurement  
- Where the data is recorded  
- Corrective actions and references to associated policy and procedure documents  

The plan can take the form of a spreadsheet, a specialized digital document, or a hard-copy posting at a workstation. The source gives the example of a chocolate bar process. For the step "Addition of sugar to batch," the CTQ is total amount added, with a lower specification limit of 4.90 cups and an upper specification limit of 5.10 cups. The method of measurement is a 6-cup sugar test bowl, sampling one batch every two hours. The corrective action instructs the operator to manually measure the correct amount for the current batch, calibrate the sugar disbursement machine per a standard operating procedure, and test the first batch after calibration. For the "Heating of batch" step, temperature is monitored with an integrated digital thermometer, and the corrective action requires the operator to turn off the machine, waste the inappropriately heated batch, and report the calibration issue to maintenance.

## Do: Operating the Process and Collecting Data

During the Do step, operators run the process according to standard procedures. The source describes how operators participate in total productive maintenance (TPM) by preventing deterioration through regular inspections, correcting deterioration through cleaning, and measuring deterioration through data collection. Visual management tools support correct execution: signs, posted matrixes, colour coding, pictorial standard operating procedures on posters, and step-by-step graphics on equipment. In the chocolate bar example, the mixing operator uses a designated measuring tool, records data in a mix operation log spreadsheet every two hours, and follows the visual and written instructions.

## Check: Monitoring with SPC and OEE

The Check step compares actual performance against the planned standards. Two primary monitoring methods appear in the source texts: statistical process control (SPC) charts and overall equipment effectiveness (OEE).

### SPC Charts and the Eight Out-of-Control Tests

A basic control chart contains plot points, an x-bar (average) line, and lines at one, two, and three standard deviations above and below the average. The three-sigma lines are the upper control limit (UCL) and lower control limit (LCL). The zones between the lines are labelled C (within one standard deviation), B (between one and two), and A (between two and three). The source specifies eight tests that indicate a process may be out of control:

1. **One point outside the UCL or LCL.** This signals a major problem that requires immediate action; the probability of a random point beyond three standard deviations is only 3 in 1,000.  
2. **Nine points in a row on one side of the centre line.** This suggests a shift in the process. If the shift was intentional and the reason is known, no action is needed; otherwise, investigate.  
3. **Six points in a row trending up or down.** This indicates a developing trend toward lower or higher values, requiring investigation unless a known reason exists.  
4. **Fourteen points alternating up and down.** This pattern may indicate variation due to machines, employees, shifts, or overcorrection.  
5. **Two out of three points in Zone A (or beyond) on the same side.** This points to a special cause creating sudden high variation.  
6. **Four out of five points in Zone B (or beyond) on the same side.** This suggests a major cause or a shift problem.  
7. **Fifteen points in a row within Zone C above or below the centre line.** This often means the control limits are no longer appropriate because variation has been reduced; teams should recalculate limits.  
8. **Eight points in a row on either side of the centre line with none in Zone C.** This may indicate mixed resources or two separate processes being charted as one.

Automated data collection and dashboard displays allow continuous checking. When manual collection is necessary, periodic graphing still applies, though it is less likely to catch a control problem in real time.

### OEE as a Checkpoint

OEE helps assess when equipment is making good product compared with the total potential time. The source defines three factors with numerical examples:

- **Availability:** The percentage of planned available time that the equipment actually operates. Example: 1500 available hours minus 250 hours of unplanned downtime yields (1500 – 250) / 1500 = 83.33%.  
- **Performance efficiency:** The ratio of the theoretical time needed for the units produced to the actual operating time. Example: cycle time 0.5 hours/unit times 2000 units equals 1000 hours; divided by 1250 operating hours gives 0.80.  
- **Quality rate:** First-pass yield, the percentage of output that is good product.

Tracking these components reveals whether losses come from downtime, reduced speed, or defects, and tells the team where to act.

## Act: Corrective Action, FMEA Revision, and Future Planning

The Act step begins when the Check step detects an out-of-control signal or a declining OEE component. The control plan prescribes the response. In the chocolate bar example, a sugar amount outside limits triggers operator action: manually measure the correct amount, calibrate the machine following the SOP, and test the first batch after calibration. If temperature goes out of limits, the operator stops the machine, wastes the batch, and reports to maintenance because the operator cannot calibrate the temperature sensor. Building corrective action at the operator level whenever possible minimises downtime and keeps employees engaged with quality.

TPM participants also act on findings. Maintenance personnel perform root cause analysis of downtime, conduct preventive maintenance, and train operators and supervisors. Engineers help eliminate design weaknesses, design for maintainability, and prevent contamination. Managers and supervisors ensure accountability and that data collection sheets are completed.

During the Control phase, teams revisit the failure modes and effects analysis (FMEA). They mark completed actions and recalculate risk priority numbers. This confirms that the solutions from the Improve phase actually reduced risk and helps identify the next priority for continuous improvement.

After the process demonstrates stability and capability, the team holds a celebration and reflection meeting. They close loose ends, recognise contributions, and brainstorm ideas for future improvement projects while the lessons are fresh. Those ideas flow into the next planning cycle.

## Exam Tips

- Map each PDCA phase to a specific Control phase deliverable: Plan to the control plan document, Do to daily operation and data collection, Check to SPC rules and OEE, Act to corrective actions and updated FMEA.  
- When presented with an SPC chart, identify which of the eight tests triggered the alarm and describe the corrective action exactly as a control plan would prescribe.  
- Understand that OEE breaks equipment losses into availability, performance, and quality, and that each factor points to a different category of corrective action (downtime, speed, defects).  
- For a scenario showing 15 points inside Zone C, recognise that the control limits need recalculation because process variation has been reduced; this is an Act activity.  
- Explain why operator-level corrective action, as in the chocolate bar example, is preferred: it reduces downtime and empowers process owners.  
- Remember that revisiting the FMEA during Control provides documented proof of risk reduction and seeds the next improvement project, completing the PDCA loop.