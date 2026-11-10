# Wazuh SIEM Lab Architecture

## 1. Overview

The lab uses a single-node Wazuh deployment to monitor a Windows 11 endpoint

The Wazuh central components run through Docker Desktop using Ubuntu 24.04 under WSL2

## 2. Architecture Components

### Windows 11 Endpoint

The monitored system

Responsibilities:
- Generate Windows Security Events
- Produce authentication telemetry
- Generate file activity
- Run the Wazuh Windows Agent

### Wazuh Agent

Installed on the Windows endpoint

Responsibilities:
- Collect configured endpoint security telemetry
- Monitor configured files and directories
- Forward events to the Wazuh Manager

### Wazuh Manager

Central security analysis component

Responsibilities:
- Receive endpoint events
- Analyse collected telemetry
- Apply detection rules
- Generate security alerts

### Wazuh Indexer

Stores and indexes security information for searching and analysis

### Wazuh Dashboard

Provides the graphical interface for:
- Monitoring security events
- Viewing alerts
- Investigating endpoint activity
- Reviewing file integrity changes

## 3. Communication

The lab uses the following standard ports for Wazuh 4.x:

| Port | Purpose |
|---|---|
| TCP 1514 | Agent communication |
| TCP 1515 | Agent enrollment |
| TCP 55000 | Wazuh API |
| TCP 9200 | Indexer API |
| TCP 443 | Dashboard HTTPS |

## 4. Security Monitoring Scenarios

- Windows failed authentication – Event ID 4625
- User account creation – Event ID 4720

## 5. Architecture Flow

Windows 11  
→ Wazuh Agent  
→ Wazuh Manager  
→ Wazuh Indexer  
→ Wazuh Dashboard  
→ SOC Analyst Investigation
