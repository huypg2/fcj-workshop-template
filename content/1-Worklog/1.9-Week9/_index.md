---
title: "Week 9 Worklog"
date: 2026-06-19
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Week 9: Building the Frontend Interface for NextGenPay and Supporting API Load Testing

### Week 9 Objectives:

* Build the Frontend interface for the NextGenPay payment system.
* Design screens for system overview, account management, bill payment, transaction history, and API load testing.
* Build a payment request interface with Idempotency Key support to test the duplicate transaction prevention mechanism.
* Display payment responses, transaction status, and transaction history by User ID.
* Prepare the interface for Backend/API integration and system load testing in the next steps.

### Tasks to be implemented this week:

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Monday | - Analyze the interface requirements for the NextGenPay system<br>&emsp; + Identify the main screens, including Overview, Account Management, Bill Payment, Transaction History, and API Load Testing<br>&emsp; + Define the information that needs to be displayed, such as system status, account information, transaction data, and payment results<br>&emsp; + Create the overall layout for the sidebar, header, and main content area | 15/06/2026 | 15/06/2026 |  |
| Tuesday | - Build the main interface layout<br>&emsp; + Design the sidebar navigation for the system features<br>&emsp; + Build the header section to display system status and the refresh status button<br>&emsp; + Add a language switch button to support bilingual interface display | 16/06/2026 | 16/06/2026 |  |
| Wednesday | - Build the bill payment interface<br>&emsp; + Create input fields for Source Account ID, User ID, transaction amount, and currency<br>&emsp; + Add the Idempotency Key field and the Gen button to generate a duplicate-prevention key<br>&emsp; + Build the payment submit button and prepare request data to send to the Backend/API | 17/06/2026 | 17/06/2026 |  |
| Thursday | - Build the payment response and transaction audit sections<br>&emsp; + Display the response from the payment gateway, including HTTP Status, Success Status, Message, Payment ID, and State<br>&emsp; + Build the transaction query function by User ID<br>&emsp; + Display the transaction history, including amount, status, and processing time | 18/06/2026 | 18/06/2026 |  |
| Friday | - Complete the interface and prepare for API load testing<br>&emsp; + Review the layout, colors, spacing, and display responsiveness of the interface<br>&emsp; + Test the flow for submitting a payment request, receiving the response, and viewing transaction history<br>&emsp; + Prepare the API Load Testing section to monitor requests, processing status, and test results in the next steps | 19/06/2026 | 19/06/2026 |  |

### Week 9 Achievements:

* Built the basic Frontend interface for the NextGenPay system.
* Completed the sidebar navigation with Overview, Account Management, Bill Payment, Transaction History, and API Load Testing sections.
* Built the header section to display system status and the refresh status function.
* Added the language switch button to support bilingual interface display.
* Built the bill payment screen with Source Account ID, User ID, transaction amount, currency, and Idempotency Key fields.
* Added the Idempotency Key generation function to support testing the duplicate transaction prevention mechanism.
* Displayed the payment gateway response, including HTTP Status, Success Status, Message, Payment ID, and State.
* Built the transaction audit section based on User ID.
* Displayed transaction history with amount, status, and transaction time.
* Prepared the API Load Testing interface to support monitoring requests, processing status, and test results in the next steps.
* Completed the Frontend interface and made it ready for Backend/API integration.