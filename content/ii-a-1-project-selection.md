---
title: "Project Selection"
description: "How to evaluate and select Six Sigma DMAIC projects using a weighted viability matrix and process-level identification."
---

**BoK:** II-A-1  **Bloom's level:** Understand

## Project Selection Overview

Not every process problem makes a suitable Six Sigma project. Organisations must choose projects that align with strategic goals, can be completed within a reasonable timeframe, and are likely to deliver measurable benefits. The Define phase introduces a structured method for comparing candidate projects so teams invest resources where they will have the greatest impact. The primary tool for this is the 15-point project viability matrix, which produces a numerical score that indicates whether a project fits the DMAIC methodology. When a process requires a complete redesign rather than incremental improvement, the DMADV approach may be more appropriate, but the viability matrix shows whether DMAIC is the right path.

## The 15-Point Project Viability Matrix

The matrix uses a set of 15 yes/no questions, each weighted by the team according to its importance for the organisation. The team assigns a weight from 1 (least important) to 5 (most important) to every question. After weighting, team members answer each question by placing a mark in one of five columns: No (1), Mostly No (2), Possibly (3), Mostly Yes (4), or Yes (5). The resulting grid converts into a single project score.

### Criteria List

The 15 standard questions, with an example weighting drawn from the source, are:

- Is there a sponsor or champion? (weight 3)
- Do project goals align with corporate goals? (weight 4)
- Is data available or accessible? (weight 3)
- Are defects well defined? (weight 3)
- Is the process stable? (weight 1)
- Are there customer benefits to the project? (weight 5)
- Are there company benefits to the project? (weight 5)
- Can the project be completed within 6 months? (weight 3)
- Is the solution unknown? (weight 4)
- Is it likely a discovered solution will be implemented? (weight 3)
- Would a new solution cost little to no cash? (weight 5)
- Are Six Sigma team members available for the project? (weight 3)
- Can inputs in the process be controlled? (weight 5)
- Can the process be improved without a full redesign? (weight 2)
- Will the improvements maintain or improve quality across the value chain? (weight 5)

### Scoring Procedure

Follow these steps to calculate the project score.

1. **Convert each weight to a multiplier.** Divide the assigned weight by 3.  
   $$\text{Multiplier} = \frac{\text{Weight}}{3}$$  
   Example: a weight of 5 gives \$5/3 \approx 1.7$, a weight of 3 gives \$1$, and a weight of 1 gives \$0.33$.

2. **Multiply the answer value by the converted weight.** For each row, take the column number where the team placed its mark (1 through 5) and multiply by the multiplier from step 1. This produces a weighted value for that row.  
   $$\text{Weighted Answer} = \text{Multiplier} \times \text{Column Number}$$

3. **Sum the weighted values in each column.** Total the weighted answers for all 15 rows separately for each of the five columns (No, Mostly No, Possibly, Mostly Yes, Yes). These column sums become the basis for the final calculation.

4. **Multiply each column sum by its column number.**  
   $$\text{Column Product} = \text{Column Sum} \times \text{Column Number}$$  
   For example, the sum of the “Yes” column (column 5) is multiplied by 5.

5. **Add the five column products.** This sum is the weighted total for the project.

6. **Add the five column sums from step 3.** This gives the total of all weighted answers (ignoring the column number multiplication).

7. **Divide the result from step 5 by the result from step 6.**  
   $$\text{Project Score} = \frac{\text{Sum of Column Products}}{\text{Sum of Column Sums}}$$

### Worked Numerical Example

Using the example weights and answer grid from the source, the matrix produced these column sums after step 3: No = 1.3, Mostly No = 4.4, Possibly = 4.7, Mostly Yes = 3.3, Yes = 4.4.

Step 4 multiplies each column sum by its column number:

- No column: \$1.3 \times 1 = 1.3$
- Mostly No column: \$4.4 \times 2 = 8.8$
- Possibly column: \$4.7 \times 3 = 14.1$
- Mostly Yes column: \$3.3 \times 4 = 13.2$
- Yes column: \$4.4 \times 5 = 22.0$

Step 5 sum of column products: \$1.3 + 8.8 + 14.1 + 13.2 + 22.0 = 59.4$

Step 6 sum of column sums: \$1.3 + 4.4 + 4.7 + 3.3 + 4.4 = 18.1$

Step 7 division: \$59.4 \div 18.1 \approx 3.28$

The project score is 3.28.

### Interpreting the Score

The final number tells you whether the project is viable under DMAIC.

- **Below 2.0:** Not viable for DMAIC.
- **2.0 to 3.0:** Possibly viable; the team should validate further before committing.
- **Above 3.0:** A viable DMAIC project.

A score above 3.0 indicates that the project is well-suited to the define, measure, analyse, improve, and control approach. The matrix does not measure the overall worth of an improvement idea; it only determines DMAIC fit. A project that scores low may still be important but might need the DMADV framework when a full redesign is required.

## Process-Level Project Selection

Departmental leaders and staff often identify improvement opportunities without needing complex brainstorming. They can use Pareto charts to highlight the few sources that cause the largest portion of defects or delays. Once these high-impact areas are identified, the team validates each candidate by filling out the 15-point viability matrix. This approach quickly narrows the list and ensures that any selected project meets the structural requirements for a DMAIC effort. Because departmental staff are close to the work, they frequently recognise which processes are unstable, where data already exists, and whether a sponsor will support the effort.

## Why Project Selection Matters

Poor project selection consumes resources on efforts that cannot deliver the expected return. The viability matrix forces teams to think about critical success factors before they invest time: the presence of a sponsor, alignment with company goals, availability of data, and the likelihood that a discovered solution will actually be implemented. Scoring multiple projects with the same matrix allows the leadership council to compare them on a common scale and fund the ones with the highest probability of success. The discipline of weighting and scoring also builds consensus among team members about what makes a project important.

## Exam Tips

- Memorise the viability thresholds: below 2.0 is not viable, 2.0 to 3.0 is possibly viable but needs further validation, and above 3.0 is a viable DMAIC project. Expect direct questions about these cut-offs.
- Understand that the 15-point matrix specifically assesses DMAIC suitability. A low score does not mean the problem is unimportant; it may require a DMADV redesign approach.
- Be able to reproduce the calculation steps: weight divided by 3, multiply by column number, sum by columns, multiply column sums by column numbers, divide the total of those products by the total of all weighted answers.
- Know that at the process level, teams often use Pareto charts to spot candidates for improvement and then apply the viability matrix to confirm the selection.
- Recognise that the team must assign weights before answering the questions. The weighting reflects organisational priorities and should not be changed to manipulate the score.