1. If I want my instance to run on a single-tenant hardware, which value do I have to set the instance’s tenancy attribute to?

    a. dedicated
    
    b. isolated
    
    c. one
    
    d. reserved

    Đáp án: A

2. You have a video transcoding application running on Amazon EC2. 
Each instance polls a queue to find out which video should be transcoded, and then runs a transcoding process. If this process is interrupted, the video will be transcoded by another instance based on the queuing system. You have a large backlog of videos, which need to be transcoded, and would like to reduce this backlog by adding more instances. You will need these instances only until the backlog is reduced. Which type of Amazon EC2 instances should you use to reduce the backlog in the most cost efficient way?
   
   a. Reserved instances
   
   b. Spot instances
   
   c. Dedicated instances
   
   d. On-demand instances
   
   Đáp án: B
   
3. The one-time payment for Reserved Instances is __________ refundable if the reservation is cancelled.
   
   a. always
   
   b. in some circumstances
   
   c. never
   
   Đáp án: C
   
4. You run a web application where web servers on EC2 Instances are In an 
Auto Scaling group Monitoring over the last 6 months shows that 6 web servers are necessary to handle the minimum load. During the day up to 12 servers are needed Five to six days per year, the number of web servers required might go up to 15. What would you recommend to minimize costs while being able to provide hill availability?
    
    a. 6 Reserved instances (heavy utilization). 6 Reserved instances (medium utilization), rest covered by On-Demand instances
    
    b. 6 Reserved instances (heavy utilization). 6 On-Demand instances, rest covered by Spot Instances 
   
    c. 6 Reserved instances (heavy utilization) 6 Spot instances, rest covered by On-Demand instances 
    
    d. 6 Reserved instances (heavy utilization) 6 Reserved instances (medium utilization) rest covered by Spot instances 
    
    Đáp án: A. Spot Instance ko đảm bảo tính Available
    
5. A user is running one instance for only 3 hours every day. The user wants to save some cost with the instance. Which of the below mentioned Reserved Instance categories is advised in this case?
    
    a. The user should not use RI; instead only go with the Scheduled Reserved instances 
    
    b. The user should use the AWS high utilized RI
    
    c. The user should use the AWS medium utilized RI
    
    d. The user should use the AWS low utilized RI    
    
    Đáp án: A
6. You have a distributed application that periodically processes large volumes of data across multiple Amazon EC2 Instances. The application is designed to recover gracefully from Amazon EC2 instance failures. You are required to accomplish this task in the most cost-effective way. Which of the following will meet your requirements?
   
   a. Spot Instances
   
   b. Reserved instances
   
   c. Dedicated instances
   
   d. On-Demand instances
   
   Đáp án: A
   
   
7. Can I move a Reserved Instance from one Region to another?
   
   a. No
   
   b. Only if they are moving into GovCloud
   
   c. Yes
   
   d. Only if they are moving to US East from another region 
     
   Đáp án: A
     
8. An application you maintain consists of multiple EC2 instances in a default tenancy VPC. This application has undergone an internal audit and has been determined to require dedicated hardware for one instance. Your compliance team has given you a week to move this instance to single-tenant hardware. Which process will have minimal impact on your application while complying with this requirement?
    
    a. Create a new VPC with tenancy=dedicated and migrate to the new VPC
    
    b. Use ec2-reboot-instances command line and set the parameter “dedicated=true”
    
    c. Right click on the instance, select properties and check the box for dedicated tenancy
    
    d. Stop the instance, create an AMI, launch a new instance with tenancy=dedicated, and terminate the old instance     
    
    Đáp án: D
    
    Có 2 cách để tạo 1 dedicated instance:
        
        - tạo VPC với tenancy = dedicated => tất cả EC2 trong VPC này sẽ mặc định dedicated
        
        - tạo 1 EC2 mới trong default VPC với tenancy = dedicated.
        
9. A user is launching an EC2 instance in the US East region. Which of the below mentioned options is recommended by AWS with respect to the selection of the availability zone?
   
   a. Always select the US-East-1-a zone for HA
   
   b. Do not select the AZ; instead let AWS select the AZ
   
   c. The user can never select the availability zone while launching an instance
   
   d. Always select the AZ while launching an instance  
         
   Đáp án: B
   
