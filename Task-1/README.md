### Task 1: Network Isolation and Segmentation for the Web Application

#### What:
To provide network isolation and segmentation for the web application, we will create an Azure virtual network with subnets. Additionally, we will configure virtual network peering to enable secure and private communication between the virtual networks.

#### Why:
Network isolation and segmentation enhance security by restricting communication between different components of the infrastructure. Virtual network peering enables seamless connectivity between virtual networks while ensuring traffic remains isolated and secure.

#### How:

1. **Create Virtual Networks and Subnets:**
   - Navigate to the Azure portal and log in.
   - Search for "Virtual Networks" and select it.
   - Click on "+ Create" to begin creating a virtual network.
   - Fill out the required information using the following values:
     - **Resource Group:** RG1
     - **Name:** app-vnet
     - **Region:** East US
     - **IPv4 Address Space:** 10.1.0.0/16
     - **Subnet Name:** frontend
     - **Subnet Address Range:** 10.1.0.0/24
     - **Subnet Name:** backend
     - **Subnet Address Range:** 10.1.1.0/24
   - Follow the same steps to create the "shared-services-vnet" virtual network with the following values:
     - **Resource Group:** RG1
     - **Name:** shared-services-vnet
     - **Region:** East US
     - **IPv4 Address Space:** 10.0.0.0/16
     - **Subnet Name:** frontend
     - **Subnet Address Range:** 10.0.0.0/24
   - Confirm the deployment of both virtual networks in the RG1 resource group.

2. **Setup Virtual Network Peering:**
   - In the Azure portal, navigate to the RG1 resource group and select the "app-vnet" virtual network.
   - Select "Peerings" from the context menu on the left-hand side.
   - Click on "+ Add" to create a new peering.
   - Fill out the form using the following values:
     - **This Virtual Network Peering Link Name:** app-vnet-to-sharedservices
     - **Remote Virtual Network Peering Link Name:** sharedservices-to-app-vnet
     - **Virtual Network:** shared-services-vnet
   - Leave all other settings as their defaults and select "Add" to create the virtual network peering.
   - Validate that the peering status is set to "Connected" after the configuration updates.

#### Exercise Instructions:
1. Ensure you have an Azure subscription with the Contributor RBAC role assigned.
2. Follow the provided step-by-step instructions to create virtual networks and subnets.
3. Configure virtual network peering as instructed.
4. Validate the peering status to ensure successful connection between virtual networks.

#### Next Steps:
Proceed to Task 2: Control the Network Traffic to and from the Web Application.