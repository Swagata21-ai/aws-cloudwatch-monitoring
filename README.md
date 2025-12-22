🔹 Project Overview


This project implements a cloud monitoring, alerting, auditing, and secrets management solution using AWS services.
It monitors EC2 instance performance using Amazon CloudWatch, sends real-time email alerts via SNS, tracks AWS API activity using CloudTrail, and securely stores sensitive data using AWS Secrets Manager.
The project focuses on observability, security awareness, and operational monitoring in a cloud environment.

🔹 AWS Services Used


1)	AWS CloudTrail- For tracking and auditing cloud activity logs
2)	AWS S3- For secure storage of log files
3)	AWS CloudWatch Logs- For real-time log monitoring and analysis
4)	AWS CloudWatch Alarms- For sending alerts based on monitored events
5)	AWS SNS- For sending security notifications and alerts to the user.


🔹 Architecture Diagram


🔹 Step-by-Step Implementation

1) User Activity


All AWS user and service API actions (such as login, EC2 start/stop, IAM policy changes) are automatically captured.


2) AWS CloudTrail

CloudTrail records all management events and delivers them to:

•	S3 bucket (for storage and long-term audit)

•	CloudWatch Logs (for real-time analysis)


3) AWS S3

•	Acts as a central log repository.

•	Stores all CloudTrail event logs in a versioned and encrypted format.

•	Data can later be analyzed using Athena or visualized via QuickSight.


4) AWS CloudWatch Logs

CloudTrail streams logs here for continuous monitoring.

Metric Filters are configured to search for key patterns, such as:

•	Unauthorized API calls
•	Console login failures
•	Root account usage
•	IAM role or user changes


5) CloudWatch Alarms

•	Each metric filter is linked to an alarm.

•	When conditions are met (e.g., >0 failed logins), the alarm changes to ALARM state.

6) AWS SNS (Simple Notification Service)

•	CloudWatch Alarms trigger SNS topics.

•	SNS then sends email/SMS alerts to the administrator or security team.

For dashboards:

	Purpose: Provides visual dashboards for security posture and trends.

	Data Source: Amazon S3 (CloudTrail logs) or Amazon Athena (SQL queries over S3 data).

Key Dashboards:

•	Login activity by user and region
•	Top services accessed
•	IAM changes over time
•	Failed login attempts trend
•	API activity heatmap

	Refreshes daily or hourly from S3.

🔹 Security Measures
🔹 Monitoring & Alerts
🔹 Screenshots
🔹 Learnings

