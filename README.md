# azure-virtual-machine
This repository was created to demonstrate the knowledge and skills acquired during the DIO.me AZ-900 labs.

# Objectives

- Understand the benefits of cloud computing.
- Learn the concepts of availability, scalability, and elasticity.
- Explore Azure security and governance features.
- Create a Virtual Machine using the Microsoft Azure Portal.
- Document the learning process.

---

# Cloud Computing Benefits

## 1. High Availability

High Availability is the ability of a system to remain operational even when infrastructure failures occur.

Azure is designed to minimize service interruptions. If a physical server fails, another one can take over. Likewise, depending on the architecture, applications can continue running even if an entire datacenter becomes unavailable.

### SLA (Service Level Agreement)

An SLA is Microsoft's commitment regarding the availability of a service over a given period (typically one month).

Examples include:

- 99%
- 99.9%
- 99.95%
- 99.99%
- 99.999%

The higher the SLA percentage, the lower the expected downtime.

### Relationship Between High Availability and SLA

High Availability is what enables Microsoft to offer higher SLA guarantees.

For example:

**Scenario 1**

- A single Virtual Machine.

If that VM experiences a failure, the application becomes unavailable.

**Scenario 2**

- Two Virtual Machines;
- Deployed across different Availability Zones;
- Behind an Azure Load Balancer.

If one VM fails, the other continues serving users, significantly reducing downtime and increasing the overall SLA.

---

## 2. Scalability

Scalability is the ability to increase or decrease resources according to application demand.

In Azure, you can scale resources such as:

- CPU
- Memory (RAM)
- Storage

A common question is:

> Does adding more resources increase costs?

Yes, but Azure follows a **pay-as-you-go** pricing model.

This means:

- You only pay for the resources you use.
- When demand decreases, resources can be reduced, lowering operational costs.

### Vertical Scaling

Vertical scaling increases the capacity of an existing virtual machine.

Examples:

- Upgrade from 2 to 4 vCPUs.
- Increase memory from 8 GB to 16 GB.

---

## 3. Elasticity

Elasticity is the ability to automatically (or manually) add or remove resources according to changes in workload.

For example:

During an online store promotion, traffic may suddenly increase.

Azure can automatically deploy additional virtual machines to handle the increased demand.

Once traffic returns to normal, those extra resources can be removed, optimizing costs.

---

## 4. Reliability

Azure provides a globally distributed infrastructure.

Applications can be deployed across multiple geographic regions.

Even if an entire region experiences a major outage or natural disaster, other regions can continue operating, ensuring greater resilience and business continuity.

---

## 5. Predictability

Predictability allows organizations to confidently estimate both application performance and operational costs.

This benefit is supported by the **Microsoft Azure Well-Architected Framework**, which provides best practices for designing reliable, secure, and cost-effective cloud solutions.

---

## 6. Security

Azure provides a wide range of security tools and services.

However, security responsibilities vary depending on the selected cloud service model.

### Infrastructure as a Service (IaaS)

The customer is responsible for:

- Operating system management;
- Software updates;
- Security patching;
- Installed applications.

### Platform as a Service (PaaS)

Microsoft automatically manages most infrastructure maintenance, operating system updates, and security patches.

---

## 7. Governance

Cloud governance ensures that resources comply with organizational standards and policies.

Its main benefits include:

- Automated compliance auditing;
- Identification of non-compliant resources;
- Policy enforcement;
- Automated software updates and security patches.

Implementing governance early helps maintain a secure, organized, and well-managed cloud environment.

---

## 8. Manageability

Azure offers multiple ways to manage cloud resources.

### Cloud Management

Refers to managing cloud resources themselves.

Examples include:

- Automatic resource scaling;
- Infrastructure deployment using templates;
- Resource automation.

### Management in the Cloud

Refers to the tools used to administer cloud environments.

Examples include:

- Azure Portal;
- Azure CLI;
- Azure PowerShell;
- REST APIs.

---

# Creating a Virtual Machine in Azure

For this challenge, the Virtual Machine was created using the Microsoft Azure Portal following the official Microsoft documentation.

Official documentation:

https://learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal

## Steps Performed

1. Access the Azure Portal.
2. Create a new Resource Group.
3. Select **Virtual Machine**.
4. Configure:
   - Virtual Machine name;
   - Region;
   - Operating System image;
   - VM size.
5. Create the administrator username and password.
6. Allow Remote Desktop (RDP - Port 3389).
7. Review the configuration.
8. Deploy the Virtual Machine.
9. Wait for the deployment to complete.
10. Connect to the VM using Remote Desktop.

---

# What I Learned

This project demonstrated that creating a Virtual Machine in Azure involves much more than simply provisioning a server.

It provided a practical understanding of how cloud computing benefits contribute to building modern applications, including concepts such as:

- High Availability;
- Service Level Agreement (SLA);
- Scalability;
- Elasticity;
- Reliability;
- Security;
- Governance;
- Manageability.

It also provided hands-on experience with the Azure Portal and the process of deploying and managing Virtual Machines.

---

# Conclusion

Creating a Virtual Machine in Microsoft Azure demonstrated how cloud computing simplifies infrastructure provisioning while providing scalability, security, and flexibility.

Combining practical implementation with cloud computing concepts reinforced the importance of High Availability, Elasticity, Governance, and other Azure capabilities when building reliable and modern cloud solutions.

---

# References

- Microsoft Learn – Create a Windows Virtual Machine in Azure

  https://learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal

- Microsoft Learn – Microsoft Azure Fundamentals

  https://learn.microsoft.com/en-us/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/
