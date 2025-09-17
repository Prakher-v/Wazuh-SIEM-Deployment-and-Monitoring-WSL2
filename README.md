# Wazuh-SIEM-Deployment-and-Monitoring-WSL2

## Overview
This project demonstrates the deployment and configuration of Wazuh, an open-source security monitoring platform. The implementation included setting up a Wazuh server, configuring a Linux agent, and visualizing security events through the Wazuh dashboard. The project showcases how Wazuh can be used for real-time threat detection, log analysis, and security event monitoring.

## Objectives
- Deploy a functional Wazuh server within a resource-constrained environment.
- Configure and register a Linux agent to forward system events.
- Validate the setup by generating and analyzing events on the Wazuh dashboard.
- Explore the monitoring capabilities of Wazuh for cybersecurity operations.
  
## Implementation
### 1. Wazuh Server Setup
- Installed on Ubuntu (WSL2) to accommodate hardware limitations.
- Configured core components: Wazuh Indexer, Wazuh Server, and Wazuh Dashboard.
- Set up repositories, prerequisites, and completed installation using apt.
- Retrieved system credentials and accessed the dashboard via port 5601.

### 2. Wazuh Agent Setup
- Installed the Wazuh agent on a Kali Linux instance (WSL2).
- Registered and named the agent (Prakher-Linux-Agent).
- Connected the agent to the Wazuh server for continuous log forwarding.

### 3. Dashboard and Event Monitoring
- Accessed the Wazuh dashboard to visualize system events in real time.
- Validated agent activity by monitoring incoming events.
- Planned to simulate attacks with an Nmap TCP SYN scan to test alerting, but the scan was documented rather than executed due to resource limitations.

## Results
- Successfully deployed and integrated a Wazuh server with a Linux agent.
- Demonstrated centralized event collection, monitoring, and alert generation.
- Showcased how Wazuh provides visibility into system activities and potential security incidents.

## Challenges and Optimization
- Running Wazuh within WSL2 instead of a VM was necessary due to limited system resources (Wazuh requires ≥ 2 CPU cores, 4 GB RAM, and 50 GB storage).
- Despite constraints, the setup validated Wazuh’s ability to effectively collect and display agent events.

## Illustrations
# My Project

Here's a screenshot of my project:

![ Img: Installing the Wazuh Server in Ubuntu](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/1.png)
