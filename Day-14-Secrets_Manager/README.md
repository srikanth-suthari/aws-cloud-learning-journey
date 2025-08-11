## Day 14: AWS Security Services - Encryption, Firewalls & Governance 🚀

> **Today's Focus:** Deep diving into the essential AWS services that protect data, manage network perimeters, detect threats, and ensure compliance in the cloud.

### 💡 What I Learned

Today's session covered the multi-layered approach AWS provides for securing your cloud environment, from the network edge right down to your data.

#### Network & Perimeter Protection

* **AWS Network Firewall:** A managed, stateful firewall service that gives you fine-grained control over traffic flowing into and out of your VPC. It allows you to create rules to filter traffic based on source/destination IP, port, protocol, and even domain names.
* **AWS Firewall Manager:** A central management service that simplifies the administration of firewall rules across multiple AWS accounts and resources. You can create a single policy and apply it to your Network Firewalls, WAF rules, and Security Groups throughout your organization.

#### Encryption & Secrets Management

![1740342705247](https://github.com/user-attachments/assets/fabd1c3a-b350-4577-961e-2e1206e1c549)

* **AWS KMS (Key Management Service):** A foundational security service that makes it easy to create, manage, and control cryptographic keys. KMS is integrated with almost all AWS services that store data, allowing you to centrally manage the keys that encrypt your data at rest.
* **AWS Certificate Manager (ACM):** A service that handles the complexity of provisioning, managing, and deploying public and private SSL/TLS certificates. It's used to secure network communications and is integrated with services like Elastic Load Balancing and CloudFront.
* **AWS Secrets Manager:** A service designed to protect and manage secrets like database credentials, API keys, and other sensitive tokens. It replaces hardcoded credentials in your code with an API call, and it can automatically rotate secrets to improve your security posture.

#### Threat Detection, Governance & Compliance

* **Amazon GuardDuty:** An intelligent threat detection service that continuously monitors your AWS accounts for malicious activity and unauthorized behavior. It analyzes various data sources like CloudTrail logs, VPC Flow Logs, and DNS logs to identify potential threats like reconnaissance by attackers or compromised instances.
* **IAM Access Analyzer:** A service that helps you identify resources in your account that are shared with an external entity. It mathematically analyzes access policies to find and report on resources (like S3 buckets or IAM roles) that are accessible from outside your zone of trust, helping you achieve least privilege.
* **AWS Artifact:** A central resource for compliance-related information. It provides on-demand access to AWS's security and compliance reports, such as SOC reports, PCI reports, and certifications from various accreditation bodies.

### 🛠️ Hands-On Lab

1.  Navigated to **AWS KMS** and created a new symmetric, customer-managed key (CMK).
2.  Created a new S3 bucket and configured its default encryption settings to use the newly created KMS key, ensuring all future objects uploaded to the bucket are automatically encrypted with my key.
3.  Used **AWS Secrets Manager** to store a dummy database password, allowing Secrets Manager to generate a secure, random password.
4.  Explored the secret's configuration and initiated the process for automatic credential rotation.
5.  Enabled **Amazon GuardDuty** for the account to begin monitoring for potential threats and viewed the console to see if any sample findings were available.

### ✨ Key Takeaway

Security on AWS is a multi-layered discipline. AWS provides a deep set of purpose-built tools that work together to secure the cloud environment at every level. From protecting the network perimeter with **Network Firewall**, to encrypting data with **KMS**, to intelligently detecting threats with **GuardDuty**, a proactive and defense-in-depth security strategy is essential for any workload running in the cloud.

![AWS-RAM-ACMPCA-2020-Figure-1-ForSocial-1024x512](https://github.com/user-attachments/assets/6e801d73-1ec5-4d9d-8be4-29b5b46ce239)

<img width="1180" height="660" alt="1--1-" src="https://github.com/user-attachments/assets/95ed4df9-55b0-41bb-9f7e-0e859177b019" />
