1.You are designing an enterprise data storage system. Your data management software system requires mountable disks and a real filesystem, so you cannot use S3 for storage. You need persistence, so you will be using AWS EBS Volumes for your system. The system needs as low-cost storage as possible, and access is not frequent or high throughput, and is mostly sequential reads. Which is the most appropriate EBS Volume Type for this scenario?
  
  a. gp1
  
  b. io1
  
  c. standard 
  
  d. gp2
  
  Đán án: C. Standard or Magnetic volumes are suited for cold workloads where data is infrequently accessed, or scenarios where 
  the lowest storage cost is important
  
2. Which EBS volume type is best for high performance NoSQL cluster deployments?
   
   a. io1 
   
   b. gp1
   
   c. standard
   
   d. gp2  
   
   Đáp án A. io1 volumes, or Provisioned IOPS (PIOPS) SSDs, are best for: Critical business applications that require sustained IOPS performance, or more than 10,000 IOPS or 160 MiB/s of throughput per volume, 
   like large database workloads, such as MongoDB.
   
3. Provisioned IOPS Costs: you are charged for the IOPS and storage whether or not you use them in a given month.
   
   a. FALSE
   
   b. TRUE   
   
   Đáp án: B. https://aws.amazon.com/ebs/pricing/
               
4. A user has provisioned 2000 IOPS to the EBS volume. The application hosted on that EBS is experiencing less IOPS than provisioned. Which of the below mentioned options does not affect the IOPS of the volume?
   
   a. The application does not have enough IO for the volume
   
   b. Instance is EBS optimized
   
   c. The EC2 instance has 10 Gigabit Network connectivity
   
   d. Volume size is too large               
   
   Đáp án: D. 
   
   Whatever your EBS volume type, if you are not experiencing the IOPS or throughput you expect in your configuration, ensure that your EC2 instance bandwidth is not the limiting factor. You should always use a current-generation, EBS-optimized instance (or one that includes 10 Gb/s network connectivity) for optimal performance. For more information, see Amazon EC2 Instance Configuration. Another possible cause for not experiencing the expected IOPS is that you are not driving enough I/O to the EBS volumes.
   
5. A user is trying to pre-warm a blank EBS volume attached to a Linux instance. Which of the below mentioned steps should be performed by the user?
   
   a. There is no need to pre-warm an EBS volume (with latest update no pre-warming is needed)
   
   b. Contact AWS support to pre-warm (This used to be the case before, but pre warming is not necessary now)
   
   c. Unmount the volume before pre-warming
   
   d. Format the device
   
   Đáp án: A
   
6. You are running a database on an EC2 instance, with the data stored on Elastic Block Store (EBS) for persistence At times throughout the day, you are seeing large variance in the response times of the database queries Looking into the instance with the isolate command you see a lot of wait time on the disk volume that the database’s data is stored on. What two ways can you improve the performance of the database’s storage while maintaining the current persistence of the data? Choose 2 answers
   
   a. Move to an SSD backed instance
   
   b. Move the database to an EBS-Optimized Instance
   
   c. Use Provisioned IOPs EBS
   
   d. Use the ephemeral storage on an m2.4xLarge Instance Instead   
   
   Đáp án: B, C
   
7. A user has deployed an application on an EBS backed EC2 instance. For a better performance of application, it requires dedicated EC2 to EBS traffic. How can the user achieve this?
   
   a. Launch the EC2 instance as EBS provisioned with PIOPS EBS
   
   b. Launch the EC2 instance as EBS enhanced with PIOPS EBS
   
   c. Launch the EC2 instance as EBS dedicated with PIOPS EBS
   
   d. Launch the EC2 instance as EBS optimized with PIOPS EBS   
   
   Đáp án: D.
   