10. You have multiple Amazon EC2 instances running in a cluster across multiple Availability Zones within the same region. What combination of the following should be used to ensure the highest network performance (packets per second), lowest latency, and lowest jitter? Choose 3 answers
    
    a. Amazon EC2 placement groups 
    
    b. Enhanced networking 
    
    c. Amazon PV AMI 
    
    d. Amazon HVM AMI
    
    e. Amazon Linux 
    
    f. Amazon VPC 
    
    Đáp án: B, D, F
    
    Yêu cầu để triển khai Enhanced network:
    
        - VPC
        - HVM
        - Ec2 loại: C3, C4, D2, I2, M4 hoặc M3
    
    Placement group chỉ hoạt động trong 1 AZ
    
11. The researchers must process massive amounts of data and run statistics. Which one of the following options provides the high performance computing for this purpose.
    
    a. Configure an Autoscaling Scaling group to launch dozens of spot instances to run the statistical analysis simultaneously
    
    b. Launch AMI instances that support SR-IOV in a single Availability Zone
    
    c. Launch compute optimized (C4) instances in at least two Availability Zones
    
    d. Launch enhanced network type instances in a placement group
    
    Đáp án: D
    
    
12. Regarding the attaching of ENI to an instance, what does ‘warm attach’ refer to?
    
    a. Attaching an ENI to an instance when it is stopped
    
    b. Attaching an ENI to an instance when it is running
    
    c. Attaching an ENI to an instance during the launch process
    
    Đáp án: A.
    
    ENI can be attached to an instance when 
    
    - it’s running (hot attach), 
    - when it’s stopped (warm attach), 
    - when the instance is being launched (cold attach).
    
13. A user has created a VPC with a public subnet. The user has terminated all the instances, which are part of the subnet. Which of the below mentioned statements is true with respect to this scenario?
    
    a. The user cannot delete the VPC since the subnet is not deleted
    
    b. All network interface attached with the instances will be deleted
    
    c. When the user launches a new instance it cannot use the same subnet
    
    d. The subnet to which the instances were launched with will be deleted    
    
    Đáp án: B
    
    
14. Your system automatically provisions EIPs to EC2 instances in a VPC on boot. The system provisions the whole VPC and stack at once. You have two of them per VPC. On your new AWS account, your attempt to create a Development environment failed, after successfully creating Staging and Production environments in the same region. What happened?
    
    a. You didn’t choose the Development version of the AMI you are using.
    
    b. You didn’t set the Development flag to true when deploying EC2 instances.
    
    c. You hit the soft limit of 5 EIPs per region and requested a 6th. 
    
    d. You hit the soft limit of 2 VPCs per region and requested a 3rd.
    
    Đáp án: C. Vì public IP là tài nguyên có hạn, có limit 5 EIP/region
    
15. An organization has created multiple components of a single application for compartmentalization. Currently all the components are hosted on a single EC2 instance. Due to security reasons the organization wants to implement two separate SSLs for the separate modules although it is already using VPC. How can the organization achieve this with a single instance?
    
    a. Create a VPC instance, which will have both the ACL and the security group attached to it and have separate rules for each IP address.
    
    b. Create a VPC instance, which will have multiple network interfaces with multiple elastic IP addresses.
    
    c. You have to launch two instances each in a separate subnet and allow VPC peering for a single IP.
    
    d. Create a VPC instance, which will have multiple subnets attached to it and each will have a separate IP address.    
    
    Đáp án: B.
    
    Các use case của ENI:
    
    - Management network: sử dụng 1 secondary ENI cho traffic vào từ internet và primary ENI cho
     back-end traffic.
     
        ![](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/EC2_ENI_management_network.png) 
    
    - Load balance, NAT, proxy server
    - Low Budget High Availability Solution: If the instance fails, you (or more likely, the code running on your behalf) can attach the network interface to a hot standby instance. Because the interface maintains its private IP addresses, Elastic IP addresses, and MAC address, network traffic begins flowing to the standby instance as soon as you attach the network interface to the replacement instance. Users experience a brief loss of connectivity between the time the instance fails and the time that the network interface is attached to the standby instance, but no changes to the VPC route table or your DNS server are required.
    
