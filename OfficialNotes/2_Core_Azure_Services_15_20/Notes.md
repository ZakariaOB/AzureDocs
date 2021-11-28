
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

