Day 5: Hands-On with AWS Auto Scaling and Application Load Balancers 🚀

> **Today's Focus:** Implementing a High-Availability Architecture with Auto Scaling and Load Balancing.

---

## 💡 What I Learned

This session covered the core AWS services required to build a resilient and scalable application infrastructure.

-   **Amazon Machine Image (`AMI`):** Understood how to create a custom "golden image" to ensure all new EC2 instances are launched with a consistent configuration.

-   **Launch Templates:** Created a version-controlled template that defined the `AMI`, instance type, key pair, and security groups for my EC2 instances. This is the modern, recommended approach over Launch Configurations.

-   **Load Balancing Concepts:** Dived into the three main types and their use cases:
    -   **Application Load Balancer (ALB):** Best for routing HTTP/HTTPS traffic (Layer 7). It's content-aware, allowing for path-based or host-based routing.
    -   **Network Load Balancer (NLB):** Ideal for ultra-high performance and static IP addresses. It operates at the transport layer (Layer 4) for TCP/UDP traffic.
    -   **Gateway Load Balancer (GWLB):** A specialized service for deploying, scaling, and managing third-party virtual appliances like firewalls or intrusion detection systems.

-   **Target Groups:** Configured a group of EC2 instances and set up health checks to ensure the Load Balancer only sends traffic to healthy instances.

-   **Auto Scaling Groups (`ASG`):** The core of the lab. I configured an ASG to automatically manage the number of instances based on demand, ensuring both availability and cost-efficiency.

---

## 🛠️ Hands-On Lab: Auto Scaling in Action

To solidify my understanding, I built a functional demo environment.

1.  **Created a custom `AMI`** from an EC2 instance that had a simple web server installed.
2.  **Authored a Launch Template** that used the new `AMI`.
3.  **Deployed an Application Load Balancer (ALB)** to serve as the single public entry point for traffic.
4.  **Established an Auto Scaling Group** linked to the Launch Template.
    -   **Desired Capacity:** 3 Instances
    -   **Min/Max Size:** 2 / 6 Instances
    -   **Scaling Policy:** Scale out (add an instance) if average CPU utilization exceeds 70%.
5.  **Configured Security Groups** meticulously:
    -   One for the ALB, allowing public HTTP traffic (Port 80) from `0.0.0.0/0`.
    -   One for the EC2 instances, allowing traffic *only* from the ALB's security group.
6.  **Tested the setup** by terminating an instance and watching the ASG automatically launch a new one to replace it, proving the self-healing capability.


<img width="861" height="680" alt="image" src="https://github.com/user-attachments/assets/665086ec-20b3-4ef2-90f6-3188594f1412" />

---

## ✨ Key Takeaway

This lab was a practical demonstration of how to combine Load Balancers, Launch Templates, and Auto Scaling Groups to build a robust, self-healing infrastructure that responds dynamically to user demand.

