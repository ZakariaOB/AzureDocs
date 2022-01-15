# Describe core Azure identity services

## Explain the difference between authentication and authorization

- **Authentication** is the process of establishing the identity of a person or service that wants to access a resource. It involves the act of challenging a party for legitimate credentials and provides the basis for creating a security principal for identity and access control. It establishes whether the user is who they say they are.

- **Authentication** establishes the user's identity, but authorization is the process of establishing what level of access an authenticated person or service has. It specifies what data they're allowed to access and what they can do with it.

## Define Azure Active Directory 

- **For on-premises environments** : Active Directory running on Windows Server provides an identity and access management service that's managed by your own organization. Azure AD is Microsoft's cloud-based identity and access management service. With Azure AD, you control the identity accounts, but Microsoft ensures that the service is available globally. If you've worked with Active Directory, Azure AD will be familiar to you.

## Azure AD is for :

- ***IT administrators***

    Administrators can use Azure AD to control access to applications and resources based on their business requirements.

- ***App developers***

    Developers can use Azure AD to provide a standards-based approach for adding functionality to applications that they build, such as adding SSO functionality to an app or enabling an app to work with a user's existing credentials.

- ***Users***

    Users can manage their identities. For example, self-service password reset enables users to change or reset their password with no involvement from an IT administrator or help desk.

- ***Online service subscribers***

    Microsoft 365, Microsoft Office 365, Azure, and Microsoft Dynamics CRM Online subscribers are already using Azure AD.

    A tenant is a representation of an organization. A tenant is typically separated from other tenants and has its own identity.

    Each Microsoft 365, Office 365, Azure, and Dynamics CRM Online tenant is automatically an Azure AD tenant.



## Azure AD provides services such as:

- **Authentication**

   This includes verifying identity to access applications and resources. It also includes    providing functionality such as self-service password reset, multifactor authentication, a    custom list of banned passwords, and smart lockout services.

- **Single sign-on**

   SSO enables you to remember only one username and one password to access multiple    applications. A single identity is tied to a user, which simplifies the security model. As    users change roles or leave an organization, access modifications are tied to that identity,    which greatly reduces the effort needed to change or disable accounts.

- **Application management**

   You can manage your cloud and on-premises apps by using Azure AD. Features like Application       Proxy, SaaS apps, the My Apps portal (also called the access panel), and single sign-on       provide a better user experience.

- **Device management**

   Along with accounts for individual people, Azure AD supports the registration of devices.    Registration enables devices to be managed through tools like Microsoft Intune. It also    allows for device-based Conditional Access policies to restrict access attempts to only those    coming from known devices, regardless of the requesting user account.

## Multifactor authentication

- Multifactor authentication is a process where a user is prompted during the sign-in process for an additional form of identification. Examples include a code on their mobile phone or a fingerprint scan.

- Think about how you sign in to websites, email, or online gaming services. In addition to your username and password, have you ever needed to enter a code that was sent to your phone? If so, you've used multifactor authentication to sign in.

- Multifactor authentication provides additional security for your identities by requiring two or more elements to fully authenticate.

These elements fall into three categories:
   - Something the user knows
      * This might be an email address and password.
   - Something the user has
      * This might be a code that's sent to the user's mobile phone.
   - Something the user is
      * This is typically some sort of biometric property, such as a fingerprint or face scan that's used on many mobile devices.

## Conditional Access 

- it's a tool that Azure Active Directory uses to allow (or deny) access to resources based on identity signals. These signals include who the user is, where the user is, and what device the user is requesting access from.
Conditional Access helps IT administrators :
  * Empower users to be productive wherever and whenever.
  * Protect the organization's assets.


## Single sign-on 

- Enables a user to sign in one time and use that credential to access multiple resources and applications from different providers.

- More identities mean more passwords to remember and change. Password policies can vary among applications. As complexity requirements increase, it becomes increasingly difficult for users to remember them. The more passwords a user has to manage, the greater the risk of a credential-related security incident.

- Consider the process of managing all those identities. Additional strain is placed on help desks as they deal with account lockouts and password reset requests. If a user leaves an organization, tracking down all those identities and ensuring they are disabled can be challenging. If an identity is overlooked, this might allow access when it should have been eliminated.


# Describe Azure governance features

## Describe the functionality and usage of Role-Based Access Control (RBAC)

- When you have multiple IT and engineering teams, how can you control what access they have to the resources in your cloud environment? It's a good security practice to grant users only the rights they need to perform their job, and only to the relevant resources.
Instead of defining the detailed access requirements for each individual, and then updating access requirements when new resources are created, Azure enables you to control access through Azure role-based access control (Azure RBAC).
Azure provides built-in roles that describe common access rules for cloud resources. You can also define your own roles. Each role has an associated set of access permissions that relate to that role. When you assign individuals or groups to one or more roles, they receive all of the associated access permissions.

