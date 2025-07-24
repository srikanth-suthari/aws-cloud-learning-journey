### **<a name="day-1-cloud-computing-fundamentals--aws-global-infrastructure"></a>Day 1: Cloud Computing Fundamentals & AWS Global Infrastructure**

Today, I began my cloud journey by establishing a strong understanding of what cloud computing is at its core and how AWS's global infrastructure is organized. This foundational knowledge is essential before diving into specific services.

* **Core Cloud Computing Concepts:**
    * **Definition:** Explored cloud computing as the on-demand delivery of IT resources (compute, storage, databases, networking, etc.) over the internet with pay-as-you-go pricing. It shifts from capital expenditure to operational expenditure.
    * **Key Characteristics:** Understood the five essential characteristics that define cloud computing:
        * **On-demand self-service:** Users can provision compute capabilities without human interaction.
        * **Broad network access:** Capabilities are available over the network and accessed through standard mechanisms.
        * **Resource pooling:** Provider's computing resources are pooled to serve multiple consumers using a multi-tenant model.
        * **Rapid elasticity:** Capabilities can be elastically provisioned and released to scale rapidly outward and inward with demand.
        * **Measured service:** Cloud systems automatically control and optimize resource use by leveraging a metering capability.
    * **Cloud Service Models:** Differentiated between the three primary service models:
        * **IaaS (Infrastructure as a Service):** Provides fundamental computing resources (virtual machines, networks, storage). Users manage OS and applications (e.g., AWS EC2).
        * **PaaS (Platform as a Service):** Provides a platform allowing customers to develop, run, and manage applications without the complexity of building and maintaining the infrastructure (e.g., AWS Elastic Beanstalk, AWS Lambda).
        * **SaaS (Software as a Service):** Provides ready-to-use applications managed entirely by the vendor. Users simply consume the service (e.g., Gmail, Salesforce, AWS S3 for simple web hosting).
    * **Cloud Deployment Models:** Learned about different ways cloud resources can be deployed:
        * **Public Cloud:** Cloud services offered by third-party providers over the public internet (e.g., AWS, Azure, GCP).
        * **Private Cloud:** Cloud infrastructure operated exclusively for a single organization, either on-premises or by a third party.
        * **Hybrid Cloud:** A combination of public and private clouds, allowing data and applications to be shared between them, offering greater flexibility.

* **AWS Global Infrastructure:**
    * **Regions:** AWS's global presence is organized into geographically distinct and isolated areas called Regions. Each Region is a completely separate geographic area designed to be isolated from other Regions to ensure fault tolerance and stability. Data in one Region is not automatically replicated to another.
    * **Availability Zones (AZs):** Within each Region, there are multiple (typically 3 or more) isolated physical data centers called Availability Zones. Each AZ has independent power, cooling, and physical security, and they are interconnected with high-bandwidth, low-latency networking over fully redundant, dedicated metro fiber. This design allows for high availability and disaster recovery within a Region.
    * **Edge Locations (or AWS Local Zones/Outposts):** These are strategically located data centers or points of presence (PoPs) designed to deliver content with low latency to users by caching content closer to them. Primarily used by services like Amazon CloudFront and AWS Global Accelerator.

<img width="1161" height="628" alt="image" src="https://github.com/user-attachments/assets/c05db493-1bfb-448e-a92a-54ab41d5aada" />

<img width="1280" height="614" alt="image" src="https://github.com/user-attachments/assets/274dac63-7df4-4c46-a120-2a8689a99348" />	
