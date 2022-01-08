
# Describe the core Azure architectural components

## Describe the benefits and usage of Regions and Region Pairs

### Regions

- A region is a geographical area on the planet that contains at least one but potentially multiple datacenters that are nearby and networked together with a low-latency network. Azure intelligently assigns and controls the resources within each region to ensure workloads are appropriately balanced.

- Azure has more global regions than any other cloud provider. These regions give you the flexibility to bring applications closer to your users no matter where they are. Global regions provide better scalability and redundancy. They also preserve data residency for your services.

### Region Pairs

- Each Azure region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away. This approach allows for the replication of resources (such as VM storage) across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect both regions at once. If a region in a pair was affected by a natural disaster, for instance, services would automatically failover to the other region in its region pair.

## Describe the benefits and usage of Avaibility zones

- Availability zones are physically separate datacenters within an Azure region. Each availability zone is made up of one or more datacenters equipped with independent power, cooling, and networking. An availability zone is set up to be an isolation boundary. If one zone goes down, the other continues working. Availability zones are connected through high-speed, private fiber-optic networks.

## Usage of avaibility zones

- You can use availability zones to run mission-critical applications and build high-availability into    your application architecture by co-locating your compute, storage, networking, and data resources     within a zone and replicating in other zones. Keep in mind that there could be a cost to duplicating    your services and transferring data between zones.
- Availability zones are primarily for VMs, managed disks, load balancers, and SQL databases. Azure   services that support availability zones fall into three categories:
- Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
- Zone-redundant services: The platform replicates automatically across zones (for example,   - zone-redundant storage, SQL Database).
- Non-regional services: Services are always available from Azure geographies and are resilient to    zone-wide outages as well as region-wide outages.


# Describe core resources available in Azure

## Virtual machines

- You can create and provision a VM in minutes when you select a preconfigured VM image. Selecting an image is one of the most important decisions you'll make when you create a VM. An image is a template used to create a VM. These templates already include an OS and often other software, like development tools or web hosting environments

### When to use VMs

- During testing and development. VMs provide a quick and easy way to create different OS and application configurations. Test and development personnel can then easily delete the VMs when they no longer need them.
- When running applications in the cloud. The ability to run certain applications in the public cloud as opposed to creating a traditional infrastructure to run them can provide substantial economic benefits. For example, an application might need to handle fluctuations in demand. Shutting down VMs when you don't need them or quickly starting them up to meet a sudden increase in demand means you pay only for the resources you use.
- When extending your datacenter to the cloud. An organization can extend the capabilities of its own on-premises network by creating a virtual network in Azure and adding VMs to that virtual network. Applications like SharePoint can then run on an Azure VM instead of running locally. This arrangement makes it easier or less expensive to deploy than in an on-premises environment.
- During disaster recovery. As with running certain types of applications in the cloud and extending an on-premises network to the cloud, you can get significant cost savings by using an IaaS-based approach to disaster recovery. If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them down when the primary datacenter becomes operational again.

### VMs Scale Sets

- Virtual machine scale sets let you create and manage a group of identical, load-balanced VMs. Imagine you're running a website that enables scientists to upload astronomy images that need to be processed. If you duplicated the VM, you'd normally need to configure an additional service to route requests between multiple instances of the website. Virtual machine scale sets could do that work for you.

- Scale sets allow you to centrally manage, configure, and update a large number of VMs in minutes to provide highly available applications. The number of VM instances can automatically increase or decrease in response to demand or a defined schedule. With virtual machine scale sets, you can build large-scale services for areas such as compute, big data, and container workloads.

## Azure App Service

- App Service enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure. It offers automatic scaling and high availability. App Service supports Windows and Linux and enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.
- This platform as a service (PaaS) environment allows you to focus on the website and API logic while Azure handles the infrastructure to run and scale your web applications.

## Azure container instances

- Difference between a container and a VM : a VM virtualize the hardware but a container virtualize the OS .
- Azure Container Instances offers the fastest and simplest way to run a container in Azure without having to manage any virtual machines or adopt any additional services. It's a platform as a service (PaaS) offering that allows you to upload your containers, which it runs for you.

## Azure Kubernetes Service

- The task of automating, managing, and interacting with a large number of containers is known as orchestration. Azure Kubernetes Service is a complete orchestration service for containers with distributed architectures and large volumes of containers.

## Benefits of containers in your solutions

- Containers are often used to create solutions by using a microservice architecture. This architecture is where you break solutions into smaller, independent pieces. For example, you might split a website into a container hosting your front end, another hosting your back end, and a third for storage. This split allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently.

