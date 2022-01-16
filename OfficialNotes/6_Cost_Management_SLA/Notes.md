# Describe methods for planning and managing costs

- As you move to the cloud, you might ask:
   - How much will it cost?
   - What guarantees does Azure provide around uptime and connectivity?
   - How do preview services impact my production applications?

## Identify factors that can affect costs (resource types, services, locations, ingress and egress traffic)

- **What factors affect cost?**
  - *Resource type*
     A number of factors influence the cost of Azure resources. They depend on the type of  resource or how you customize it.
     For example, with a storage account you specify a type (such as block blob storage or table  storage), a performance tier (standard or premium), and an access tier (hot, cool, or  archive). These selections present different costs.
  - *Usage meters*
      When you provision a resource, Azure creates meters to track usage of that resource. Azure uses these meters to generate a usage record that's later used to help calculate your bill.
      Think of usage meters similar to how you use electricity or water in your home. You might pay a       base price each month for electricity or water service, but your final bill is based on the       total amount that you consumed.
      Let's look at a single VM as an example. The following kinds of meters are relevant to tracking its usage:
        - Overall CPU time.
        - Time spent with a public IP address.
        - Incoming (ingress) and outgoing (egress) network traffic in and out of the VM.
        - Disk size and amount of disk read and disk write operations.
      Each meter tracks a specific type of usage. For example, a meter might track bandwidth usage (ingress or egress network traffic in bits per second), number of operations, or its size (storage capacity in bytes).
      The usage that a meter tracks correlates to a quantity of billable units. Those units are charged to your account for each billing period. The rate per billable unit depends on the resource type you're using.
   - *Resource usage*
       In Azure, you're always charged based on what you use. As an example, let's look at how this billing applies to deallocating a VM.
       In Azure, you can delete or deallocate a VM. Deleting a VM means that you no longer need it. The VM is removed from your subscription, and then it's prepared for another customer.
       Deallocating a VM means that the VM is no longer running. But the associated hard disks and data        are still kept in Azure. The VM isn't assigned to a CPU or network in Azure's datacenter, so it doesn't generate the costs associated with compute time or the VM's IP address. Because the        disks and data are still stored, and the resource is present in your Azure subscription, you're        still billed for disk storage.
       Deallocating a VM when you don't plan on using it for some time is just one way to minimize        costs. For example, you might deallocate the VMs you use for testing purposes on weekends when        your testing team isn't using them. You'll learn more about ways to minimize cost later in this module.
    - *Azure subscription types*
       Some Azure subscription types also include usage allowances, which affect costs.
       For example, an Azure free trial subscription provides access to a number of Azure  products that       are free for 12 months. It also includes credit to spend within your  first 30 days of sign-up.       And you get access to more than 25 products that are  always free (based on resource and region       availability).
    - *Azure MarketPlace*
       You can also purchase Azure-based solutions and services from third-party vendors through Azure Marketplace. Examples include managed network firewall appliances or connectors to third-party backup services. Billing structures are set by the vendor.

- **The TCO Calculator Total cost of ownership**  helps you estimate the cost savings of operating your solution on Azure over time, instead of in your on-premises datacenter.

- Working with the TCO Calculator involves three steps:
   - Define your workloads.
   - Adjust assumptions.
   - View the report.

- **Does location or network traffic affect cost?**
  *Location*
    Azure infrastructure is distributed globally, which enables you to deploy your services centrally or provision your services closest to where your customers use them.

    Different regions can have different associated prices. Because geographic regions can impact where your network traffic flows, network traffic is a cost influence to consider as well.

    For example, say Tailwind Traders decides to provision its Azure resources in the Azure regions that offer the lowest prices. That decision would save the company some money. But, if they need to transfer data between those regions, or if their users are located in different parts of the world, any potential savings could be offset by the additional network usage costs of transferring data between those resources.

## Price calculator

