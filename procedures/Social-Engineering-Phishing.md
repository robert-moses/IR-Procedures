** Virus or Malicous Code Procedure **
INCIDENT RESPONSE PLAN FOR PHISHING ATTACKS
1. Introduction
Incident Response Plan (often termed as playbook) is a written document with instructions for identifying, containing, eradicating and recovering from cyber security incidents. This document describes Incident Response Plan for Phishing Campaigns/Attacks. The document describes instructions for handling e-mail based social engineering attacks.

1.1 Incident Response Plan ID:
IRP-01-PHISH

1.2 Title
Mitigation of Phishing Campaigns

1.3 Date Prepared
October 01 2018

1.4 Owner
Amol Wanave (CSIRT)

1.5 Objective
This incident response plan describes step-by-step procedures for handling user reported phishing attempts against WoodenBazaar associates. The goal is to prevent attackers from successful phishing attack. The response processes will include preparation to block phishing attempts, identification of threats in case of actual attack, containment and remediation procedures that finally ends with implementing preventive controls in organization network.

1.6 Scope
Phishing campaigns and spear phishing attacks against WoodenBazaar employees.

1.7 Assumptions and Limitations
This incident response plan is limited to the current infrastructure, configurations and deployed technology. This document should be regularly updated depending on future technological and infrastructural changes.

2. Phishing IR Plan: Procedures
The workflow below depicts the four stages of Phishing Incident Response process.

Phishing Incident Response Procedures

3. High Level Work Flow
Phishing IR Plan Work Flow
4. Procedures
4.1 Detection & Analysis
Phishing - Detection & Analysis

 

4.1.1 Initial Alert
SIEM Alert – Email Threat Analysis team will be alerted with potential phishing e-mail.
User Reported Spam Alert – Email Threat Analysis team will be alerted from report spam mailbox.
Other Sources – Email Threat Analysis team will be alerted from all other sources.
4.1.2 Gather Email Details
Validate if original e-mail headers are present.

In order to analyze the e-mail header of the potential phishing e-mail, E-mail Threat Analysis team must receive the original e-mail as an attachment from the reporting party.

4.1.3 Triage
Triage stage deals with verifying if the security alert is an incident and severity of an incident.

a. E-mail Header

Email Threat Analysis team should inspect the email header and collect the relevant data such as;

Sender Email Address
Recipient Email Address
Email Subject
Sender’s IP Address
X-Originating IP Address
Examine the email header for following phishing attributes:

Return-Path field contains an email address that is not related to the name shown in the from/sender field in the original email.
The X-Authenticated-User field contains an email address which appears suspicious
The Mail Server IP address in header is known to be malicious.
The email domain is known to be malicious.
b. Message Content

Email Threat Analysis team should inspect the email content and gather following information:

Email attachment
URL in the email body
If the original email has an attachment, collect it and store it in a password protected zip file with password “infected”.

c. Known False Positive

If the email alert is a known false positive, then close the investigation.

d. Sandbox

Submit the email attachment to the sandbox for dynamic analysis.

e. Phishing or Malicious Email

Based on the information gathered in the previous stages, the Email Threat Analysis team should decide if the email in question is a phishing email or it contains malware or links to malicious code. If the file attachment is malicious or contains malicious code, refer to the Malware Analysis IR Plan.

f. Recipients List

Review email transaction logs in SIEM to know total number of users who received this email and collect following information to profile the users:

User Name
Employee ID
Email Address
Department
Location
Designation
g. Is it a spear phishing attack?

Based on the information gathered from above steps, determine if it us a phishing campaign or a targeted phishing attack on organization or a particular person, department or location.

h. Create a case in case management tool.

Once Email Threat Analysis team confirms it is a security incident, create a case ID in case management tool under relevant category and assign priority based on information gathered.

4.1.4 Analyze the Phishing URL/ Attachment
Gather IOCs from sandbox report.
Search for hash value on VirusTotal.
Check for IP/URL reputation on Talos Intelligence portal or IPVoid and URLvoid.com
Search for URL on PhishTank.com to validate if it has already been reported as Phish.
4.1.5 Determine the Scope and Impact
Review Proxy Logs in SIEM
Review proxy logs to identify total number of users who clicked and accessed the phishing URL.

Review Firewall Logs in SIEM
Review firewall logs to identify the source IP addresses which were used to access phishing URL. From source IP address, asset owners

4.1.6 Profile Impacted Users
Profile users who have clicked on the phishing URL.

User Name
Employee ID
Department
Location
4.2 Containment
Phishing Containment

4.2.1 Block the Sender
Share the sender’s details with messaging team to block the sender in email gateway.

4.2.2 Block the URL and IP in Proxy and Firewall
Check the current URL category and reputation, if it is malicious and not blocked then initiate a block request to respective team.
Check the IP reputation and if it is blacklisted. If yes, then initiate a IP block request to respective team if it is not blocked already.
4.2.3 User Awareness Email
Based on the impact assessment, send an email to users suggesting not to open or click on the email in question.

4.2.4 Monitor Impacted User Accounts
Monitor impacted user accounts for any possible misuse.

4.3 Eradication & Recovery
Phishing - Eradication & Recovery

4.3.1 Delete Email from Users’ Mailboxes
Send an email to messaging team to delete phishing email from all impacted users’ mailboxes

4.3.2 Change Impacted Users’ Account Credentials
Affected users must change the account passwords. Confirm if the users have changed the passwords.

4.4 Post Incident Activities


4.4.1 Prepare and Review Investigation Report
Incident Manager will prepare an investigation report and will share it with CSIRT manager for review to ensure nothing was overlooked and everything is properly documented.

4.4.2 Prepare a Lessons Learned Document
CSIRT will prepare a lessons learned document capturing current security gaps and share the document with leadership.

4.4.3 Update an Incident Response Plan if required
If there are some technological or procedural changes in the IR plan, update the Incident Response Plan and share with leadership and involved stake holders.

### DETECT

### ANALYZE

### CONTAIN

### EREDICATE

### RECOVER



