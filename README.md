# Virtual Private Cloud

![image](https://user-images.githubusercontent.com/110126036/187456964-a0f792dd-aae3-4182-a79d-9d9b435566d4.png)

## What is a VPC?

A VPC is a virtual network that works in the same way as a traditional network operated in a data centre. 

## What is CIDR?

Stands for Classless Inter-Domain Routing and is a method for allocating IP addresses and IP routing.

## What is a Subnet?

A subnet, or subnetwork, is a network inside a network. Subnets make networks more efficient. Through subnetting, network traffic can travel a shorter distance without passing through unnecessary routers to reach its destination.

A subnet must reside in a single availability zone.

### Public Subnets

A public subnet has a route to the internet gateway and therefore have public IPv4 addresses (so they can be accessed through the internet). The Internet Gateway is what allows the VPC to connect to the internet.

### Private Subnets

A private subnet does not have a route to the internet gateway. They however can send requests to the internet with the use of a NAT gateway, predominantly used to retrieve software updates. They are also able to communicate with other instances within the VPC.

## Routing Tables

Route tables are responsible for directing incoming traffic which come into the VPC.

### Custom Route Table

A custom route table is associated with the public subnet. It allows for the communication with other instances inside the VPC over IPv4 and also an entry which enables instances to directly connect to the internet.

### Main Route Table

A main route table is the same as a custom route table except that the direct communication to the internet is prohibited and are also for private subnets. The internet can be reached indirectly through a NAT gateway.

## Security

### NACL vs Security Groups

NACL works as a firewall on the subnet level whereas security groups work as a firewall on the instance level.

NACL stands for: Network Access Control List

## Stateless vs Stateful

Stateless applications dont store data whereas stateful applications require backing storage.

![image](https://user-images.githubusercontent.com/110126036/187658061-e8959dd7-19c2-4ce3-a62a-7b0671d9d950.png)
