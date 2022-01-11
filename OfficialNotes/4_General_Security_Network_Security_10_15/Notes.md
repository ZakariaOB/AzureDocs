## Describe Azure security features 

### Describe basic features of Azure Security Center, including policy compliance, security alerts, secure score, and resource hygiene

- **Azure Security Center** is a monitoring service that provides visibility of your security posture across all of your services, both on Azure and on-premises. The term security posture refers to cybersecurity policies and controls, as well as how well you can predict, prevent, and respond to security threats.

   Security Center can:
    - Monitor security settings across on-premises and cloud workloads.
    - Automatically apply required security settings to new resources as they come online.
    - Provide security recommendations that are based on your current configurations, resources, and     - networks.
    - Continuously monitor your resources and perform automatic security assessments to identify potential     - vulnerabilities before those vulnerabilities can be exploited.
    - Use machine learning to detect and block malware from being installed on your virtual machines (VMs)     - and other resources. You can also use adaptive application controls to define rules that list allowed     - applications to ensure that only applications you allow can run.
    - Detect and analyze potential inbound attacks and investigate threats and any post-breach activity that     - might have occurred.
    - Provide just-in-time access control for network ports. Doing so reduces your attack surface by     - ensuring that the network only allows traffic that you require at the time that you need it to.

- **Azure Security and Compliance** Blueprints—easily create, deploy, and update compliant environments, including for certifications like ISO:27001, PCI DSS, and UK OFFICIAL. Azure Security Center—unify security management and enable advanced threat protection across hybrid cloud workloads.

- **Azure security alerts** Notification that a specific attack has been directed at an organization's information systems. Source(s): A brief, usually human-readable, technical notification regarding current vulnerabilities, exploits, and other security issues.

- **Azure Secure score** helps you prioritize and triage your response to security recommendations by assigning values to the recommendations that can most help

- **Azure security hygiene** Most prevalent recommendations and highest impact recommendations. Threat protection: Most prevalent alerts, subscriptions that have no security contact defined

### Azure Key Vault(Check an example with that)

    Azure Key Vault can help you:
     - Manage secrets You can use Key Vault to securely store and tightly control access to tokens,  passwords, certificates, API keys, and other secrets.
     - Manage encryption keys You can use Key Vault as a key management solution. Key Vault makes it easier  to create and control the encryption keys that are used to encrypt your data.
     - Manage SSL/TLS certificates Key Vault enables you to provision, manage, and deploy your public and  private Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates for both your Azure  resources and your internal resources.
     - Store secrets backed by hardware security modules (HSMs) These secrets and keys can be protected  either by software or by FIPS 140-2 Level 2 validated HSMs.


### Azure Sentinel 

It's now called Microsoft Sentinel. Microsoft Sentinel delivers intelligent security analytics and threat intelligence across the enterprise, providing a single solution for attack detection, threat visibility, proactive hunting, and threat response..

### Azure Dedicated Hosts

  - Gives you visibility into, and control over, the server infrastructure that's running your Azure VMs.
  - Helps address compliance requirements by deploying your workloads on an isolated server.
  - Lets you choose the number of processors, server capabilities, VM series, and VM sizes within the same host.


## Describe Azure network security

### Describe the concept of defense in depth

- The objective of defense in depth is to protect information and prevent it from being stolen by those who aren't authorized to access it.
A defense-in-depth strategy uses a series of mechanisms to slow the advance of an attack that aims at acquiring unauthorized access to data.
The below layers provide a guideline for you to help make security configuration decisions in all of the layers of your applications.

   - The physical security layer is the first line of defense to protect computing hardware in the    datacenter.
   - The identity and access layer controls access to infrastructure and change control.
   - The perimeter layer uses distributed denial of service (DDoS) protection to filter large-scale -    attacks before they can cause a denial of service for users.
   - The network layer limits communication between resources through segmentation and access controls.
   - The compute layer secures access to virtual machines.
   - The application layer helps ensure that applications are secure and free of security vulnerabilities.
   - The data layer controls access to business and customer data that you need to protect.


### Describe the functionality and usage of Network Security Groups (NSG)

- A network security group enables you to filter network traffic to and from Azure resources within an Azure virtual network. You can think of NSGs like an internal firewall. An NSG can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port, and protocol.

### Describe the functionality and usage of Azure Firewall

- A firewall is a network security device that monitors incoming and outgoing network traffic and decides whether to allow or block specific traffic based on a defined set of security rules. You can create firewall rules that specify ranges of IP addresses. Only clients granted IP addresses from within those ranges are allowed to access the destination server. Firewall rules can also include specific network protocol and port information.

- Azure Firewall provides a central location to create, enforce, and log application and network connectivity policies across subscriptions and virtual networks. Azure Firewall uses a static (unchanging) public IP address for your virtual network resources, which enables outside firewalls to identify traffic coming from your virtual network. The service is integrated with Azure Monitor to enable logging and analytics.

- Azure Firewall provides many features, including :
  - Built-in high availability.
  - Unrestricted cloud scalability.
  - Inbound and outbound filtering rules.
  - Inbound Destination Network Address Translation (DNAT) support.
  - Azure Monitor logging.

- Azure Application Gateway also provides a firewall that's called the web application firewall (WAF). WAF provides centralized, inbound protection for your web applications against common exploits and vulnerabilities. Azure Front Door and Azure Content Delivery Network also provide WAF services.

### Describe the functionality and usage of Azure DDoS protection

- A distributed denial of service attack attempts to overwhelm and exhaust an application's resources, making the application slow or unresponsive to legitimate users. DDoS attacks can target any resource that's publicly reachable through the internet, including websites.

- DDoS Protection identifies the attacker's attempt to overwhelm the network and blocks further traffic from them, ensuring that traffic never reaches Azure resources. Legitimate traffic from customers still flows into Azure without any interruption of service.

- DDoS Protection can also help you manage your cloud consumption. When you run on-premises, you have a fixed number of compute resources. But in the cloud, elastic computing means that you can automatically scale out your deployment to meet demand. A cleverly designed DDoS attack can cause you to increase your resource allocation, which incurs unneeded expense. DDoS Protection Standard helps ensure that the network load you process reflects customer usage. You can also receive credit for any costs accrued for scaled-out resources during a DDoS attack.
