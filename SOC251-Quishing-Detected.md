	Medium	Jan, 01, 2024, 12:37 PM	SOC251 - Quishing Detected (QR Code Phishing)	214	Exchange	
	
EventID : 214

Event Time : Jan, 01, 2024, 12:37 PM

Rule : SOC251 - Quishing Detected (QR Code Phishing)

Severity : Medium

Level : Security Analyst

SMTP Address : 158[.]69.201.47

Source Address : security[@]microsecmfa.com

Destination Address : Claire[@]letsdefend.io

E-mail Subject : New Year's Mandatory Security Update: Implementing Multi-Factor Authentication (MFA)

Device Action : Allowed


Description:

A malicious email containing a phishing QR code was sent to the user.


Tools Involved:

            - Log Management (SIEM).
            - Endpoint Security (SIEM).
            - Email Security (SIEM).
            - Threat Intel (VirusTotal).
            - Threat Intel (SIEM).
            - Threat Intel (IsThisQrSafe)

Action Taken:

            - SMTP Adress Investigation: Malicious linked with Qhishing.
            - Email Investigation: Phishing Qr code (Quishing).
            - Phishing Confirmation: Successful attack identified.
            - Categorization: Phishing.

-Initial Investigation

EDR Data:

            - Malicious Process

Threat Intel (SIEM, VirusTotal and IsThisQrSafe): 


            - Malicious QR code: https://ipfs.io/ipfs/Qmbr8wmr41C35c3K2GfiP2F8YGzLhYpKpb4K66KU6mLmL4.


Log Management:

            - Malicious Email sender IP: 172[.]16.20.3.
            - Malicious IP: 158[.]69.201.47.


Timeline: 

            - Investigation started at: Jul, 28, 2026, 08:50 PM.
            - Investigation ended at: Jul, 11, 2026, 09:15 PM.
            - Attack started: Jan, 01, 2024, 12:00 PM.
            - Last attempt: Jan, 01, 2024, 12:37 PM.
            - Targeted server: 172[.]16.17.181.
            - Hostname: Claire.

Short-Term Actions:

            - Block source IP (158[.]69.201.47).
            - Temporarily disable the targeted server for review.
            - Alert the server administrator/owner.

-PlayBook

1.Determine the Type of Reconnaissance

            - Phishing for Information.

2.Attacker IP Analysis

            - External

3.IP Reputation Check 

            - Malicious 

4.Determine the Scope 

            - Only one device affected

5.Containment

            - Host Contained

6.Add Artifacts

            - 172[.]16.20.3 -- Malicious IP --
            - 158[.]69.201.47 -- Malicious IP --
            - security[@]microsecmfa.com -- Email sender --
            - https://ipfs.io/ipfs/Qmbr8wmr41C35c3K2GfiP2F8YGzLhYpKpb4K66KU6mLmL4 -- Phishing Qr  --

Results

The user opened the phishing email and was infected,
the device has already been contained, and the incident has been reported.


True Positive