16. Select the incorrect statement
    
    a. In Amazon EC2, the private IP addresses only returned to Amazon EC2 when the instance is stopped or terminated
    
    b. In Amazon VPC, an instance retains its private IP addresses when the instance is stopped.
    
    c. In Amazon VPC, an instance does NOT retain its private IP addresses when the instance is stopped
    
    d. In Amazon EC2, the private IP address is associated exclusively with the instance for its lifetime    
    
    Đáp án: C. 
    
    - EC2-VPC: khi restart, reboot: giữ nguyên private IP, đổi public IP (trừ khi nó là EIP) 
    - EC2-Classic: restart: thay đổi private IP và public IP
     
17. What is a placement group?
    
    a. A collection of Auto Scaling groups in the same Region
    
    b. Feature that enables EC2 instances to interact with each other via high bandwidth, low latency connections
    
    c. A collection of Elastic Load Balancers in the same Region or Availability Zone
    
    d. A collection of authorized Cloud Front edge locations for a distribution     
    
    Đáp án: B
    
18. In order to optimize performance for a compute cluster that requires low inter-node latency, which feature in the following list should you use?
    
    a. AWS Direct Connect
    
    b. Placement Groups
    
    c. VPC private subnets
    
    d. EC2 Dedicated Instances
    
    e. Multiple Availability Zones 
       
    Đáp án B.
    
19. What is required to achieve gigabit network throughput on EC2? You already selected cluster-compute, 10GB instances with enhanced networking, and your workload is already network-bound, but you are not seeing 10 gigabit speeds.
    
    a. Enable biplex networking on your servers, so packets are non-blocking in both directions and there’s no switching overhead.
    
    b. Ensure the instances are in different VPCs so you don’t saturate the Internet Gateway on any one VPC.
    
    c. Select PIOPS for your drives and mount several, so you can provision sufficient disk throughput
    
    d. Use a placement group for your instances so the instances are physically near each other in the same Availability Zone. 
    
    Đáp án: D. 10GB speeed chỉ đc đảm bảo trong Placement group
    
20. You need the absolute highest possible network performance for a cluster computing application. You already selected homogeneous instance types supporting 10 gigabit enhanced networking, made sure that your workload was network bound, and put the instances in a placement group. What is the last optimization you can make?
    
    a. Use 9001 MTU instead of 1500 for Jumbo Frames, to raise packet body to packet overhead ratios. (For instances that are collocated inside a placement group, jumbo frames help to achieve the maximum network throughput possible, and they are recommended in this case)
    
    b. Segregate the instances into different peered VPCs while keeping them all in a placement group, so each one has its own Internet Gateway.
    
    c. Bake an AMI for the instances and relaunch, so the instances are fresh in the placement group and do not have noisy neighbors
    
    d. Turn off SYN/ACK on your TCP stack or begin using UDP for higher throughput.    
    
    Đáp án A:
    
    - MTU: maximum transmission unit: là dung lượng max của 1 package khi đc truyền tải trong network
    - Jumbo frame: 9001 MTU: chỉ ở trong 1 mạng VPC, hoặc VPC peering hoặc EC2-classic. Ra ngoài internet => lại về 1500 MTU
    - normal: 1500 MTU
    
21. A user has launched an EC2 instance from an instance store backed AMI. The infrastructure team wants to create an AMI from the running instance. Which of the below mentioned credentials is not required while creating the AMI?
    
    a. AWS account ID
    
    b. 509 certificate and private key
    
    c. AWS login ID to login to the console
    
    d. Access key and secret access key
    
    Đáp án C: http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/creating-an-ami-instance-store.html
    Chúng ta ko dùng AWS Console để tạp AMI từ instance store EC2.
    
