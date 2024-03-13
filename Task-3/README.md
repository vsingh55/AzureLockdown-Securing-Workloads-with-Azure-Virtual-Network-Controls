## Task 3: Protect the Web Application from Malicious Traffic and Block Unauthorized Access

#### Scenario:
Your organization's web application is a critical asset that requires robust protection from malicious traffic and unauthorized access. With the increasing sophistication of cyber threats, it's essential to implement advanced security measures to safeguard the application's integrity and availability. By configuring Azure Firewall and defining strict firewall policies, you can fortify the defense mechanisms of the web application, ensuring that only legitimate traffic is allowed and potential security vulnerabilities are mitigated effectively.

#### What:
To bolster the security posture of the web application, Azure Firewall will be deployed along with a comprehensive firewall policy. This setup will enable the enforcement of stringent rules for filtering network traffic, both at the application and network level. By implementing Azure Firewall Policy, you can define granular controls over inbound and outbound traffic, facilitating the detection and prevention of malicious activities.

#### Why:
Protecting the web application from malicious traffic and unauthorized access is paramount to safeguarding sensitive data, maintaining compliance, and upholding the organization's reputation. Azure Firewall offers advanced threat protection capabilities and a centralized management interface for configuring and monitoring firewall rules. By creating a robust firewall policy, you can establish a defense-in-depth strategy, complementing existing security measures and mitigating potential risks effectively.

#### How:
1. **Create Azure Firewall Subnet in the Existing Virtual Network:**
   - Navigate to the Azure portal and access the "Virtual networks" section.
   - Select the "app-vnet" virtual network.
   - Define a new subnet named "AzureFirewallSubnet" with the address range 10.1.63.0/24 to host the Azure Firewall.

2. **Create an Azure Firewall:**
   - Search for "Firewall" in the Azure portal and initiate the creation of a new Azure Firewall.
   - Specify the required parameters such as resource group, name, region, and virtual network.
   - Choose the appropriate Firewall SKU and management options, opting to use a Firewall Policy to manage the firewall configuration.

3. **Update the Firewall Policy:**
   - Navigate to the "Firewall Policy" section in the Azure portal.
   - Select the existing firewall policy ("fw-policy").
   - Configure application rules to allow or deny specific types of traffic based on defined criteria, such as source IP addresses, destination FQDNs, and protocols.
   - Define network rules to control traffic flow based on source and destination IP addresses, protocols, and ports.

4. **Verify Firewall and Firewall Policy Provisioning:**
   - Confirm that the Azure Firewall and Firewall Policy have been provisioned successfully by checking their provisioning states in the Azure portal.

#### Exercise Instructions:
1. Ensure you have an Azure subscription with the Contributor RBAC role assigned.
2. Follow the provided step-by-step instructions to create an Azure Firewall and configure a firewall policy.
3. Update the firewall policy with application and network rules as specified in the scenario.
4. Verify the provisioning state of the Azure Firewall and firewall policy to ensure successful deployment.

#### Next Steps:
Proceed to Task 4: Route Traffic to the Firewall.