# AWS VPC Creation — Manual Deployment

# Overview

This document explains how to create and configure an Amazon Virtual Private Cloud (VPC) using the AWS Management Console.
A VPC is a logically isolated virtual network in AWS where cloud resources such as Amazon EC2 instances, load balancers, and databases can be deployed.

## Objectives

  - Understand the purpose of an Amazon VPC.
  - Create a custom VPC for the WordPress deployment.
  - Configure the IPv4 CIDR block.
  - Enable DNS resolution and DNS hostnames.
  - Apply resource tags for identification and management.
  - Verify that the VPC has been created successfully.

4. Network Design

The following CIDR block is proposed for the project.

| Configuration | Value |
| ------------- | ----- |
| VPC Name | wordpress-three-tier-vpc |
| IPv4 CIDR | 10.0.0.0/16 |
| IPv4 Address Range | 10.0.0.0 – 10.0.255.255 |
| Total IPv4 Addresses | 65,536 |
| IPv6 CIDR| Not configured initially |
| Tenancy | Default |
| DNS Resolution |  Enabled |
| DNS Hostnames | Enabled |
The VPC CIDR block defines the private IPv4 address range available for subnets and resources within this network.

## Steps to Create a VPC

### Step 1: Open the VPC Dashboard

  - Sign in to the AWS Management Console.
  - Search for VPC in the AWS services search bar.
  - Open the Amazon VPC console.
  - Confirm that you are working in the intended AWS Region.
  - Navigate to Your VPCs.
<img width="1678" height="842" alt="image" src="https://github.com/user-attachments/assets/c28fd6b6-24e0-48a0-b442-cd52dd896a57" />

### Step 2: Start VPC Creation

  - Click Create VPC.
  - Select VPC only to create the network without automatically creating subnets or gateways.
  - Enter the following configuration:
vpc-name, cidr
<img width="820" height="600" alt="image" src="https://github.com/user-attachments/assets/ff5b3ce8-c6d0-4b12-8518-ba3352d208f1" />

### Step 3: Add Tags for identification 

<img width="820" height="600" alt="image" src="https://github.com/user-attachments/assets/90cf8452-7a94-4484-a464-f3b3a3266e19" />

### Step 4: Verify DNS Settings

  - Select wordpress-vpc.
  - Open the VPC details or actions menu.
<img width="815" height="660" alt="image" src="https://github.com/user-attachments/assets/60d09f6d-f34e-411b-a1a1-7ea9290ef665" />

Locate the DNS settings.
  - Ensure that DNS resolution is enabled.
  - Ensure that DNS hostnames are enabled.
<img width="1671" height="796" alt="image" src="https://github.com/user-attachments/assets/a54b9896-93cc-4939-aa32-b9b58c7dcb33" />

subnet creation - VPC select

<img width="815" height="660" alt="image" src="https://github.com/user-attachments/assets/ee5697fb-8e0b-47be-b36a-1c058ba2af30" />

subnet name, cidr
<img width="815" height="660" alt="image" src="https://github.com/user-attachments/assets/49259439-5d48-4ec3-992c-7af5023b4e3a" />

tags, 
<img width="1670" height="731" alt="image" src="https://github.com/user-attachments/assets/ccbacb1d-5975-4cb2-8686-5af75dd3c35c" />

subnet created 
<img width="815" height="660" alt="image" src="https://github.com/user-attachments/assets/0b86dbfa-7f59-40eb-8a36-3d10d24db774" />

create route table
<img width="1671" height="796" alt="image" src="https://github.com/user-attachments/assets/54abe912-f6fe-4bb7-8415-e2dc8246ca12" />

fill the details
<img width="1671" height="796" alt="image" src="https://github.com/user-attachments/assets/17641fe6-da72-452f-b51e-629cb1ec8dfc" />

click subnet association
<img width="1671" height="796" alt="image" src="https://github.com/user-attachments/assets/aab76b15-3ce0-4fb9-848b-b7d95ebe0c0b" />

select subnets for association
<img width="1690" height="625" alt="image" src="https://github.com/user-attachments/assets/c2a67062-fea2-46af-aa3d-e7e0437452f4" />

create internet gateway
<img width="1673" height="600" alt="image" src="https://github.com/user-attachments/assets/4051ac87-3614-4435-abd0-535549604bf6" />

fill details
<img width="1653" height="725" alt="image" src="https://github.com/user-attachments/assets/83d567cf-6eff-4aa1-aedd-2bc5a92e1c92" />

attach vpc with internet gateway
<img width="1687" height="420" alt="image" src="https://github.com/user-attachments/assets/f1bc038b-d71b-4f0b-a975-d2b00fcf271e" />

attached successfully
<img width="1687" height="420" alt="image" src="https://github.com/user-attachments/assets/986bc21c-4c53-4d26-a708-ea122ff4849e" />

Nat
<img width="1671" height="796" alt="image" src="https://github.com/user-attachments/assets/1eb0531c-061b-4346-8264-d5cd6880a61a" />

fill details
<img width="1555" height="736" alt="image" src="https://github.com/user-attachments/assets/2ffdda52-f6ec-489c-85ba-dee236b8c80a" />
<img width="1555" height="736" alt="image" src="https://github.com/user-attachments/assets/57d8076d-9fc6-495a-a5ec-82cbb64d6bc7" />

private route table
<img width="1555" height="736" alt="image" src="https://github.com/user-attachments/assets/88a67d83-02d7-4cc3-8184-42f55c4dfbda" />

add route and nat gateway 
<img width="1678" height="557" alt="image" src="https://github.com/user-attachments/assets/316e7d0c-723c-4d2b-8e5c-db571c0db0d4" />