22. A user has launched an EC2 Windows instance from an instance store backed AMI. The user wants to convert the AMI to an EBS backed AMI. How can the user convert it?
    
    a. Attach an EBS volume to the instance and unbundle all the AMI bundled data inside the EBS
    
    b. A Windows based instance store backed AMI cannot be converted to an EBS backed AMI
    
    c. It is not possible to convert an instance store backed AMI to an EBS backed AMI
    
    d. Attach an EBS volume and use the copy command to copy all the ephemeral content to the EBS Volume
    
    Đáp án: B
    
23. A user has launched two EBS backed EC2 instances in the US-East-1a region. The user wants to change the
    zone of one of the instances. How can the user change it?
    
    A.
    Stop one of the instances and change the availability zone
    
    B.
    The zone can only be modified using the AWS CLI
    
    C.
    From the AWS EC2 console, select the Actions – > Change zones and specify new zone
    
    D.
    Create an AMI of the running instance and launch the instance in a separate AZ
    
    Đáp án D: Zone được chọn khi launch EC2, ko chọn thì AWS pick. Sau khi launch ko thể thay đổi
    
24. A user has launched a large EBS backed EC2 instance in the US-East-1a region. The user wants to achieve Disaster Recovery (DR) for that instance by creating another small instance in Europe. How can the user achieve DR?
    
    a. Copy the running instance using the “Instance Copy” command to the EU region
    
    b. Create an AMI of the instance and copy the AMI to the EU region. Then launch the instance from the EU AMI
    
    c. Copy the instance from the US East region to the EU region
    
    d. Use the “Launch more like this” option to copy the instance from one region to another
    
    Đáp án: B, như câu trên
    
25. A user has launched an EC2 instance store backed instance in the US-East-1a zone. The user created AMI #1 and copied it to the Europe region. After that, the user made a few updates to the application running in the US-East-1a zone. The user makes an AMI#2 after the changes. If the user launches a new instance in Europe from the AMI #1 copy, which of the below mentioned statements is true?
    
    a. The new instance will have the changes made after the AMI copy as AWS just copies the reference of the original AMI during the copying. Thus, the copied AMI will have all the updated data
    
    b. The new instance will have the changes made after the AMI copy since AWS keeps updating the AMI
    
    c. It is not possible to copy the instance store backed AMI from one region to another
    
    d. The new instance in the EU region will not have the changes made after the AMI copy    
    
    Đáp án D: 
    
    
26. George has shared an EC2 AMI created in the US East region from his AWS account with Stefano. George copies the same AMI to the US West region. Can Stefano access the copied AMI of George’s account from the US West region?
    a. No, copy AMI does not copy the permission
    
    b. It is not possible to share the AMI with a specific account
    
    c. Yes, since copy AMI copies all private account sharing permissions
    
    d. Yes, since copy AMI copies all the permissions attached with the AMI    
    
    Đáp án: A
    
27. EC2 instances are launched from Amazon Machine images (AMIS). A given public AMI can:
    be used to launch EC2 Instances in any AWS region.
    
    a. only be used to launch EC2 instances in the same country as the AMI is stored.
    
    b. only be used to launch EC2 instances in the same AWS region as the AMI is stored. 
    
    c. only be used to launch EC2 instances in the same AWS availability zone as the AMI is stored.
    
    Đáp án: B. “AMIs are a regional resource. Therefore, sharing an AMI makes it available in that region. To make an AMI available in a different region, copy the AMI to the region and then share it.”
    
