Implemented and Managed Virtual Networking

Designed a hybrid networking environment where on-premises networks connected securely to Azure resources using Azure's networking capabilities, ensuring secure data transition and effective resource access controls.

- **Azure Virtual Network Setup:**

    Provisioned an Azure Virtual Network (VNet) in the chosen region.
    Created multiple subnets within this VNet to segregate resources effectively (e.g., WebApp Subnet, Database Subnet, Admin Subnet).

- **On-Premises Network Simulation:**

    For the sake of this project, used another VNet to simulate the on-premises environment. This was in another Azure region or the same region based on preference.

- **Secure Connectivity:**

    Implemented Azure VPN Gateway to create a site-to-site VPN connection between the simulated on-premises environment (VNet) and the main Azure VNet.
    Verified the connection and ensured resources from one VNet could communicate with another, effectively simulating a hybrid environment.

- **Resource Deployment:**

    Deployed test resources (like VMs) in each subnet of the main Azure VNet. For instance, deployed a web server VM in the WebApp Subnet, a database in the Database Subnet, etc.

- **Network Access Control:**

    Used Network Security Groups (NSGs) to define inbound and outbound access rules for each subnet, ensuring that only valid traffic was allowed. For instance, only allowed HTTP/HTTPS traffic to the WebApp Subnet.

- **Secure Administrative Access:**

    Implemented Azure Bastion for secure and seamless RDP and SSH access to virtual machines, ensuring VMs were not exposed to the public internet.

- **Private Access to Azure PaaS Services:**

    Used Azure Private Link to access Azure PaaS services (like Azure SQL Database) over a private endpoint within the VNet, ensuring data didn't traverse over the public internet.

- **DNS and Load Balancing:**

    Configured Azure DNS to have custom domain names for resources.
    Implemented Azure Load Balancer to distribute traffic across VMs in the WebApp Subnet.

- **Performance and Security Testing:**

    Simulated various network scenarios to test performance, such as data transition between on-premises and Azure.
    Attempted to access resources from outside the permitted paths to validate the security configurations in place.

- **Monitoring and Auditing:**

    Enabled monitoring and diagnostics on the VPN Gateway, NSGs, and other network resources to gain insights into network operations.
    Reviewed logs and set up alerts for any suspicious activities.