- Imagine your website back-end has reached capacity but the front end and storage aren't being stressed. You could:
    - Scale the back end separately to improve performance.
    - Decide to use a different storage service.
    - Replace the storage container without affecting the rest of the application.

## Azure Virtual Desktop 

- It's a desktop and application virtualization service that runs on the cloud. It enables your users to use a cloud-hosted version of Windows from any location. Azure Virtual Desktop works across devices like Windows, Mac, iOS, Android, and Linux. It works with apps that you can use to access remote desktops and apps. You can also use most modern browsers to access Azure Virtual Desktop-hosted experiences.

## Azure virtual Networks

- Azure virtual networks enable Azure resources, such as VMs, web apps, and databases, to  communicate with each other, with users on the internet, and with your on-premises client computers. You can think of an Azure network as a set of resources that links other Azure resources.

  Azure virtual networks provide the following key networking capabilities :
      
    - Isolation and segmentation
    - Internet communications
    - Communicate between Azure resources
    - Communicate with on-premises resources
    - Route network traffic
    - Filter network traffic
    - Connect virtual networks

## VPN gatways

- Gateway : A computer that sits between different networks or applications. The gateway converts information, data or other communications from one protocol or format to another. A router may perform some of the functions of a gateway. An Internet gateway can transfer communications between an enterprise network and the Internet.

- A VPN gateway is a type of networking device that connects two or more devices or networks together in a VPN infrastructure.

- It is designed to bridge the connection or communication between two or more remote sites, networks or devices and/or to connect multiple VPNs together.

- A VPN gateway can be a router, server, firewall or similar device with internetworking and data transmission capabilities. However, in most cases, a VPN gateway is a physical router device.

- The VPN gateway is generally installed on the core VPN site or infrastructure. The VPN gateway is configured to pass, block or route VPN traffic. It provides core VPN-specific networking services such as IP address assignment and management, dynamic and static routing and the maintenance of routing tables.

- VPNs use an encrypted tunnel within another network. They're typically deployed to connect two or more trusted private networks to one another over an untrusted network (typically the public internet). Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks.

- A VPN gateway is a type of virtual network gateway. Azure VPN Gateway instances are deployed in Azure Virtual Network instances and enable the following connectivity:
   - Connect on-premises datacenters to virtual networks through a site-to-site connection.
   - Connect individual devices to virtual networks through a point-to-site connection.
   - Connect virtual networks to other virtual networks through a network-to-network connection.

- VNet peering enables you to seamlessly connect Azure virtual networks. Once peered, the VNets appear as one, for connectivity purposes.

- ExpressRoute provides direct connectivity to Azure cloud services and connecting Microsoft’s global network. All transferred data is not encrypted, and do not go over the public Internet.
VPN Gateway provides secured connectivity to Azure cloud services over public Internet. All transferred data is encrypted in a private tunnel as it crosses the internet.

## Azure storage

- **Disk Storage** provides disks for Azure virtual machines. Applications and other services can access and use these disks as needed, similar to how they would in on-premises scenarios. Disk Storage allows data to be persistently stored and accessed from an attached virtual hard disk.

- **Disks** come in many different sizes and performance levels, from solid-state drives (SSDs) to traditional spinning hard disk drives (HDDs), with varying performance tiers. You can use standard SSD and HDD disks for less critical workloads, premium SSD disks for mission-critical production applications, and ultra disks for data-intensive workloads such as SAP HANA, top tier databases, and transaction-heavy workloads. Azure has consistently delivered enterprise-grade durability for infrastructure as a service (Iaas) disks, with an industry-leading ZERO% annualized failure rate.

- **Azure Blob Storage** is an object storage solution for the cloud. It can store massive amounts of data, such as text or binary data. Azure Blob Storage is unstructured, meaning that there are no restrictions on the kinds of data it can hold. Blob Storage can manage thousands of simultaneous uploads, massive amounts of video data, constantly growing log files, and can be reached from anywhere with an internet connection.

- **Blob** Storage is ideal for:
    - Serving images or documents directly to a browser.
    - Storing files for distributed access.
    - Streaming video and audio.
    - Storing data for backup and restore, disaster recovery, and archiving.
    - Storing data for analysis by an on-premises or Azure-hosted service.
    - Storing up to 8 TB of data for virtual machines.

- **Containers** You store blobs in containers, which helps you organize your blobs depending on your business needs.

