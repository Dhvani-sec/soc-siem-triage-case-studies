🚨 Case 04 – Spike in Domain Discovery Commands
## Alert Overview

A medium-severity SIEM alert was triggered due to a sudden spike in Active Directory reconnaissance commands (e.g., whoami, net user, nltest, net group "Domain Admins"), which are commonly associated with attacker enumeration activity following initial access.

## Investigation Steps

-Reviewed the affected server role (public-facing mail server in DMZ segment)

-Identified the executing security context (SYSTEM-level privileges)

-Analyzed the sequence of domain discovery commands executed

-Investigated process hierarchy and parent-child relationships

-Assessed whether the activity aligned with legitimate administrative operations

## Process Lineage Observed

-Parent process: web server worker process

-Child process: suspicious reverse shell executable

-Spawned process: command shell (cmd.exe)

## Findings

The commands were executed under elevated privileges and originated from a web-facing service process.

The presence of a reverse shell process within the execution chain strongly indicates unauthorized command execution following potential web application compromise.

The command sequence aligns with common attacker post-exploitation behavior, specifically domain reconnaissance and privilege enumeration.

## Verdict

True Positive – Confirmed Suspicious Activity

Escalation and incident response procedures would be required in a real-world scenario.

## Key Takeaways

-Spikes in domain discovery commands are high-value indicators when correlated with suspicious process lineage.

-Process hierarchy analysis is critical in distinguishing legitimate administrative activity from attacker reconnaissance.

-SYSTEM-level execution combined with reverse shell indicators significantly increases confidence of compromise.
