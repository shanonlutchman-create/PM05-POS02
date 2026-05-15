RPA Developer Learning Activity - Student Worksheet
Module: RPA Testing and Evaluation
Student Name: _____________________________
Student ID: _____________________________
Date: _____________________________
1. Introduction
Welcome to this learning activity on RPA Testing and Evaluation. This module is designed to equip you with the essential skills to ensure the robustness, reliability, and maintainability of RPA solutions. You will explore various testing methodologies, exception handling techniques, and stakeholder communication strategies, all within the context of real-world business scenarios. You will be using UiPath and Microsoft Power Automate for the practical exercises.
2. Learning Outcomes
Before you begin, familiarize yourself with the learning outcomes for this module:
Practical Application Outcomes (PA)
•PA0201: Run test cases and accurately evaluate their outcomes.
•PA0202: Document and communicate outcomes to relevant stakeholders, initiating change requests when necessary.
•PA0203: Identify possible issues with underlying applications (e.g., server crashes, slow/unresponsive bots, application changes, environment changes).
•PA0204: Identify any exception such as non-conformity to expected response times, infrastructural issues, business scenarios that have not been handled during process configuration and all other exceptions that might occur.
•PA0205: Refer anomalies to appropriate stakeholders.
•PA0206: Analyze exceptions and understand its implications on business.
Applied Knowledge Outcomes (AK)
•AK0201: The application and use of test or simulation tools.
•AK0202: The approval process for testing the bot.
•AK0203: Difference between different types of testing such as unit, sub-system, system, automated.
•AK0204: Different simulation tool providers and how to use their tools.
•AK0205: Different sources of information available for designing tests and how to access these.
3. Theoretical Concepts and Background Questions
Review the provided information above and any additional resources. Answer the following questions to solidify your understanding of the theoretical concepts.
1. Why is testing crucial in RPA development? Discuss at least three reasons, referencing concepts like reliability, accuracy, and resilience.
____________________________________

2. Differentiate between Unit Testing, System Testing, and User Acceptance Testing (UAT) in the context of an RPA project. Provide a brief example for each.
____________________________________

3. Explain the difference between a business exception and a technical exception in RPA. Give an example of each from a typical invoice processing automation.
____________________________________



4. Describe the purpose of a Try-Catch block in UiPath or an Error Handling block in Power Automate. How does it contribute to a robust automation?
____________________________________

5. Imagine an RPA bot processing customer orders. What key metrics would you monitor to assess its performance? How would you use these metrics to identify potential issues?
____________________________________

6. Why is detailed logging important for RPA solutions? Discuss its role in debugging, auditing, and compliance.
____________________________________
7. Who are the typical stakeholders for an RPA project, and why is effective communication with them essential, especially when anomalies occur?
____________________________________


4. Practical Exercises
For these exercises, you will use the provided datasets: south_african_invoices.csv and rpa_processing_logs.csv.

Exercise 4.1: Basic Invoice Processing Automation
Objective - Create a basic RPA workflow to process invoice data.
Instructions
1. Choose your tool - Select either UiPath Studio or Microsoft Power Automate Desktop.
2. Load Data - Create a workflow that reads the south_african_invoices.csv file.
3. Simulate Data Entry - For each row in the CSV, simulate entering the Invoice_ID, Vendor_Name, Amount_ZAR, and Payment_Due_Date into a hypothetical target application. You can simulate this by:
• Writing these values to a new Excel file.
• Displaying them in a message box.
• (Optional, advanced) Creating a simple web form locally and automating data entry into it.
4. Run and Observe - Run your workflow with the south_african_invoices.csv dataset. Observe the output.
Reflection:


• What challenges did you encounter during this basic automation?
_______________________________________________________

• How did your chosen tool handle the data reading and simulated entry?
_______________________________________________________




Exercise 4.2: Implementing Exception Handling
Objective - Enhance your workflow to handle various exceptions.
Instructions
1. Identify Exceptions - Review the Exception_Type column in south_african_invoices.csv. Your bot should be able to identify and handle these specific exceptions.
2. Implement Error Handling - Modify your workflow from Exercise 4.1 to include robust error handling for the following Exception_Type values:
• Duplicate Invoice - If an invoice ID is encountered that has already been processed (you can simulate this by checking against a list of already processed IDs or a simple flag).
• Amount Mismatch - If the Amount_ZAR is outside an expected range (e.g., less than 100 ZAR or greater than 50,000 ZAR – you define the range).
• Missing PO Number - If the PO_Number field is empty.
• Vendor Not Found - If the Vendor_Name is not in a predefined list of approved vendors (create a small list of 3-4 approved vendors).
• Date Format Error - If the Invoice_Date or Payment_Due_Date is not in the expected YYYY-MM-DD format.
3. Logging - For each exception caught, log the Invoice_ID, Exception_Type, and a descriptive Error_Description to a separate text file named exception_log.txt.
4. Continue Processing - Ensure that your bot continues to process other invoices even after encountering an exception.


Reflection
• How did implementing error handling change the complexity of your workflow?
_____________________________________________
• Describe the mechanisms you used (e.g., Try-Catch, If conditions, loops) to handle different exceptions.
_____________________________________________
• How would the exception_log.txt be useful to a stakeholder?
_____________________________________________


Exercise 4.3: Simulating Application Issues
Objective - Understand how to design bots that are resilient to application issues.


Instructions
1. Review Log Data - Examine the rpa_processing_logs.csv file. Pay attention to Error_Type values like 'Server Crash', 'Slow Response', and 'Application Change'.

2. Simulate and Handle - Choose ONE of the following scenarios and simulate it while running your bot from Exercise 4.2:

• Scenario A (Slow/Unresponsive Application) - Introduce a deliberate delay (e.g., using a Delay activity in UiPath or a Wait action in Power Automate) before an interaction with your simulated target application. Configure your bot to handle this delay gracefully (e.g., by increasing timeouts or implementing retry mechanisms).

• Scenario B (UI Element Change) - Manually change a UI element (e.g., rename a column header in your simulated Excel target, or change the id of an input field in a local web form). Run your bot and observe its behavior. Then, modify your bot to adapt to this change (e.g., by using more robust selectors or dynamic element identification).
3. Document - Describe the scenario you chose, how you simulated it, and how your bot responded. Explain the changes you made to your bot to handle the issue.
Reflection
• How can RPA developers proactively design bots to be resilient to application changes or performance issues?

• What are the implications of an unhandled application issue on business operations?


