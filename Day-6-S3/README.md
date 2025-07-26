## Day 6: Amazon S3 & Data Transfer Deep Dive 🚀

> **Today's Focus:** Mastering object storage with Amazon S3 and exploring AWS's physical and hybrid data transfer solutions.

### 💡 What I Learned

-   **S3 Buckets:** These are the fundamental containers for data in S3. Each bucket must have a **globally unique name** and is created in a specific AWS Region.

-   **S3 Versioning:** A crucial safety feature. When enabled, it preserves every version of every object, protecting against accidental overwrites and deletions. You can restore previous versions of an object at any time.

-   **S3 Encryption:** Data can be secured both in transit (using SSL/TLS) and at rest. Server-Side Encryption (SSE) options include **SSE-S3** (AWS manages the keys), **SSE-KMS** (you manage keys via AWS KMS), and **SSE-C** (you provide your own keys).

-   **Static Website Hosting:** A simple and powerful feature that allows you to serve a static website (HTML, CSS, JavaScript) directly from an S3 bucket, making it highly available and scalable at a low cost.

-   **S3 Bucket Policies:** JSON-based policies attached to a bucket to grant permissions to users and accounts. They are a powerful way to manage access to all objects within a single bucket.

-   **S3 Replication (CRR & SRR):**
    -   **Cross-Region Replication (CRR):** Automatically copies objects to a bucket in a different AWS Region. Used for disaster recovery and reducing latency for users in different geographic locations.
    -   **Same-Region Replication (SRR):** Copies objects to another bucket in the *same* AWS Region. Used for aggregating logs or creating separate development/production accounts.

-   **S3 Storage Classes:** Different tiers of storage that balance cost against retrieval time and availability. Choosing the right class is key to optimizing costs.
    -   `S3 Standard`
    -   `S3 Intelligent-Tiering`
    -   `S3 Standard-Infrequent Access (Standard-IA)`
    -   `S3 One Zone-Infrequent Access (One Zone-IA)`
    -   `S3 Glacier Instant Retrieval`
    -   `S3 Glacier Flexible Retrieval`
    -   `S3 Glacier Deep Archive`

-   **AWS Snow Family (Snowball):** A service that uses physical devices to transfer petabyte-scale data into and out of AWS. It's ideal when network transfer would be too slow or expensive.

-   **AWS Storage Gateway:** A hybrid cloud storage service that connects your on-premises applications to AWS storage. It provides low-latency access to data by caching frequently used data on-premises while storing the full dataset securely in S3.

<img width="1400" height="632" alt="0_aJ6BpnaRXbf01pEB" src="https://github.com/user-attachments/assets/a0c17c91-5c0a-47fc-86dd-34230a1cd8b9" />
![471048509-234a1dc4-0c00-4c0d-971f-71ea2fff2bc0](https://github.com/user-attachments/assets/38ab86cb-9ac4-43c3-8223-f0385da9edd7)
<img width="810" height="431" alt="a999e274-0a3e-4c2c-a2db-6659d3105d05" src="https://github.com/user-attachments/assets/5113cb09-2180-427c-83dd-795407e4d7a4" />

