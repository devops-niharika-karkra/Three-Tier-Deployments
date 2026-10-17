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

subnet created 
<img width="815" height="660" alt="image" src="https://github.com/user-attachments/assets/0b86dbfa-7f59-40eb-8a36-3d10d24db774" />

