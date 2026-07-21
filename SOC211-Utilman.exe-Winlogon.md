Medium	Jun, 21, 2023, 11:02 AM	SOC211 - Utilman.exe Winlogon Exploit Attempt	161	LOLBin	
	
EventID : 161

Event Time : Jun, 21, 2023, 11:02 AM

Rule : SOC211 - Utilman.exe Winlogon Exploit Attempt

Level : Security Analyst

Hostname : Henry

Ip Address : 172.16.17.149

Process Name : Utilman.exe

Process Hash : ded8fd7f36417f66eb6ada10e0c0d7c0022986e9

Parent Process : Winlogon.exe

Command Line : net user superman onepunch123 /add

Trigger Reason : Command Launched from Winlogon

Device Action : Allowed




Description:

       A malicious command was executed by a legitimate Windows program.

Tools Involved:

            - Log Management (SIEM).
            - Endpoint Security (SIEM).
            - Email Security (SIEM).
            - Threat Intel (VirusTotal).
            - Threat Intel (SIEM).

Action Taken:

            - Categorisation: Privilege Escalation.
            - Privilege Escalation Confirmation: Successful attack identified.
            - Email Investigation: Nothing found.

-Initial Investigation

EDR Data:

            - Browser: Nothing Found.
            - Terminal History: Malicious Privilege Escalation commands.
            - Processes: Confirmation Privilege Escalation attack.
            - Network Action: High volume of traffic from the same IP address (172[.]31.19.74).

Log Management: 

            - Proxy: One malicious IP.
            - Firewall: One diferent malicious IP.

Threat Intel (SIEM and VirusTotal): 

            - Malicious IP: 93[.]184.220.29.
            - Malicious IP: 149[.]154.167.99.

Timeline: 

            - Investigation started at: Jul, 21, 2026, 03:00 PM
            - Investigation ended at: Jul, 21, 2026, 03:29 PM
            - Attack started: Jun, 21, 2023, 11:02 AM.
            - Last attempt: Jun, 21, 2023, 12:24 PM.
            - Targeted server: 172[.]16.17.149.
            - Hostname: Henry.

Short-Term Actions:

            - Block source IP (172[.]31.19.74).
            - Temporarily disable the targeted server for review.
            - Alert the server administrator/owner.
        
-PlayBook

1. Determine Suspicious Activity

            - Suspicious.

2.What Is Suspicious Activity?

            - UAC bypass.

3.Who Performed the Activity?

            - Malware (Because of the volume of trafic from the same and diferents IPs).

4.Containment.

            - Host Contained.

5.Add Artifacts

            - 172[.]31.19.74 -- Malicious IP --
            - 93[.]184.220.29 -- Malicious IP --
            - 149[.]154.167.99 -- Malicious IP --

Results :

        The command was executed by a legitimate Windows program,
        possibly triggered by malware, given the volume of traffic
        from a single IP address and several other distinct IPs. 
        Such commands are typically used for privilege escalation.

True Positive
