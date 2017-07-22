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
    
    
    
    