- Scopes include :
   - A management group (a collection of multiple subscriptions).
   - A single subscription.
   - A resource group.
   - A single resource.

- When you grant access at a parent scope, those permissions are inherited by all child scopes. For example :
     - When you assign the Owner role to a user at the management group scope, that user can manage everything in all subscriptions within the management group.
     - When you assign the Reader role to a group at the subscription scope, the members of that group can view every resource group and resource within the subscription.
     - When you assign the Contributor role to an application at the resource group scope, the application can manage resources of all types within that resource group, but not other resource groups within the subscription.

- Use Azure RBAC when you need to:
   - Allow one user to manage VMs in a subscription and another user to manage virtual networks.
   - Allow a database administrator group to manage SQL databases in a subscription.
   - Allow a user to manage all resources in a resource group, such as virtual machines, websites, and subnets.
   - Allow an application to access all resources in a resource group.

- Azure RBAC is enforced on any action that's initiated against an Azure resource that passes through Azure Resource Manager. Resource Manager is a management service that provides a way to organize and secure your cloud resources.

- RBAC uses an allow model. When you're assigned a role, RBAC allows you to perform certain actions, such as read, write, or delete. If one role assignment grants you read permissions to a resource group and a different role assignment grants you write permissions to the same resource group, you have both read and write permissions on that resource group.

- **Who does Azure RBAC apply to?** You can apply Azure RBAC to an individual person or to a group. You can also apply Azure RBAC to other special identity types, such as service principals and managed identities. These identity types are used by applications and services to automate access to Azure resources.
Tailwind Traders has the following teams with an interest in some part of their overall IT environment:
  - IT Administrators This team has ultimate ownership of technology assets, both on-premises and in the cloud. The team requires full control of all resources.
  - Backup and Disaster Recovery This team is responsible for managing the health of regular backups and invoking any data or system recoveries.
  - Cost and Billing People in this team track and report on technology-related spend. They also manage the organization's internal budgets.
  - Security Operations This team monitors and responds to any technology-related security incidents. The team requires ongoing access to log files and security alerts.

## Describe the functionality and usage of resource locks

- A resource lock prevents resources from being accidentally deleted or changed.
Even with Azure role-based access control (Azure RBAC) policies in place, there's still a risk that people with the right level of access could delete critical cloud resources. Think of a resource lock as a warning system that reminds you that a resource should not be deleted or changed.

- You can apply locks to a subscription, a resource group, or an individual resource. You can set the lock level to CanNotDelete or ReadOnly.
  - CanNotDelete means authorized people can still read and modify a resource, but they can't delete the resource without first removing the lock.
  - ReadOnly means authorized people can read a resource, but they can't delete or change the resource. Applying this lock is like restricting all authorized users to the permissions granted by the Reader role in Azure RBAC.

- **To modify a locked resource** you must first remove the lock. After you remove the lock, you can apply any action you have permissions to perform. This additional step allows the action to be taken, but it helps protect your administrators from doing something they might not have intended to do.
Resource locks apply regardless of RBAC permissions. Even if you're an owner of the resource, you must still remove the lock before you can perform the blocked activity.

- **What if a cloud administrator accidentally deletes a resource lock ?** If the resource lock is removed, its associated resources can be changed or deleted.
To make the protection process more robust, you can combine resource locks with Azure Blueprints. Azure Blueprints enables you to define the set of standard Azure resources that your organization requires. For example, you can define a blueprint that specifies that a certain resource lock must exist. Azure Blueprints can automatically replace the resource lock if that lock is removed.


## Organize your Azure resources by using tags

- One way to organize related resources is to place them in their own subscriptions. You can also use resource groups to manage related resources. Resource tags are another way to organize resources. Tags provide extra information, or metadata, about your resources. This metadata is useful for:
    - Resource management Tags enable you to locate and act on resources that are associated with specific workloads, environments, business units, and owners.
    - Cost management and optimization Tags enable you to group resources so that you can report on costs, allocate internal cost centers, track budgets, and forecast estimated cost.
    - Operations management Tags enable you to group resources according to how critical their availability is to your business. This grouping helps you formulate service-level agreements (SLAs). An SLA is an uptime or performance guarantee between you and your users.
    - Security Tags enable you to classify data by its security level, such as public or confidential.
    - Governance and regulatory compliance Tags enable you to identify resources that align with governance or regulatory compliance requirements, such as ISO 27001. Tags can also be part of your standards enforcement efforts. For example, you might require that all resources be tagged with an owner or department name.
    - Workload optimization and automation Tags can help you visualize all of the resources that participate in complex deployments. For example, you might tag a resource with its associated workload or application name and use software such as Azure DevOps to perform automated tasks on those resources

