# 26SS_Zoo_Basel
## Project Description
This project focuses on improving the employee recruitment process by combining process modeling, decision automation, and workflow automation. The goal is to create a structured and efficient recruitment flow using BPMN for process modeling, DMN for decision-making, and Make for automation.

---

## Process Overview
The recruitment process is modeled using BPMN and includes the following main steps:
- Job posting creation and publication  
- Candidate application submission via a Google Form  
- First screening of applications  
- Online assessment  
- Evaluation of assessment results  

The process integrates automated decision-making and communication to reduce manual effort and improve consistency.

---

## First Screening Automation
The first screening step is automated using a DMN decision table and a Google Form.

- A **Google Form** is used to collect structured candidate data such as work permit, experience, and language level.  
- A **DMN decision table** evaluates this data and performs the initial filtering of candidates.  
- Based on predefined criteria, the system automatically assigns one of two outcomes:
  - **Reject** → candidate does not meet minimum requirements  
  - **Continue** → candidate proceeds to the next step (online assessment)  

This decision is integrated into the BPMN process using a **Business Rule Task**, and the result is used in a gateway to route the process accordingly.

---

## Assessment & Evaluation
The next step of the process is handled through an automated scenario built in Make.

- After the assessment is completed, the results are stored in **Google Sheets**  
- A Make scenario is triggered using **“Watch New Rows”**  
- The system evaluates the assessment score using decision logic  
- Based on the result:
  - A **continue email** is sent if the candidate passes  
  - A **rejection email** is sent if the candidate does not meet the criteria  

This step automates the evaluation and communication process, ensuring quick and consistent responses to candidates.

---

## Next Steps
The next step of the project is to fully connect the first screening logic with the automation workflow.

- Integrate the DMN decision result with a Make scenario  
- Automatically send the online assessment link to candidates who pass the first screening  
- Improve and refine decision rules based on feedback  
- Extend automation to additional steps of the recruitment process  

The objective is to create a fully integrated and automated recruitment workflow.