- As you've learned, an accurate cost estimate takes all of the preceding factors into account. Fortunately, the Azure Pricing calculator helps you with that process.
The Pricing calculator displays Azure products in categories. You add these categories to your estimate and configure according to your specific requirements. You then receive a consolidated estimated price, with a detailed breakdown of the costs associated with each resource you added to your solution. You can export or share that estimate or save it for later. You can load a saved estimate and modify it to match updated requirements.
You also can access pricing details, product details, and documentation for each product from within the Pricing calculator.


## Price calculator vs TCO Calculator

They are two very different tools. The Azure Calculator is meant to get pricing when you know exactly what you need in Azure, or want to look up pricing for the resources you know about. TCO Calculator is meant when you want to estimate how much it would cost to move your resources from on-premises to Azure, by inputting what you are currently using, and letting it convert that into Azure equivalence.

## Describe the functionality and usage of Azure Cost Management

- Understand estimated costs before you deploy
  To help you plan your solution on Azure, carefully consider the products, services, and resources you need. Read the relevant documentation to understand how each of your choices is metered and billed.

- Use **Azure Advisor** to monitor your usage
  Ideally, you want your provisioned resources to match your actual usage.
  Azure Advisor identifies unused or underutilized resources and recommends unused resources that    you can remove. This information helps you configure your resources to match your actual    workload.

- Use spending limits to restrict your spending
  If you have a free trial or a credit-based Azure subscription, you can use spending limits to prevent accidental overrun.
  For example, when you spend all the credit included with your Azure free account, Azure   resources that you deployed are removed from production and your Azure virtual machines (VMs)   are stopped and deallocated. The data in your storage accounts is available as read-only. At   this point, you can upgrade your free trial subscription to a pay-as-you-go subscription.

- Use Azure Reservations to prepay
  Azure Reservations offers discounted prices on certain Azure services. Azure Reservations can save you up to 72 percent as compared to pay-as-you-go prices. To receive a discount, you reserve services and resources by paying in advance.
  For example, you can prepay for one year or three years of use of VMs, database compute   capacity, database throughput, and other Azure resources.

- Choose low-cost locations and regions
  The cost of Azure products, services, and resources can vary across locations and regions. If   possible, you should use them in those locations and regions where they cost less.

- Research available cost-saving offers
  Keep up to date with the latest Azure customer and subscription offers, and switch to offers   that provide the greatest cost-saving benefit.

- Use Azure Cost Management + Billing to control spending
  Azure Cost Management + Billing is a free service that helps you understand your Azure bill,   manage your account and subscriptions, monitor and control Azure spending, and optimize resource   use.

- Apply tags to identify cost owners
  Tags help you manage costs associated with the different groups of Azure products and resources.   You can apply tags to groups of Azure resources to organize billing data.

- Resize underutilized virtual machines
  A common recommendation that you'll find from Azure Cost Management + Billing and Azure Advisor   is to resize or shut down VMs that are underutilized or idle.

- Delete unused resources
  This recommendation might sound obvious, but if you aren't using a resource, you should shut it   down. It's not uncommon to find nonproduction or proof-of-concept systems that are no longer   needed following the completion of a project.

- Migrate from IaaS to PaaS services
  As you move your workloads to the cloud, a natural evolution is to start with infrastructure as   a service (IaaS) services because they map more directly to concepts and operations you're   already familiar with.

- Save on licensing costs
  Licensing is another area that can dramatically impact your cloud spending. Let's look at some   ways you can reduce your licensing costs.
    - Choose cost-effective operating systems
        Many Azure services provide a choice of running on Windows or Linux. In some cases, the    cost      depends on which you choose. When you have a choice, and your application doesn't    depend on the      underlying operating system, it's useful to compare pricing to see    whether you can save money.
    - Use Azure Hybrid Benefit to repurpose software licenses on Azure
        If you've purchased licenses for Windows Server or SQL Server, and your licenses are covered by Software Assurance, you might be able to repurpose those licenses on VMs on Azure.
        Some of the details vary between Windows Server or SQL Server. We'll provide resources at the         end of this module where you can learn more.


## Describe Azure Service Level Agreements (SLAs) and service lifecycles

### Describe the purpose of an Azure Service Level Agreement (SLA)

