### **<a name="day-3-aws-ec2-elastic-compute-cloud---compute-pricing--application-deployment"></a>Day 3: AWS EC2 (Elastic Compute Cloud) - Compute, Pricing & Application Deployment**

Today was a comprehensive deep dive into **Amazon EC2**, AWS's core compute service. I not only grasped its fundamental concepts and various pricing models but also gained valuable hands-on experience by deploying a small application, configuring popular web servers in the process.

* **Amazon EC2 (Elastic Compute Cloud) - Core Compute Concepts:**
    * **Definition:** Provides secure, resizable compute capacity (virtual servers, known as *instances*) in the cloud. It's the workhorse for running virtually any application on AWS.
    * **Core Concepts:** Learned about the process of launching, managing, and connecting to EC2 instances. Explored the concept of **Instance Types**, which are optimized combinations of CPU, memory, storage, and networking capacity tailored for different workloads (e.g., general purpose, compute optimized, memory optimized).
    * **Amazon Machine Images (AMIs):** Understood AMIs as pre-configured templates (including OS, application server, applications) used to launch instances.
    * **Security Groups:** Learned about Security Groups as virtual firewalls that control inbound and outbound traffic to EC2 instances.
 
    *   ![EC2](https://github.com/user-attachments/assets/623fe197-31fd-4352-8974-6ed898776edb)

* **EC2 Pricing Models (Crucial for Cost Optimization):**
    * **On-Demand Instances:** The most flexible option; you pay by the hour or second for compute capacity. Ideal for short-term, irregular workloads where you can't commit to a long-term plan. No upfront costs or long-term commitments.
    * **Reserved Instances (RIs):** Offer significant discounts (up to 75%) compared to On-Demand by committing to a 1-year or 3-year term. Best for steady-state, predictable workloads.
    * **Spot Instances:** Leverage unused EC2 capacity for up to 90% savings. Instances can be interrupted by AWS with a 2-minute warning. Ideal for fault-tolerant, flexible workloads like batch processing, data analysis, or stateless web servers.
    * **Savings Plans:** A more flexible commitment-based pricing model that offers lower prices on EC2, Fargate, and Lambda usage in exchange for a commitment to a consistent amount of compute usage (measured in $/hour) for a 1-year or 3-year term. They automatically apply to eligible usage, regardless of instance family, size, OS, or Region.
    * **Cost Optimization Insights:** This deep dive emphasized that selecting the appropriate EC2 purchasing option is a key strategy for minimizing cloud spend based on specific workload characteristics and predictability.

* **EC2 Application Deployment (Apache2 & Nginx):**
    * **Practical Application:** Moved from theoretical understanding to hands-on deployment on an EC2 instance. This provided invaluable experience in making applications accessible in the cloud.
    * **Instance Provisioning & Connection:** Successfully launched and configured an EC2 instance and securely connected to it via SSH.
    * **Web Server Installation & Configuration:**
        * **Apache2:** Installed and configured Apache HTTP Server, understanding its role as a robust web server for serving web content and handling dynamic requests.
        * **Nginx:** Explored Nginx, which is highly efficient as a reverse proxy, load balancer, and for serving static content. I configured it to work in conjunction with Apache2 (e.g., Nginx acting as a reverse proxy to Apache for dynamic content while serving static files directly for performance).
    * **Application Deployment:** Placed a small application's files onto the EC2 instance and configured the web servers to serve it, making it accessible via HTTP.
    * **Firewall Configuration (Security Groups):** Crucially, configured the EC2 instance's Security Group to allow inbound HTTP/HTTPS traffic to the web servers, ensuring the application was publicly accessible while maintaining necessary security.
* **Key Learnings:** This combined day provided a holistic view of EC2 – from provisioning and understanding its cost implications to the practical steps of deploying and making an application live. It solidified the EC2 lifecycle and the roles of common web server software in a cloud environment.


<img width="1400" height="788" alt="EC2-1" src="https://github.com/user-attachments/assets/247eca2e-7cbf-41fe-b899-504d6ecddbc7" />
