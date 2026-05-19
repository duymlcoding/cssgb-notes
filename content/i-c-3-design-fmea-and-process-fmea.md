---
title: "Design FMEA and Process FMEA"
description: "Define and distinguish between Design FMEA and Process FMEA, and apply the FMEA methodology to prioritize failure risks using the Risk Priority Number."
---

**BoK:** I-C-3  **Bloom's level:** Apply

## Failure Mode and Effects Analysis Overview

Failure Mode and Effects Analysis (FMEA) is a systematic, team-based tool that identifies potential failure modes in a product, process, or system and assesses their risk. In Six Sigma projects, teams often begin constructing an FMEA during the Measure phase because it reveals risk priorities for various inputs and errors, setting the stage for root cause analysis later. The FMEA uses three factors to quantify risk: Severity (S), Occurrence (O), and Detection (D). Their product gives the Risk Priority Number (RPN):

$$RPN = S \times O \times D$$

Higher RPN values signal failure modes that demand the most urgent attention. The FMEA is a living document; after countermeasures are implemented, the team recalculates the RPN to verify that risk has been reduced.

## Creating an FMEA

Teams typically build the FMEA in a spreadsheet. The initial nine columns are completed during the Measure phase, while the remaining columns (actions, timing, and rescoring) belong to the Improve phase. The columns include Process Step, Potential Failure, Potential Failure Effect, SEV, Potential Cause of Failure, OCC, Current Monitor/Control, DET, RPN, Recommended Changes/Actions, Who and When, Action Completed, and recalculated SEV, OCC, DET, RPN.

For each process step or design element, the team brainstorms every credible failure mode, even those that occur only occasionally. They then assign ratings on a scale that the team has standardized to fit their business. The ASQ CSSGB Handbook advises against simply copying a 1–10 scale from another industry; the descriptions of each level must reflect the organization's actual risk tolerance. After the initial RPN scores are tabulated, management reviews the data and agrees on a cutoff score. Risks with an RPN above the cutoff become priorities for action.

When two failure modes have the same RPN, the risk with the higher severity rating is escalated.

## RPN Calculation Example

Consider a process FMEA for a customer refund process. One row might contain the following data:

- Process step: Refund request is entered in the system.
- Potential failure: Incorrect amount is entered.
- Effect: Customer receives more or less refund than anticipated.
- SEV: 8
- Potential cause: Data-entry employee transposes numbers.
- OCC: 10
- Current control: Supervisor randomly reviews a sample of requests.
- DET: 7

The RPN is calculated as:

$$RPN = 8 \times 10 \times 7 = 560$$

A second row addresses check printing:

- Process step: Refund check is printed.
- Potential failure: Printed check has defects.
- Effect: Customer cannot cash the check.
- SEV: 9
- Potential cause: Printer misalignment or low ink.
- OCC: 1
- Current control: The person signing checks reviews them.
- DET: 2

$$RPN = 9 \times 1 \times 2 = 18$$

The first failure mode (RPN 560) clearly demands priority over the second (RPN 18). The team would later recommend changes to reduce the high occurrence or improve detection.

## Distinguishing Design FMEA and Process FMEA

Both Design FMEA and Process FMEA follow the same RPN logic, but they address different aspects of product realization. The key question is the end goal of the FMEA document.

**Design FMEA** focuses on the product design itself. Designers and engineers use it to examine how choosing one design characteristic over another could lead to failures. The failure modes originate from the product's geometry, materials, or interfaces. For example, a Design FMEA for a toy might ask whether small parts could detach and become choking hazards. Design FMEA helps catch issues before production tooling is finalized.

**Process FMEA** examines the steps used to manufacture or deliver the product. The failure modes are tied to process activities: assembly, material handling, data entry, packaging, and so on. The Process FMEA asks, "What can go wrong during this step?" and evaluates the controls currently in place. In many manufacturing settings, a Process FMEA may be built without a prior Design FMEA available, forcing the engineer to work with limited knowledge of the design intent.

The recommended sequence is to create a Concept FMEA first, then a Design FMEA, and finally a Process FMEA. A Concept FMEA explores high-level system or service concepts. The Design FMEA refines the product design, and the Process FMEA ensures that the production steps can meet the design requirements. In a Six Sigma project, understanding this distinction helps the team target its FMEA effort correctly; a project aimed at reducing assembly defects would rely on a Process FMEA, while a project focused on redesigning a component to improve durability would begin with a Design FMEA.

## Using the FMEA to Drive Continual Improvement

Once the team assigns actions to reduce high RPN values, the FMEA becomes a road map for ongoing improvement projects. After implementing changes, the team meets again to rescore severity, occurrence, and detection, and recalculates the RPN. A lower RPN confirms that the action was effective. If the new RPN stays the same or increases, the team must try a different countermeasure.

The ASQ handbook emphasizes that an FMEA should be treated as a business risk management tool, not a one-off compliance exercise. Successful implementation requires leadership commitment. Teams that maintain an FMEA database significantly reduce the time spent on successive FMEAs. When the analysis becomes tedious, the team can split the process into major blocks and perform FMEA by block.

FMEA teams should follow these guidelines.

- Provide FMEA training to every member before assignment.
- Use a cross-functional team and seek subject matter expertise when needed.
- Talk to the customer about how the product will be used.
- Standardize the rating scales within the organization so that comparisons across FMEAs are meaningful.
- Avoid fighting over small rating differences of one point. If the team disagrees by two or three points, analyze the impact thoroughly.
- Do not force a 1–10 scale if your industry has fewer discernible levels; a 1–5 scale can work.
- Update the FMEA with any newly learned risks.

## Exam Tips

- Memorize the RPN formula $RPN = S \times O \times D$ and remember that when two failure modes have the same RPN, the one with the higher severity rating gets priority. The exam