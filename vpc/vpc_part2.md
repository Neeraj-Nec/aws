# AWS VPC Types

## 1. Default VPC
- Automatically created by AWS in each region.
- Comes with public subnets, internet gateway, route tables, and security groups pre-configured.
- All EC2 instances launched in the default VPC get a public IP by default.
- Suitable for simple setups, testing, or workloads needing internet access.

## 2. Custom VPC
- Created manually by you to meet specific networking needs.
- You can define private and public subnets, custom route tables, NAT gateways, etc.
- Offers better control over security and access (e.g., private subnets for databases).
- No internet access unless explicitly set up with an Internet Gateway.

![vpc part2](https://github.com/Neeraj-Nec/aws/blob/main/images/vpc_4.png)

## Default Configration that you will made to create VPC
 - Create VPC
 - Create Subnet for this VPC
 - Create Internet Table
 - Create route Table
   
![vpc part2](https://github.com/Neeraj-Nec/aws/blob/main/images/vpc_5.png)

