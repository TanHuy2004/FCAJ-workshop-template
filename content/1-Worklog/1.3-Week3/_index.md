---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it directly** into your report, including this warning.
{{% /notice %}}

### Week 3 Objectives:

* Understand and implement a Hybrid Cloud networking model on AWS.
* Configure Amazon Web Services Transit Gateway to connect multiple VPCs.
* Set up Hybrid DNS using Amazon Web Services Route 53 Resolver for domain name resolution between AWS and on-premises environments.

### Tasks implemented during this week:

| Day | Tasks | Start Date | Completion Date | References |
| --- | --- | --- | --- | --- |
| 2 | - Learn the concepts and functions of Transit Gateway. <br> - Create VPCs for network connection. | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 3 | - Create Transit Gateway. <br> - Configure ASN and DNS support. <br> - Create Transit Gateway Attachments to connect VPCs. <br> - Create Transit Gateway Route Tables. | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 4 | - Configure route tables for each subnet. <br> - Add routes from VPCs to Transit Gateway. <br> - Test connectivity between VPCs using ping. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 5 | - Initialize infrastructure using CloudFormation Templates. <br> - Configure Security Groups for DNS, RDP, and SSH. <br> - Create Route 53 Outbound Endpoint and Resolver Rules. | 07/05/2026 | 07/05/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 6 | - Create Route 53 Inbound Endpoints. <br> - Verify routing and DNS operations. <br> - Clean up resources to avoid unnecessary costs: <br>&emsp; + Delete Resolver Rules <br>&emsp; + Delete Endpoints <br>&emsp; + Delete Transit Gateway Attachments <br>&emsp; + Delete Transit Gateway and Route Tables. | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |

### Week 3 Results:

* Successfully deployed Amazon Web Services Transit Gateway to connect multiple VPCs within the network system.

* Configured routing between VPCs through Transit Gateway and successfully tested connectivity using ping.

* Initialized infrastructure using CloudFormation Templates for the Hybrid DNS model.

* Successfully configured Hybrid DNS using Amazon Web Services Route 53 Resolver.

* Created and configured:
  * Route 53 Outbound Endpoint
  * Route 53 Inbound Endpoint
  * Resolver Rules

* Cleaned up resources after completing the lab to avoid unnecessary charges.