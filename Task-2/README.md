## Task 2: Control the Network Traffic to and from the Web Application

### Scenario
Your organization requires control of the network traffic to and from the web application. To further enhance the security of the web application, network security groups (NSG) and application security groups (ASG) can be configured. NSG is a security layer that filters network traffic to and from Azure resources, while ASG allows grouping of resources to be managed collectively. These security groups provide fine-grained control over the network traffic to and from the web application components.

#### What:
To enhance the security of the web application, we will control the network traffic using network security groups (NSGs) and application security groups (ASGs). NSGs act as a firewall, filtering traffic to and from Azure resources, while ASGs group resources to be managed collectively, providing fine-grained control over network traffic.

#### Why:
Controlling network traffic helps in preventing unauthorized access and securing the web application from potential threats. NSGs and ASGs allow administrators to define specific rules and policies to manage traffic effectively, ensuring the integrity and confidentiality of the application.

#### How:

1. **Create Application Security Group (ASG):**
   - Navigate to the Azure portal and search for "Application security group".
   - Select "+ Create" to create a new ASG.
   - Fill out the required information using the following values:
     - **Subscription:** Select your subscription
     - **Resource Group:** RG1
     - **Name:** app-backend-asg
     - **Region:** East US
   - Select "Review + create" and then "Create" to create the ASG.

2. **Create and Associate the Network Security Group (NSG):**
   - Search for "Network security group" in the Azure portal.
   - Click on "+ Create" to create a new NSG.
   - Provide the following information:
     - **Subscription:** Select your subscription
     - **Resource Group:** RG1
     - **Name:** app-vnet-nsg
     - **Region:** East US
   - Select "Review + create" and then "Create" to create the NSG.
   - Once created, associate the NSG with the subnet of the virtual network.
     - Navigate to the NSG settings and select "Subnets".
     - Associate the NSG with the "backend" subnet of the virtual network "app-vnet".

3. **Create Network Security Group Rules:**
   - Navigate to the NSG settings and select "Inbound security rules".
   - Click on "+ Add" to create a new inbound security rule.
   - Enter the following information:
     - **Source:** Any
     - **Source Port Ranges:** *
     - **Destination:** Application Security Group
     - **Destination Application Security Group:** app-backend-asg
     - **Service:** SSH
     - **Action:** Allow
     - **Priority:** 100
     - **Name:** AllowSSH
   - Select "Add" to create the rule.

4. **Associate Application Security Group to Network Interface:**
   - Navigate to the VM2 resource in the RG1 resource group.
   - Go to the networking tab of VM2 and select "+ Add application security groups" from the Application security groups section.
   - Choose "app-backend-asg" from the list of application security groups and select "Add".

#### Exercise Instructions:
1. Ensure you have an Azure subscription with the Contributor RBAC role assigned.
2. Follow the provided step-by-step instructions to create an ASG, NSG, and associate them accordingly.
3. Create NSG rules as instructed to control inbound traffic.
4. Associate the ASG to the network interface of VM2.
5. Validate that the configuration is applied correctly by verifying the network security and application security groups associated.

#### Next Steps:
Proceed to Task 3: Protect the Web Application from Malicious Traffic and Block Unauthorized Access.