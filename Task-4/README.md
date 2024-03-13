### Task 4: Route Traffic to the Firewall

#### Scenario:
With the firewall and associated policies in place, the next step is to route network traffic to the firewall subnet. By configuring route tables, you can direct network traffic to the firewall, allowing it to filter and inspect the traffic according to the defined security requirements. Route tables provide control over the routing of network traffic, ensuring that all traffic passes through the firewall for enhanced security and compliance.

#### What:
In this task, we will create and configure a route table to manage the routing of network traffic within the virtual network. The route table will be linked to the subnets containing the web application components, ensuring that all inbound and outbound traffic is subject to the firewall rules enforced by the Azure Firewall. By associating the route table with the appropriate subnets, we establish a path for network traffic to reach the firewall for inspection and filtering.

#### Why:
Routing traffic through the firewall is essential for enforcing security policies and protecting the web application from malicious activities. By directing all traffic through the firewall subnet, we ensure that every packet is inspected and filtered according to the defined rules, mitigating potential security risks and unauthorized access attempts. Route tables provide the necessary infrastructure for managing network routing within the Azure environment, enabling seamless integration with the firewall for enhanced security measures.

#### How:
1. **Create a Route Table:**
   - Record the private and public IP addresses of the Azure Firewall from the Firewall overview.
   - Navigate to the Azure portal and search for "Route tables".
   - Click on "+ Create" to create a new route table.
   - Provide the required information, including subscription, resource group, region, and name for the route table.
   - Review the configuration and select "Create" to deploy the route table.

2. **Associate the Route Table with Subnets:**
   - Navigate to the created route table in the Azure portal.
   - Associate the route table with the subnets containing the web application components.
   - Repeat the association process for all relevant subnets within the virtual network.

3. **Create a Route in the Route Table:**
   - Within the route table settings, navigate to the "Routes" section.
   - Click on "+ Add" to create a new route.
   - Specify the route name and destination type as "IP addresses".
   - Enter the destination IP addresses/CIDR range as "0.0.0.0/0" to represent all outbound traffic.
   - Set the next hop type as "Virtual appliance" and specify the private IP address of the Azure Firewall recorded earlier.
   - Save the route to add it to the route table.

#### Exercise Instructions:
1. Record the private and public IP addresses of the Azure Firewall from the Firewall overview.
2. Create a new route table in the Azure portal with the specified configuration.
3. Associate the route table with the subnets containing the web application components.
4. Create a route in the route table to route traffic to the Azure Firewall subnet for inspection and filtering.

#### Next Steps:
Proceed to Task 5: Record and Resolve Domain Names Internally.