---
title: "Control Plan"
description: "Comprehensive study notes on control plans for the ASQ Certified Six Sigma Green Belt exam, including purpose, core elements, dynamic control planning, integration with FMEA, SOPs, gage control plans, and visual management."
---

## Purpose and Scope of Control Plans

A control plan is a structured, living document that defines the methods for sustaining process improvements and controlling the total system. It provides a single reference for operators, engineers, and process owners to track key performance indicators, take measurements, and respond to out-of-control conditions. The plan shifts the focus from blaming individuals to managing the system. Studies indicate that 80 percent of the time, the true cause of issues lies in the system rather than in operator error, so the control plan reinforces that operators follow a documented scheme. If a problem occurs, the plan helps demonstrate that the system, not the person, is at fault.

Control plans serve as the primary mechanism for transitioning an improved process back to the process owner at the end of a DMAIC project. They must be concise and easy to reference, guiding the business team on when to monitor, how to monitor, acceptable data ranges, and corrective actions. The scope encompasses dynamic control plans, quality process sheets, and standard operating procedures.

Once a process has been improved, the SDCA cycle (standardize, do, check, act) is often used to update control plans and process sheets, locking in improvements and standardizing changes across the organization.

## Key Elements of a Control Plan

Every control plan, whether a simple spreadsheet or a specialized digital document, should include a consistent set of information. Combining the template and examples from the ASQ CSSGB Handbook with the common elements listed in the training manual, the following components are essential:

- **Document identification:** Company, division, or department name; control plan number; revision level and date; originator; key contact.
- **Process and product references:** Plant, operation, part number or assembly, revision, and part name.
- **Process owner:** Person responsible for the process.
- **Process steps requiring control:** Each step where measurements or actions are applied.
- **Critical-to-quality (CTQ) characteristic or metric:** The specific feature being controlled (for example, diameter, torque, temperature).
- **Specification limits:** Lower specification limit (LSL) and upper specification limit (USL), or nominal with tolerance.
- **Unit of measurement** (cups, degrees F, IN LB, etc.).
- **Measurement method and equipment:** Identification of the gage, test equipment, or evaluation technique, including the equipment serial number when applicable.
- **Sample size and frequency:** How many units to measure and how often (for example, one per hour, five per shift, 100% inspection).
- **Control method:** The type of control tool used (X-bar chart, R chart, go/no-go gage, check sheet, separate X-bar charts).
- **Person responsible for measurement:** Operator, inspector, or other designated role.
- **Data recording location:** Where measurements are logged (control chart, log spreadsheet, process log).
- **Reaction plan or corrective actions:** Detailed steps to take when a measurement falls outside limits or a special cause is detected.

The reaction plan deserves special emphasis. Effective plans include a four-step approach modeled in the example control plan for a soft start-up valve:
1. **Containment:** Segregate nonconforming units and potentially affected product (for example, the previous hour of production) for material review board (MRB) evaluation.
2. **Diagnosis:** Verify setup, torque, component dimensions, or machine settings using checklists. Identify the root cause.
3. **Verification:** Confirm that corrective action eliminates the problem, often by testing remedied units or monitoring subsequent subgroups.
4. **Disposition:** Scrap nonconforming components, rework assemblies, retest product, or release with engineering approval.

Additional characteristics of successful control plans noted in the handbook include confirmation with operators, engineers, and internal customers; visual representation with flowcharts or graphical symbols; display of special characteristics; descriptions of relationships between characteristics and controlled process settings; identification of gages and test equipment along with sample sizes and frequencies; and traceability of actions back to the plan.

## Dynamic Control Plan (DCP)

A dynamic control plan (DCP) consolidates multiple documents into one living system. It combines standard operating procedures, control plans, failure mode and effects analyses (FMEA), gage control plans, and quality planning sheets. The DCP is treated as a document that operators have the right and responsibility to update whenever changes occur, ensuring information always reflects the current state of the process.

The DCP includes a matrix, sometimes called the DCP critical path, that contains:
- DCP launch activities and team structure.
- A question log for tracking issues and lessons learned.
- Supporting information such as blueprints, specifications, prototype plans, flowcharts, and statistical data.
- Prelaunch or preliminary controls.
- Process failure mode and effects analysis (PFMEA).
- The core control plan.
- Illustrations and instructions, often posted at the job site for easy reference.
- Implementation and maintenance procedures.

