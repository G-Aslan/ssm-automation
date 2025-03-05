This project focuses on automating the configuration and management of four groups of Amazon EC2 instances using AWS Systems Manager (SSM). The automation standardizes instance setup across various environments.
Project Overview
AWS SSM: Centralized tool for automating the configuration and management of multiple EC2 instances.
Instance Groups:
Group 1: Tagged as Environment: Dev
Group 2: Tagged as Environment: Staging
Group 3: Tagged as Environment: Prod
Group 4: Tagged as Environment: Test
Automation Details
The SSM automation document performs the following tasks for each instance across all groups:
Connect to each instance using SSM.
Install Nginx to set up a basic web server.
Deploy a basic web application that displays "Hello World".
Parameterization
The process includes updating the SSM Parameter Store with the automation outcome. The parameter AutomationOutcome reflects:
0 if the process completes successfully.
1 if any step encounters a failure.
Scheduled Automation
The automation process is configured to run daily at 10:00 AM UTC +3, ensuring each instance group is consistently managed and updated.
Conclusion
This project exemplifies how AWS SSM can streamline the configuration and management of multiple EC2 instance groups. By automating key setup tasks, the process ensures consistent and reliable operation across development, staging, production, and testing environments.
