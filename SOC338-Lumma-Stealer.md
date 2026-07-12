EventID : 316

Event Time : Mar, 13, 2025, 09:44 AM

Rule : SOC338 - Lumma Stealer - DLL Side-Loading via Click Fix Phishing

Level : Security Analyst

Severity: Critical

SMTP Address : 132[.]232.40.201

Source Address : update@windows-update.site

Destination Address : dylan@letsdefend.io

E-mail Subject : Upgrade your system to Windows 11 Pro for FREE

Device Action : Allowed

Trigger Reason : Redirected site contains a click fix type script for Lumma Stealer distribution.

Description:

The user received an email with the content "Upgrade your system to Windows 11 Pro for FREE"
, this email contains a malicious URL hosting Lumma Stealer
, a powerful information-stealing malware.


Tools Involved:

            - Log Management (SIEM).
            - Endpoint Security (SIEM).
            - Email Security (SIEM).
            - Threat Intel (VirusTotal).
            - Threat Intel (SIEM).

Action Taken:

            - SMTP Adress Investigation: Malicious linked with Lumma Stealer.
            - Email Investigation: Marked as Malicious, Malwere, Pishing.
            - Data Leakege Confirmation: Successful attack identified.
            - Categorisation: Data Leakege.

-Initial Investigation

EDR Data:

            - Terminal History: Malicious code designed to trick the system into downloading and executing malware.
            - Browser: Malicious URL found.
            - Processes: timed task failure.
            - Processes: Malicious Hash found.

Threat Intel (SIEM and VirusTotal): 

            - Malicious Hash: 15c80b5be235bf2a8c38291eb697a702c07dde087eb459e9ea46a2bee17c5f03.
            - Malicious IP: 132[.]232.40.201.
            - Malicious URL: https://www.windows-update.site/.


Timeline: 

            - Investigation started at: Jul, 11, 2026, 07:50 PM
            - Investigation ended at: Jul, 11, 2026, 08:49 PM
            - Attack started: Mar, 13, 2025, 09:44 AM.
            - Last attempt: Mar, 13, 2025, 11:26 PM.
            - Targeted server: 172[.]16.17.216.
            - Hostname: Dylan.

Short-Term Actions:

            - Block source IP (132[.]232.40.201).
            - Temporarily disable the targeted server for review.
            - Alert the server administrator/owner.

-PlayBook

1. Are there attachments or URLs in the email?

            - Yes, https://www.windows-update.site/.

2. Analyze Url/Attachment

           - Malicious (Positive 11/92 VirusTotal -- Positive SIEM).

3. Check If Mail Delivered to User?

           - Delivered (Checked in EDR).

4.Delete Email From Recipient!

           - Email Deleted.

5.Check If Someone Opened the Malicios File/URL?

           - Opened by 172[.]16.17.216 (Target server).

6.Containment

           - Host Contained.

7.Add Artifacts

           - https://www.windows-update.site/ --Malicious URL--
           - update@windows-update.site -- Malicious E-Mail Sender --
           - 132[.]232.40.201 -- Malicious IP --
           - 15c80b5be235bf2a8c38291eb697a702c07dde087eb459e9ea46a2bee17c5f03 -- Malicious Hash --

Result: 

Analysis indicated that the 'Lumma Stealer' malware gained access to the user's machine and may have compromised it,
a more technical analysis is required to identify any leaked files.
The machine has been properly isolated pending further instructions. 
The user must be notified of the incident. 
This event highlights the real risks associated with malicious emails.

References:
    
           -https://malpedia-caad-fkie-fraunhofer-de.translate.goog/details/win.lumma?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt&_x_tr_pto=