- A **Service-level agreement (SLA)** is a formal agreement between a service company and the customer. For Azure, this agreement defines the performance standards that Microsoft commits to for you, the customer.
In this part, you'll learn more about Azure SLAs, including why SLAs are important, where you can find the SLA for a specific Azure service, and what you'll find in a typical SLA.

- **Why are SLAs important ?**
Understanding the SLA for each Azure service you use helps you understand what guarantees you   can expect.
When you build applications on Azure, the availability of the services that you use affect your   application's performance. Understanding the SLAs involved can help you establish the SLA you   set with your customers.
Later in this module, you'll learn about some strategies you can use when an Azure SLA doesn't   meet your needs.

- **How do percentages relate to total downtime ?**
Downtime refers to the time duration that the service is unavailable.
The difference between 99.9 percent and 99.99 percent might seem minor, but it's important to understand what these numbers mean in terms of total downtime.
These amounts are cumulative, which means that the duration of multiple different service outages would be combined, or added together.

- **What are service credits?**
  A service credit is the percentage of the fees you paid that are credited back to you according to the claim approval process.

  An SLA describes how Microsoft responds when an Azure service fails to perform to its   specification. For example, you might receive a discount on your Azure bill as compensation when   a service fails to perform according to its SLA.
  
  Credits typically increase as uptime decreases. Here's how credits are applied for Azure   Database for MySQL according to uptime:
  
  WHAT ARE SERVICE CREDITS?
  Monthly uptime percentage	Service credit percentage
  < 99.99	10
  < 99	25
  < 95	100

- **What's the SLA for free services?**
  Free products typically don't have an SLA.
  For example, many Azure services provide a free or shared tier that provides more limited   functionality. Services like Azure Advisor are always free. The SLA for Azure Advisor states   that because it's free, it doesn't have a financially backed SLA.

- **How do I know when there's an outage?**
Azure status provides a global view of the health of Azure services and regions. If you suspect there's an outage, this is often a good place to start your investigation.
Azure status provides an RSS feed of changes to the health of Azure services that you can subscribe to. You can connect this feed to communication software such as Microsoft Teams or Slack.

- **How can I request a service credit from Microsoft?**
Typically, you need to file a claim with Microsoft to receive a service credit. If you purchase Azure services from a Cloud Solution Provider (CSP) partner, your CSP typically manages the claims process.
Each SLA specifies the timeline by which you must submit your claim and when Microsoft processes your claim. For many services, you must submit your claim by the end of the calendar month following the month in which the incident occurred.


## Identify actions that can impact an SLA (i.e. Availability Zones) 

- To ensure high availability, you might plan for your application to have duplicate components across several regions, known as redundancy. Conversely, to minimize costs during non-critical periods, you might run your application only in a single region. Tailwind Traders might consider this if there's a trend that the special order rates are much higher during certain months or seasons.
To achieve maximum availability in your application, add redundancy to every single part of the application. This redundancy includes the application itself, as well as the underlying services and infrastructure. Be aware, however, that doing so can be difficult and expensive, and often results in solutions that are more complex than they need to be.
Consider how critical high availability is to your requirements before you add redundancy. There may be simpler ways to meet your application SLA.

## Very high performance is difficult to achieve

- Performance targets above 99.99 percent are very difficult to achieve. An SLA of 99.99 percent means 1 minute of downtime per week. It's difficult for humans to respond to failures quickly enough to meet SLA performance targets above 99.99 percent. Instead, your application must be able to self-diagnose and self-heal during an outage.


## What is the service lifecycle?

- The service lifecycle defines how every Azure service is released for public use.
  Every Azure service starts in the development phase. In this phase, the Azure team collects and   defines its requirements, and begins to build the service.
  
  Next, the service is released to the public preview phase. During this phase, the public can   access and experiment with it and provide real-world feedback. Your feedback helps Microsoft   improve services. More importantly, providing feedback gives you the opportunity to request new   or different capabilities so that services better meet your needs.
  
  After a new Azure service has been validated and tested, it's released to all customers as a   production-ready service. This is known as general availability (GA).