8. You have launched an EC2 instance with four (4) 500 GB EBS Provisioned IOPS volumes attached. The EC2 Instance is EBS-Optimized and supports 500 Mbps throughput between EC2 and EBS. The two EBS volumes are configured as a single RAID 0 device, and each Provisioned IOPS volume is provisioned with 4,000 IOPS (4000 16KB reads or writes) for a total of 16,000 random IOPS on the instance. The EC2 Instance initially delivers the expected 16,000 IOPS random read and write performance. Sometime later in order to increase the total random I/O performance of the instance, you add an additional two 500 GB EBS Provisioned IOPS volumes to the RAID. Each volume is provisioned to 4,000 IOPS like the original four for a total of 24,000 IOPS on the EC2 instance Monitoring shows that the EC2 instance CPU utilization increased from 50% to 70%, but the total random IOPS measured at the instance level does not increase at all. What is the problem and a valid solution?
   
   a. Larger storage volumes support higher Provisioned IOPS rates: increase the provisioned volume storage of each of the 6 EBS volumes to 1TB.
   
   b. EBS-Optimized throughput limits the total IOPS that can be utilized use an EBS-Optimized instance that provides larger throughput. (EC2 Instance types have limit on max throughput and would require larger instance types to provide 24000 IOPS)
   
   c. Small block sizes cause performance degradation, limiting the I’O throughput, configure the instance device driver and file system to use 64KB blocks to increase throughput.
   
   d. RAID 0 only scales linearly to about 4 devices, use RAID 0 with 4 EBS Provisioned IOPS volumes but increase each Provisioned IOPS EBS volume to 6.000 IOPS.
   
   e. The standard EBS instance root volume limits the total IOPS rate, change the instant root volume to also be a 500GB 4,000 Provisioned IOPS volume   
   
   Đáp án: B. Loại D, E
   
   Launching an instance that is EBS-optimized provides you with a dedicated connection between your EC2 instance and your EBS volume. However, it is still possible to provision EBS volumes that exceed the available bandwidth for certain instance types, especially when multiple volumes are striped in a RAID configuration. Be sure to choose an EBS-optimized instance that provides more dedicated EBS throughput than your application needs; otherwise, the Amazon EBS to Amazon EC2 connection will become a performance bottleneck.
   
9. _____ is a durable, block-level storage volume that you can attach to a single, running Amazon EC2 instance.
   
   a. Amazon S3
   
   b. Amazon EBS
   
   c. None of these
   
   d. All of these   
   
   Đáp án B.
   
10. Which Amazon storage do you think is the best for my database-style applications that frequently encounter many random reads and writes across the dataset?
    
    a. None of these.
    
    b. Amazon Instance Storage
    
    c. Any of these
    
    d. Amazon EBS  
     
   Đáp án D.
   
11. What does Amazon EBS stand for?
    
    a. Elastic Block Storage
    
    b. Elastic Business Server
    
    c. Elastic Blade Server
    
    d. Elastic Block Store   
    
    Đáp án D. Be careful, Store not Storage.
    
12. Select the correct set of steps for exposing the snapshot only to specific AWS accounts
    
    a. Select Public for all the accounts and check mark those accounts with whom you want to expose the snapshots and click save.
    
    b. Select Private and enter the IDs of those AWS accounts, and click Save.
    
    c. Select Public, enter the IDs of those AWS accounts, and click Save.
    
    d. Select Public, mark the IDs of those AWS accounts as private, and click Save.    
    
    Đáp án: B. Only unencrypted snapshots can be shared. Encrypted snapshots cannot be shared between accounts or made public
    
13. If an Amazon EBS volume is the root device of an instance, can I detach it without stopping the instance?
    
    a. Yes but only if Windows instance
    
    b. No
    
    c. Yes
    
    d. Yes but only if a Linux instance    
    
    Đáp án: B. If an EBS volume is the root device of an instance, you must stop the instance before you can detach the volume.
    
14. Can we attach an EBS volume to more than one EC2 instance at the same time?
    
    a. Yes
    
    b. No
    
    c. Only EC2-optimized EBS volumes.
    
    d. Only in read mode. 
    
    Đáp án: B. An Amazon EBS volume is a durable, block-level storage device that you can attach to a single EC2 instance.
    (http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumes.html)
