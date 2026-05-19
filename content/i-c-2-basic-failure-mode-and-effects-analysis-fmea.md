---
title: "Basic Failure Mode and Effects Analysis (FMEA)"
description: "Detailed study notes on Failure Mode and Effects Analysis covering definitions, purpose, types, team approach, step-by-step procedure, rating scales, risk priority number calculation, and integration into Six Sigma projects."
---
## What Is FMEA

Failure Mode and Effects Analysis (FMEA) is a systematic method for studying risk. The ASQ handbook defines risk through three aspects: impact (severity), probability (occurrence), and event (detection). An FMEA evaluates a product or process to identify what might cause it to fail, the effects those failures could have, and the current controls in place. It then prioritises risks using a structured scoring system so the team can focus on preventing or reducing the most critical failure modes.

The tool aligns with the ISO 31000 Risk Road Map: plan risk management, identify risks, analyse and evaluate risk, plan risk response, and monitor and control risk. FMEA was initially formalised as Failure Mode, Effects, and Criticality Analysis (FMECA) by the U.S. military in 1949 and evolved through NASA, Ford, AIAG, and SAE standards. Today it is applied in manufacturing, service, software, and healthcare.

## Why Use FMEA

The AIAG describes FMEA as a systematic group of activities intended to:

- Recognise and evaluate the potential failure of a product or process and the effects of that failure
- Identify actions that could eliminate or reduce the chance of the potential failure occurring
- Document the entire process

FMEA is a front-end tool. It helps teams anticipate failure modes and take actions to eliminate or reduce failure during deployment and throughout the product or process life cycle. The old adage “a stitch in time saves nine” captures the philosophy: thinking through the process formally on paper predicts and prevents unpleasant issues. Completed FMEAs provide benefits such as assessing effects on all customers, evaluating design alternatives, identifying causes and controls, developing a prioritised action list, validating the intended design or process, and documenting special characteristics that require special controls.

## Types of FMEA

The primary types relevant to Six Sigma work are design FMEA (DFMEA) and process FMEA (PFMEA). Concept FMEA, machinery FMEA, and system FMEA also exist but fall outside the Green Belt Body of Knowledge.

- **DFMEA** focuses on potential failures in product design. Its column headers (Figure 3.2) include Item/Function, Potential Failure Mode, Potential Effect(s) of Failure, Severity (S), Potential Cause(s)/Mechanism(s) of Failure, Occurrence (O), Current Design Controls (Prevention and Detection), Detection (D), RPN, Recommended Actions, Responsibility and Target Completion Date, and Action Results.
- **PFMEA** examines failures in manufacturing or assembly processes. Its column headers (Figure 3.3) mirror DFMEA but the focus is on process steps, with current process controls and actions directed at process changes.

## Team and Scope

A cross-functional team of five to seven people conducts the FMEA. The team should include design, manufacturing, quality, testing, reliability, maintenance, purchasing, suppliers, shop floor operators, sales, marketing, and customer service representatives as needed. Process experts must be present during a DFMEA, and design experts must be present during a PFMEA. Subject matter experts for safety, regulatory, or legal issues are added when necessary.

The team first defines the scope: Is the FMEA for a concept, system, design, or process? What boundaries apply? How detailed will the analysis be? A clear scope prevents the team from becoming too narrow (capturing too few control factors), too vague, or distracted by rating systems unrelated to robustness.

## FMEA Procedure in Detail

FMEA uses a spreadsheet matrix format. The basic three-step logic, shown in the FMEA flowchart (Figure 3.4), guides the team through the columns:

1. **Step 1: Identify functions and potential failures.** Begin with the item or process step and its function. Ask: What can go wrong? The potential failure modes can be no function, partial or over-function, degraded performance over time, intermittent function, or unintended function.
2. **Step 2: Determine effects and severity.** For each failure mode, list the potential effect on the customer. Ask: How bad is it? Assign a severity rating.
3. **Step 3: Identify causes, current controls, and detection.** List the potential causes or mechanisms of the failure. Ask: How can this be prevented and detected? Rate the likelihood of occurrence, describe current design or process controls (separated into prevention and detection types), and rate how well the controls can detect the failure before it reaches the customer.

