# 26SS_Zoo_Basel
---
## Team members
| Name                    | email         |
| ------------------------| ------------- |
| Julia Schönthal         | <julia.schoenthal@students.fhnw.ch> |
| Coraline Meyer          | <coraline.meyer@students.fhnw.ch> |
| Laura Roggo             | <laura.roggo@students.fhnw.ch>  |
| Aleksandra Grzegorczyk  | <aleksandra.grzegorczyk@students.fhnw.ch> |

## Coaches
Andreas Martin

Charuta Pande

Devid Montecchiari

---

## Project Description
This project focuses on improving the employee recruitment process by making it more structured and efficient. We use BPMN to model the process, DMN to support decision-making, and Make to automate selected steps.

---

## 1. AS-IS Process Overview
The recruitment process is modeled in BPMN and covers the main steps from job posting to candidate evaluation. It includes:
1. The hiring process starts when a department manager identifies a hiring need and creates a job requisition.
2. HR reviews the requisition; if it is not approved, the process ends with rejection. If approved, HR publishes the job posting and stores the posting details in the database.
3. Candidates submit applications, which HR receives and reviews for compliance.
4. Non-compliant applications are rejected, while compliant applications are reviewed further by the department manager.
5. The department manager decides whether the application should proceed. Approved candidates are sent to HR for interview approval and scheduling; rejected candidates are notified.
6. HR schedules and conducts interviews, then decides whether to employ the candidate.
7. If the candidate is rejected after interview, a rejection notification is sent. If selected, HR sends an employment offer.
8. After the candidate responds to the offer, HR checks whether the offer is accepted. If not, the candidate is rejected.
9. Once the offer is accepted, HR prepares employment documents, including the employment contract and other scanned documents.
10. The process ends when the employment documents are sent to the candidate.

The goal is to clearly structure the process and reduce manual effort by automating repetitive tasks and decisions where possible.

<img width="8004" height="2370" alt="Hiring process_Group project_AS-IS" src="https://github.com/user-attachments/assets/18a5e4bf-1ba2-45e0-9f70-9a1cca4fafa2" />


---
## 2. TO-BE Process Overview

The updated TO-BE process keeps the same overall hiring flow, but it adds more control points, clearer communication, and extra steps before final employment documentation. TO-BE process automate mainly the administrative and communication activities, such as storing records, sending confirmations, sending rejection messages, issuing offer documents, and managing employment documents.
The manual work remains focused on decision-making and judgement, such as approving requisitions, reviewing candidates, conducting interviews, selecting candidates, and validating employment documentation.

<img width="13944" height="2430" alt="Hiring process_Group project_TO-BE_Version 2" src="https://github.com/user-attachments/assets/90fbf3d2-fbcb-4d90-a919-44719c465510" />

---
## 2.1 First Screening Automation
For the first screening, we created a Google Form to collect relevant candidate information such as work permit, experience, and language level.

This data is evaluated using a DMN decision table, which automatically determines whether a candidate should be rejected or allowed to continue. The decision logic is integrated into the BPMN model through a Business Rule Task, and the result is used in a gateway to route the process accordingly.

This step helps ensure that only candidates who meet the minimum requirements proceed to the next stage.

---
## 2.2 Assessment & Evaluation
The assessment and evaluation step is implemented using a Make scenario.

Once a candidate completes the online assessment, the results are stored in Google Sheets. This triggers an automated workflow that evaluates the score and sends an email to the candidate.

Depending on the outcome, the candidate either continues in the process or receives a rejection email. This allows for faster and more consistent communication.

---

## 2.3.Next Steps
The next step is to connect the first screening decision with the automation workflow. Candidates who pass the initial screening should automatically receive the assessment link.

Further improvements include refining the decision rules and extending automation to additional parts of the recruitment process.
The objective is to create a fully integrated and automated recruitment workflow.
