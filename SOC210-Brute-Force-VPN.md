High	Jun, 21, 2023, 01:51 PM	SOC210 - Possible Brute Force Detected on VPN	162	Brute Force	
	
EventID : 162

Event Time : Jun, 21, 2023, 01:51 PM

Rule : SOC210 - Possible Brute Force Detected on VPN

Severity: High

Level : Security Analyst

Source Address : 37[.]19.221.229

Destination Address : 33[.]33.33.33

Destination Hostname : Mane

Username : mane@letsdefend.io

Alert Trigger Reason : A successful VPN login was detected shortly after failed login attempts from the same source IP address

L1 Note : I checked the authentication logs and saw many login failures from the same IP address.
It was also detected that the same IP address was attempting to login for different users.
Successful login looks suspicious after these failed login attempts.

Description:

 Many login failures from the same IP address.
It was also detected that the same IP address was attempting to login for different users.
Successful login looks suspicious after these failed login attempts.



Tools Involved:

            - Log Management (SIEM).
            - Endpoint Security (SIEM).
            - Email Security (SIEM).
            - Threat Intel (VirusTotal).
            - Threat Intel (SIEM).

Action Taken:

            - Source Adress Investigation: Marked as malicious.
            - Email Investigation: Nothing found.
            - Categorization: Brute force (Large volume of login attempts).
            - Brute Force Confirmation: Successful attack identified.

-Initial Investigation

EDR Data:

            - Terminal History: Suspicious commands.
            - Browser: Nothing suspicious.
            - Network Action: High volume from the same IP.
            - Process: Incomun processes.

Threat Intel (SIEM and VirusTotal): 

            - Malicious IP: 37[.]19.221.229.
            - Malicious IP: 33[.]33.33.33.

Timeline: 

            - Investigation started at: Jul, 22, 2026, 05:00 PM
            - Investigation ended at: Jul, 22, 2026, 05:40 PM
            - Attack started: Jun, 21, 2023, 09:20 AM.
            - Last attempt: Jun, 21, 2023, 01:51 PM.
            - Targeted server: 172[.]16.17.210.
            - Hostname: Mane.

Short-Term Actions:

            - Block source IP (37[.]19.221.229).
            - Temporarily disable the targeted server for review.
            - Alert the server administrator/owner.

-PlayBook

1.Enrichment & Context

            -External.

2.Log Management

            - Successful acess from the attacker.

3.Does the device need to be isolated?

            - Yes.

4.Containment

            -Host Contained.

5.Add Artifacts

            - 33.33.33.33 -- Malicious IP --
            - 37.19.221.229 -- Malicious IP --

Results: 

 The target was subjected to a brute-force attack,
indicated by a high volume of login attempts from the same source IP,
the attack was successful, and the machine has already been isolated.

True Positive
