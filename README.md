# Azure Sentinel SIEM Exposure Project

## Project Overview
This project involves using **Microsoft Sentinel**, Azure's cloud-native SIEM and SOAR solution, integrated with an **Azure Virtual Machine** and an **Azure Firewall**. The goal of the project was to expose myself to Microsoft Sentinel and learn how to integrate it with a VM and firewall, in addition I wanted to be able to create my own diagnostic setting. Plus connect it with Azure Activity (a data connector). Through online resources, documentation and Azure Portal's built in Co-pilot I did my best to achieve this project.

---

## Objectives
- Deploy and configure Microsoft Sentinel using a Log Analytics Workspace.
- Connect data sources: **Azure VM** and **Azure Firewall**.
- Monitor security events using **custom KQL analytics rules**.
- Visualize insights via Sentinel **Workbooks**.

---

## Architecture Diagram


---

## Technologies Used
- Microsoft Sentinel
- Azure Log Analytics
- Azure Virtual Machine (Linux)
- Azure Firewall
- Azure Logic Apps
- Kusto Query Language (KQL)

---

## Setup Steps

### 1. Create Log Analytics Workspace
- Created `SentinelWorkspace` in `eastus`.
- Attached workspace to Sentinel instance.

### 2. Deploy Azure Sentinel
- Enabled Sentinel on `SentinelWorkspace` via Azure Portal.

### 3. Provision and Configure Azure VM
- Deployed Linux VM (`linux-vm`).
- Enabled Diagnostic Settings → Forwarded event logs to Log Analytics.

### 4. Deploy and Configure Azure Firewall
- Created VNet with `AzureFirewallSubnet`.
- Deployed Firewall, attached Public IP.
- Enabled Diagnostic Settings → Forwarded firewall logs to Log Analytics.

### 5. Connect Data Sources in Sentinel
- Connected:
  - Azure Activity

### 6. Created Custom Analytics Rules
- **Rule:** Detect denied outbound traffic from Firewall logs

### 7. Configured Sentinel Workbooks
- Customized dashboard to display:
  - Firewall denial logs

### 8. Built Automation Playbooks (SOAR)
- Example: Trigger email alert and disable user on login anomaly
- Logic App triggered by Sentinel incident

### 9. Simulated Security Events
- Generated blocked outbound traffic through Firewall


