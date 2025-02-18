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
 - Create Internet gateway
 - Create route Table
   
![vpc part2](https://github.com/Neeraj-Nec/aws/blob/main/images/vpc_5.png)

## 3. Public Subnet vs. Private Subnet

### **Public Subnet**
A **public subnet** is a subnet in a VPC that has direct access to the internet. It is used for resources that need to communicate with the outside world, such as web servers.

#### **Characteristics:**
- Associated with a **route table** that has a route to the **Internet Gateway (IGW)**.
- Instances in a public subnet can have a **public IP** or **Elastic IP** to allow internet access.
- Used for resources that need to be accessible from the internet, such as web servers and bastion hosts.

### **Private Subnet**
A **private subnet** is a subnet that does **not** have direct access to the internet. It is used for resources that should not be publicly accessible, such as databases and internal services.

#### **Characteristics:**
- No direct route to an **Internet Gateway (IGW)**.
- Instances do **not** receive public IP addresses.
- To access the internet, instances can use a **NAT Gateway (Network Address Translation)** or **NAT Instance** in a public subnet.
- Used for backend services like **databases, application servers, and internal APIs**.

### **Difference Between Public and Private Subnet**

| Feature            | Public Subnet | Private Subnet |
|--------------------|--------------|---------------|
| **Internet Access** | Direct internet access via Internet Gateway | No direct access; needs NAT Gateway or VPN |
| **Public IP** | Instances can have public IPs | Instances do not have public IPs |
| **Use Case** | Web servers, Bastion hosts | Databases, internal services |
| **Route Table** | Has a route to the Internet Gateway | No route to the Internet Gateway |
| **Security** | More exposed, needs tight security | More secure, restricted from public access |


![VPC Subnet](https://github.com/Neeraj-Nec/aws/blob/main/images/vpc_6.png)

