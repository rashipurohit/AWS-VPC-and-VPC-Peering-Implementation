# AWS VPC and VPC Peering Implementation

## Project Overview
This project demonstrates the implementation of AWS VPC Peering to establish secure communication between EC2 instances located in two different VPCs.

The setup includes:

- Creation of two VPCs (Test and Production)
- Public subnets configuration
- Internet Gateway attachment
- Route table configuration
- Security Group inbound rules setup
- VPC Peering Connection establishment
- Route propagation for communication
- Successful ICMP (Ping) connectivity test between EC2 instances

## Architecture Components

### VPCs
- test-vpc-project
- prod-vpc-project

### Networking Components
- Public Subnets
- Route Tables
- Internet Gateways
- Security Groups
- VPC Peering Connection

## Connectivity Test
Successful ping communication was established between EC2 instances across different VPCs using private IP addresses.

## Screenshots Sequence

1. VPC Creation
2. Subnet Creation
3. Internet Gateway Configuration
4. Route Tables Setup
5. Security Group Rules Configuration
6. VPC Peering Connection Creation
7. Route Table Updates for Peering
8. EC2 Instances Running
9. Ping Test from Test → Prod
10. Ping Test from Prod → Test

## Outcome
Successfully implemented secure cross-VPC communication using AWS VPC Peering.
