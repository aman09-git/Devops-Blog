---
title: "AWS Resource Tracker Project using Shell for Devops"
seoTitle: "Shell Scripting"
datePublished: Sat Nov 25 2023 16:29:15 GMT+0000 (Coordinated Universal Time)
cuid: clpe9nqoy000109jo5nym3ni0
slug: aws-resource-tracker-project-using-shell-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1700928834798/eae31884-c944-4300-8d53-dee1c492c2f3.jpeg
tags: automation, devops, shell-script, devops-articles, 90daysofdevops

---

### Why?

So, In organizations, we have multiple AWS services/resources running in their environment and at times people forget to stop the unused resources/services and they go unused. And DevOps is all about optimizing the factors that support efficient development.

In the real-world DevOps scenario, The **AWS Resource Tracker** script is widely used to provide an overview of the AWS resources being utilized within an environment.

It aims to help organizations monitor and manage their AWS resources effectively. The script utilizes the AWS Command Line Interface (**CLI**) to fetch information about different AWS services, such as **S3 buckets, EC2 instances, Lambda functions, and IAM users**.

### What we will get from this project?

By running the AWS Resource Tracker script, users can quickly obtain a list of S3 buckets, EC2 instances, Lambda functions, and IAM users associated with their AWS account.

This information can be valuable for various purposes, including auditing, inventory management, resource optimization, and security assessment.

### Create an EC2 instance

So, the first thing that we need to do is to create an EC2 instance in AWS. Please check out the below link to get started with EC2 instance creation. In this blog, we have covered EC2 creation and connecting it through SSH.

%[https://aman09.hashnode.dev/amazon-ec2] 

Once the EC2 instance is created, we will need to connect it through the SSH like below and then go to the root user with sudo su.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699702336174/97f4bcad-a591-439d-8081-169696b1966b.png align="center")

### AWS CLI Configuration

Once we are connected install the AWS CLI with the below command.

```plaintext
sudo yum install aws-cli   OR 
sudo yum install aws-cli -y 

aws --version - To check the version of CLI
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699702488516/be092e35-105f-4c81-87a1-dabf7152c3a3.png align="center")

Now we have to configure the AWS credentials and default configuration with the AWS CLI. To do this we need to run the below command and give the below information when prompted in CLI.

```plaintext
aws configure
```

1. **AWS Access Key ID:** This is your AWS access key, which is associated with an AWS IAM user. It is used to authenticate your CLI requests to AWS services.
    
2. **AWS Secret Access Key:** This is the corresponding secret key that goes along with the access key. It is used to authenticate your CLI requests.
    
3. **Default Region:** You can specify a default AWS region that the CLI should use for requests. If not specified, the CLI will use the region `us-east-1` by default.
    
4. **Default Output Format:** You can choose the default output format for the AWS CLI responses, such as JSON, text, or table. JSON is commonly used for machine-readable output.
    

To get your AWS Access and AWS Secret Access key, follow the below paths.

1. In the AWS console search for IAM.
    
2. Go to the users section on the left-hand side.
    
3. Select the user for whom you want to set AWS CLI
    
4. Now Scroll down and you will get an option to create an AWS **Access key and an AWS Secret Access key.**
    

Something like below :

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699703020446/a2d71f02-09f8-4dcc-9cb1-d3c662aedafa.png align="center")

### The Script:

Now, that our set-up is completed, let's jump to create the scrips.

```plaintext
"aws_tracker" 35L, 553B                                                                                                                                                                   18,0-1        All
#########################
# Author: Your Name
# Date: 10/11/23
# Version: v1
#
# This script will report the AWS resource usage
########################

set -x

# AWS S3
# AWS EC2
# AWS Lambda
# AWS IAM Users

# list s3 buckets
echo "List of s3 buckets"
aws s3 ls

# list EC2 Instances
echo "List of ec2 instances"
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'

# list lambda
echo "List of lambda functions"
aws lambda list-functions

# list IAM Users
echo "List of iam users"
aws iam list-users
```

* It is a good convention to always provide your details so that it will make it easier for other developers to contribute if they want to ie, metadata.
    
* The command `set -x` is given here to debug the script, this will print the command that we are running and then print the output.
    
* The commands `aws s3 ls`, `aws lambda list-functions` and `aws iam list-users` print the information of the given statement.
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><code>aws ec2 describe instances | jq '.Reservations[].Instances[].InstanceId'</code> will give you all the Instance IDs present in your <code>aws</code> in <code>JSON</code> format.</div>
</div>

### Test the script:

Run the below command :

```plaintext
./aws_tracker
```

So, the script that I have created is getting 2 EC2 instances, 2 users one S3 bucket and there are no Lamda functions running.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699704151340/294f8ee8-71f2-45a5-ad03-310b592d8b09.jpeg align="center")

### Schedule it with crontab:

Here's what each field in the cron schedule means:

* `0`: Minute (0-59)
    
* `3`: Hour (0-23)
    
* **\`\`**: Every day of the month
    
* **\`\`**: Every month
    
* **\`\`**: Every day of the week
    

Also with the below command, we can get the output of the script in a text format and get this saved in the file.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700928577996/5fc2d05c-4c9b-4267-8138-1425b12265b0.png align="center")

Here is the output of the command:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1700928676173/34c22a57-0782-40ce-948f-78024b3bf776.png align="center")

***Hope this was helpful. Thank you for your time !!***

***Stay Connected, many more to come !!***

Special thanks to @[Abhishek Veeramalla](@AbhishekVeeramalla) !!