15. Can I delete a snapshot of the root device of an EBS volume used by a registered AMI?
    
    a. Only via API
    
    b. Only via Console
    
    c. Yes
    
    d. No 
        
    Đáp án D. http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-deleting-snapshot.html
    Note that you can't delete a snapshot of the root device of an EBS volume used by a registered AMI. You must first deregister the AMI before you can delete the snapshot.     
        
16. By default, EBS volumes that are created and attached to an instance at launch are deleted when that instance is terminated. You can modify this behavior by changing the value of the flag_____ to false when you launch the instance
    
    a. DeleteOnTermination
    
    b. RemoveOnDeletion
    
    c. RemoveOnTermination
    
    d. TerminateOnDeletion        
    
    Đáp án A.
    
17. Your company policies require encryption of sensitive data at rest. You are considering the possible options for protecting data while storing it at rest on an EBS data volume, attached to an EC2 instance. Which of these options would allow you to encrypt your data at rest? (Choose 3 answers)
    
    a. Implement third party volume encryption tools
    
    b. Do nothing as EBS volumes are encrypted by default
    
    c. Encrypt data inside your applications before storing it on EBS
    
    d. Encrypt data using native data encryption drivers at the file system level
    
    e. Implement SSL/TLS for all services running on the server    
    
    Đáp án: A,C, D. 
    E sai vì SSL/TLS chỉ encrypt data khi transfer
    B sai vì mặc định EBS ko encrypt data
    
18. Which of the following are true regarding encrypted Amazon Elastic Block Store (EBS) volumes? Choose 2 answers
    
    a. Supported on all Amazon EBS volume types
    
    b. Snapshots are automatically encrypted
    
    c. Available to all instance types
    
    d. Existing volumes can be encrypted
    
    e. Shared volumes can be encrypted    
    
    Đáp án: A, B. This feature is supported on all Amazon EBS volume types (General Purpose (SSD), Provisioned IOPS (SSD), and
                  Magnetic). You can access encrypted Amazon EBS volumes the same way you access existing volumes;
                  encryption and decryption are handled transparently and they require no additional action from you, your
                  Amazon EC2 instance, or your application. Snapshots of encrypted Amazon EBS volumes are automatically
                  encrypted, and volumes that are created from encrypted Amazon EBS snapshots are also automatically
                  encrypted.
                  http://docs.aws.amazon.com/kms/latest/developerguide/services-ebs.html
                  
19. What is the scope of an EBS volume?
    
    a. VPC
    
    b. Region
    
    c. Placement Group
    
    d. Availability Zone   
    
    Đáp án: D. An Amazon EBS volume is tied to its Availability Zone and can be attached only to instances in the same Availability
               Zone.
               http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/resources.html
    Muốn vượt AZ thì cần tạo snapshot => tạo EBS mới dựa trên snapshot trong AZ mới.
    Muốn vượt Region thì cần tạo snapshot => copy snapshot sang vùng mới => tạo EBS mới dựa trên snapshot.
                                  
20. An EC2 instance has one additional EBS volume attached to it. How can a user attach the same volume to another running instance in the same AZ?
    
    a. Terminate the first instance and only then attach to the new instance
    
    b. Attach the volume as read only to the second instance
    
    c. Detach the volume first and attach to new instance
    
    d. No need to detach. Just select the volume and attach it to the new instance, it will take care of mapping internally                                  

    Đáp án C.
                         
21. A user is planning to use EBS for his DB requirement. The user already has an EC2 instance running in the VPC private subnet. How can the user attach the EBS volume to a running instance?
    
    a. The user must create EBS within the same VPC and then attach it to a running instance.
    
    b. The user can create EBS in the same zone as the subnet of instance and attach that EBS to instance. (Should be in the same AZ)
    
    c. It is not possible to attach an EBS to an instance running in VPC until the instance is stopped.
    
    d. The user can specify the same subnet while creating EBS and then attach it to a running instance                         
    
    Đáp án B.
    Attach EBS to EC2:
    
        - Encrypted EBS chỉ có thể attach to EC2 hỗ trợ EBS encryption
        - nếu EBS có AWS Marketplace product code: chỉ có thể attach to stoped EC2. 
        - còn lại có thể hot attach.
        - chỉ attach được EC2 cùng AZ.
        - attach xong phải mount mới xai được (http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-using-volumes.html)
