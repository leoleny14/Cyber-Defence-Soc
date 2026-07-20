	Medium	Sep, 17, 2024, 12:05 PM	SOC326 - Impersonating Domain MX Record Change Detected	304	ThreatIntel	
	

EventID : 304

Event Time : Sep, 17, 2024, 12:05 PM

Rule : SOC326 - Impersonating Domain MX Record Change Detected

Level : Security Analyst

Severity : Medium

Source Address : no-reply@cti-report.io

Destination Address : soc@letsdefend.io

Subject : Impersonating Domain MX Record Change Detected

Trigger Reason : The MX record of a suspicious domain was changed, suggesting potential phishing activity.

Domain : letsdefwnd[.]io

Mx_record : mail.mailerhost[.]net

Device Action : Allowed



Description : 
    
    A malicious email was sent containing a list of IP addresses,
    one of these IPs sent a phishing email to another user.


Tools Involved : 

               - Log Management (SIEM).
               - Endpoint Security (SIEM).
               - Email Security (SIEM).
               - Threat Intel (VirusTotal).
               - Threat Intel (SIEM).

Action Taken :

               - Email Investigation: Found a list of IPs, almost every been malicious, using one of this E-mails
               in the list on the Log Management its possible to find one host, Mateo.
               Mateo has recieved a phising email.
               - Categorisation: Phising
               - Phishing Confirmation: Successful attack identified.
        


-Initial Investigation

EDR Data : 

               - Processes: unauthorization acess.
               - Terminal History: Nothing found.
               - Browser History: Malicious URL.


Log Management :

               - Malicious URL Found : https://letsdefwnd.io.
               - Host affected Found : Mateo.


Threat Intel (SIEM and VirusTotal) :

               - Malicious IPs :
               - 72[.]14.185.43.
               - 72[.]14.178.174.
               - 45[.]33.30.197.
               - 45[.]79.19.196.
               - 96[.]126.123.244.
               - 45[.]33.20.235.
               - 45[.]33.18.44.
               - 45[.]33.2.79.
               - 198[.]58.118.167.
               - 45[.]33.23.183.
               - Malicious URL : http://letsdefwnd.io.
               



Timeline :

            - Investigation started at: Jul, 20, 2026, 01:07 PM
            - Investigation ended at: Jul, 20, 2026, 01:37 PM
            - Attack started: Sep, 17, 2024, 12:05 PM.
            - Last attempt: Sep, 18, 2024, 01:32 AM.
            - Targeted server: 172[.]16.17.162.
            - Hostname: Mateo.

Short-Term Actions :

            - Block source IP (45[.]33.23.183).
            - Temporarily disable the targeted server for review.
            - Alert the server administrator/owner.

-PlayBook

1.Are there attachments or URLs in the email?

            - Yes.

2.Analyze Url/Attachment

            - Malicious (Positive VirusTotal -- Positive SIEM).

3.Check If Mail Delivered to User?

            - Delivered ( Browser History .

4.Delete Email From Recipient!

            - Deleted.

5.Check If Someone Opened the Malicios File/URL?

            - Opened ( Browser History ).

6.Containment

            - Host Contained.

7.Add Artifacts

            - http://letsdefwnd.io -- Malicious URL --
            - 172[.]16.17.162 -- Target IP address --
            - 45[.]33.23.183 -- Malicious IP address --

Results :

    One of the IPs on the list sent a phishing email to a user,
    the user accessed the email and had their account compromised.
    The user's machine has been contained and will be analyzed.

True Positive
