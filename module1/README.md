# **AWS Transfer for SFTP**

### Using IP whitelisting to secure your AWS Transfer for SFTP servers

© 2020 Amazon Web Services, Inc. and its affiliates. All rights reserved.
This sample code is made available under the MIT-0 license. See the LICENSE file.

Errors or corrections? Contact [russboye@amazon.com](mailto:russboye@amazon.com).

---

# Module 1
## Deploy resources via CloudFormation

In this module, you will use CloudFormation scripts to deploy resources in an AWS region. This CloudFormation template will deploy a new VPC in the chosen region with a private CIDR block, two subnets within that CIDR block, an Internet Gateway for routing public internet traffic, and two Elastic IPs for hosting your AWS SFTP endpoint

## Module Steps

#### 1. Deploy AWS resources in your desired region

1. Click one of the launch links in the table below to deploy the required resources using CloudFormation.  To avoid errors during deployment, select a region in which you have previously created AWS resources.

  | **Region Code** | **Region Name** | **Launch** |
  | --- | --- | --- |
  | us-west-1 | US West (N. California) | [Launch in us-west-1](https://console.aws.amazon.com/cloudformation/home?region=us-west-1#/stacks/new?stackName=AWSSFTPWorkshop-IPwhitelisting&templateURL=https://aws-transfer-samples.s3-us-west-2.amazonaws.com/workshops/ip-whitelisting/sftp-workshop-endpoint.yaml) |
  | us-west-2 | US West (Oregon) | [Launch in us-west-2](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=AWSSFTPWorkshop-IPwhitelisting&amp;templateURL=https://aws-transfer-samples.s3-us-west-2.amazonaws.com/workshops/ip-whitelisting/sftp-workshop-endpoint.yaml) |
  | us-east-1 | US East (N. Virginia) | [Launch in us-east-1](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=AWSSFTPWorkshop-IPwhitelisting&templateURL=https://aws-transfer-samples.s3-us-west-2.amazonaws.com/workshops/ip-whitelisting/sftp-workshop-endpoint.yaml) |
  | us-east-2 | US East (Ohio) | [Launch in us-east-2](https://console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/new?stackName=AWSSFTPWorkshop-IPwhitelisting&templateURL=https://aws-transfer-samples.s3-us-west-2.amazonaws.com/workshops/ip-whitelisting/sftp-workshop-endpoint.yaml) |
  | eu-west-1 | Ireland | [Launch in eu-west-1](https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/new?stackName=AWSSFTPWorkshop-IPwhitelisting&templateURL=https://aws-transfer-samples.s3-us-west-2.amazonaws.com/workshops/ip-whitelisting/sftp-workshop-endpoint.yaml) |
  | eu-central-1 | Frankfurt | [Launch in eu-central-1](https://console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/new?stackName=AWSSFTPWorkshop-IPwhitelisting&templateURL=https://aws-transfer-samples.s3-us-west-2.amazonaws.com/workshops/ip-whitelisting/sftp-workshop-endpoint.yaml) |

2. Click **Next**  on the Create Stack page.
3. Click **Next** (there are no stack parameters).
4. Click **Next**.
5. Click **Next**  Again. (skipping the Options and Advanced options sections)
6. On the Review page, scroll to the bottom and click  **Create stack**.

The template allocates two Elastic IP addresses while creating a VPC, two subnets, and an Internet Gateway. AWS SFTP uses a Multi-AZ architecture to achieve high availability. By creating two subnets and assigning an Elastic IP address to each, your SFTP service is able to withstand the loss of an Availability Zone.

Note: While this solution uses Elastic IP addresses, you can also use EC2 BYOIP to import your own static IP addresses.  The BYOIP feature is particularly useful when you are migrating from an existing SFTP server and you must maintain the same endpoint IP addresses.

Once the AWS CloudFormation stack has been created, you see the following in the outputs tab:

![](images/image2.jpg)

## Module Summary

In this module, you deployed all of the resources necessary to complete this workshop in both the on-premises region and the in-cloud region.  You have also mounted the NFS export on the Application server and verified your data set.

In the next module, you will create a DataSync task to do an initial copy of files from the NFS server to the S3 bucket.

Go to [Module 2](/workshops/nfs-migration/module2).
