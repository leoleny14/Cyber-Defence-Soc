	

 Splunk App for Lookup File Editing RCE via User XSLT

EventID : 201

Event Time : Nov, 21, 2023, 12:24 PM

Severity: High.

Rule : SOC239 - Remote Code Execution Detected in Splunk Enterprise

Level : Security Analyst

Source IP Address : 180[.]101.88.240

Destination IP Address : 172[.]16.20.13

Hostname : Splunk Enterprise

HTTP Request Method : POST

Requested URL : http://18.219.80.54:8000/en-US/splunkd/__upload/indexing/preview?output_mode=json&props.NO_BINARY_CHECK=1&input.path=shell.xsl

Trigger File Path : /opt/splunk/var/run/splunk/dispatch/1700556926.3/shell.xsl

Alert Trigger Reason : Detected a malicious XSLT upload in Splunk Enterprise with the potential to trigger remote code execution.

Device Action : Allowed

Description:

A malicious XSLT was uploaded to the user's machine, 
and this XSLT was successfully executed.

Tools Involved:

           - Log Management (SIEM).
           - Endpoint Security (SIEM).
           - Threat Intel (SIEM).
           - Threat Intel (VirusTotal).

Action Taken:

           - Categorisation: Remote code Execution.
           - Remote Code Execution Confirmation: Result 200 OK, The login attempt was successful.
           - Source IP Address: Nothing suspicious was detected.

-Initial Investigation

Log Management: 

           - Malicious Raw Data:  Date=2023-11-21 12:23:56, Client IP=172[.]16.20.13, Source IP=180[.]101.88.240, Source Port=54321, Destination IP=18[.]219.80.54, Destination Port=8000, Request=POST, 
URI=/account/login, Username=admin, Password=SPLUNK-i-04673a41b8017af54, Protocol=HTTP/1.1 python3.9, Response=200.

EDR Data:

           - Processes: Suspicious Python script executed.
           - Terminal History: Suspicious commands.

Threat Intel (SIEM and VirusTotal): 

           - Malicious URL: http://18[.]219.80.54:8000/en-US/splunkd/__upload/indexing/preview?output_mode=json&props.NO_BINARY_CHECK=1&input.path=shell.xsl.
           - Malicious IP: 180[.]101.88.240.

Timeline: 

           - Investigation Started at: Jul, 13, 2026, 08:10 PM.
           - Investigation Ended at:
           - Attack Started: Nov, 21, 2023, 12:23 PM.
           - Lest Attempt: Nov, 22, 2023, 02:37 AM.
           - Target Server: 172[.]16.20.13.
           - Hostname: Splunk Enterprise.


Short-Term Actions:

           - Block source IP (180[.]101.88.240).
           - Temporarily disable the targeted server for review.
           - Alert the server administrator/owner.

-Playbook

1. Is Traffic Malicious?

          - Yes, Malicious Script found.

2. What Is The Attack Type?

          - XML Injection.

3. Check If It Is a Planned Test?

         - Not Planned.

4. What Is the Direction of Traffic?

        - Internet -> Company Network.

5. Check Whether the Attack Was Successful

        - Successful, 200 OK Displayed.

6. Containment

        - Host Contained.

7. Add Artifacts

        - 180.101.88.240 -- Malicious IP --
        - http://18[.]219.80.54:8000/en-US/splunkd/__upload/indexing/preview?output_mode=json&props.NO_BINARY_CHECK=1&input.path=shell.xsl. --Malicious URL--
        -
        -

8. Do You Need Tier 2 Escalation?

        - Yes.

Result: 

     A malicious XSLT file was uploaded to the user's machine and successfully executed.
    The XSLT was triggered by a Python script originating from a malicious IP address in China, granting access to an administrator-level account,
    a more in-depth investigation will be required.
