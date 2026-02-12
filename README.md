# Digital Forensics Incident Timeline Reconstruction

## Overview
This project reconstructs a cyber attack timeline using Windows Event Logs (.evt) and NTFS $MFT metadata from the Magnet CTF 2019 dataset.

The investigation combines data correlation, anomaly detection, and forensic artifact analysis to identify persistence mechanisms and data exfiltration.

## Tools & Technologies
- Python
- Pandas
- Scikit-learn (Isolation Forest)
- Google Colab
- NTFS $MFT analysis
- Windows Security Event Logs

## Key Findings
- Detected 184 automated successful logins on Feb 25 (anomalous behavior)
- Identified TeamViewer installation as persistence mechanism
- Confirmed OneDrive archive exfiltration on March 18
- Discovered 153-day suspicious logging gap
- Correlated authentication events with file system artifacts (±2 min window)

## Investigation Phases
1. Initial Compromise (Feb 25)
2. Persistence via Remote Access Tool
3. Data Exfiltration (March 18)
4. Gap Analysis & Time Manipulation Review

## Conclusion
The analysis confirmed a two-stage Advanced Persistent Threat (APT) involving credential compromise, persistence installation, and sensitive data exfiltration.