22. A user is using an EBS backed instance. Which of the below mentioned statements is true?
    
    a. The user will be charged for volume and instance only when the instance is running
    
    b. The user will be charged for the volume even if the instance is stopped
    
    c. The user will be charged only for the instance running cost
    
    d. The user will not be charged for the volume if the instance is stopped    
    
    Đáp án B. 
    
23. A user has stored data on an encrypted EBS volume. The user wants to share the data with his friend’s AWS account. How can user achieve this?
    
    a. Create an AMI from the volume and share the AMI
   
    b. Copy the data to an unencrypted volume and then share
    
    c. Take a snapshot and share the snapshot with a friend
    
    d. If both the accounts are using the same encryption key then the user can share the volume directly    
    
    Đáp án B. 
    Chỉ có unencrypted EBS mới có thẻ share / make public. 
24. An organization wants to move to Cloud. They are looking for a secure encrypted database storage option. Which of the below mentioned AWS functionalities helps them to achieve this?
    
    a. AWS MFA with EBS
    
    b. AWS EBS encryption
    
    c. Multi-tier encryption with Redshift
    
    d. AWS S3 server-side storage    
    
    Đáp án B. 
    
25. You are running a database on an EC2 instance, with the data stored on Elastic Block Store (EBS) for persistence At times throughout the day, you are seeing large variance in the response times of the database queries Looking into the instance with the isolate command you see a lot of wait time on the disk volume that the database’s data is stored on. What two ways can you improve the performance of the database’s storage while maintaining the current persistence of the data? Choose 2 answers
    
    a. Move to an SSD backed instance
    
    b. Move the database to an EBS-Optimized Instance
    
    c. Use Provisioned IOPs EBS
    
    d. Use the ephemeral storage on an m2.4xLarge Instance Instead 
       
26. You are running a database on an EC2 instance, with the data stored on Elastic Block Store (EBS) for persistence At times throughout the day, you are seeing large variance in the response times of the database queries Looking into the instance with the isolate command you see a lot of wait time on the disk volume that the database’s data is stored on. What two ways can you improve the performance of the database’s storage while maintaining the current persistence of the data? Choose 2 answers
    
    a. Move to an SSD backed instance
    
    b. Move the database to an EBS-Optimized Instance
    
    c. Use Provisioned IOPs EBS
    
    d. Use the ephemeral storage on an m2.4xLarge Instance Instead   
        
    Đáp án: B, C
        
27. A user is planning to schedule a backup for an EBS volume. The user wants security of the snapshot data. How can the user achieve data encryption with a snapshot?
        
    a. Use encrypted EBS volumes so that the snapshot will be encrypted by AWS
    
    b. While creating a snapshot select the snapshot with encryption
    
    c. By default the snapshot is encrypted by AWS
    
    d. Enable server side encryption for the snapshot using S3    
         
        Đáp án A. Chỉ có 2 cách tạo encrypted snapshot:
        
            - copy từ 1 snapshot và chọn encrypt option
            - tạo snapshot từ 1 encrypted EBS
            
28. A user is trying to launch an EBS backed EC2 instance under free usage. The user wants to achieve
    encryption of the EBS volume. How can the user encrypt the data at rest?
    
    A.
    Use AWS EBS encryption to encrypt the data at rest
    
    B.
    The user cannot use EBS encryption and has to encrypt the data manually or using a third party tool
    
    C.
    The user has to select the encryption enabled flag while launching the EC2 instance
    
    D.
    Encryption of volume is not available as a part of the free usage tier
                
    Đáp án: B. The EBS supports encryption for the selected
               instance type and the newer generation instances, such as m3, c3, cr1, r3, g2. It is not supported with a micro
               instance.
                           
                           
                    
