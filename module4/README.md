# **AWS Transfer for SFTP**

### Using IP whitelisting to secure your AWS Transfer for SFTP servers

© 2020 Amazon Web Services, Inc. and its affiliates. All rights reserved.
This sample code is made available under the MIT-0 license. See the LICENSE file.

Errors or corrections? Contact [russboye@amazon.com](mailto:russboye@amazon.com).

---

# Module 4
## Cleaning up after this workshop

In this module, you will clean up after completing this workshop. Cleaning up is critical, as components of this workshop fall outside of the free tier, and additional charges will accrue if you do not delete the resources created while completing the workshop.

## Module Steps

#### Cleaning Up

To clean up the resources you created as part of this post, you want to delete your **AWS SFTP** server. Additionally, you will need to clean up the **Security Group** that you manually created in **Module 1** of the workshop. Once the server and Security Group have been deleted, you can then proceed to delete the **AWS CloudFormation stack** that you deployed in Module 1. Taking these steps ensures you incur no additional costs from following along with this post.

## Module Summary

In this module, cleaned up after this workshop to ensure no additional charges are incurred.

In the next module, you will clean up the resources deployed in this workshop, to prevent incurring any additional charges.

### Workshop Summary

In this workshop, we showed you how to use **VPC Security Groups** to whitelist access to your **AWS SFTP** servers. First we deployed an **AWS CloudFormation template** to configure the needed network elements to configure the sample architecture. Next, we created a new **AWS SFTP server** with an endpoint hosted inside a **VPC**. Then, we demonstrated how to use the **Security Group** associated with that VPC to whitelist access to your server endpoint only to specific IPs, and optionally to peered VPCs inside or outside your account.

Using these features, you can limit **AWS Transfer for SFTP** endpoint access to the IPs of your trusted customers and business partners. This adds an additional layer of security, and in addition to the authentication mechanisms supported by **AWS SFTP**, prevents unknown or untrusted entities from even reaching the endpoint. Additionally, a major benefit to hosting the endpoint with two Elastic IPs is that it gives your customers the ability to filter SFTP outbound when their firewalls don’t support URL-based filtering. These benefits can be helpful when working with tightly regulated data such as financial records or Personal Health Information (PHI).

To learn more about **AWS Transfer for SFTP**, check out the following links:

*	[AWS Transfer for SFTP product page](https://aws.amazon.com/sftp/)
*	[AWS Transfer for SFTP documentation](https://docs.aws.amazon.com/transfer/latest/userguide/what-is-aws-transfer-for-sftp.html)

Go to [Workshop Home](/README.md).
