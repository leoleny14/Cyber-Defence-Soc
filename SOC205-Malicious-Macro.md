Medium	Feb, 28, 2024, 08:42 AM	SOC205 - Malicious Macro has been executed	231	Malware	
	
EventID : 231

Event Time : Feb, 28, 2024, 08:42 AM

Rule : SOC205 - Malicious Macro has been executed

Severity: Medium

Level : Security Analyst

Hostname : Jayne

Ip Address : 172.16.17.198

File Name : edit1-invoice.docm

File Path : C:\Users\LetsDefend\Downloads\edit1-invoice.docm

File Hash : 1a819d18c9a9de4f81829c4cd55a17f767443c22f9b30ca953866827e5d96fb0

Trigger Reason : Suspicious file detected on system.

AV/EDR Action : Detected

Description : 

A suspicious file was executed on the machine,
it accessed suspicious URLs and executed commands in the terminal.

Tools Involved :

              - Log Management (SIEM).
              - Endpoint Security (SIEM).
              - Threat Intel (SIEM).
              - Threat Intel (VirusTotal).

Action Taken :

              - Categorization: Maware.
              - Malware Confirmation: Invasion confirmed.
              - Email Investigation: Marked as Malicious, Malwere, Pishing.

-Initial Investigation

EDR Data :

              - Nothing found.

Log Management :
 
              - Malicious URL executed by a command in PowerShell.
              - Malicious command ran by the Email malware.

Threat Intel (SIEM, VirusTotal) :

              - Suspicious URL 'HTTP://WWW.GREYHATHACKER[.]NET'.
              - Malicious Hash 1a819d18c9a9de4f81829c4cd55a17f767443c22f9b30ca953866827e5d96fb0.
              - Malicious Email archive https://download.cyberlearn.academy/download/download?url=https://files-ld.s3.us-east-2.amazonaws.com/edit1-invoice.docm.zip.

Timeline :

              - Investigation started at: Jul, 15, 2026, 03:55 PM
              - Investigation ended at: Jul, 15, 2026, 04:15 PM
              - Attack started: Feb, 28, 2024, 08:41 AM.
              - Last attempt: Feb, 29, 2024, 04:04 AM.
              - Targeted server: 172[.]16.17.198.
              - Hostname: Jayan.

Short-Term Actions:

              - Temporarily disable the targeted server for review.
              - Alert the server administrator/owner.

-PlayBook

1.Define Threat Indicator : 

              - Other, Phishing.

2.Check if the malware is quarantined/cleaned :

              - Not quaranteined.

3.Analyze Malware :

              - Malicious.

4.Check If Someone Requested the C2 :

              - Accessed

5.Containment :

              - Host Contained

6.Add Artifacts : 

              - HTTP://WWW.GREYHATHACKER.NET -- Suspicious URL --
              - 1a819d18c9a9de4f81829c4cd55a17f767443c22f9b30ca953866827e5d96fb0 -- Malicious hash --
              - https://download.cyberlearn.academy/download/download?url=
https://files-ld.s3.us-east-2.amazonaws.com/edit1-invoice.docm.zip -- Malicious Archive in the Email --
              - jake.admin@cybercommunity.info -- C2 Email --
              - 92.204.221[.]16 -- C2 IP --

Results: 

The file originated from a phishing email,
when the email's content was executed and opened,
the malware ran terminal commands, accessed suspicious websites, and tampered with the EDR.

True Positive