28. A t2.medium EC2 instance type must be launched with what type of Amazon Machine Image (AMI)?
    
    a. An Instance store Hardware Virtual Machine AMI
    
    b. An Instance store Paravirtual AMI
    
    c. An Amazon EBS-backed Hardware Virtual Machine AMI
    
    d. An Amazon EBS-backed Paravirtual AMI 
       
    Đáp án: C
    
    ![](https://i0.wp.com/jayendrapatil.com/wp-content/uploads/2016/04/screen-shot-2016-04-15-at-7-06-50-am.png?w=1312)   
    
29. You have identified network throughput as a bottleneck on your m1.small EC2 instance when uploading data Into Amazon S3 In the same region. How do you remedy this situation? 

    a. Add an additional ENI
    
    b. Change to a larger Instance
    
    c. Use DirectConnect between EC2 and S3
    
    d. Use EBS PIOPS on the local volume   
     
    Đáp án: B. 
     
30. What does Amazon EC2 provide?
    
    a. Virtual servers in the Cloud
    
    b. A platform to run code (Java, PHP, Python), paying on an hourly basis.
    
    c. Computer Clusters in the Cloud.
    
    d. Physical servers, remotely managed by the customer.
    
31. A user has enabled termination protection on an EC2 instance. The user has also set Instance initiated shutdown behavior to terminate. When the user shuts down the instance from the OS, what will happen?
    
    a. The OS will shutdown but the instance will not be terminated due to protection
    
    b. It will terminate the instance
    
    c. It will not allow the user to shutdown the instance from the OS
    
    d. It is not possible to set the termination protection when an Instance initiated shutdown is set to Terminate
    
    Đáp án: B. Termination protection bị vô hiệu trong các trường hợp:
        
        - EC2 thuộc auto scaling group
        - spot instance (sống chết phụ thuộc vào AWS)
        - shutting down behavior là terminate

32. A user has launched an EC2 instance and deployed a production application in it. The user wants to prohibit any mistakes from the production team to avoid accidental termination. How can the user achieve this?
    
    a. The user can the set DisableApiTermination attribute to avoid accidental termination
    
    b. It is not possible to avoid accidental termination
    
    c. The user can set the Deletion termination flag to avoid accidental termination
    
    d. The user can set the InstanceInitiatedShutdownBehavior flag to avoid accidental termination        
    
    Đáp án: A
    
33. You have been doing a lot of testing of your VPC Network by deliberately failing EC2 instances to test whether instances are failing over properly. Your customer who will be paying the AWS bill for all this asks you if he being charged for all these instances. You try to explain to him how the billing works on EC2 instances to the best of your knowledge. What would be an appropriate response to give to the customer in regards to this?
    a. Billing commences when Amazon EC2 AMI instance is completely up and billing ends as soon as the instance starts to shutdown.
    
    b. Billing commences when Amazon EC2 initiates the boot sequence of an AMI instance and billing ends when the instance shuts down.
    
    c. Billing only commences only after 1 hour of uptime and billing ends when the instance terminates.
    
    d. Billing commences when Amazon EC2 initiates the boot sequence of an AMI instance and billing ends as soon as the instance starts to shutdown.    
    
    Đáp án: B
    
    
34. How can software determine the public and private IP addresses of the Amazon EC2 instance that it is running on?
    
    a. Query the local instance metadata
    
    b. Query the appropriate Amazon CloudWatch metric.
    
    c. Query the local instance userdata.
    
    d. Use ipconfig or ifconfig command.    
    
    Đáp án: A.
    
        - user-data: what should I do?
        - metadata: who am I?
    
35. The base URI for all requests for instance metadata is ___________
    
    a. http://254.169.169.254/latest/
    
    b. http://169.169.254.254/latest/
    
    c. http://127.0.0.1/latest/
    
    d. http://169.254.169.254/latest/    
    
    Đán án: D
    
36. Which Amazon Elastic Compute Cloud feature can you query from within the instance to access instance properties?
    
    a. Instance user data
    
    b. Resource tags
    
    c. Instance metadata
    
    d. Amazon Machine Image 
    
    Đáp án: C. Cả user-data và meta-data đều có thể được access từ EC2 nhưng câu hỏi đang nói về instance properties.
    
37. You need to pass a custom script to new Amazon Linux instances created in your Auto Scaling group. Which feature allows you to accomplish this?
    
    a. User data
    
    b. EC2Config service
    
    c. IAM roles
    
    d. AWS Config
        
    Đáp án: A. EC2 config đc cài trên window
    
38.You are responsible for a legacy web application whose server environment is approaching end of life. You would like to migrate this application to AWS as quickly as possible, since the application environment currently has the following limitations: The VM’s single 10GB VMDK is almost full. The virtual network interface still uses the 10Mbps driver, which leaves your 100Mbps WAN connection completely underutilized. It is currently running on a highly customized Windows VM within a VMware environment: You do not have the installation media. This is a mission critical application with an RTO (Recovery Time Objective) of 8 hours. RPO (Recovery Point Objective) of 1 hour. How could you best migrate this application to AWS while meeting your business continuity requirements?
   
   a. Use the EC2 VM Import Connector for vCenter to import the VM into EC2
   
   b. Use Import/Export to import the VM as an EBS snapshot and attach to EC2. (Import/Export is used to transfer large amount of data)
   
   c. Use S3 to create a backup of the VM and restore the data into EC2.
   
   d. Use the ec2-bundle-instance API to Import an Image of the VM into EC2 (only bundles an windows instance store instance)    
   
   Đáp án: A
   
39**. You are tasked with moving a legacy application from a virtual machine running inside your datacenter to an Amazon VPC. 
Unfortunately this app requires access to a number of on-premises services and no one who configured the app still works for your company. Even worse there’s no documentation for it. What will allow the application running inside the VPC to reach back 
and access its internal dependencies without 
being reconfigured? (Choose 3 answers)
      
  a. An AWS Direct Connect link between the VPC and the network housing the internal services (VPN or a DX for communication)
  
  b. An Internet Gateway to allow a VPN connection. (Virtual and Customer gateway is needed)
  
  c. An Elastic IP address on the VPC instance (Don’t need a EIP as private subnets can also interact with on-premises network)
  
  d. An IP address space that does not conflict with the one on-premises (IP address cannot conflict)
  
  e. Entries in Amazon Route 53 that allow the Instance to resolve its dependencies’ IP addresses (Route 53 is not required)
  
  f. A VM Import of the current virtual machine (VM Import to copy the VM to AWS as there is no documentation it can’t be configured from scratch)   
  
  Đáp án: A, F, D
  
  A. An AWS Direct Connect link between the VPC and the network housing the internal services. — correct, you could use this to have the instance you migrated into the VPC communicate back to the legacy on-prem servers. (You could also use a VPN instead of a circuit if you wanted)
  
  B. An Internet Gateway to allow a VPN connection. — incorrect, you don’t need an IGW to build a VPN back to your on-prem data center
  
  C. An Elastic IP address on the VPC instance. — incorrect, there is nothing in the question to indicate anything needs to communicate over the Internet, it could all be internal traffic only.
  
  D. An IP address space that does not conflict with the one on-premises. — correct, you would totally need to make sure there were no private IP conflicts between your VPC CIDR and your internal on-prem networks if you wanted the instance in the VPC to talk to the legacy on-prem servers.
  
  E. Entries in Amazon Route 53 that allow the Instance to resolve its dependencies’ IP addresses. –incorrect… You could have your instance use hard-coded private IP addresses to communicate to the on-prem servers, thus removing DNS from the equation entirely. If you did choose to use DNS to resolve them (which is probably better than hard-coded private IP addresses), you still wouldn’t wouldn’t want to do a zone transfer and configure those DNS entries in Route53. You’d just point your VPC instance to your on-prem DNS server, or alternatively set up a bind instance in your VPC with a forwarder to your on-prem DNS server.
  
  F. A VM Import of the current virtual machine. — correct, you would definitely want to leverage this in order to easily migrate the VM from on-prem to AWS.
  
40. You launch an Amazon EC2 instance without an assigned AWS identity and Access Management (IAM) role. Later, you decide that the instance should be running with an IAM role. Which action must you take in order to have a running Amazon EC2 instance with an IAM role assigned to it?
    
    a. Create an image of the instance, and register the image with an IAM role assigned and an Amazon EBS volume mapping.
    
    b. Create a new IAM role with the same permissions as an existing IAM role, and assign it to the running instance.
    
    c. Create an image of the instance, add a new IAM role with the same permissions as the desired IAM role, and deregister the image with the new role assigned.
    
    d. Create an image of the instance, and use this image to launch a new instance with the desired IAM role assigned  
    
    Đáp án: D. IAM role ko thể assign sau khi EC2 đã được launch
    
41. What does the following command do with respect to the Amazon EC2 security groups? ec2-revoke RevokeSecurityGroupIngress
    
    a. Removes one or more security groups from a rule.
    
    b. Removes one or more security groups from an Amazon EC2 instance.
    
    c. Removes one or more rules from a security group
    
    d. Removes a security group from our account.    
    
    Đáp án: C
    
42. Which of the following cannot be used in Amazon EC2 to control who has access to specific Amazon EC2 instances?
    
    a. Security Groups
    
    b. IAM System
    
    c. SSH keys
    
    d. Windows passwords  
      
    B. IAM chỉ kiểm soát actions nào user có thể perform chứ ko kiểm soát quyền access.
      
43. You must assign each server to at least _____ security group
    
    a. 3
    
    b. 2
    
    c. 4
    
    d. 1
          
    D.
    
44. A company is building software on AWS that requires access to various AWS services. Which configuration should be used to ensure that AWS credentials (i.e., Access Key ID/Secret Access Key combination) are not compromised?
    
    a. Enable Multi-Factor Authentication for your AWS root account.
    
    b. Assign an IAM role to the Amazon EC2 instance
    
    c. Store the AWS Access Key ID/Secret Access Key combination in software comments.
    
    d. Assign an IAM user to the Amazon EC2 Instance. 
          
    B.
              
45. Which of the following items are required to allow an application deployed on an EC2 instance to write data to a DynamoDB table? Assume that no security keys are allowed to be stored on the EC2 instance. (Choose 2 answers)
    
    a. Create an IAM Role that allows write access to the DynamoDB table
    
    b. Add an IAM Role to a running EC2 instance.
    
    c. Create an IAM User that allows write access to the DynamoDB table.
    
    d. Add an IAM User to a running EC2 instance.
    
    e.Launch an EC2 Instance with the IAM Role included in the launch configuration               
  
    A, E. B sai vì ko thể assign IAM role vào 1 EC2 đang running
    
46. You have an application running on an EC2 Instance, which will allow users to download files from a private S3 bucket using a pre-assigned URL. Before generating the URL the application should verify the existence of the file in S3. How should the application use AWS credentials to access the S3 bucket securely?
    
    a. Use the AWS account access Keys the application retrieves the credentials from the source code of the application.
    
    b. Create a IAM user for the application with permissions that allow list access to the S3 bucket launch the instance as the IAM user and retrieve the IAM user’s credentials from the EC2 instance user data.
    
    c. Create an IAM role for EC2 that allows list access to objects in the S3 bucket. Launch the instance with the role, and retrieve the role’s credentials from the EC2 Instance metadata
    
    d. Create an IAM user for the application with permissions that allow list access to the S3 bucket. The application retrieves the IAM user credentials from a temporary directory with permissions that allow read access only to the application user.    
    
    Đáp án: C. Mọi thứ liên quan đến giao tiếp securely giưa các service => IAM role
    
47. You try to connect via SSH to a newly created Amazon EC2 instance and get one of the following error messages: “Network error: Connection timed out” or “Error connecting to instance], reason: -> Connection timed out: connect,” You have confirmed that the network and security group rules are configured correctly and the instance is passing status checks. What steps should you take to identify the source of the behavior? Choose 2 answers
    
    a. Verify that the private key file corresponds to the Amazon EC2 key pair assigned at launch.
    
    b. Verify that your IAM user policy has permission to launch Amazon EC2 instances.
    
    c. Verify that you are connecting with the appropriate user name for your AMI.
    
    d. Verify that the Amazon EC2 Instance was launched with the proper IAM role.
    
    e. Verify that your federation trust to AWS has been established.    
    
    Đáp án: A, C. 
    
