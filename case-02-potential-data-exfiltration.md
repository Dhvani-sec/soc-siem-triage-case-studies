🚨 Case 02 – Potential Data Exfiltration Alert
## Alert Overview

A critical SIEM alert was triggered due to more than 5GB of outbound data transferred from a single internal asset to an external destination within a 24-hour period, potentially indicating data exfiltration.

## Investigation Steps

Reviewed the source asset and associated network segment
Analyzed total outbound vs inbound traffic patterns
Verified the reputation of the destination domain
Assessed the asset role and typical operational behavior
Correlated activity timing with expected business operations

## Findings

The traffic was directed to a legitimate video conferencing platform.
The source asset was identified as a meeting room system, which can generate significant outbound traffic during virtual meetings or screen-sharing sessions.

No indicators of malicious domains, unusual geolocation, or additional suspicious activity were observed.

## Verdict

False Positive

## Key Takeaways

High outbound traffic volume alone does not confirm data exfiltration.
Asset role validation, traffic pattern analysis, and domain reputation checks are critical before escalating high-severity alerts.