- You can also manage tags by using Azure Policy. For example, you can apply tags to a resource group, but those tags aren't automatically applied to the resources within that resource group. You can use Azure Policy to ensure that a resource inherits the same tags as its parent resource group. You'll learn more about Azure Policy later in this module.


## Describe the functionality and usage of Azure Policy 

- In a previous exercise in this module, you identified your governance and business requirements. How do you ensure that your resources stay compliant? Can you be alerted if a resource's configuration has changed?

- **Azure Policy** is a service in Azure that enables you to create, assign, and manage policies that control or audit your resources. These policies enforce different rules across all of your resource configurations so that those configurations stay compliant with corporate standards

- Azure Policy enables you to define both individual policies and groups of related policies, known as initiatives. Azure Policy evaluates your resources and highlights resources that aren't compliant with the policies you've created. Azure Policy can also prevent noncompliant resources from being created.

- Azure Policy comes with built-in policy and initiative definitions for Storage, Networking, Compute, Security Center, and Monitoring. For example, if you define a policy that allows only a certain SKU (stock-keeping unit) size for the virtual machines (VMs) to be used in your environment, that policy is invoked when you create a new VM and whenever you resize existing VMs. Azure Policy also evaluates and monitors all current VMs in your environment.

- **An Azure Policy initiative** is a way of grouping related policies together. The initiative definition contains all of the policy definitions to help track your compliance state for a larger goal.
For example, Azure Policy includes an initiative named Enable Monitoring in Azure Security Center. Its goal is to monitor all of the available security recommendations for all Azure resource types in Azure Security Center.
Under this initiative, the following policy definitions are included:
Monitor unencrypted SQL Database in Security Center This policy monitors for unencrypted SQL databases and servers.
Monitor OS vulnerabilities in Security Center This policy monitors servers that don't satisfy the configured OS vulnerability baseline.
Monitor missing Endpoint Protection in Security Center This policy monitors for servers that don't have an installed endpoint protection agent.
In fact, the Enable Monitoring in Azure Security Center initiative contains over 100 separate policy definitions.
Azure Policy also includes initiatives that support regulatory compliance standards, such as HIPAA and ISO 27001.

## Describe the functionality and usage of Azure Blueprints

- What happens when your cloud environment starts to grow beyond just one subscription? How can you scale the configuration of these features, knowing they need to be enforced for resources in new subscriptions?
Instead of having to configure features like Azure Policy for each new subscription, with Azure Blueprints you can define a repeatable set of governance tools and standard Azure resources that your organization requires. In this way, development teams can rapidly build and deploy new environments with the knowledge that they're building within organizational compliance with a set of built-in components that speed the development and deployment phases.

- When you form a cloud center of excellence team or a cloud custodian team, that team can use Azure Blueprints to scale their governance practices throughout the organization.
Implementing a blueprint in Azure Blueprints involves these three steps:
  - Create an Azure blueprint.
  - Assign the blueprint.
  - Track the blueprint assignments.
With Azure Blueprints, the relationship between the blueprint definition (what should be deployed) and the blueprint assignment (what was deployed) is preserved. In other words, Azure creates a record that associates a resource with the blueprint that defines it. This connection helps you track and audit your deployments.
Blueprints are also versioned. Versioning enables you to track and comment on changes to your blueprint.

- **Artifact** Each component in the blueprint definition is known as an artifact.
It is possible for artifacts to have no additional parameters (configurations). An example is the Deploy threat detection on SQL servers policy, which requires no additional configuration.
Artifacts can also contain one or more parameters that you can configure. The following screenshot shows the Allowed locations policy. This policy includes a parameter that specifies the allowed locations.

## Describe the Cloud Adoption Framework for Azure

- As mentioned in the video, Cloud Adoption Framework consists of tools, documentation, and proven practices. The Cloud Adoption Framework includes these stages:
  - Define your strategy.
  - Make a plan.
  - Ready your organization.
  - Adopt the cloud.
  - Govern and manage your cloud environments.


## Describe privacy and compliance resources

### Describe the Microsoft core tenets of Security, Privacy, and Compliance

- **Compliance** Microsoft's online services build upon a common set of regulatory and compliance controls. Think of a control as a known good standard that you can compare your solution against to ensure security. These controls address today's regulations and adapt as regulations evolve

