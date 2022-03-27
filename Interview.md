

**\*\* Cloud Access Control\*\***

**How would you control access to a cloud network?**

**Restate the Problem - How would I restrict areas in a cloud network to certain sets of rules?**

**Provide a Concrete Example Scenario - In Project 1, did you deploy an on-premises or cloud**

**network?** I deployed a cloud network

**Did you have to configure access controls to this network?**

I did configure access controls to the network using security rules.

**What kinds of access controls did you configure, and why were they necessary?**

I configured a security group and assigned an inbound security rule that allowed ssh to port 22 from the

Red Team virtual network. It was necessary for the DVWA VMs to gain access to ELK through port 22.

**How do these details relate to the interview question?**

They relate because they show how access controls will help an individual to protect their cloud-based

infrastructure by assuring that only authorized persons can work with critical files.

**Explain the Solution Requirements - In Project 1, what kinds of access controls did you have**

**to implement?**

I deployed NSG’s around the ELK VNet and VMs. The local firewalls deployed around the VMs were

embedded in the NSG for the VNet. I also allowed TCP protocols as part of my security rules.

**What did each access control achieve, and why was this restriction necessary for the project?**

\*The NSGs created rules that allow or deny inbound network traffic. It was necessary for the project

because it helped to specify the source, destination, port, and protocols that were needed for this

project.

\* Local firewalls which were embedded in the NSGs helped to eliminate the occurrence of unwanted

network communications and this allowed all legitimate communication for the project to flow freely.

\* The TCP was used to verify the integrity of data traveling between two endpoints which was

necessary for access from the jump box to the DVWAs

**Explain the Solution Details - Which rules do you set for each NSG in the network?**

I allowed inbound traffic to the load balancers by setting the source IP address to 10.1.0.4 and the

destination to the virtual Network. The port was 80 and protocol, TCP. I allowed ssh from my personal IP

to the virtual networks by setting the source IP address to the destination of virtual networks. The port

was set to 22 and protocol set to any. I allowed Elk to be accessible by my PC by setting the source IP

address to 20.112.108.76, the destination to the virtual network. The port was 5601 and protocol was

set to any.

**How does access to the jump box work?**





I accessed the jump box by using ssh and a private key with the jumpbox public IP address.

**How does access from the jump box to the web servers work?**

It works by using ssh and a private key with the webserver’s private address.

**Identify Advantages/Disadvantages of the Solution - Does your solution scale? Is there a**

**better solution than a jump box?**

Jump box is very good but this approach can also expose organizations to enormous risks. If a malicious

user breaches the perimeter, they could navigate through the organization’s networks and resources

without difficulty. Switching to more dynamic methods such as zero trust security, in which all network

traffic is untrusted by default can be a better solution.

**What are the disadvantages of implementing a VPN that kept you from doing it this time?**

\* They require an in-depth understanding of public network security issues and proper deployment

options.

\* Availability and performance depend on factors largely outside of their control.

\* VPNs require accommodation of protocols other than IP and existing internal network technology.

**What are the advantages of a VPN?**

\* A VPN protects private data

\* They potentially give remote and international locations in particular better reach and service quality.

\* VPNs can help avoid data-throttling

**When is it appropriate to use a VPN?**

It is appropriate to use a VPN when protecting data to make sure it can be accessed securely through

various devices