The process FMEA and the control plan form the primary focus of the DCP. All supporting information must be available to operators before launching a new line or product. Management commitment is essential to support DCP upkeep. Teams maintain a process history that feeds into a lessons-learned database and supports future designed experiments. The DCP thus strengthens the standard control plan by embedding team structure, support information, preliminary controls, and a PFMEA summary directly into everyday operations.

## Control Plan and FMEA Integration

Six Sigma teams originally use Failure Modes and Effects Analysis (FMEA) during the Analyze phase to identify potential failures and rank them by severity, occurrence, and detection, calculating a risk priority number (RPN). At the start of the Control phase, teams revisit the FMEA to recalculate RPNs after solutions have been implemented. This revision serves two purposes: it demonstrates that risk has been reduced through improvement actions, and it highlights the next failure mode or root cause that could be addressed in future projects, reinforcing continuous improvement.

The control plan then directly addresses the high-priority failure modes identified in the updated FMEA. Table 22.1 in the handbook illustrates this side-by-side relationship: for each failure mode (example: system error, bar code mismatch, timing error, power outage), the FMEA lists severity, occurrence, detection, and RPN, while the control plan defines the mitigation (graceful shutdown, bar code checking, alarm, cable backup), validation, and run-time controls. This linkage ensures that process controls are deliberately designed to prevent the failures most critical to quality.

## Standard Operating Procedures (SOPs)

Once a process has been updated and validated, standard operating procedures document the step-by-step instructions for completing tasks. SOPs create consistency and establish the proper methods for performing work. Documented evidence of the correct procedure prevents fault-finding and protects operators from being blamed for system-level issues. SOPs often serve as the foundation from which visual aids are derived, such as posted pictorial instructions for complex assembly or safety steps, supporting visual management.

## Gage Control Plan

A gage control plan ensures the measurement system itself remains reliable. It specifies proper storage and care of gages and test equipment, calibration requirements and frequency, handling procedures, and the parts or processes for which each gage is used. Gage repeatability and reproducibility (R&R) studies support the conclusions of the gage control plan by confirming measurement system accuracy before the plan is finalized.

## Visual Management and SPC Integration

Visual management helps business teams maintain process control by making instructions and performance instantly visible. Common devices include signs, posted matrixes and instructions, auditing boards that track group performance over time, color coding, and safety signals. SOPs can be distilled into posters that reduce errors during execution.

Statistical process control (SPC) charts are integrated directly into the control plan. A basic control chart contains a line chart of data points, an x-bar centre line, lines at 1, 2, and 3 standard deviations from the centre, and upper and lower control limits (UCL and LCL) at ±3 standard deviations. The control plan designates which chart type to use, the sample size, and the frequency of plotting. If automated data collection is in place, the control plan shifts from measurement instructions to instructions for reviewing automated SPC charts and taking corrective action when out-of-control signals appear. In all cases, the reaction plan guides the operator through the steps to return the process to a stable state.

## Exam Tips

- Given a scenario where a process has been improved, identify the components that belong in a control plan: document identification, process steps, CTQ, specification limits (LSL/USL), measurement method, sample size and frequency, responsible person, and a detailed reaction plan with containment, diagnosis, verification, and disposition.
- Differentiate between a control plan and a dynamic control plan (DCP). Recognize that a DCP incorporates team structure, preliminary controls, PFMEA, illustrations, and maintenance procedures, and that it is a living document updated by operators when changes occur.
- Apply the sequence of revisiting the FMEA before finalizing the control plan. Know that RPNs are recalculated to confirm risk reduction, and that the control plan directly addresses the high-priority failure modes identified in the updated FMEA.
- Given a control chart and a control plan excerpt, determine the appropriate corrective action when a point exceeds a control limit. The action must include immediate containment, root cause diagnosis, verification of effectiveness, and disposition of affected material.
- Recognize that standard operating procedures (SOPs) and visual management tools (posted instructions, auditing boards) are part of the control plan's sustainment strategy, especially when transitioning a process to the business owner who may not be a statistical expert.