# AWS Certified Cloud Practitioner (ACCP) Exam Notes

These are notes regarding ACCP exam which were gradually completed while studying the exam objectives.

You can find every updated information in this [link](https://aws.amazon.com/certification/certified-cloud-practitioner/) which is the official and reputable information.

Also you can donload [the official exam guide](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf).

Another profitable resource is the [whitepaper Overview of Amazon Web Services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/introduction.html).

[Exam Prep Official Question Set](https://explore.skillbuilder.aws/learn/course/external/view/elearning/14050/aws-certified-cloud-practitioner-official-practice-question-set-clf-c02-english)

[The new AWS Cloud Practitioner (CLF-C02): What to expect](https://www.pluralsight.com/resources/blog/cloud/new-aws-clf-c02-exam0)

* * *

### Table of contents
- Foundations of Cloud Computing
	- [Shared responsibility model](#shared-responsibility-model)
	- [AWS Well-Architected Framework](#aws-well-architected-framework)
	- [Advantages of Amazon Cloud (Benefits)](#advantages-of-amazon-cloud-benefits)
	- [Geographical Services](#geographical-services)
	- [AWS Global Infrastructure](#aws-global-infrastructure)
- Security, Compliance, and Governance
	- [AWS Shield](#aws-shield)
	- [AWS Shared Responsibility Model](#aws-shared-responsibility-model)
	- [AWS CloudHSM](#aws-cloudhsm)
	- [Key Management Service (KMS)]()
	- [Amazon GuardDuty](#amazon-guardduty)
	- [Amazon IAM](#amazon-iam)
- Pricing, Billing, Support and Governance
	- [AWS Trust & Safety team](#aws-trust--safety-team)
	- [AWS Support plans](#aws-support-plans)
   	- [AWS Partner Network]()
   	- [Infrastructure Event Management]()
   	- [AWS Budgets](#aws-budgets)
- Auditing, Monitoring, Logging
	- [Amazon CloudWatch](#amazon-cloudwatch)
	- [AWS Trusted Advisor](#aws-trusted-advisor)
	- [AWS CloudTrail](#aws-cloudtrail)
- Storage Technology
	- [Amazon S3](#amazon-s3)
	- [Amazon EBS volumes types](#amazon-ebs-volumes-types)
- Content Delivery and Networking Technology
	- [Popular HTTTP code](#popular-htttp-code)
  	- [VPC peering connection](#vpc-peering-connection)
	- [Amazon VPC](#amazon-vpc)
   	- [Amazon Load Balancers](#amazon-load-balancers)
 	- [AWS Network Access Control List (ACL)](#aws-network-access-control-list-acl)
 	- [AWS Security Groups](#aws-security-groups)
 	- [AWS Internet Gateway](#aws-internet-gateway)
	- [Amazon Route 53](#amazon-route-53)
	- [Amazon CloudFront](#amazon-cloudfront)
- Database Technology
	- [Amazon Athena](#amazon-athena)
	- [Amazon DynamoDB](#amazon-dynamodb)
	- [AWS Database SQL type](#aws-database-sql-type)
- Development, Messaging, and Deployment
	- [Amazon Simple Notification Service (SNS)](#amazon-simple-notification-service-sns)
	- [Amazon Simple Queue Service (SQS)](#amazon-simple-queue-service-sqs)
	- Simple Email Service (SES)()
- Migration and Transfer
	- [Amazon S3 Transfer Acceleration](#amazon-s3-transfer-acceleration)
	- [Amazon Neptune](#amazon-neptune)
	- [AWS Direct Connect](#aws-direct-connect)
	- [AWS Snow family](#aws-snow-family)
- Artificial Intelligence and Machine Learning
	- [Amazon Machine Image (AMI)](#amazon-machine-image-ami)
	- [Amazon SageMaker](#amazon-sagemaker)

 - Elastic MapReduce (EMR)()
 - [AWS Compute Optimizer](#aws-compute-optimizer)
 - [Amazon Elastic Load Balancer (ELB)](#amazon-elastic-load-balancer-elb)
 - [AWS Scalability](#aws-scalability)
 - [AWS Inspector](#aws-inspector)
 - [AWS Personal Health Dashboard](#aws-personal-health-dashboard)
 - [AWS X-Ray](#aws-x-ray)
 - [AWS TCO Calculator](#aws-tco-calculator)
 - [Amazon Elastic Block Store (EBS)](#amazon-elastic-block-store-ebs)
 - [Amazon Kinesis](#amazon-kinesis)
 - [AWS CloudFormation](#aws-cloudformation)
 - [AWS Elastic Beanstalk](#aws-elastic-beanstalk)
 - [AWS Lambda](#aws-lambda)
 - [AWS WAF](#aws-waf)
 - [AWS AD Connector](#aws-ad-connector)
 - [AWS Simple AD](#aws-simple-ad)
 - [Amazon Elastic Container Service for Kubernetes (EKS)](#amazon-elastic-container-service-for-kubernetes-eks)
 - [Amazon Elastic Container Service (ECS)](#amazon-elastic-container-service-ecs)
 - [Amazon Elastic Container Registry (ECR)](#amazon-elastic-container-registry-ecr)
 - [Virtual Private Gateway](#virtual-private-gateway)
 - [Amazon Cognito](#amazon-cognito)
 - [AWS Organizations](#aws-organizations)
 - [AWS Device Farm](#aws-device-farm)
 - [AWS Config](#aws-config)
 - [Amazon RDS](#amazon-rds)
 - [AWS Auto Scaling Group](#aws-auto-scaling-group)
 - [AWS Auto Scaling](#aws-auto-scaling)
 - [AWS Glacier](#aws-glacier)
 - [AWS Storage Gateway Volume Gateway](#aws-storage-gateway-volume-gateway)
 - [AWS Step Functions](#aws-step-functions)
 - [Amazon Simple Workflow Service (SWF)](#amazon-simple-workflow-service-swf)
 - [Amazon Security Token Service (STS)](#amazon-security-token-service-sts)
 - [AWS Server Migration Service (SMS)](#aws-server-migration-service-sms)
 - [AWS Database Migration Service (DMS)](#aws-database-migration-service-dms)
 - [Amazon DevPay](#amazon-devpay)
 - [Amazon Elasticsearch Service](#amazon-elasticsearch-service)
 - [Amazon QuickSight](#amazon-quicksight)
 - [Amazon CodeStar](#amazon-codestar)
 - [Amazon Cloud9](#amazon-cloud9)
 - [Amazon EC2](#amazon-ec2)
 - [AWS Cost Explorer](#aws-cost-explorer)
 - [AWS Cost Anomaly Detection](#aws-cost-anomaly-detection)
 - [Amazon Elastic Transcoder](#amazon-elastic-transcoder)
 - [AWS Glue](#aws-glue)
 - [AWS Artifact](#aws-artifact)
 - [AWS Service Catalog](#aws-service-catalog)
 - [AWS Managed Services](#aws-managed-services)
 - [Amazon Comprehend](#amazon-comprehend)
 - [Amazon Resource Names (ARNs)](#amazon-resource-names-arns)
 - [AWS IoT Core](#aws-iot-core)
 - [AWS Fargate](#aws-fargate)
 - [Amazon Detective](#amazon-detective)
 - [Amazon Global Accelerator](#amazon-global-accelerator)
 - [AWS Data Sync](#aws-data-sync)
 - [AWS CodePipeline ](#aws-codepipeline)
 - [Amazon Macie](#amazon-macie)
 - [AWS OpsWorks](#aws-opsworks)
 - [Notes](#notes)

***

### Shared responsibility model
- AWS:
  	- AWS Global Infrastructure, Regions, edge locations, and Availability Zones.
  	- AWS controls access to its data centers where your data resides.
  	- AWS maintains networking components: generators, uninterruptible power supply etc.
  	- AWS is responsible for any managed service like RDS, S3, ECS, or Lambda, patching of host operating systems.
- CUSTOMER:
	- You are responsible for managing your application data, which includes encryption options.
 	- You are responsible for securing your account and API calls, rotating credentials, restricting internet access from your VPCs.
  	- You are responsible for the guest operating system (OS), which includes updates and security patches.
  	- You are responsible for application security and identity and access management.
  	- You are responsible for network traffic protection, which includes security group firewall configuration.
  	- You are responsible for your application code, installed software, and more. You should frequently scan for and patch vulnerabilities in your code.
- SHARED:
	- Awareness & Training - AWS trains AWS employees, but a customer must train their own employees.
	- Configuration Management – AWS maintains the configuration of its infrastructure devices, but a customer is responsible for configuring their own guest operating systems, databases, and applications.
	- Patch Management – AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications.

### AWS Global Infrastructure
- Deploying to multiple AZs replicates applications across multiple data centers in the same Region and provides High Availability.
- Multi-Region deployments are best for applications that have extremely high availability requirements.
- A **Region** is a geographical area of the world that is a collection of data centers logically grouped into Availability Zones.
- **Availability Zones (AZs)** consist of 1 or more physically separated data centers.
- AZ:
	- Contain redundant networking.
   	- Contain physically separated data centers.
   	- Contain redundant connectivity.
   	- They are physically separated, connected through low-latency links, fault tolerant, and allow high availability.
   	- Availability Zones are a collection of data centers within a specific region. 
- Regions:
	- A Region is a geographic area that hosts 2 or more Availability Zones.
  	- A specific geographic location designed to provide high availability to a certain area.
	- They are grouped in geographic locations.
	- They are fully independent and isolated.
	- They contain only the resources and services specifically deployed to them.
- There are more Availability Zones than Regions.
- There are more edge locations than Regions.
- There are more edge locations than Availability Zones.

### AWS Budgets
You can use AWS Budgets to set a monthly cost budget with a fixed target amount to track all costs associated with your account. You can choose to be alerted for both actual (after accruing) and forecasted (before accruing) spends.  You can ALSO use AWS Budgets to monitor your aggregate utilization and coverage metrics for your Reserved Instances (RIs) or Savings Plans.

-Usecase: You want to monitor the cost of using your AWS services and receive alerts when the thresholds you define are met. Which of the following AWS Budgets types should you create?
	- You need to create a cost budget with AWS Budgets if you want to monitor the cost of using your AWS services.

### Amazon S3
- **CRR** (Cross-region replication): enables automatic, asynchronous copying of objects across buckets in different AWS Regions.
- You cannot reserve capacity.
- Bucket names rules:
	- Names must be unique across all of AWS.
	- Names must be 3 to 63 characters in length.
	- Names can only contain lowercase letters, numbers and hyphens.
	- Names cannot be formatted as an IP address.
- Amazon S3 storage tier:
	- **S3 Standard** -> 99.99% SLA -> for data that is accessed less frequently, but requires rapid access when needed.
	- **S3 Standard-IA** -> 99.9% SLA -> offers the high durability, high throughput, and low latency of S3 Standard.
	- **S3 One Zone-IA** -> 99% SLA -> *the most cost-effective* Amazon S3 storage tier for data that is not often accessed but requires high durability and it stores data in a **single** AZ.
	- **Glacier** -> No SLA.
- **Multipart upload** can be used to speed up uploads to S3.
- **S3 Copy** -> up to 5GB in size in a single atomic operation.
- **S3 Intelligent-Tiering** is an appropriate Amazon S3 storage class for "data with unknown/changing access pattern".
- **Data consistency** models available are:
	- Read after write consistency for PUTS of new objects.
	- Eventual consistency for overwrite PUTS and DELETES (it takes time to propagate).
- "**MFA delete**" adds a layer of additional security to prevent accidental deletion.
- Amazon S3 **objects** consist of:
	- Key
	- Value
	- Version ID
	- Metadata
- **Object lifecycle management** can be used with objects so that they are stored cost effectively throughout their lifecycle. Objects can be transitioned to another storage class or expired. It enables you to **set rules** to **automatically transfer** objects between different storage classes at defined time intervals.
- **Standard-IA** and **One Zone-IA** both have a minimum storage duration charge of **30** days
- **Bucket policies** allow you to control access to entire buckets.
- You can use **ACLs** to grant basic read/write permissions to other AWS accounts.
- A customer has set up an Amazon S3 bucket and wants to limit access to specific users: You can add a bucket access policy directly to an Amazon S3 bucket to grant IAM users access permissions for the bucket and the objects in it. While you can control access to a bucket with user policies, this is not the most efficient way to achieve this.
- Usecase: You have decided to use the **AWS Cost and Usage Report** to track your EC2 Reserved Instance costs:
	- You cannot store the Cost and Usage Report in a bucket owned by AWS.
 	- You can use Cost and Usage Reports to publish your AWS billing reports to an S3 bucket you own. 

### Advantages of Amazon Cloud (Benefits)
- Replace upfront capital expenses with low variable costs. (Trade capital expense for variable expense)
- Benefit from massive economies of scale.
- Stop guessing about capacity.
- Increase speed and agility.
- Stop spending money running and maintaining data centres.
- Go global in minutes.
- Elasticity.Agility.Variable expense.

### AWS Compute Optimizer
It helps avoid overprovisioning and underprovisioning, based on your utilization data, four types of AWS resources:
- Amazon Elastic Compute Cloud (EC2) instance types.
- Amazon Elastic Block Store (EBS) volumes.
- Amazon Elastic Container Service (ECS) services on AWS Fargate.
- AWS Lambda functions.

### Amazon EBS volumes types
- **General purpose (gp2)**(SSD)
	- it provides a good balance of price to performance, is suitable for most workloads and can be used as a system boot volume.
- **Provisioned IOPS (io1)**(SSD)
	- it is a high-performance volume type that is more expensive and should be used for apps that require the higher performance.
- **Cold HDD (sc1)**
	- it cannot be used as a boot volume and is good for throughput oriented storage for infrequently accessed data.
- **Throughput Optimized (st1)**
	- it is ideal for streaming workloads with fast throughput such as big data and data warehouses.

### Amazon Elastic Load Balancer (ELB)
- It distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, in multiple Availability Zones.
- It offers multiple types of load balancers that all feature the high availability, automatic scaling and robust security, necessary to make your applications fault-tolerant.
- ELB Health Check gets first insights about potential issues.
- A **listener** is a process that checks for connection requests, using the protocol and port that you configure.
- Each listener has a default **rule**.
- Each rule **action** has a type.
- There are two types of **rule condition**:
	- Host
	- Path
- The primary **benefits** of using AWS ELB:
	- High availability
	- Elasticity

### Amazon Load Balancers
- Application Load Balancers (ALB)
	- process traffic at the HTTP, HTTPS level (layer 7)
	- routes traffic to targets within Amazon VPC
- Network Load Balancers (NLB)
	- process traffic at the TCP, UDP, TLS level (layer 4)
   	- capable of handling millions of requests per second while maintaining ultra-low latencies
- Gateway Load Balancers (GLB)
	- handle millions of requests per second, volatile traffic patterns, and introduces extremely low latency
- Classic Load Balancers (CLB)
	- process traffic at the TCP, SSL, HTTP and HTTPS levels (layer 4 & 7).

- *Load balancing with session affinity* can be used for **horizontal scaling** of **stateful** components.

### AWS Network Access Control List (ACL)
- Stateless
- By default: all in - all out
- It operates on VPC subnet level
- Not used in S3
- Network ACLs operate at the **subnet** level NOT AZ level. It provides a firewall / security layer at the subnet level.
- Network ACLs are **stateless** so you must create rules in both directions to allow traffic through.

### AWS Security Groups
- Stateful firewalls
- By default: none in - all out
- Only `allow` rules, it is not possible to have `deny` rules
- It allows access through specific port
- It is possible to have **inbound** and **outbound** rules in a security group
- It operates on EC2 instance level
- Not used in S3
- The security group acts as a virtual firewall to protect the EC2 instance. (A company wants to block network traffic from accessing an EC2 instance)
- New security groups allow only outbound traffic and block all incoming traffic. (By default, new security groups start with only an outbound rule to allow all traffic to leave the instances. You must add rules to enable any inbound traffic.)

### AWS Internet Gateway
- Do not have `allow` or `deny` rules
- It allows public traffic to access VPC resources
- It operates on VPC level

### AWS Scalability
AWS Scaling **vertically**: 
- increasing the instance size, CPU, RAM, DISK

AWS Scaling **horizontally**:
- adding more EC2 instances, AWS Lambda
- adding concurrently executing functions
- adding read replicas to an Amazon RDS database

### Amazon Simple Notification Service (SNS)
- **Topics**: how you label and group different endpoints that you send messages to
- **Subscriptions**: the endpoints that a topic sends messages to
- **Publisher**: the person/alarm/event that gives SNS the message that needs to be sent

- It is a web service that makes it easy to **set up**, **operate**, and **send notifications** from the cloud.
- SNS supports notifications over multiple transports including HTTP/HTTPS, Email/Email-JSON, SQS and SMS.
- It is used for building and integrating **loosely-coupled**, *distributed applications*.

### Amazon Simple Queue Service (SQS)
- It is a fully managed message queuing service that enables you to *decouple* and *scale microservices*, *distributed systems*, and *serverless applications*.
- **Use case**: *Decoupling application* components to ensure that there is no dependency on the availability of a single component.
- It can be used to ensure the **persistence** of **in-flight** *transactions independently* of any single application component.
- It is a message queue used for **decoupling** application components

### Simple Email Service (SES)
Amazon Simple Email Service (Amazon SES) lets you reach customers confidently without an on-premises Simple Mail Transfer Protocol (SMTP) email server using the Amazon SES API or SMTP interface.

### AWS Inspector
- Inspector is an *automated security assessment* service that helps improve the security and compliance of applications deployed on AWS.
- It uses an **agent** installed in EC2 instances and assesses applications for *vulnerabilities* and *deviations* from best practices.
- Organization can assess applications for vulnerabilities and **deviations** *from best practices*.

### AWS Trusted Advisor
- An **online resource** that helps to *reduce cost*, *increase performance* and *improve security*.
- Trusted Advisor can check:
	- Cost optimization (Low utilization on EC2 instances)
	- Security (Open-access permissions for S3 buckets, Exposed access keys)
	- Performance
	- Service limits (has a service limit dashboard)
	- Fault tolerance
- Trusted Advisor can't check:
	- Amazon services down
- It can be used to provide **real time guidance** on provisioning resources following *AWS best practices*.

### AWS Personal Health Dashboard
- It provides **alerts** and **remediation** *guidance* when AWS is experiencing events that may *impact* you.

### AWS X-Ray
- It is a service that helps developers **analyze** and **debug** distributed applications.
- It understand how your application and its underlying services are performing to identify and troubleshoot the root cause of performance issues and errors.

### AWS TCO Calculator
- It can be used to **compare** the *cost of running* your applications in an *on-premises* or colocation environment to *AWS*.
- "**Compute Hardware**" and "**Data Center Security**" should be included in a TCO analysis comparing on-premise to AWS Cloud.

### Amazon Elastic Block Store (EBS)
- [EBS volumes types](#amazon-ebs-volumes-types)
- The **easiest** way to store a backup of an EBS volume on Amazon S3: Create a **snapshot** of the volume.
- Amazon EBS snapshots are stored on *S3*.
- EBS volumes must be **in the same AZ** as the instances they are attached to.
- You can use *Amazon Data Lifecycle Manager* (**Amazon DLM**) to automate the creation, retention, and deletion of snapshots taken to back up your Amazon EBS volumes.
- The Fundamental *charges* for EBS volumes are:
	- the amount of data **provisioned** (**not** *consumed*) *per* <ins>month</ins>.
	- amount you provision in **IOPS**
- The **root** EBS volumes are **deleted** on termination by <ins>default</ins>.
- Extra **non-root** volumes are **not deleted** on termination by <ins>default</ins>.
- Both non-root and root if launched from an **encrypted** AMI.

### Amazon SageMaker
- That enables developers and data scientists to quickly and easily **build**, **train**, and **deploy** <ins>machine learning models</ins> at any scale.
- While SageMaker will help the company find trends and patterns in data using machine learning, SageMaker **doesn't analyze data using Hadoop**.

### Elastic MapReduce (EMR)
EMR is analytics service. NOT COMPUTE SERVICE.
- EMR helps you process large amounts of data using big data frameworks like Hadoop.
- EMR is a service that makes it easy to process large amounts of data efficiently.

### Amazon Kinesis
- There are four **types** of Kinesis services:
	- Kinesis Video Streams
	- Kinesis Data Streams
	- Kinesis Data Firehose
	- Kinesis Data Analytics
- It enables you to build custom applications that process or analyze **streaming data** for specialized needs.
- **Producers** continually push data to Kinesis data Streams and **Consumers** process the data in *real time*.
- Consumers can <ins>store their results</ins> using an AWS service such as:
	- Amazon DynamoDB
	- Amazon Redshift
	- Amazon S3
 - Usecase: A company with a popular website would like to analyze website clickstreams in real time to determine site usability.

### AWS CloudFormation
- It provides a **common language** for you to <ins>describe</ins> and <ins>provision</ins> all the infrastructure resources in your cloud environment.
- It's free of charge.
- **Change sets** allow you to preview how proposed changes to a stack might impact your running resources.

### AWS Elastic Beanstalk
-  The **fastest** and **simplest** way to get web applications up and running on AWS.
-  Create mobile API backends for your applications
-  Deploy scalable web applications in minutes without the complexity of provisioning and managing underlying infrastructure.
-  Wide selection of application platforms (Java, .NET, Node.js, PHP, Ruby, Python, Go, and Docker)
-  Application Health (collects 40+ key metrics and attributes)
-  Updates and management
-  Meets the criteria for ISO, PCI, SOC 1, SOC 2, and SOC 3 compliance along with the criteria for HIPAA eligibility.
-  Uses Elastic Load Balancing and Auto Scaling 

### AWS Lambda
- Lambda functions can be invoked in response to **events**.
	- Invoke a function in response to resource lifecycle events, such as with Amazon **S3**. (*Lambda & S3*)
	- Respond to incoming **HTTP requests**. (*Lambda & API Gateway*)
	- Consume events *from* a **queue**. (*Lambda & SQS*)
	- Run a function on a **schedule**. (*Lambda & CloudWatch*)

### AWS Well-Architected Framework
[AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected)

The framework is based on six pillars: 
- Operational excellence
	- Deploy smaller, reversible changes.
	- Plan for and anticipate failure.
 	- Script operations as code.
- Security
	- Track who did what and when.
	- Assign only the least privilege required.
- Reliability
- Performance efficiency
	- Information gathered through the evaluation process to actively drive adoption of new services or resources.
	- Use multi-region deployments.
	- Use a serverless architecture first.
- Cost optimization
- Sustainability

Operational excellence Design principles:
	- Perform operations as code: In the cloud, you can apply the same engineering discipline that you use for application code to your entire environment. You can define your entire workload (applications, infrastructure, etc.) as code and update it with code. You can script your operations procedures and automate their process by launching them in response to events. By performing operations as code, you limit human error and create consistent responses to events.
	- Make frequent, small, reversible changes: Design workloads that are scaleable and loosely coupled to permit components to be updated regularly. Automated deployment techniques together with smaller, incremental changes reduces the blast radius and allows for faster reversal when failures occur. This increases confidence to deliver beneficial changes to your workload while maintaining quality and adapting quickly to changes in market conditions.
	- Refine operations procedures frequently: As you evolve your workloads, evolve your operations appropriately. As you use operations procedures, look for opportunities to improve them. Hold regular reviews and validate that all procedures are effective and that teams are familiar with them. Where gaps are identified, update procedures accordingly. Communicate procedural updates to all stakeholders and teams. Gamify your operations to share best practices and educate teams.
	- Anticipate failure: Perform “pre-mortem” exercises to identify potential sources of failure so that they can be removed or mitigated. Test your failure scenarios and validate your understanding of their impact. Test your response procedures to ensure they are effective and that teams are familiar with their process. Set up regular game days to test workload and team responses to simulated events.
	- Learn from all operational failures: Drive improvement through lessons learned from all operational events and failures. Share what is learned across teams and through the entire organization.
	- Use managed services: Reduce operational burden by using AWS managed services where possible. Build operational procedures around interactions with those services.
	- Implement observability for actionable insights: Gain a comprehensive understanding of workload behavior, performance, reliability, cost, and health. Establish key performance indicators (KPIs) and leverage observability telemetry to make informed decisions and take prompt action when business outcomes are at risk. Proactively improve performance, reliability, and cost based on actionable observability data.

Performance efficiency Design principles:
- Democratize advanced technologies: Make advanced technology implementation easier for your team by delegating complex tasks to your cloud vendor.
- Go global in minutes: Deploy your workload in multiple AWS Regions.
- Use serverless architectures: Serverless architectures remove the need for you to run and maintain physical servers for traditional compute activities. 
- Experiment more often: With virtual and automatable resources, you can quickly carry out comparative testing using different types of instances, storage, or configurations.
- Consider mechanical sympathy: Consider data access patterns when you select database or storage for your workload.

Cost optimization Design principles:
1. Adopt a consumption model
2. Measure overall efficiency
3. Stop spending money on data center operations
4. Analyze and attribute expenditure
5. Use managed services to reduce cost of ownership

Reliability Design principles:
1. Test recovery procedures
2. Automatically recover from failure
3. Scale horizontally to increase aggregate system availability:
4. Stop guessing capacity
5. Manage change in automation

Security Design principles:
1. Implement a strong identity foundation
2. Enable traceability
3. Apply security at all layers
4. Automate security best practices
5. Protect data in transit and at rest
6. Prepare for security events

### AWS WAF
- AWS Web Application Firewall creates custom rules that block <ins>common attack patterns</ins>, to protect against **common exploits** that could compromise application availability and security or consume excessive resources, such as:
	- SQL injection.
	- Cross-site scripting.
	- Rules that are designed for your specific application

### AWS Shield
- AWS Shield is a managed DDoS protection service, working with AWS WAF
	- AWS Shield Standard: no costs, defense from common and frequent DDoS attacks
	- AWS Shield Advanced: paid service, diagnostics and ability to detect and mitigate DDoS attacks

### AWS AD Connector
- A directory gateway for **redirecting** <ins>directory requests</ins> to your on-premise Active Directory.
- Connects your **existing** *on-premise AD* to AWS.

### AWS Simple AD
- An inexpensive **Active Directory**-compatible service with common directory features.
- It is a **standalone**.
- It does **not** connect your on-premise AD to AWS

### Amazon Elastic Container Service for Kubernetes (EKS)
- It's a managed Kubernetes service that makes it easy for you to run Kubernetes on AWS without needing to install, operate, and maintain your own Kubernetes **control plane**.

### Amazon Elastic Container Service (ECS)
- It is used for running Docker containers on <ins>EC2 instances</ins>.

### Amazon Elastic Container Registry (ECR)
- It is container registry offering high-performance hosting, so you can reliably deploy application images and artifacts anywhere.

### Virtual Private Gateway
- It's the VPN concentrator on the **Amazon side** of the <ins>VPN connection</ins>.
- You create a virtual private gateway and *attach* it to the **VPC** from which you want to create the VPN connection.
- <ins>NAT devices and firewalls</ins> are **not** required for an *AWS managed VPN*.
- A **customer gateway** is a physical device or software application on **your side** of the VPN connection.

### VPC peering connection
- If you have **more than one AWS account**, you can **peer** the VPCs across those accounts to create a <ins>file sharing network</ins>.
- You **cannot** peer *subnets*.
- It is a way of <ins>allowing routing between VPCs</ins> in *different AWS accounts*.
- It enables you to route traffic via **private IP addresses** between *two* peered VPCs.

### AWS support plans
[Compare AWS Support Plans](https://aws.amazon.com/premiumsupport/plans/)

- **Basic Support** is included for all AWS customers and includes:
	- Customer Service and Communities - 24x7 access to customer service, documentation, whitepapers, and AWS re:Post.
	- AWS Trusted Advisor - Access to core Trusted Advisor checks.
	- AWS Health - A personalized view of the health of AWS services, and alerts when your resources are impacted.
- **Developer**
- **Business**
- **Enterprise On-Ramp**
- **Enterprise**
	- Technical Account Manager (TAM).
 	- Access to AWS Incident Detection and Response for an additional fee.
  	- AWS Trusted Advisor Priority.

### Amazon IAM
- IAM (Identity and Access Management) controls authentication and authorization within an AWS account.
- You **cannot** use IAM to create **local user accounts** on any system.
- You are also not charged for what you use, <ins>IAM is free to use</ins>.
- You can share access to your AWS account.
- Identity federation.
- PCI DSS compliance.
- AWS recommended **best practices**:
	- Create individual IAM users
	- Least privilege principle: granting only the permissions that are needed to perform specific tasks
- IAM **supported authentication** methods include:
	- Console passwords
	- Access keys
	- Server certificates
- Best practice to ensure the security of AWS account
	- **Don’t generate** an access key for the **root account** user. Delete your root access keys.
	- Use **Temporary Security Credentials** (IAM Roles) Instead of Long-Term Access Keys
	- Manage IAM User Access Keys Properly
- You can enable single sign-on (**SSO**) to your AWS accounts by using **federation** and AWS Identity and Access Management (IAM).
- All you can do with an **access key** once it has been generated is to:
	- Make active
	- Make inactive
	- Delete
- IAM Policy Simulator evaluates the policies that you choose and determines the effective permissions for each of the actions that you specify.
- The IAM credential report lists all the users and the status of their various credentials, including passwords, access keys, server certificates, and MFA devices in order to support auditing and compliance efforts.
- Usecase: At each month-end, the staff member needs access to an application running on EC2: Have the user request temporary security credentials for the application by assuming a role.
- Which term refers to the Identity and Access Management (IAM) resource objects that AWS uses for authentication?
- Entities - **IAM entities are the users (IAM users and federated users) and roles** that are created and used for authentication.

**Resources** – The AWS resource object upon which the actions or operations are performed.

**Principal** – The person or application that used an entity (user or role) to send the request. Information about the principal includes the policies that are associated with the entity that the principal used to sign in.

An **IAM identity** represents a human user or programmatic workload, and can be authenticated and then authorized to perform actions in AWS. Each IAM identity can be associated with one or more policies. 

### Amazon Cognito
- Amazon Cognito Identity Pool provides temporary AWS credentials for users who are guests (unauthenticated) and for users who have been authenticated and received a token. An identity pool is a store of user identity data specific to your account.
- Amazon Cognito User Pool is a user directory in Amazon Cognito. It doesn't enable access to unauthenticated identities. You have to use an Identity Pool instead.

### AWS Organizations
- **One bill provided** per AWS organization
- Best practices:
	-  Always enable **multi-factor** authentication (MFA) on the root account
	-  Always use a **strong and complex password** on the root account
	-  The **Paying account** should be used for **billing purposes only**. Do not deploy resources into the Paying account
- Features:
	- Service control policies (SCPs). Central governance and management for multiple accounts. No permissions are granted by an SCP. An SCP defines a guardrail, or sets limits. **The most efficient way to establish controls that all IAM users within an organization adhere to.**
- With below options organizations can **reduce their cost**:
	-  "Create an AWS Organization configuration linking the accounts"
	-  "Setup consolidated billing between the accounts"
- Volume pricing discounts applied **across multiple accounts**.
- **Service control policies** case: What can the customer use to restrict the same permissions across all AWS accounts managed under AWS Organizations: Organization service control policies (SCPs) allow you to create permissions guardrails that apply to all accounts within a given organization.
- Usecase: Create an Organizational Unit structure in AWS Organizations with separate underlying accounts for production, development, and testing environments.

### Popular HTTTP code
- A HTTP 200 codes: successful
- A HTTP 300 codes: redirection
- A HTTP 400 codes: client error
- A HTTP 500 codes: server error

### AWS CloudTrail
- It is a web service that **records activity** made on your account and delivers <ins>log files</ins> to an **Amazon S3 bucket**.
- Logging and saves a history of API calls for your AWS account.
- It is for **auditing**.
- It records account activity and service events from most AWS services and logs the following records:
	- The identity of the API caller.
	- The time of the API call.
	- The source IP address of the API caller.
	- The request parameters.
	- The response elements returned by the AWS service.

### Amazon CloudWatch
- It is a service that enables you to monitor and manage various metrics and configure alarm actions based on data from those metrics. If metrics are above or under a threshold, a CloudWatch Alert can be triggered
- A repository for metrics and logs.
- CloudWatch Dashboard is a single location that allows to access all resources metrics
- The CloudWatch service is used to create billing alarms. 

### Amazon DynamoDB
- It's a fully managed **NoSQL** database service. (schema-less)
- You can scale the DB at any time **without incurring downtime**.
- DaynamoDB pricing models:
	- **On-demand capacity mode**: charges you for the data reads and writes your application
	- **Provisioned capacity mode**: you specify the number of reads and writes per second that you expect
- Availability model:
	- **Data is synchronously** replicated across **3** facilities in a region
- Best practices for storing **large items** and attributes in DynamoDB:
	- <ins>Compress</ins> large attribute values
	- Store large attributes as objects in <ins>Amazon S3</ins>.

### AWS Database SQL type
- Amazon RDS
- Amazon Aurora
- Amazon RedShift

### AWS Device Farm
- It is an **app testing service** that lets you **test** and **interact** with your **Android**, **iOS**, and **web apps** on <ins>many devices</ins> at once, or reproduce issues on a device in real time

### AWS Config
-  It allows you to **automate the evaluation of recorded** configurations against desired configuration.
-  It enables you to **assess**, **audit**, and **evaluate** the <ins>**configurations of your AWS resources**</ins>.
-  It continuously **monitors** and **records** your <ins>AWS resource configurations</ins> and allows you to automate the evaluation of recorded configurations against desired configurations.
-  It can be used to **keep track** of configuration changes on AWS resources, *keeping multiple date-stamped* versions in a reviewable history.
-  It can be used to **retrieve configuration** changes made to AWS resources causing *operational issues*.

### AWS Shared Responsibility Model
- AWS is responsible for:
	- Software: Compute, storage, database, networking **infrastructures**.
 	- Hardware: Regions, Availability Zones, Edge Locations.
  	- Infrastructure patches and configuration (shared responsibility)

- Customers are responsible for:
	- *Networking traffic protection*.
	- *Network and firewall configuration*.
 	- Data
	- Platform, Applications, Identity and Access Management (IAM)
	- Operating systems
	- Client-side data encryption, server-side data encryption
  	- OS / Applications / Database patches and configuration (shared responsibility)

- Shared responsibilities:
	- Patch Management.
	- Configuration Management.

### Amazon RDS
- Read replicas are used for **offloading read traffic** from the primary RDS database.
	- You can configure **read replicas** to be:
		- within as AZ
		- across AZs
		- across regions
- It provides "**Multi-AZ**" and "**Read Replicas**" to deliver *scalability*, *availibility* and *durability*.
- You can **restore** a DB instance to a specific **point in time** with a granularity of **5 minutes**
- **Multi-AZ**: <ins>synchronously</ins>
- **Read Replicas**: <ins>asynchronously</ins>
- RDS supports the following **engines**:
	- SQL Server
	- Oracle
	- MySQL Server
	- PostgreSQL
	- Aurora
	- MariaDB
- **Read replicas** are available for:
	- MySQL
	- PostgreSQL
	- MariaDB
	- Aurora
- RDS **automated** *backups* allow point in time recovery to any point within the retention period down to a second.
- RDS supports **automated backups** as a **default** configuration
- With RDS you are **charged for**:
	- the type and size of DB
	- document type (e.g multi AZ)
	- data transfer outbound
	- requests
	- the uptime
	- any additional storage of backup

### AWS Auto Scaling Group
- **Scaling Policy** determine when, if, and how the ASG scales and shrinks:
	- **on-demand** (dynamic scaling).
	- **cyclic** (scheduled scaling).
- **Scaling Plan** define the triggers and when instances should be provisioned / deprovisioned.

### AWS Auto Scaling
- The **scaling policies** include:
	- simple
	- scheduled
	- dynamic
	- step scaling
- vertical scaling -> scaling-up
- horizontal scaling -> scaling-out

### AWS CloudHSM
- **Cloud-based hardware security module** (HSM) that allows you to generate and store encryption keys and add high performance crypto operations to your AWS applications.
- CloudHSM has **no upfront costs** and provides the ability to *start* and *stop* HSMs **on-demand**, allowing you to provision cpacity when and where it is needed quickly and cost-effectively.
- CloudHSM is a managed service that **automates** <ins>time-consuming administrative tasks</ins>, such as hardware provisioning, **software patching**, **high availability**, and **backups**.
- It uses a highly secure *hardware storage device* to **store encryption keys**

### AWS Glacier
- Data access option **retrieves** data:
	- **Standard**: takes 3-5 hours
	- **Expedited**: within 1-5 minutes
- That is accessed though  S3.
- You *pay* for <ins>storage on a per GB/month</ins> basis, <ins>retrival requests</ins> and <ins>quantity</ins> (based on expedited, standard or bulk).
- For **interacting** with AWS **Glacier** require that you use the **AWS CLI** or write code (using **REST API**).
- Only Amazon Glacier has **a minimum storage** duration charge of **90** days.

### AWS Storage Gateway Volume Gateway
- The volume gateway represents the family of gateways that *support* **block-based volumes**, previously referred to as gateway-cached and gateway-stored modes. it allows you to <ins>use block-based volumes on-premise</ins> that are then **asynchronously** backed up to Amazon **S3**.
	- **Stored Volumes mode**:  the *entire dataset is stored on-site* and is **asynchronously** backed up to S3 (EBS point-in-time snapshots). Snapshots are incremental and compressed
	- **Cached Volume mode**: the *entire dataset is stored on S3* and a cache of the *most frequently accessed* data is cached on-site.

### AWS Step Functions
- It lets you **coordinate** *multiple AWS services* into **serverless** workflows so you can build and update apps quickly.
- It lets you build **visual** *workflows*.

### Amazon Simple Workflow Service (SWF)
- helps developers build, run, and scale background jobs that have parallel or sequential steps.
- SWF is **not** a <ins>*visual*</ins> workflow tool.
- It can assist with **coordinating tasks** across *distributed application* components.

### Amazon Security Token Service (STS)
- It's used for requesting **temporary** credentials.

### AWS Server Migration Service (SMS)
- It's an **agentless** service which makes it easier and faster for you migrate on-premises workloads to AWS.
- You can migrarte Virtual Machines from **VMware vSphere** and **Windows Hyper-V** to AWS with this sevice.

### AWS Database Migration Service (DMS)
On-premises, Amazon RDS DB instance, database on an Amazon EC2. From an AWS service to an on-premises database. Between source and target endpoints that use the same database engine, such as from Oracle to Oracle. Between source and target endpoints that use different database engines, such as from Oracle to PostgreSQL.
- Replicate ongoing changes
- Move to managed databases
- Remove licensing costs and accelerate business growth

### Amazon DevPay
- That makes it easy for budinesses to **sell applications** that are built in, or run on top of, *Amazon Web Services*.

### Amazon Elasticsearch Service
- For **operational analytics** such as:
	- application monitoring
	- log analytics
	- clickstream analytics
- It allows you to search, explore, filter, aggregate and visualize your data in near real-time.

### Amazon Athena
- For interactive analysis.
- Analyze (query) data directly in **S3** and **Glacier** using <ins>standard SQL queries</ins>.

### Amazon QuickSight
- For dashboards and visualizations.

### Amazon CodeStar
- It enables you to **quickly develop**, **build**, and **deploy** applications on AWS. AWS CodeStar provides a **unified user interface**, enabling you to easily manage your software development activities <ins>in one place</ins>.

### Amazon Cloud9
- It's a cloud-based integrated development environment (**IDE**) that lets you write, run, and debug your code with just a **browser**.

### Amazon CodeDeploy
- It is a deployment service that **automates application deployments** to:
	- Amazon Elastic Compute Cloud (EC2)
 	- Amazon Elastic Container Service (ECS)
 	- on-premises instances
 	- AWS Lambda
  	- AWS Fargate
  - Monitor health and rollback
  - Deploy to many hosts
  - Launch and track your application deployments' status through the AWS Management Console or AWS Command Line Interface (CLI).
  - Reuse your existing setup code and integrate with your existing software release process or continuous delivery toolchain.

### Amazon Route 53
- It has a **global scope**.
- Both **CNAME** records and **Alias** records can be used to <ins>map a domain name to a target domain name</ins>. However, only a **CNAME** record can be used to map to a target domain **external** to AWS.
- You can transfer domains to Route 53 only if the Top Level Domain (**TLD**) is supported.
- Amazon **Route 53 health checks** monitors the health and performance of your web applications, web servers, and other resources.
- It offers the following *functions*:
	- Domain Name registry.
	- DNS resolution.
	- Health checking of resources.
- **Routing policies** include:
	- Simple.
	- Weighted.
	- Latency-based.
	- Failover.
	- Geolocation.
 - Can be used to route users to infrastructure outside of AWS or to the nearest data center to reduce latency.
 - DDoS protection via Shield Advanced is supported on several services, including Route 53.

### Amazon CloudFront
- It has a **global scope**.
- It is a content delivery network (**CDN**) that allows you to store (cache) your content at "**edge locations**" located around the world.
- This allows customers to access content **more quickly** and provides security against **DDoS attacks**.
- It can be used for **data**, **videos**, **applications**, and **APIs**.
- Routing policies:
	- Simple.
	- Weighted.
	- Latency-based.
	- Failover.
	- Geolocation.
	- Geoproximity.
	- Multi-value.
	- Traffic flow.
- It supports below **origins**:
	- S3 Bucket.
	- EC2 instance.
	- Elastic Load Balancer.
	- Route 53.
 - You can use several different kinds of origins with CloudFront. You can use an Amazon S3 bucket, a MediaStore container, a MediaPackage channel, an Application Load Balancer, or an AWS Lambda function URL (valid domain name).

### Amazon Lightsail
- It provides developers compute, storage, and networking capabilities to deploy and manage websites, web applications, and databases in the cloud. Also it provides **preconfigured VPS** that inclouds **everything required to deploy** or create a **DB**.
- The **product set** includes:
	- **VPS** (Virtual Private Servers)
	- Managed **MySQL** databases
	- **HA** storage
	- **Load balancing**
- Launch a WordPress website.

### Amazon EC2
- Types:
	- **General Purpose**: instances provide a balance of compute, memory and networking resources, and can be used for diverse workloads; these are ideal for applications that use resources in equal proportions such as web servers and code repositories.
	- **Compute Optimized**: instances are ideal for compute bound applications that benefit from high performance processors; these are well suited for batch processing workloads, media transcoding, high performance web servers, high performance computing (HPC), scientific modeling, dedicated gaming servers and ad server engines, machine learning inference and other compute intensive applications.
	- **Memory Optimized**: instances are designed to deliver fast performance for workloads that process large data sets in memory.
	- **Accelerated Computing**: instances use hardware accelerators, or co-processors, to perform functions, such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs.
	- **Storage Optimized**: instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage; these are optimized to deliver tens of thousands of low-latency, random I/O operations per second (IOPS) to applications.
	- **High Performance Computing**: instances are built to offer the best price performance for running HPC workloads at scale on AWS; these are ideal for applications that benefit from high-performance processors such as large, complex simulations and deep learning workloads.
- EC2 pricing model:
	- **On-Demand**: Fixed price billed by the second. No upfront payments or commitments. No interruption. For unpredictable workloads. If workload won't run longer that a year. For developing, HA, Disaster Recovery, Capacity Assurance. **Capacity Reservations** hold capacity whether or not you run an instance.
	- **Spot**: Take advantage of unused EC2 capacity. When start and stop time don't matter. Can interrupt workload. **THE CHEAPEST OPTION**. Pay at the beginning of the hour. No capacity reservation.
	- **Dedicated Host**: Pay for a physical server. Bring ypur own server-bound software license (per socket, core, VM). Corporate compliance requirements around tenancy (hardware sharing resourses with other companies). No sharing.**Dedicated Instance** runs on the host.
	- **Reserved Instances**: Commit to a SPECIFIC instance type for 1 to 3 years. Pay upfront. App requires a capacity reservation. Reserve capacity.
	- **Savings Plan**: Commit to compute usage for 1 to 3 years (per hour). Lower bill across multiple compute (EC2, Lambda, Fargate, SageMaker). No capacity reservation.
- It offers SLAs of **95%** for *each region*.
- EC2 **benefits** over using non-cloud servers:
	- Elastic Web-Scale computing
	- Inexpensive
- Types of Reserved Instance(RI):
	- **Standard RIs**: These provide the **most significant discount** (up to 75% off On-Demand) and are best suited for **steady-state** usage.
	- **Convertible RIs**: These provide a discount (up to 54% off On-Demand) and the <ins>capability to change</ins> the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value. Like Standard RIs, Convertible RIs are best suited for steady-state usage.
	- **Scheduled RIs**: These are available to launch within the time windows you reserve. This option allows you to match your capacity reservation to a predictable recurring schedule that only requires a **fraction of a day, a week, or a month**.
	- Payment options for reserverd instances include All Upfront, Partial Upfront, and NoUpfront.
- With EC2 you are billed either by the **second**, for some Linux instances or by **hour**.
- With "**Inter-Region VPC Peering**" a company can connect their EC2 instances in <ins>*one region*</ins> with EC2 instances in <ins>*another region*</ins> using **private IP** addresses.

### AWS Cost Explorer
-  It is a free tool that allows you to **view charts** of your costs. You can view cost data for the **past 13 months** and **forecast** how much you are likely to spend over the **next 3 months**. Cost Explorer can be used to **discover patterns** in how much you spend on AWS resources over time and to **identify cost problem** area.
- Not for billing alarms (CloudWatch service is used to create billing alarms)

### AWS Cost Anomaly Detection
- Reduce cost surprises and enhance control without slowing innovation.
- Send alerts when anomalous spending is detected.

### Amazon Elastic Transcoder
- It **converts video and audio files** from their source format into versions that will **playback** on devices like smartphones, tablets and PC.

### AWS Glue
- Is a fully managed **extract**, **transform**, and **load** (**ETL**) service that makes it easy for customers to prepare and load their <ins>data for analytics</ins>.

### AWS Artifact
- It is a self-service audit artifact retrieval **portal** that provides our customers with on-demand access to AWS’ compliance **documentation** and AWS **agreements**.
- You can use **AWS Artifact Reports** to download AWS security and compliance documents, such as <ins>AWS ISO certifications</ins>, <ins>Payment Card Industry (PCI)</ins>, and <ins>System and Organization Control (SOC) reports</ins>.
- It is **online**, self-service portal that AWS provides to enable customers to *view reports* and, such as *PCI reports*, and *accept agreements*.
- It is your **go-to**, central resource for compliance-related information that matters to you.

### AWS Service Catalog
- It can be used to <ins>create and manage a selection of AWS services</ins> that are approved for use on AWS.
- These IT services **can include everything** from virtual machine images, servers, software, and databases to complete multi-tier application architectures.

### AWS Managed Services (AMS)
AWS Managed Services (AMS) offers monitoring, incident detection, response, and remediation for AWS infrastructure and security incidents.

What we DON'T do:
- While AMS simplifies application deployment by providing a number of manual and automated options, you're responsible for the development, testing, updating, and management of your application. AMS provides troubleshooting assistance for infrastructure issues that impact applications, but AMS can't access or validate your application configurations.

- It manages the **daily operations** of your AWS infrastructure in alignment with **ITIL** processes and provides a **baseline integration** with IT Service Management (**ITSM**) tools such as the ServiceNow platform.
- Managed Services helps you efficiently operate your AWS infrastructure and **reduces operational risks and overhead**.

AMS features:
- Logging, Monitoring, Guardrails, and Event Management
- Backup and Restore
- Security and access management
- Patch management
- Change management
- Automated and self-service provisioning management (provision AWS resources)
- Incident management/Problem management/Reporting
- Service request management
- Designated resources
- Developer mode
- Firewall management
- Customer-managed account
- AWS support/Service Desk 

### Amazon Machine Image (AMI)
- It contains three catagories:
	- Community AMIs
	- AWS Marketplace AMIs
	- My AMIs
- It stores the **information** that defines an **EC2 instance** such as the template for the *root volume*, *launch permissions* and *block device mappings*.
- A Golden AMI can create an exact copy of a resource in another region.

### Amazon S3 Transfer Acceleration
- It enables fast, easy, and secure **transfers** of files **over long distances** between your client and your Amazon S3 bucket.

### Amazon Neptune
- Amazon Neptune is a fast, reliable, fully-managed **graph database** service that makes it easy to build and run applications that work with highly connected datasets.

### AWS Direct Connect
- Benefits:
	- Reduce cost when using large volumes of traffic
	- Increase reliability (predictable performance)
	- Increase bandwidth (predictable bandwidth)
	- Decrease latency
- It uses <ins>private network connections</ins> (It's **NOT** based on internet connection)
- It is available in **1Gbps** and **10Gbps** speeds.
- When connecting to AWS over Direct Connect:
	- You can connect to all AZs **within the VPC** of the **local region**.
	- You can connect to public services in **remote regions**.
- You can use **AWS Direct Connect Gateway** for connecting a company from their on-premises network to VPCs in **multiple regions** using **private connections**
- Hybrid Deployment Model uses Direct Connect.

### AWS Snow family
- AWS Snowcone is a small, rugged, and secure edge computing and data transfer device. It features 2 CPUs, 4 GB of memory, and up to 14 TB of usable storage.
- AWS Snowball is a **petabyte-scale** <ins>data transport</ins> solution that uses devices designed to be secure to transfer large amounts of data **into and out of** the AWS Cloud.
	- Snowball Edge Storage Optimized devices are well suited for large-scale data migrations and recurring transfer workflows.
 	- Snowball Edge Compute Optimized provides powerful computing resources for use cases such as machine learning, full motion video analysis, analytics, and local computing stacks.
- AWS Snowmobile is an exabyte-scale data transfer service used to move large amounts of data to AWS, up to 100 petabytes of data, a 45-foot long ruggedized shipping container, pulled by a semi trailer truck.

### Amazon Comprehend
- Amazon Comprehend is a natural language processing (**NLP**) service that uses **machine learning** to find insights and relationships in **text**.

### Amazon Resource Names (ARNs)
- It is used to **uniquely identify AWS resources**.

### AWS IoT Core
- It lets **connected devices** *easily* and *securely* interact with cloud applications and other devices.

### AWS Fargate
- Fargate <ins>removes the need to provision and manage servers</ins>.
- Amazon ECS is a container orchestration service used to provision and manage container clusters.
- It's **Serverless** offering (**no** EC2 instances)

### Amazon Detective
- It uses **machine learning** and **graph theory** capability collected log data to help you conduct faster and efficient security invedtigations.

### Amazon Global Accelerator
- You are asked to **improve the performance** of the application for <ins>local and global users</ins>. As part of this initiative, you must **monitor** the **application endpoint health** and **route traffic** to the most appropriate endpoint. For aiming this we should use amazon global accelerator.
- Usecase: A company has developed a popular online multiplayer gaming application. How can the company enhance its players' online experience and improve overall application availability and reduce in-game latency?

### AWS Data Sync
- It is a simple and fast way to **move huge amounts** of data (hundreds of terabytes) between **on-premise** storage to **S3**, **EFS**, **FSx**.

### AWS CodePipeline
- AWS CodePipeline is a **continuous delivery service** you can use to **model**, **visualize**, and **automate the steps** required to release your software. You can quickly model and configure the different stages of a software release process. CodePipeline automates the steps required to release your software changes continuously.
- To orchestrate and **automate** the **various phases** involved in the release of application updates in-line with a predefined release model.

### Amazon GuardDuty
The most efficient intelligent threat detection service that can be used to analyze malicious or unauthorized activity and continuously monitor CloudTrail event logs, Amazon VPC Flow Logs, and DNS logs.
- Amazon GuardDuty is a **threat detection** service that **continuously monitors** your **AWS accounts** and **workloads** for malicious activity and delivers detailed security findings for visibility and remediation.
- For implementing a threat detection service that continuously monitors malicious activities and **unauthorized behaviors** protect AWS account, workloads and data stored in Amazon S3 we use this service.
- Not for DDoS protection

### Amazon Macie
- It can be used to **detect users' personal credit card numbers** from data stored in Amazon **S3**.

### AWS OpsWorks
- It is a service that allows you to host your own Puppet Enterprise infrastructure.

### Geographical Services
- Global level
	- AWS Route 53
	- AWS Cloud Front
	- AWS Direct Connect Gateway
	- AWS Global Accelerator
	- S3 (but data Regional)
	- IAM
	- WAF
	- AWS SNS
- Regional level
	- VPC
	- Security Groups
	- Resource Identifiers
 	- EFS	
	- ECS
	- ECR
	- Amazon GuardDuty
	- Amazon Detective
	- Amazon Inspector
	- Amazon Macie
	- AWS Security Hub
	- AWS Migration Hub
	- AWS Config
- Availability Zone level
	- Subnet
	- Elastic Load Balancer
	- EC2 Instances
	- EBS Volumes
	- Cluster Placement Groups

### AWS Trust & Safety team
Use the Report Amazon AWS abuse form to report suspected abuse of AWS resources (Web content/non-copyright intellectual property, Copyright , Email abuse, Network activity, Hacking).

### Amazon VPC
With Amazon Virtual Private Cloud (Amazon VPC), you can launch AWS resources in a logically isolated virtual network that you've defined.

- Amazon VPC is a **free of charge** service.
- Security groups: act like built-in firewalls for your virtual servers — the rules you create define what is allowed to talk to your instances and how.
Note: Although **network access control lists** can be used to block or deny traffic, these operate at the subnet level (covering all instances in the subnet with the same ruleset), not per instance as the question specifies.
- Route tables: tell traffic where it should go next to reach its destination.
- NAT gateway: Is required to allow resources in a private subnet to access the internet.
- Internet gateway:
	- Enables resources inside your VPC to reach the internet, as long as route tables and IP addresses are correctly configured in your environment.
	- An internet gateway allows public traffic to the internet from a VPC.
   	- For a subnet to be public and send non-local traffic to the internet

### Infrastructure Event Management
AWS Infrastructure Event Management is a structured program available to **Enterprise Support** customers that helps you plan for large-scale events, such as product or application launches, infrastructure migrations, and marketing events. It is also available to Business Support customers, but they need to pay an additional fee to use this service and cannot use it normally as part of their plan.

### Amazon Aurora

- Aurora delivers up to **five times** the throughput of MySQL, not three times.
- You can use the AWS Management Console, AWS CLI commands, and API operations to handle routine database tasks
- It is compatible with the MySQL and PostgreSQL database engines.

***
### Notes
- **Loose Coupling**: a desirable attribute of an IT system is that it can be broken into smaller, loosly coupled components.
- **Bootstrapping** and **Infrastructure as code** are two echniques for using automated, repeatable processes that are fast and avoid human error.
- **Golden Image Instances**: a golden image is a snapshot of a particular state for that resource (e.g. EC2 instances, RDS instances, EBS volumes).
- "**Direct Connect**" and "**VPN CloudHub**" are two ways of connecting to an *Amazon VPC* from an *on-premise* data center.
- If you have **multiple VPN connections**, you can provide secure communication **between sites** using the **AWS VPN CloudHub**.
- Health Insurance Portability and Accountability Act of 1996 (**HIPAA**) is used for **secure AWS environment** to process, maintain and store protected health information.
- "**File Gateway**" and "**Gateway Virtual Tape Library**" are types of <ins>AWS storage gateway</ins>.
- "**Virtual Gateway**" on the <ins>VPC side</ins> and a **Customer Gateway** on <ins>the on-premise network side</ins> need to connect VPC with a VPN connection (those are <ins>parts of Amazon Managed VPN connection</ins>).
- *AWS Managed VPN* uses **internet connection**.
- **Resource groups** make it easy to group resources using the tags that are assigned to them. You can group resources that share one or more tags.
- "**PCI DSS**" is an **information security standard** applies to entities that store, process or transmit credit **cardholder data**.
- With the public cloud the consumer organization typically incurs **OPEX costs for usage**.
- You **cannot detach** a primary network interface (**eth0**) from an instance. You can create and attach **additional** network interfaces.[elastic network interface(**ENI**)].
- **NAT Instances** are managed by **you** and they must be **scaled manually** and <ins>do not privide HA</ins>. They can be used as **bastion** hosts and can be *assigned to security groups*.
- **NAT Gateway** is managed for you by **AWS**. They can **scale automatically** and they are **not** *associated with any security groups*. They are highly available in **each AZ**.
- You can use **DynamoDB** and **SWF** for create "stateless" applications.
- These are valid use cases for using AWS services to implement **real-time auditing**:
	- Use Amazon Inspector to monitor for compliance.
	- Use AWS Lambda to scan log files.
- The options available in the **VPC Wizard** are:
	- VPC with a Single Public Subnet.
	- VPC with Public and Private Subnets.
	- VPC with Public and Private Subnets and Hardware VPN Access.
	- VPC with a Private Subnet Only and Hardware VPN Access.
- Only the **Memcached** and **Redis** database engines can be used with **ElastiCache**.
- **AWS Migration Hub** provides a **single location** to <ins>track the progress of application migrations</ins> across multiple AWS and partner solutions.
- Amazon **CloudWatch**:
	- **Basic** monitoring: collects metrics **every 5 minutes**.
	- **Detailed** monitoring: collects metrics **every 1 minute**.
- Your payment model in cloud is operational (**OPEX**).
- "**AWS Concierge**" is available to support customers on an **Enterprise** support plan.
- You use a **key pair** to decrypt the Administrator password through the console or using the CLI (For Amazon EC2 **Windows** instance).
- An **RTMP** distribution (It is a type of Amazon CloudFront distribution) is used to distribute streaming media files using **Adobe Flash** Media Server’s RTMP protocol.
- The **public cloud** is offered under a purely **pay as you go** model, and allows companies to completely **avoid** *CAPEX costs*.
- AWS **Lambda** and Amazon **API Gateway** are both **app-facing** components of the AWS Serverless infrastructure.
- Amazon **DynamoDB** and **EFS** are *database and storage* services of the serverless infrastructure.
- The *EC2 container registry* (**ECR**) is a managed AWS Docker registry service for storing, managing and deploying Docker images.
- **Amazon Aurora Multi-Master** can scale out **write** performance for their Amazon Aurora database across *multiple* availability zones.
- **Placement groups** are a logical grouping of instances in one of the following configurations:
	- A **Cluster**: It's a logical grouping on intances **within a single AZ**. Cluster placement groups are recommended for **applications** that benefit from **low network latency**, **high network throughput**, or both, and if the majority of the network traffic is between the instances in the group.
	- A **spread**:  that are each placed on **distinct** underlying hardware. Spread placement groups are recommended for **applications** that have **a small number of critical instances** that should be kept separate from each other.
- With "**EC2**, **Auto Scaling** and **E**lastic **L**oad **B**alancing" combination of AWS services could be used to deploy a **stateless** web application that can automatically and elastically scale.
- With the AWS cloud you get **fine-grained** billing and can **turn off resources** you are not using easily and not have to pay for them.
- To install a **PCI-compliant** workload on AWS:
	-  Use an AWS service that is in scope for PCI compliance and apply PCI controls at the application layer.
-  In IAM user access and secrert keys:
	-  The customer is responsible for **rotating** keys.
- Access control lists (ACLs) are one of the resource-based options.
- IaaS offers building blocks that can be rented. EC2 is an example of IaaS.
- You are using your corporate directory to grant your users access to AWS services. What is this called? **Federated access** is when you use an external directory, such as your corporate one, to grant users in that directory access to AWS resources. 