The following 15-column spreadsheet structure merges columns typically completed across the Measure and Improve phases.

### Columns 1 to 9 (Completed During Measure)

| Column | Content |
|---|---|
| 1. Process step | The specific step, activity, or input being examined. |
| 2. Potential failure | What might go wrong for that step. |
| 3. Potential failure effect | The impact on the customer if the failure occurs. |
| 4. SEV | Severity rating (1 to 10). |
| 5. Potential cause of failure | Reasons the failure might occur. |
| 6. OCC | Occurrence rating (1 to 10). |
| 7. Current monitor/control | Existing controls that prevent or monitor the failure. |
| 8. DET | Detection rating (1 to 10). |
| 9. RPN | Risk Priority Number = SEV × OCC × DET. |

### Columns 10 to 15 (Completed During Improve)

| 10. Recommended changes/actions | Actions to reduce severity, occurrence, or improve detection. |
|---|---|
| 11. Who and When? | Person responsible and target completion date. |
| 12. Action completed | Record of actions taken. |
| 13. SEV (new) | Revised severity after action. |
| 14. DET (new) | Revised detection after action. |
| 15. RPN (new) | Recalculated RPN to confirm risk reduction. |

During the Analyze and Improve phases, the team recommends and implements changes, then rescore the FMEA. If the new RPN is higher or unchanged, the change was ineffective and another cycle is needed.

## Severity, Occurrence, and Detection Rating Scales

The cross-functional team scores each failure mode using rating tables that usually run from 1 to 10. Some organisations use 1 to 5 scales, but the 1-to-10 approach is the most common in manufacturing standards such as SAE J-1739 and AIAG PFMEA-4. The exact tables must fit the industry and organisation; reliability engineers often build company-specific scales using warranty data and historical knowledge.

Key descriptors from the sources:
- **Severity (SEV):** 1 = no effect; 5 = minor disruption to production; 9 or 10 = endangers a process or person, causing harm to workers or customers.
- **Occurrence (OCC):** 1 = very unlikely failure; 10 = almost inevitable failure.
- **Detection (DET):** 1 = automated detection that rarely fails; 10 = no detection at all.

When disagreement arises, the team may take a middle-ground score, note the item for further study, and keep the FMEA moving.

## Risk Priority Number (RPN)

The RPN is calculated by multiplying the three ratings: RPN = SEV × OCC × DET. This number helps the team prioritise which failure modes to address first. A higher RPN signals a greater risk. For example, a failure mode with SEV=8, OCC=10, and DET=7 yields an RPN of 560, while another with SEV=9, OCC=1, DET=2 yields only 18. The team would focus on the 560 failure because it presents a higher combined risk.

## Living Document and Control

The FMEA is a living document, not a one-time event. It must be periodically reviewed and updated as new risks and failures emerge during deployment. The FMEA must be part of the quality management system, with revision control to track changes over time. In a well-designed QMS, the FMEA links to quality function deployment and to control plans.

## FMEA in DMAIC Phases

Although the Body of Knowledge places FMEA under DFSS methodologies, teams can use FMEA in any DMAIC phase from Define through Analyze. The CSSC training manual notes that teams often begin FMEA work in the Measure phase because it helps identify risk priorities for inputs and process errors. The information gathered sets the stage for root cause analysis. Hard borders between DMAIC phases do not exist; measure phase tasks sometimes start before the Define tollgate, and analysis often begins while data collection continues.

## Exam Tips

- Distinguish DFMEA from PFMEA by focus: design versus process. Know the column headers common to both and when design experts or process experts must be on the team.
- Given a scenario with severity, occurrence, and detection ratings, calculate the RPN correctly and determine which failure mode a team should address first based on the highest RPN.
- Explain why rescoring columns appear after recommended actions in the Improve phase: to verify that implemented changes actually reduced the risk.
- Recognize that FMEA is a front-end, preventive tool and a living document that must be revised as new knowledge becomes available.
- Understand that the three risk aspects, impact (severity), probability (occurrence), and event (detection), form the foundation of the rating system and the RPN calculation.
- Be prepared to identify appropriate actions when an RPN is unacceptably high; design changes, process changes, special controls, or updates to standards and procedures are all valid responses.