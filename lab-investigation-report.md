# SOC Investigation Report – Wazuh Windows Lab

## 1. Executive Summary

This report documents two controlled security monitoring exercises performed using Wazuh SIEM and a Windows 11 endpoint

The objective was to practise security event investigation and endpoint monitoring 

## 2. Environment

| Component | Configuration |
|---|---|
| SIEM | Wazuh 4.14.10 |
| Endpoint | Windows 11 |
| Agent | Wazuh Windows Agent |
| Hostname | WIN11-SOC-LAB |
| Linux environment | Ubuntu 24.04 / WSL2 |
| Deployment | Docker Desktop |

## 3. Investigation One – Failed Authentication

**Windows Event ID:** 4625

### Objective

Identify and investigate an unsuccessful Windows authentication attempt

### Activity

A dedicated test account was created and a controlled failed login was generated

### Evidence Reviewed

- Windows Security Event Log
- Authentication event details
- Affected endpoint
- Target account
- Authentication failure information

### Security Analysis

A failed authentication event may indicate an incorrect password, user error or suspicious authentication activity

Repeated failures from the same source may warrant further investigation

A single failed attempt does not independently establish a brute-force attack

### Recommended Actions

- Review related authentication events
- Identify repeated failed attempts
- Investigate the source of suspicious activity
- Verify whether the account owner recognises the activity

## 4. Investigation Two – User Account Creation

**Windows Event ID:** 4720

### Objective

Investigate Windows user account creation activity

### Activity

A dedicated test account was created for the lab

### Evidence Reviewed

- Newly created account
- Account creation event
- Initiating account
- Event timestamp
- Affected endpoint

### Security Analysis

Unexpected account creation may indicate unauthorized account management or persistence activity

The event should be correlated with the identity of the initiating user and surrounding system activity

### Recommended Actions

- Verify the legitimacy of the new account
- Identify who created the account
- Review account privileges
- Escalate unauthorized account creation

## 5. Conclusion

The exercises demonstrate the use of Wazuh for centralized Windows security monitoring and investigation

The lab covers authentication event analysis and account management investigations

## 6. Evidence

Supporting screenshots are stored in the repository screenshots directory
