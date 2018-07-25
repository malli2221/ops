Amazon Elastic Compute Cloud:
Amazon EC2 provides scalable computing capacity in the Amazon Web Services (AWS) cloud. Using Amazon EC2 eliminates your need to invest in hardware up front, so you can develop and deploy applications faster. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic.

Features of Amazon EC2:
        
Virtual computing environments, known as instances.                
Various configurations of CPU, memory, storage, and networking capacity for your instances, known as instance types.
Storage volumes for temporary data that's deleted when you stop or terminate your instance, known as instance store volumes.
Persistent storage volumes for your data using Amazon Elastic Block Store known as Amazon EBS volumes.    
A firewall that enables you to specify the protocols, ports, and source IP ranges that can reach your instances using security groups.    
Static IPv4 addresses for dynamic cloud computing, known as Elastic IP addresses
Virtual networks you can create that are logically isolated from the rest of the AWS cloud, and that you can optionally connect to your own network, known as virtual private clouds (VPCs).
Types of EC2 Instances:
Instance types comprise varying combinations of CPU, memory, storage, and networking capacity and give you the flexibility to choose the appropriate mix of resources for your applications.
a)General purpose:
T2 instances are Burstable Performance Instances that provide a baseline level of CPU performance with the ability to burst above the baseline.
M5 instances are the latest generation of General Purpose Instances. This family provides a balance of compute, memory, and network resources, and it is a good choice for many applications.
b)Compute Optimized:
C5 instances are optimized for compute-intensive workloads and deliver very cost-effective high performance at a low price per compute ratio.
2. C4 instances are optimized for compute-intensive workloads and deliver very cost-effective high performance at a low price per compute ratio.
c)Memory Optimized:
X1e instances are optimized for high-performance databases, in-memory databases and other memory intensive enterprise applications. X1e instances offer one of the lowest price per GiB of RAM among Amazon EC2 instance types.
R4 instances are optimized for memory-intensive applications and offer better price per GiB of RAM than R3.
d) Accelerated Computing:
P3 instances are the latest generation of general purpose GPU instances.
P2 instances are intended for general-purpose GPU compute applications.
G3 instances are optimized for graphics-intensive applications.
F1 instances offer customizable hardware acceleration with field programmable gate arrays (FPGAs).
e) Storage Optimized
H1 instances feature up to 16 TB of HDD-based local storage, deliver high disk throughput, and a balance of compute and memory.
I3 instance family provides Non-Volatile Memory Express (NVMe) SSD-backed instance storage optimized for low latency, very high random I/O performance, high sequential read throughput and provide high IOPS at a low cost.  I3 also offers Bare Metal instances (i3.metal), powered by the Nitro System, for non-virtualized workloads, workloads that benefit from access to physical resources, or workloads that may have license restrictions.
D2 instances feature up to 48 TB of HDD-based local storage, deliver high disk throughput, and offer the lowest price per disk throughput performance on Amazon EC2.

Instance Categories:
                                               
1) On-Demand Instances:
Pay for the instances that you use by the second, with no long-term commitments or upfront payments. With On-Demand instances, you pay for compute capacity by per hour or per second depending on which instances you run. 
2) Reserved Instances:                    
Make a low, one-time, up-front payment for an instance, reserve it for a one- or three-year term, and pay a significantly lower hourly rate for these instances. 
3) Spot Instances:                    
Request unused EC2 instances, which can lower your costs significantly.
Tags:
A tag is a label that you assign to an AWS resource. Each tag consists of a key and an optional value, both of which you define. 
Elastic IP:
An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is associated with your AWS account. With an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account.


