### **<a name="day-2-aws-iam-identity-and-access-management"></a>Day 2: AWS IAM (Identity and Access Management)**

Today, I focused entirely on AWS Identity and Access Management (IAM), a fundamental service for securing your AWS environment. Understanding IAM is crucial for controlling who can do what within your AWS account.

* **AWS IAM (Identity and Access Management):**
    * **Purpose:** The central service for securely managing access to AWS services and resources. It allows you to control *who is authenticated* (Identity) and *what they are authorized to do* (Access Management). It's the absolute foundation of security in AWS.
    
    * ![IAM](https://github.com/user-attachments/assets/da576ce3-d237-48ed-9163-e980d134a2a2)
      
    * **IAM Users:** Represent individual people or applications that need to interact with AWS. Each user has unique, long-term security credentials (username/password for console access, or access keys for programmatic access).
    * **IAM Groups:** Logical collections of IAM users. Attaching policies to groups simplifies permission management; all users within a group inherit the permissions of the group's attached policies. This promotes scalability and manageability.
    * 
    * **IAM Roles:** Designed to delegate temporary permissions to trusted entities. Roles are assumed by:
        * AWS services (e.g., an EC2 instance needing to access an S3 bucket).
        * Users or applications outside your AWS account (cross-account access).
        * Federated users (e.g., users logging in via Okta or Active Directory).
        Crucially, roles utilize **temporary security credentials** (unlike long-term user access keys), which is a significant security enhancement.

    * **IAM Policies & Permissions:** The core of access control. These are JSON documents that define *what actions are allowed or denied* on *which specific AWS resources* under *what conditions*.
        * **Identity-based Policies:** Attached directly to IAM users, groups, or roles.
        * **Resource-based Policies:** Attached directly to a resource (e.g., an S3 bucket policy) to specify who has access to that resource and what actions they can perform on it.
        * Understood the granularity of control available (e.g., `s3:GetObject`, `ec2:RunInstances`).
    * **Key Security Principles & Best Practices Learned:**
        * **Principle of Least Privilege:** Granting only the minimum necessary permissions required for a user or service to perform its task, and no more. This significantly reduces the attack surface.
        * Enabling **Multi-Factor Authentication (MFA):** Adding an extra layer of security by requiring a second verification factor (e.g., a code from a mobile app) in addition to a password. Essential for all users, and especially for the root account.
        * Avoiding the **Root User:** Never using the root account for daily operational tasks. Its unrestricted access makes it a high-risk target. Always create an IAM user for administrative tasks.
        * Using **IAM Roles for AWS Services:** Always recommend services assume roles rather than using hardcoded access keys. This provides a more secure and manageable way for services to interact with other AWS resources.
        * Regularly **Reviewing Permissions:** Periodically auditing IAM policies to ensure they still adhere to the principle of least privilege.