48. Please select the most correct answer regarding the persistence of the Amazon Instance Store
    
    a. The data on an instance store volume persists only during the life of the associated Amazon EC2 instance
    
    b. The data on an instance store volume is lost when the security group rule of the associated instance is changed.
    
    c. The data on an instance store volume persists even after associated Amazon EC2 instance is deleted    
    
    Đáp án: A
    
49. A user has launched an EC2 instance from an instance store backed AMI. The user has attached an additional instance store volume to the instance. The user wants to create an AMI from the running instance. Will the AMI have the additional instance store volume data?
    
    a. Yes, the block device mapping will have information about the additional instance store volume
    
    b. No, since the instance store backed AMI can have only the root volume bundled
    
    c. It is not possible to attach an additional instance store volume to the existing instance store backed AMI instance
    
    d. No, since this is ephemeral storage it will not be a part of the AMI    
    
    A. 
    
50. When an EC2 instance that is backed by an S3-based AMI Is terminated, what happens to the data on the root volume?
    
    a. Data is automatically saved as an EBS volume.
    
    b. Data is automatically saved as an EBS snapshot.
    
    c. Data is automatically deleted
    
    d. Data is unavailable until the instance is restarted.    
    
    Đáp án C: S3-based AMI = Instance store-backed AMI
    
