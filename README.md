# AWS Certified Cloud Practitioner - Notes
Repositório de anotações para estudo da prova AWS Certified Cloud Practitioner.

## Introduction

Problems Solved by Cloud

* Flexibility
* Cost-Effectiviness
* Scalability
* Elasticity
* High Availability and Fault-Tolerance
* Agility

## Pricing

* Compute</br>
    * Pay for computing time

* Storage</br>
    * Pay for data stored in the Cloud

* Data transfer OUT of the Cloud:</br>
    * Data transfer in is free
    
Only Manage application and Data (PaaS)

Which Global Infrastructure is composed of one or more discrete data centers with redundant power, nertworking, and connectiviy and are used to deploy infrastructure

Multi-Tenancy and resource pooling is one of five characteristics of cloud computng, supports multi-tenant model and multiple customers are services from the same physical resources

Five Characteristics of Cloud Computing

On-Demand self service
Multi-tenancy  and resource pooling
Broad network access
Rapid elasticity and scalability
Measured Service

Four points when choosing an AWS Region are:
Compliance with data governance and legal requirements
proximity to customers
available services and features within a Region
pricing

Cloud Computing def: On-demand availability of computer system resources, especially data storage (cloud storage) and computing power, without direct active management by the user

Elaticity def: Automatic and quick ability to acquire resources as you need them and relear resources when you no longer need them


------------------------------------------------------------------------------------

IAM - Identity and Access Managemente, Global Service
root account
users
groups only contains users, not groups

IAM: Permissions
users or groups can be assigned json documents called policies
least privilege principle: dont give more permissions than a user needs

IAM Policies Structure
   Version
   ID
   Statmente

IAM Password Policiers
    variable and different password types
  or
   MFA   - Multi Factor Authentication
    MFA = password you know + security device you own (token)
    
    Virtual MFA device (google authentication and Authy)
   
   IAM Roles for Services
   IAM Role will be just like a user, but instead they will be used by aws services
   EC2 Instance Roles
   Lambda Functions Roles
   Roles for CloudFormation
   
   IAM Securyti Tools
      IAM  Credentials Report (account-level)
      IAM  Access Advior (userlever)
      
 Shared Responsability Model for IAM
 
 AWS
 Infrastructure (global network security)
 Configuration and vulnerability analys
 Compliance validation
 
 You
 Users, Groups, Roles, POlicies management and monitoring
 Enable MFA 
 Rotate your keys
 Use IAM 
 Analsyse patterns
 -----------------------------------------------------
 Amazon EC2
   EC2 = Elastic Cloud Computing
      Renting virtual machine - EC2
      Storing Data on virtual drivers - EBS
      Distribuiting load across machine - ELB
      Scaling the services using an auto-scaling group - ASG
 
 EC2 Instance Types - Compute Optimized - C Series
 Batch Processing workloads
 Media transcoding
 High performance web servers
 High performance computing (HPC)
 scientific modeling & machine learning
 dedicated gaming servers
 
 EC2 Instance Types - Memory Optimized - R Series
 High performance relational non-relation databases
 
 EC2 Instance Types - Storage Optimized - I/G/H Series
 
 Security Groups
 
 Security Groups only contain Allows Rules
   Regulate:
      Access to ports
      Authorised IP Ranges
      Conftrol of inbound/outbound network
      
22 = SSH
21 = FTP
22 = SFTP
80 = HTTP
443 = HHTPS
3389 = RDP
 
EC2 Instances Purschasing Options

   On-Demand Instances: short workload, predictable pricing
   Pay for what you use
      Linux = billing per second after the first minute
      All others OS billing per hour
   Has the highest cost but no upfront payment
   No long-term commitment
   Recommend for short-term and un-interrupted workloads, where you can't predict  how the application will behave
   
Reserved: (Minimum 1 year) 0 Up to 75% discount compared to On-demand
   Reservetion period: 1 year = + discount | 3 years = +++ discount
   Purchase option: no upfront, partial upfront, all upfront
   Reserve a specif insface type
   Recommended for steady-stage usage applications (think database)
   Reserved Instances: long workloads
   
   Convertible Reserved Instances: log workloads with flexible instances
      Up to 54% discount - can change ec2 instance type
      
   Scheduled Reserved Instances: example - every Thursday between 3 and 6pm
      launch within time window you reserve
      when you require a fraction of day / week / month
      still commitment over 1 to 3 years
   
   Spot Instances: short workloads, cheap, can lose instances (less rebliable)
      Highest discount on AWS up to 90%
      Instances that you can "lose" at any point if your max price is less than the current spot price
      The most cost-efficient instance in AWS
      Useful for workloads that are resilient to failure
      batch jobs
      data analysis
      image processing
      any distributed workloads
      NOT SUITABLE FOR CRITICAL JOBS OR DATABASE
      
   Dedicated Hosts: book an entire physical server, control instance placement
      FULLY DEDICATED ENTIRE SERVER DATA CENTER
      Compliance requirements
      user your existing server-bound software licenses
      More expensive

EC2 IMAGE BUILDER
   => Automate the creation, maintain, validate and test EC2 AMIs

EC2 INSTANCE STORE
   BETTER I/O PERFORMANCE
   EC2 INSTANCE STORE LOSE THEIR STORAGE IF STOPPED
   GOOD FOR BUFFER / CACHE / TEMPORARY CONTENT
   RISK OF DATA LOSS IF HARDWARE FAILS
   BACKUP AND REPLICATION ARE YOUR RESPONSABILITY

EBS VOLUMES
   NETWORK DRIVER ATTACHED TO ONE EC2

AMI - CREATE READY-TO-USE EC2 WITH CUSTOMIZATIONS


EFS - ELASTIC FILE SYSTEM
   Managed NFS (netowrk file system) can be mounted on 100s of EC2
   Highly available, scalable, expensive, pay-per-use, no capacity planning

AMAZON FSx for Windows File Server
   SMB Protocol

AMAZON FSx for Lustre
   HPC - Luste is Linux and Cluster
   Machine Learning, analystics, financial modeling

==================================================

ELB & ASG - ELASTIC LOAD BALANCING & AUTO SCALING GROUPS

   Scalability - Application/System can handle greater loads by adapting
      Vertical Scalability
      Horizontal Scalability = elasticity

   VERTICAL SCALABILITY - increase the size of instance
      non-distributed system, such as database
      limit how much you can vertically scale
   
   HORIZONTAL SCALABILITY - increase the number os instances
      
   HIGH AVAILABILITY - means running your application in at least 2 AZ
      load balance in multi az

   ELASTIC LOAD BALANCING
      server that forward internet traffic to multiple ec2 instances
      Application Load Balancer (HTTP/HTTPs only) - Layer 7
      Network Load Balancer (ultra high performance, allows for TCP) - Layer 4
      Classic Load Balancer (slowly retiring)
   
   HIGH AVAILABILITY
      application thriving even in case of a disaster