- **Stack overflow** 
   
   Which you choose is entirely up to you, but objectively:

  - Azure File Storage may be mounted as an SMB volume (so that all instances of your app can work with   - it). Note: This is not something readily supported with Web Apps currently - you'd only be able to  - write to the file share via API, not via attached disk. Azure File Storage volumes support up to 5TB   - each, and throughput is max. 60MB/sec across the share. It's backed by Azure blob storage (so, just   - as durable as blobs).
  - Azure Disks are again blob-backed (page blobs), up to 1TB each. Each disks is mountable to a single   - VM. Throughput is higher than File Storage (60/Sec per blob). Cannot be shared across VMs without   - your own solution to sync data. Once mounted and formatted, accessible just like any other local  - file (e.g. no modifications to your app)
  - Azure blobs: Up to 500TB per storage account, each block blob can be up to 200GB 4.77TB. Access via   - REST API/SDK, not mountable as a disk / drive. Without modifying your app, you'd need to make sure  - blob contents were copied to local disk to perform operations on the content (you can't just open a  - blob as a file and modify it).

- **Storage access tier**
  
  - Azure Storage offers different access tiers for your blob storage, helping you store object data in the most cost-effective manner. The available access tiers include:

  - ***Hot access tier*** : Optimized for storing data that is accessed frequently (for example, images for  your website).
  - ***Cool access tier*** : Optimized for data that is infrequently accessed and stored for at least 30 days  (for example, invoices for your customers).
  - ***Archive access tier*** : Appropriate for data that is rarely accessed and stored for at least 180 days,   with flexible latency requirements (for example, long-term backups).
  The following considerations apply to the different access tiers:

  - Only the hot and cool access tiers can be set at the account level. The archive access tier isn't   available at the account level.
  Hot, cool, and archive tiers can be set at the blob level, during upload or after upload.
  Data in the cool access tier can tolerate slightly lower availability, but still requires high  durability, retrieval latency, and throughput characteristics similar to hot data. For cool data, a  slightly lower availability service-level agreement (SLA) and higher access costs compared to hot  data are acceptable trade-offs for lower storage costs.
  Archive storage stores data offline and offers the lowest storage costs, but also the highest costs   to rehydrate and access data.


- **Azure Database**

- *Azure Cosmos DB* is a globally distributed, multi-model database service. You can elastically and independently scale throughput and storage across any number of Azure regions worldwide. You can take advantage of fast, single-digit-millisecond data access by using any one of several popular APIs. Azure Cosmos DB provides comprehensive service level agreements for throughput, latency, availability, and consistency guarantees.

- *Azure Cosmos DB* supports schema-less data, which lets you build highly responsive and "Always On" applications to support constantly changing data. You can use this feature to store data that's updated and maintained by users around the world.

- *Azure SQL Database* is a platform as a service (PaaS) database engine. It handles most of the database management functions, such as upgrading, patching, backups, and monitoring, without user involvement. SQL Database provides 99.99 percent availability. PaaS capabilities that are built into SQL Database enable you to focus on the domain-specific database administration and optimization activities that are critical for your business. SQL Database is a fully managed service that has built-in high availability, backups, and other common maintenance operations. Microsoft handles all updates to the SQL and operating system code. You don't have to manage the underlying infrastructure.

- *Azure Database for MySQL* is a relational database service in the cloud, and it's based on the MySQL Community Edition database engine, versions 5.6, 5.7, and 8.0. With it, you have a 99.99 percent availability service level agreement from Azure, powered by a global network of Microsoft-managed datacenters. This helps keep your app running 24/7. With every Azure Database for MySQL server, you take advantage of built-in security, fault tolerance, and data protection that you would otherwise have to buy or design, build, and manage. With Azure Database for MySQL, you can use point-in-time restore to recover a server to an earlier state, as far back as 35 days.

- *Azure Database for PostgreSQL* is a relational database service in the cloud. The server software is based on the community version of the open-source PostgreSQL database engine. Your familiarity with tools and expertise with PostgreSQL is applicable when you're using Azure Database for PostgreSQL.

- *Azure SQL Managed Instance* is a scalable cloud data service that provides the broadest SQL Server database engine compatibility with all the benefits of a fully managed platform as a service. Depending on your scenario, Azure SQL Managed Instance might offer more options for your database needs.

- *Azure SQL Database and Azure SQL Managed Instance* offer many of the same features; however, Azure SQL Managed Instance provides several options that might not be available to Azure SQL Database. For example, Tailwind Traders currently uses several on-premises servers running SQL Server, and they would like to migrate their existing databases to a SQL database running in the cloud. However, several of their databases use Cyrillic characters for collation. In this scenario, Tailwind Traders should migrate their databases to an Azure SQL Managed Instance, since Azure SQL Database only uses the default SQL_Latin1_General_CP1_CI_AS server collation.


- **Azure Marketplace**

- Azure Marketplace is an online store that contains thousands of IT software applications and services built by industry-leading technology companies. In Azure Marketplace you can find, try, buy, and deploy the software and services you need to build new solutions and manage your cloud infrastructure

