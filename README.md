# Wazuh Windows SOC Home Lab – SIEM Threat Detection

## Project Overview

This project demonstrates the deployment and practical use of Wazuh SIEM to monitor a Windows 11 endpoint, collect security events, investigate authentication activity and detect file modifications

The lab simulates selected responsibilities of a Level 1 Security Operations Centre (SOC) Analyst in a controlled environment

## Project Objectives

- Deploy a Wazuh SIEM environment
- Connect a Windows 11 endpoint to Wazuh
- Collect and analyse Windows Security Event Logs
- Investigate failed authentication attempts
- Investigate user account creation events
- Document security findings and evidence

## Technologies and Tools

| Technology | Purpose |
|---|---|
| Wazuh 4.14.10 | SIEM and endpoint security monitoring |
| Windows 11 | Monitored endpoint |
| Ubuntu 24.04 | Linux environment using WSL2 |
| WSL2 | Linux subsystem |
| Docker Desktop | Container deployment |
| Windows Event Viewer / Security Logs | Event investigation |
| PowerShell | Security event generation and analysis |

## Lab Architecture

Windows 11 Endpoint  
↓  
Wazuh Windows Agent  
↓  
Wazuh Manager  
↓  
Wazuh Indexer  
↓  
Wazuh Dashboard

The Windows endpoint forwards security telemetry to the centralized Wazuh environment for monitoring and investigation

## Security Scenarios

### Scenario 1: Failed Authentication Investigation

**Windows Event ID:** 4625

Activities:
- Created a dedicated test account
- Generated a controlled failed authentication attempt
- Reviewed Windows Security Event Logs
- Investigated the event in Wazuh
- Examined authentication details and relevant event metadata

### Scenario 2: User Account Creation Investigation

**Windows Event ID:** 4720

Activities:
- Created a dedicated lab account
- Identified the corresponding account creation event
- Investigated the event in Wazuh
- Examined the affected account and event details

## Skills Demonstrated

- SIEM deployment and configuration
- Windows endpoint monitoring
- Security event collection
- Authentication event investigation
- Windows Event Log analysis
- File Integrity Monitoring
- Security alert investigation
- PowerShell
- Basic incident response
- Security documentation

## Evidence

The screenshots directory contains evidence of the environment deployment, endpoint connection and security investigations

## References

- [Wazuh Official Documentation](https://documentation.wazuh.com/)
- [Wazuh Docker Repository](https://github.com/wazuh/wazuh-docker)
- [Microsoft WSL Documentation](https://learn.microsoft.com/en-us/windows/wsl/)
- [Microsoft Windows Security Auditing](https://learn.microsoft.com/en-us/windows/security/threat-protection/auditing/)
