## Cloud Security Monitoring System
# 🌐 Project Overview

This project implements a **cloud monitoring, alerting, auditing, and secrets management solution** using AWS services.  
It monitors EC2 instance performance using **Amazon CloudWatch**, sends real-time email alerts via **SNS**, tracks AWS API activity using **CloudTrail**, and securely stores sensitive data using **AWS Secrets Manager**.  
The project focuses on **observability, security awareness, and operational monitoring** in a cloud environment.

---

## ⚙️ AWS Services Used

1. **AWS CloudTrail** – For tracking and auditing cloud activity logs  
2. **AWS S3** – For secure storage of log files  
3. **AWS CloudWatch Logs** – For real-time log monitoring and analysis  
4. **AWS CloudWatch Alarms** – For sending alerts based on monitored events  
5. **AWS SNS** – For sending security notifications and alerts to the user  

---

## 🏗️ Architecture Diagram

🔹 **Step-by-Step Implementation**

1. **User Activity**  
   All AWS user and service API actions (such as login, EC2 start/stop, IAM policy changes) are automatically captured.

2. **AWS CloudTrail**  
   - Records all management events and delivers them to:  
     • S3 bucket (for storage and long-term audit)  
     • CloudWatch Logs (for real-time analysis)  

3. **AWS S3**  
   - Acts as a central log repository.  
   - Stores all CloudTrail event logs in a versioned and encrypted format.  
   - Data can later be analyzed using Athena or visualized via QuickSight.  

4. **AWS CloudWatch Logs**  
   - Streams logs for continuous monitoring.  
   - Metric Filters configured to search for key patterns:  
     • Unauthorized API calls  
     • Console login failures  
     • Root account usage  
     • IAM role or user changes  

5. **CloudWatch Alarms**  
   - Each metric filter is linked to an alarm.  
   - When conditions are met (e.g., >0 failed logins), the alarm changes to ALARM state.  

6. **AWS SNS**  
   - CloudWatch Alarms trigger SNS topics.  
   - SNS then sends email/SMS alerts to the administrator or security team.  

---

# 📖 Publication

My book chapter *“Emerging Technologies in Cybersecurity”* (co-authored with Jyoti Pruthi) is officially listed as **Chapter 10** in  
*Blockchain and Quantum Computing Technologies for Cybersecurity* (Bentham Science Publishers, UAE).

### Submission Files
- [Chapter PDF](docs/BookChapter.pdf)  
- [Chapter DOCX](docs/BookChapter.docx)  
- [Plagiarism Report](docs/PlagiarismReport.pdf)  
- [Copyright Form](docs/CopyrightForm.pdf)  
- [Book TOC (Proof of Indexing)](docs/Book_TOC.pdf)  

### 📌 Notes
- Plagiarism compliance: **7%** (below required <10%).  
- Indexed as **Chapter 10** in the official Table of Contents.  
- Submitted in both PDF and DOCX formats as per publisher guidelines.  

---

## ✅ Conclusion

This repository demonstrates both **hands-on AWS cloud security implementation** and my **academic contribution** to the field of cybersecurity.  
It serves as a **portfolio of practical skills + published research**.
