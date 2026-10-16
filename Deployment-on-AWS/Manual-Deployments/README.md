# Three-Tier Wordpress Site Deployment on AWS

## Project Overview
This project aims to deployment of a wordpress site on Amazon Web Services (AWS) using a custom Virtual Private Cloud(VPC), multiple EC2 instances, an Application load balance, and a private MYSQL database. 

## What Is Three-Tier Architecture?
Three-tier architecture separates an application into three logical layers:
 - **Presentation Tier:** The user-facing interface that receives and displays requests.
 - **Application Tier:** The application logic that processes requets and communicates with the data tier.
 - **Data Tier:** The database or storage layer that persists application data.
   
## Project Objectives
 - Design a custom AWS VPC with public and private subnets.
 - Configure an Internet Gateway and NAT Gateway.
 - Deploy two WordPress frontend EC2 instances.
 - Deploy a MySQL database on a private EC2 instance.
 - Configure an internet-facing Application Load Balancer.
 - Restrict network access using security groups.
 - Configure shared storage for WordPress media uploads.
 - Validate application availability and frontend failover.
 - Document the deployment process, testing results, and troubleshooting steps.
 - Maintain a structured Git history using feature branches and meaningful commits.

## Architecture
The planned architecture contains the following components:

 - User: Accesses the WordPress website through a web browser.
 - Internet Gateway: Provides internet connectivity to resources in the public subnet when routing and security rules permit it.
 - Application Load Balancer: Receives incoming HTTP/HTTPS requests and distributes them across healthy frontend instances.
 - Frontend EC2 Instance 1: Hosts Apache, PHP, and WordPress.
 - Frontend EC2 Instance 2: Hosts the same WordPress application and connects to the same database.
 - Private Database EC2 Instance: Hosts MySQL and stores WordPress application data.
 - NAT Gateway: Allows supported outbound internet connections from private-subnet resources without exposing them to unsolicited inbound internet connections.
 - Shared Storage: Planned shared storage for WordPress media files so that both frontend instances can access the same uploads.

## Architecture Diagram

<img width="1291" height="622" alt="architecture" src="https://github.com/user-attachments/assets/c1343fcf-57e9-47ca-817e-7fd699acc966" />