- **Compliance example** Azure, Intune, and Microsoft Power BI have obtained Cloud Security Alliance (CSA) STAR Certification, which involves a rigorous independent third-party assessment of a cloud provider's security posture.
STAR Certification is based on achieving International Organization of Standards/International Electrotechnical Commission (ISO/IEC) 27001 certification and meeting criteria specified in the Cloud Controls Matrix (CCM). This certification demonstrates that a cloud service provider:
   - Conforms to the applicable requirements of ISO/IEC 27001.
   - Has addressed issues critical to cloud security as outlined in the CCM.
   - Has been assessed against the STAR Capability Maturity Model for the management of activities in CCM control areas.


### Describe the purpose of the Microsoft Privacy Statement, Online Services Terms (OST) and Data Protection Amendment (DPA)

- **The Microsoft Privacy Statement** explains what personal data Microsoft collects, how Microsoft uses it, and for what purposes.
The privacy statement covers all of Microsoft's services, websites, apps, software, servers, and devices. This list ranges from enterprise and server products to devices that you use in your home to software that students use at school.
Microsoft's privacy statement also provides information that's relevant to specific products such as Windows and Xbox.

- **The Data Protection Addendum (DPA)** further defines the data processing and security terms for online services. These terms include:
   - Compliance with laws.
   - Disclosure of processed data.
   - Data Security, which includes security practices and policies, data encryption, data access, customer responsibilities, and compliance    - with auditing.
   - Data transfer, retention, and deletion.

- **The Online Services Terms (OST)** is a legal agreement between Microsoft and the customer. The OST details the obligations by both parties with respect to the processing and security of customer data and personal data. The OST applies specifically to Microsoft's online services that you license through a subscription, including Azure, Dynamics 365, Office 365, and Bing Maps.

### Describe the purpose of the Trust Center

- **The Trust Center** showcases Microsoft's principles for maintaining data integrity in the cloud and how Microsoft implements and supports security, privacy, compliance, and transparency in all Microsoft cloud products and services. The Trust Center is an important part of the Microsoft Trusted Cloud Initiative and provides support and resources for the legal and compliance community.
- The Trust Center provides:
  - In-depth information about security, privacy, compliance offerings, policies, features, and practices across Microsoft cloud products.
  - Additional resources for each topic.
  - Links to the security, privacy, and compliance blogs and upcoming events.
The Trust Center is a great resource for other people in your organization who might play a role in security, privacy, and compliance. These people include business managers, risk assessment and privacy officers, and legal compliance teams.

### Describe the purpose of the Azure compliance documentation

- **The Azure compliance documentation** provides you with detailed documentation about legal and regulatory standards and compliance on Azure.
Here you find compliance offerings across these categories:
  - Global
  - US government
  - Financial services
  - Health
  - Media and manufacturing
  - Regional
  - There are also additional compliance resources, such as audit reports, privacy information, compliance implementations and mappings, and   white papers and analyst reports. Country and region privacy and compliance guidelines are also included. Some resources might require   you to be signed in to your cloud service to access them.


### Describe the purpose of Azure Sovereign Regions (Azure Government cloud services and Azure China cloud services)

- **Azure Government** is a separate instance of the Microsoft Azure service. It addresses the security and compliance needs of US federal agencies, state and local governments, and their solution providers. Azure Government offers physical isolation from non-US government deployments and provides screened US personnel.
- **Azure Government services** handle data that is subject to certain government regulations and requirements:
    - Federal Risk and Authorization Management Program (FedRAMP)
    - National Institute of Standards and Technology (NIST) 800.171 Defense Industrial Base (DIB)
    - International Traffic in Arms Regulations (ITAR)
    - Internal Revenue Service (IRS) 1075
    - Department of Defense (DoD) L4
    - Criminal Justice Information Service (CJIS)
    - To provide the highest level of security and compliance, Azure Government uses physically isolated datacenters and networks located only - in the US. Azure Government customers, such as the US federal, state, and local government or their partners, are subject to validation - of eligibility.

Azure Government provides the broadest compliance and Level 5 DoD approval. Azure Government is available in eight geographies and offers the most compliance certifications of any cloud provider.

- **Azure China 21Vianet** is operated by 21Vianet. It's a physically separated instance of cloud services located in China. Azure China 21Vianet is independently operated and transacted by Shanghai Blue Cloud Technology Co., Ltd. ("21Vianet"), a wholly owned subsidiary of Beijing 21Vianet Broadband Data Center Co., Ltd.
According to the China Telecommunication Regulation, providers of cloud services, infrastructure as a service (IaaS) and platform as a service (PaaS), must have value-added telecom permits. Only locally registered companies with less than 50 percent foreign investment qualify for these permits. To comply with this regulation, the Azure service in China is operated by 21Vianet, based on the technologies licensed from Microsoft.