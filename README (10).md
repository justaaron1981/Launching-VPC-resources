<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Launching VPC Resources

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-ec2)

**Author:** Aaron  
**Email:** justaaron1981@yahoo.com

---

## Launching VPC Resources

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-ec2_8ee57662)

---

## Introducing Today's Project!

### What is Amazon VPC?

IT allows you to create a logically isolated section within the AWS Cloud where you can launch AWS resources in a virtual network you define.

### How I used Amazon VPC in this project

I used Amazon VPC to create my own VPC with different resources (e.g security groups, network ACLs) private resources (e.g. a private subnet) and EC2 instances in both my public and private subnets

### One thing I didn't expect in this project was...

I didn't expect the resource map to be visual and interactive. It was a faster way of setting up an entire VPC architecture.

### This project took me...

this project took 2 and a half hours

---

## Setting Up Direct VM Access

Directly accessing a virtual machine means logging into and managing the operating system or software of the machine as if you were using it in front of you, but over the internet.

### SSH is a key method for directly accessing a VM

SSH trafic or Secure Shell is the protocol we use for this secure access to a remote machine. When you connect to the instance, SSH verifies you possess the correct private key corresponding to the public key on the server, ensuring only authorized users can access the instance.

### To enable direct access, I set up key pairs

Key pairs help engineers directly access their virtual machines, like EC2 instances.

The specific way a private key, used for encryption and decryption, is stored and structured within a file

my private key's file format .pem format, which stands for Privacy Enhanced Mail. 

---

## Launching a public server

I had to change my EC2 instance's networkings settings by changing the default VPC to one I created 

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-ec2_88727bef)

---

## Launching a private server

My private server has it's own dedicated security group  to enhance security by controlling network traffic and isolating it from other resources. This dedicated security group acts like a firewall, allowing only authorized traffic to reach the server and preventing unauthorized access. 

My private server's security group's source is nextwork public security group which means only SSH traffic from the resource in side the security group would be allowed

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-ec2_4a9e8014)

---

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I used the VPC and more option which give a resource map to use when creating the VPC and all it's components e.g. security groups, internet gateways and route tables.

A VPC resource map is a visual diagram that maps my VPC's components and relationships/connections between them. A resource map is interactive i.e it will highlight the connections relevant to the resource I highlight

My new VPC has a CIDR block of 10.0.0.0/16 It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because VPC are already isolated from each other still this not best practice especially if we need VPC peering

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-ec2_1cbb1b88)

---

## Speeding up VPC creation

### Tips for using the VPC resource map

When determining the number of public subnets in my VPC, I only had two options: either none or one in each availability zone.  This was because best practice (improves redundancy and high availability) at least subnet/AZ

The set up page also offered to create NAT gateways, which are connectors/gateways that will let resources in my private subnet get access to the internet (e.g, security updates) while still blocking off incoming traffic from the internet.

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-ec2_8ee57662)

---

---
