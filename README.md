# AzureLockdown-Securing-Workloads-with-Azure-Virtual-Network-Controls

The project focuses on network isolation, traffic control, protection against malicious traffic, routing, and DNS configuration to enhance the security posture of the network.


## Introduction
This project aims to configure secure access to workloads using Azure virtual networking services. It is designed to prepare Azure Administrators for configuring secure access to web applications hosted on Azure. The project focuses on network isolation, traffic control, protection against malicious traffic, routing, and DNS configuration to enhance the security posture of the network.

## Architecture Diagram
![az-networking](https://github.com/user-attachments/assets/495fab94-8e79-4910-a28b-e287be916910)


## Objectives
- Create and configure virtual networks to provide network isolation and segmentation.
- Control network traffic using Network Security Groups (NSGs) and Azure Firewall.
- Protect the web application from malicious traffic and unauthorized access.
- Route traffic to the firewall for inspection.
- Record and resolve domain names internally using DNS configuration.

## Project Structure
The project consists of several skilling areas, each with corresponding tasks:

1. **Create and Configure Virtual Networks:**
   - Create a virtual network.
   - Configure subnets.
   - Configure virtual network peering.

2. **Create and Configure Network Security Groups (NSGs):**
   - Create an NSG.
   - Associate an NSG to a subnet or a network interface.
   - Create NSG rules.
   - Create and use Application Security Groups (ASGs) in NSG rules.

3. **Create and Configure Azure Firewall:**
   - Create an Azure Firewall.
   - Create and configure a public IP address.
   - Create and configure a firewall policy.

4. **Configure Network Routing:**
   - Create and configure a route table.
   - Link a route to a subnet.

5. **Create DNS Zones and Configure DNS Settings:**
   - Create and configure a private DNS zone.
   - Create and configure DNS records.
   - Configure DNS settings on a virtual network.

## Prerequisites
- Azure subscription with sufficient permissions to create and manage resources.
- Basic understanding of networking concepts.
- Familiarity with Azure Portal and Azure CLI.

## Instructions
1. **Clone the Repository:**
   ```
   git clone https://github.com/krvsc/AzureLockdown-Securing-Workloads-with-Azure-Virtual-Network-Controls.git
   ```

2. **Navigate to the Project Directory:**
   ```
   cd AzureLockdown-Securing-Workloads-with-Azure-Virtual-Network-Controls
   ```

3. **Setup Azure Environment:**
   - Log in to Azure Portal.
   - Create necessary resource groups and subscriptions.
   - Ensure proper permissions for the Azure account.

4. **Complete Each Task:**
   - Follow the provided instructions for each skilling area.
   - Refer to Azure documentation for detailed guidance.
   - Execute commands using Azure CLI or Azure Portal as per preference.

5. **Share Your Progress:**
   - Update the README.md file with your progress and any relevant notes.
   - Include screenshots or code snippets if necessary.


### Contributions
Contributions to this project are welcome. If you find any issues or improvements, feel free to open an issue or create a pull request. Ensure that contributions align with the project objectives and maintain clarity and correctness in documentation.

### Conclusion
By completing this project, you will gain practical experience in configuring secure access to workloads using Azure virtual networking services. This hands-on experience will enhance their skills in network security, routing, and DNS configuration in the Azure environment.

