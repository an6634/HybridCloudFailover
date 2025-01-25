# Hybrid Cloud Failover

A project demonstrating hybrid cloud failover using Azure and AWS with DNS-based traffic redirection.

---

## **1. Project Title**

**Hybrid Cloud Failover Implementation: Azure and AWS**

This project demonstrates a hybrid cloud solution that ensures business continuity and redundancy through DNS-based traffic redirection between Azure and AWS.

---

## **2. Project Summary**

- **Brief Description**:  
  This project implements a hybrid cloud failover solution using Azure and AWS. It highlights business continuity, scalability, and redundancy by leveraging dynamic DNS, cloud load balancers, and web servers.

- **Environments Used**:  
  - **Azure**:  
    - Resource Group, Virtual Machine, and Load Balancer.  
  - **AWS**:  
    - VPC, EC2 Instance, and Application Load Balancer.

- **Technologies/Applications/Services**:  
  - **DuckDNS** for dynamic DNS.  
  - **IIS** (Internet Information Services) for web hosting.  
  - **Load Balancers** from Azure and AWS for traffic routing and failover.

---

## **3. Media (Images and/or Video)**

The following screenshots demonstrate the project implementation:

### **Azure Environment**
1. `Azure_Load_Balancer.png`: Configuration details of the Azure Load Balancer.
2. `Azure_Resource_Group_Overview.png`: Overview of all Azure resources.
3. `Azure_VM_Details.png`: Azure VM details, including public IP and network configuration.
4. `Failover_To_Azure.png`: DuckDNS subdomain pointing to Azure, showing IIS page with "Welcome to Azure."

### **AWS Environment**
1. `AWS_Load_Balancer.png`: Configuration details of the AWS Application Load Balancer.
2. `AWS_VPC_Details.png`: VPC details, including CIDR block and subnets.
3. `AWS_EC2_Instance_Details.png`: EC2 instance details, including public IP and instance configuration.
4. `AWS_Target_Group_Healthy.png`: Target group with EC2 instance marked as healthy.
5. `Failover_To_AWS.png`: DuckDNS subdomain pointing to AWS, showing IIS page with "Welcome to AWS."

---

## **4. Demonstration**

### **Step-by-Step Walkthrough**

#### **Azure Setup**
1. Created a Resource Group.
2. Provisioned a Virtual Network and a Windows Server Virtual Machine.
3. Configured an Azure Load Balancer with backend pools, health probes, and load balancing rules.
4. Customized the IIS default page to display "Welcome to Azure."

#### **AWS Setup**
1. Created a VPC with appropriate subnets.
2. Provisioned a Windows Server EC2 instance.
3. Configured an AWS Application Load Balancer with a target group.
4. Customized the IIS default page to display "Welcome to AWS."

#### **Failover Demonstration**
1. Updated the DuckDNS subdomain to point to Azure.
2. Accessed the subdomain to confirm "Welcome to Azure" displayed.
3. Updated the DuckDNS subdomain to point to AWS.
4. Accessed the subdomain to confirm "Welcome to AWS" displayed.

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

This project successfully demonstrates a hybrid cloud failover strategy between Azure and AWS. By utilizing DuckDNS, Azure Load Balancer, and AWS Application Load Balancer, the project ensures high availability and seamless failover. The manual DNS-based failover ensures application continuity, and the project can be enhanced by automating the failover process using monitoring tools or scripts.

# Backend Tracker

## Next Steps
- Automate resource deployment with Terraform or PowerShell scripts.
- Integrate monitoring tools like Azure Monitor or AWS CloudWatch for real-time alerts.
- Enhance failover with automated DNS updates via API calls to DuckDNS.

## Tasks Pending Validation
- Verify load balancer behavior during automated failover testing.
- Test scalability under simulated high traffic.
