# 26SS_Zoo_Basel
## Project Description
This project focuses on improving the employee recruitment process by making it more structured and efficient. We use BPMN to model the process, DMN to support decision-making, and Make to automate selected steps.

---

## Process Overview
The recruitment process is modeled in BPMN and covers the main steps from job posting to candidate evaluation. It includes receiving applications, performing a first screening, sending an online assessment, and evaluating the results.

The goal is to clearly structure the process and reduce manual effort by automating repetitive tasks and decisions where possible.

---

## First Screening Automation
For the first screening, we created a Google Form to collect relevant candidate information such as work permit, experience, and language level.

This data is evaluated using a DMN decision table, which automatically determines whether a candidate should be rejected or allowed to continue. The decision logic is integrated into the BPMN model through a Business Rule Task, and the result is used in a gateway to route the process accordingly.

This step helps ensure that only candidates who meet the minimum requirements proceed to the next stage.

---

## Assessment & Evaluation
The assessment and evaluation step is implemented using a Make scenario.

Once a candidate completes the online assessment, the results are stored in Google Sheets. This triggers an automated workflow that evaluates the score and sends an email to the candidate.

Depending on the outcome, the candidate either continues in the process or receives a rejection email. This allows for faster and more consistent communication.

---

## Next Steps
The next step is to connect the first screening decision with the automation workflow. Candidates who pass the initial screening should automatically receive the assessment link.

Further improvements include refining the decision rules and extending automation to additional parts of the recruitment process.
The objective is to create a fully integrated and automated recruitment workflow.