51. Which of the following will occur when an EC2 instance in a VPC (Virtual Private Cloud) with an associated Elastic IP is stopped and started? (Choose 2 answers)
    
    a. The Elastic IP will be dissociated from the instance
    
    b. All data on instance-store devices will be lost
    
    c. All data on EBS (Elastic Block Store) devices will be lost
    
    d. The ENI (Elastic Network Interface) is detached
    
    e. The underlying host for the instance is changed    
    
    Đáp án: E, C
    
52. A user has launched an EC2 Windows instance from an instance store backed AMI. The user has also set the Instance initiated shutdown behavior to stop. What will happen when the user shuts down the OS?
    
    a. It will not allow the user to shutdown the OS when the shutdown behavior is set to Stop
    
    b. It is not possible to set the termination behavior to Stop for an Instance store backed AMI instance
    
    c. The instance will stay running but the OS will be shutdown    
    
    Đáp án B. Instance store-backed EC2 chỉ running or terminated.
    
53. A user has launched an EC2 instance from an instance store backed AMI. If the user restarts the instance, what will happen to the ephemeral storage data?
    
    a. All the data will be erased but the ephemeral storage will stay connected
    
    b. All data will be erased and the ephemeral storage is released
    
    c. It is not possible to restart an instance launched from an instance store backed AMI
    
    d. The data is preserved    
    
    Đáp án D. Stop => start thì data lost, restart (reboot) thì data vẫn retain.
    
