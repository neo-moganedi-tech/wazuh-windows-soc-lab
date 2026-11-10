# Screenshot Evidence – Wazuh Windows SOC Lab

This folder contains visual evidence documenting the setup, configuration, and planned security monitoring activities of the Wazuh Windows SOC Lab

The screenshots are organised in numerical order to make the project easier to follow

## Screenshot List

| No. | Filename | Description |  
|---|---|---|---|
| 01 | `01-wsl-ubuntu-installed.png` | Ubuntu 24.04 installation and WSL 2 verification
| 02 | `02-docker-desktop-running.png` | Docker Desktop running on Windows 11
| 03 | `03-wazuh-containers-running.png` | Wazuh Manager, Indexer, and Dashboard containers running
| 04 | `04-wazuh-dashboard.png` | Wazuh web dashboard after successful login
| 05 | `05-windows-agent-active.png` | Windows endpoint successfully connected to Wazuh Manager
| 06 | `06-failed-login-detection.png` | Windows failed authentication event investigation (Event ID 4625)
| 07 | `07-account-creation-investigation.png` | Windows account creation event investigation (Event ID 4720)

## Evidence Notes

- Screenshots 01 and 03 document completed setup and deployment verification
- Screenshot 03 confirms that all three Wazuh containers were running during verification
- The Wazuh Indexer logs also showed cluster health reaching GREEN
