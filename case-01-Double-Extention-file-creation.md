🚨 Case 01 – Double-Extension File Creation Alert
## Alert Overview

A high-severity alert was triggered due to the creation of a file using a double extension (.mp4.exe), a technique commonly used to disguise malicious executables as legitimate media files.

## Investigation Process
Identified the affected workstation
Reviewed associated user activity
Analyzed the parent process responsible for execution
Investigated file path and download source
Evaluated reputation of the external domain
Checked for additional correlated events on the endpoint

## Findings

The file was downloaded from an untrusted external domain. The double-extension pattern and delivery method align with common phishing and malware delivery techniques.

No further suspicious lateral movement or persistence activity was observed within available log visibility.

## Verdict

True Positive – Suspicious file creation requiring escalation and containment procedures.

## Key Learning

Double-extension files are strong phishing indicators.
Context validation (user behavior + source validation + host correlation) is critical in determining severity.