54. A user has launched an EBS backed instance. The user started the instance at 9 AM in the morning. Between 9
    AM to 10 AM, the user is testing some script. Thus, he stopped the instance twice and restarted it. In the same
    hour the user rebooted the instance once. For how many instance hours will AWS charge the user?
    
    A.
    3 hours
    
    B.
    4 hours
    
    C.
    2 hours
    
    D.
    1 hour
        
    Đáp án: A.
    A user can stop/start or reboot an EC2 instance using the AWS console, the Amazon EC2 CLI or the Amazon
    EC2 API. Rebooting an instance is equivalent to rebooting an operating system. When the instance is rebooted
    AWS will not charge the user for the extra hours. In case the user stops the instance, AWS does not charge the
    running cost but charges only the EBS storage cost. If the user starts and stops the instance multiple times in a
    single hour, AWS will charge the user for every start and stop. In this case, since the instance was rebooted
    twice, it will cost the user for 3 instance hours.
        
55. A user has launched an EBS backed EC2 instance. What will be the difference while performing the restart or stop/start options on that instance?
    
    a. For restart it does not charge for an extra hour, while every stop/start it will be charged as a separate hour
    
    b. Every restart is charged by AWS as a separate hour, while multiple start/stop actions during a single hour will be counted as a single hour
    
    c. For every restart or start/stop it will be charged as a separate hour
    
    d. For restart it charges extra only once, while for every stop/start it will be charged as a separate hour        
    
    Đáp án A.
    
56. A user has launched an EBS backed EC2 instance. The user has rebooted the instance. Which of the below mentioned statements is not true with respect to the reboot action?
    
    a. The private and public address remains the same
    
    b. The Elastic IP remains associated with the instance
    
    c. The volume is preserved
    
    d. The instance runs on a new host computer    
    
    Đáp án D. Reboot k làm thay đổi hardware
    
57. 
        
        
