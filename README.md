# AWS-VPC-and-VPC-Peering-Implementation
Implemented AWS VPC Peering to enable secure communication between EC2 instances across two VPCs using, internet gateways , route tables, subnets, and security groups.
# Project Screenshots
## 1 . VPC Creation
![VPC Creation](1-vpc-list.png.png)

In this step, two separate VPCs were created to isolate the network environments. One VPC was configured for testing purposes and the other for production. This setup helps in maintaining secure communication while keeping resources separated. Proper CIDR blocks were assigned to both VPCs.

## 2 . Subnet Creation
![Subnet Creation](2-subnets.png.png)

Subnets were created inside both VPCs to organize resources within different network sections. Each subnet was configured with an appropriate IP range. This step helps in better traffic management and deployment of EC2 instances. Subnets are essential for structuring cloud networks efficiently.

## 3 . Route Tables Configuration
![Route Tables](3-route-tables.png.png)

Route tables were configured to manage traffic flow between the VPC resources. Custom routes were added to ensure communication between different networks. This configuration plays an important role in directing packets correctly. Proper routing is necessary for successful VPC peering.

## 4. Internet Gateways Setup
![Internet Gateways](4-internet-gateways.png.png)

An Internet Gateway was attached to the VPCs to provide internet connectivity. This allows EC2 instances to communicate with external networks when required. It acts as a bridge between AWS resources and the internet. Proper routing was configured to make the gateway functional.

## 5. Peering Connection Active
![Peering Connection Active](5-peering-connection-active.png.png)

A VPC Peering connection was created between the Test and Production VPCs. After configuration, the peering status became active, confirming successful connectivity. This enables secure communication between instances in separate VPCs. It allows private network traffic without using the public internet.

## 6. Test Route Table
![Test Route Table](6-test-routetable.png.png)

The Test VPC route table was configured with the required routes for communication. Routes were added to allow traffic to the Production VPC through the peering connection. This ensures that packets are properly forwarded between both environments. Correct route table configuration is essential for connectivity.

## 7. Prod Route Table
![Prod Route Table](7-prod-routetable.png.png)

The Production VPC route table was configured similarly to establish communication with the Test VPC. Required routes were added through the peering connection. This setup ensures smooth and secure traffic flow between both VPCs. It helps maintain successful bidirectional communication.

## 8. Test Security Group
![Test Security Group](8-test-security-grps.png.png)

The security group for the Test EC2 instance was configured to allow ICMP traffic. This was necessary to perform ping tests between instances. Required inbound rules were added to permit secure communication. Security groups act as virtual firewalls for EC2 instances.

## 9. Prod Security Group
![Prod Security Group](9-prod-security-grp.png.png)

The security group for the Production EC2 instance was configured with the required rules. ICMP traffic was allowed to enable connectivity testing from the Test instance. This configuration ensures secure and controlled access. Proper firewall settings are important for communication between VPCs.

## 10. EC2 Instance
![EC2 Instance](10-ec2-instance.png.png)

EC2 instances were launched inside both the Test and Production VPCs. These instances were used to verify connectivity after the VPC peering setup. Appropriate networking and security configurations were applied. The instances acted as endpoints for communication testing.

## 11. Ping test to prod
![ping test to prod ](11-ping-test-to-prod.png.png)

A ping test was performed from the Test EC2 instance to the Production EC2 instance. The successful response confirmed proper network connectivity. This verified that the VPC peering and route configurations were working correctly. Communication was established successfully between both environments.

## 12 . ping prod to test
![ping prod to test](12-ping-prod-to-test.png.png)

A reverse ping test was performed from the Production EC2 instance to the Test EC2 instance. Successful responses confirmed bidirectional communication between both VPCs. This validated that the peering setup was functioning correctly. The network connection was verified from both sides.
