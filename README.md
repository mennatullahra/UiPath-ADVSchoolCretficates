# UiPath-ADVSchoolCertificates

## Description
This repository contains automation processes built with UiPath's REFramework to manage and distribute certificates to students of ADV School using a dynamic Word template and Outlook emails.

## Robots

### Dispatcher Robot
The Dispatcher Robot reads an Excel file containing students' names and email addresses. It then stores each student's information as queue items in the Orchestrator queue, ensuring data is ready for the Performer Robot to process.

### Performer Robot
The Performer Robot utilizes the REFramework to process queue items retrieved from the Orchestrator queue. For each queue item (student), it performs the following steps:

1. Opens a Word template that serves as the certificate.
2. Adds the student's name dynamically to the template.
3. Converts the Word document to a PDF.
4. Sends an Outlook email to the student using the PDF attachment as the certificate.

## Prerequisites

- UiPath Studio and Orchestrator configured.
- Excel file with student names and emails (update path in Dispatcher workflow).
- Outlook configured for sending emails.

## Supervision
This project has been done under the supervision of **ADVANSYS-ESC**, providing guidance and support throughout the development process.
