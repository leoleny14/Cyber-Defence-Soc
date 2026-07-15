	

 As of August 2022, APT35 aka Charming Kitten was observed using a new tool called Hyperscrape to extract emails from their victims’ mailboxes

EventID : 212

Event Time : Dec, 27, 2023, 11:22 AM

Rule : SOC250 - APT35 HyperScrape Data Exfiltration Tool Detected

Severity : Medium

Level : Security Analyst

Hostname : Arthur

Ip Address : 172[.]16.17.72

Process Name : EmailDownloader.exe

Process Path : C:\Users\LetsDefend\Downloads\EmailDownloader.exe

Parent Process : C:\Windows\Explorer.EXE

Command Line : C:\Users\LetsDefend\Downloads\EmailDownloader.exe

File Hash : cd2ba296828660ecd07a36e8931b851dda0802069ed926b3161745aae9aa6daa

Trigger Reason : Unusual or suspicious patterns of behavior linked to the hash have been identified,

indicating potential malicious intent.

Device Action : Allowed

Description :

A strange pattern was identified on the machine,
followed by a malicious hash code.

Tools Involved :

              - Log Management (SIEM).
              - Endpoint Security (SIEM).
              - Threat Intel (VirusTotal).
              - Threat Intel (SIEM).

-Initial Investigation

EDR Data : 

              - Suspicious Process: EmailDownloader.exe. 

Log Management : 

              - Suspicious IP:  173[.]209.51.54.
              - Suspicious Operation Downloaded.

Threat Intel : 

              - Malicious Hash: cd2ba296828660ecd07a36e8931b851dda0802069ed926b3161745aae9aa6daa.
              - IP checked: Marked as malicious.

Timeline: 

              - Investigation started at: Jul, 14, 2026, 09:00 PM
              - Investigation ended at: Jul, 11, 2026, 09:35 PM
              - Attack started: Dec, 27, 2023, 09:48 PM.
              - Last attempt: Dec, 27, 2023, 11:26 PM.
              - Targeted server: 172[.]16.17.72.
              - Hostname: Arthur.

Short-Term Actions:

              - Block source IP (173[.]209.51.54).
              - Temporarily disable the targeted server for review.
              - Alert the server administrator/owner.

-PlayBook

1.Determine the Type of Reconnaissance

              - Gather Victim Host Information, Log in user host with a suspicious IP.

2.Attacker IP Analysis? 

              - External, IP from a malicious source, located on Canada.

3.IP Reputation Check

              - Malicious.

4.Determine the Scope

              - Only one device affected.

5. Containment

              - Host Contained.

6. Add Artifacts

              - cd2ba296828660ecd07a36e8931b851dda0802069ed926b3161745aae9aa6daa -- Malicious Hash --
              - 173.209.51.54 -- Malicious IP --

Results: 
The pattern was confirmed, a malicious IP address
located in Canada was recorded logging into the host account.

True Positive


 
