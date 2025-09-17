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

![ Img: Installing the Wazuh Server in Ubuntu](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/1.png)
![ Img: Wazuh Dashboard Login Page](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/2.png)
![ Img:](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/3.png)
![ Img:](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/4.png)
![ Img: Create a Linux Agent “Prakher-Linux-Agent”](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/5.png)
![ Linux Agent](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/6.png)
![ Img:](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/7.png)
![ Img: Events from Linux Agent in Dashboard](https://github.com/Prakher-v/Wazuh-SIEM-Deployment-and-Monitoring-WSL2/blob/main/imgaes_Wazuh/8.png)

## Challenges and How I Overcame Them

### 1. System Resource Limitations

#### Challenge: Wazuh requires at least 2 CPU cores, 4 GB RAM, and 50 GB storage, but my laptop specifications were below these requirements. Running a full virtual machine environment for Wazuh was not possible.
#### Solution: I used WSL2 (Windows Subsystem for Linux) instead of traditional virtual machines. This allowed me to deploy both the Wazuh server and agent in lightweight Linux environments while staying within my hardware limits.

### 2. Agent Connectivity Issues

#### Challenge: Initially, the Wazuh agent failed to connect with the server due to incorrect configuration of IP addresses and ports.
#### Solution: I troubleshooted by verifying network settings, adjusting firewall rules, and ensuring that the Wazuh server was listening on the correct port (5601). After re-registering the agent with the corrected configuration, the connection was successfully established.

###3. Event Simulation Constraints

#### Challenge: I intended to perform an Nmap TCP SYN scan to generate attack traffic and observe the detection in the Wazuh dashboard. However, due to resource limitations, running the scan caused system instability.
####Solution: I documented the attack methodology and validated event logging with lighter activity instead. This still proved that the Wazuh setup could collect and analyze logs effectively.

##Key Learnings

-	Understood how endpoint agents forward logs to a centralized server for analysis.
-	Practical experience with endpoint-agent communication in Wazuh.
-	Hands-on exposure to SIEM-like monitoring workflows.
-	Improved ability to resolve connectivity and configuration issues between distributed components.
-	Learned how to adapt enterprise-grade security tools (like Wazuh) to run effectively in a resource-constrained environment using WSL2.
-	Developed resilience in overcoming technical roadblocks through research, troubleshooting, and alternative approaches.
-	Enhanced understanding of real-time monitoring, alert prioritization, and compliance-related event handling.


