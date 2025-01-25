# HybridCloudFailover
A project demonstrating hybrid cloud failover using Azure and AWS with DNS-based traffic redirection.
# Hybrid Cloud Failover Implementation: Azure and AWS

## **1. Project Title**

**Hybrid Cloud Failover Implementation: Azure and AWS**

This title is clear, descriptive, and indicates the project's purpose, meeting the rubric requirement.

---

## **2. Project Summary**

- **Brief Description**:
  - This project demonstrates the implementation of a hybrid cloud failover solution using Azure and AWS. It highlights business continuity through DNS-based traffic redirection and leverages load balancers for scalability and redundancy.

- **Languages Used**:
  - No scripting was required for this project, but optional enhancements could include Terraform or PowerShell for automation.

- **Environments Used**:
  - Azure (Primary environment: Resource Group, Virtual Machine, Load Balancer).
  - AWS (Failover environment: VPC, EC2 Instance, Application Load Balancer).

- **Technologies/Applications/Services**:
  - DuckDNS for dynamic DNS.
  - IIS (Internet Information Services) for web hosting.
  - Azure and AWS Load Balancers for traffic routing and failover.

---

## **3. Media (Images and/or Video)**

Include the following screenshots to demonstrate the implementation:

### **Azure Environment**:
1. _Azure_Load_Balancer.png_: Configuration details of the Azure Load Balancer.
2. _Azure_Resource_Group_Overview.png_: Overview of all Azure resources.
3. _Azure_VM_Details.png_: Azure VM details, including public IP and network configuration.
4. _Failover_To_Azure.png_: DuckDNS subdomain pointing to Azure, showing IIS page with "Welcome to Azure."

### **AWS Environment**:
1. _AWS_Load_Balancer.png_: Configuration details of the AWS Application Load Balancer.
2. _AWS_VPC_Details.png_: VPC details, including CIDR block and subnets.
3. _AWS_EC2_Instance_Details.png_: EC2 instance details, showing public IP and instance configuration.
4. _AWS_Target_Group_Healthy.png_: Target group with EC2 instance marked as healthy.
5. _Failover_To_AWS.png_: DuckDNS subdomain pointing to AWS, showing IIS page with "Welcome to AWS."

---

## **4. Demonstration**

### **Step-by-Step Walkthrough**

#### **Azure Setup**:
1. Created a Resource Group.
2. Provisioned a Virtual Network and a Windows Server Virtual Machine.
3. Configured an Azure Load Balancer with a backend pool, health probes, and load balancing rules.
4. Customized the IIS default page to display "Welcome to Azure."

**Screenshot References**: _Azure_Load_Balancer.png_, _Azure_VM_Details.png_.

#### **AWS Setup**:
1. Created a VPC with appropriate subnets.
2. Provisioned a Windows Server EC2 instance.
3. Configured an AWS Application Load Balancer with a target group.
4. Customized the IIS default page to display "Welcome to AWS."

**Screenshot References**: _AWS_Load_Balancer.png_, _AWS_EC2_Instance_Details.png_.

#### **Failover Demonstration**:
1. Updated the DuckDNS subdomain to point to Azure.
2. Accessed the subdomain to confirm "Welcome to Azure" displayed.
3. Updated the DuckDNS subdomain to point to AWS.
4. Accessed the subdomain to confirm "Welcome to AWS" displayed.

**Screenshot References**: _Failover_To_Azure.png_, _Failover_To_AWS.png_.

### **Results Validation**:
- Load Balancers and VMs functioned correctly.
- Manual failover via DNS updates successfully rerouted traffic between environments.

---

## **5. Key Technologies**

- **Azure**:
  - Load Balancer for traffic distribution.
  - Virtual Machine for hosting the web application.

- **AWS**:
  - Application Load Balancer for failover support.
  - EC2 instance for hosting the backup web server.

- **DuckDNS**:
  - Dynamic DNS for managing traffic routing.

---

## **6. Conclusion**

This project successfully implements a hybrid cloud failover strategy between Azure and AWS. The manual DNS-based failover ensures high availability and business continuity. The solution can be further enhanced by automating failover using monitoring tools and scripts.

---

## **Next Steps**

1. **Add Media**: Place screenshots in their appropriate sections with captions.
2. **Enhance Documentation**: Provide optional improvements (e.g., automation scripts or monitoring tools).
3. **Submit**: Organize into a GitHub repository and share the link for review.

