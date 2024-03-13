## Task 5: Record and Resolve Domain Names Internally

#### Scenario:
In your organization's virtual networks, it's essential to record and resolve domain names internally for seamless communication between various workloads. Azure Private DNS offers a reliable and secure DNS service that allows you to manage and resolve domain names within a virtual network without the need for a custom DNS solution. By configuring a private DNS zone and linking it to the virtual network, you enable virtual machines to use domain names for internal communication, enhancing network efficiency and management.

#### What:
This task focuses on creating and configuring a private DNS zone using Azure Private DNS. By establishing a private DNS zone, you can define custom domain names and DNS records for internal resources within the virtual network. Additionally, configuring DNS settings on the virtual network ensures that domain names are resolved internally, providing seamless communication between virtual machines using domain names instead of IP addresses.

#### Why:
Recording and resolving domain names internally streamlines network management and simplifies communication between virtual machines within the virtual network. Azure Private DNS offers a centralized and reliable DNS service, eliminating the need for complex custom DNS solutions and reducing administrative overhead. By leveraging private DNS zones and virtual network links, you can ensure efficient and secure resolution of domain names for internal resources, enhancing overall network performance and reliability.

#### How:
1. **Create a Private DNS Zone:**
   - Access the Azure portal and navigate to "Private DNS zones".
   - Click on "+ Create" to create a new private DNS zone.
   - Provide the necessary details, including subscription, resource group, name, and region for the private DNS zone.
   - Review the configuration and select "Create" to deploy the private DNS zone.

2. **Create a Virtual Network Link to the Private DNS Zone:**
   - Within the created private DNS zone, select the option to add a virtual network link.
   - Specify the virtual network and enable auto-registration for seamless integration with the virtual network.
   - Confirm the settings to establish the virtual network link.

3. **Create a DNS Record Set:**
   - Navigate to the private DNS zone created earlier.
   - Create a new record set within the zone to define custom DNS records for internal resources.
   - Specify the name, type, TTL (Time-to-Live), and IP address for the DNS record set.
   - Save the configuration to add the DNS record set to the private DNS zone.

#### Exercise Instructions:
1. Access the Azure portal and follow the provided instructions to create a private DNS zone.
2. Link the private DNS zone to the virtual network by adding a virtual network link.
3. Create a DNS record set within the private DNS zone to define custom DNS records for internal resources.
4. Verify that the private DNS zone contains the configured record set for internal domain resolution.

#### Next Steps:
Validate Secure Access to Workloads.