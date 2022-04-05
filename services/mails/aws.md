To answer if AWS products or services are impacted, this is the official customer messaging from AWS at the moment:



“AWS is aware of the recently disclosed issue related to the open source Spring framework (CVE-2022-22965). AWS services do not deploy Java applications in a manner matching the known vulnerable pattern, and we have not identified any AWS-managed environments which provide Spring for AWS customers to use or upgrade.



Customers who use Spring to build their own Java applications intended for deployment to AWS-managed environments, such as Beanstalk and Lambda, are advised to update any development environments to the latest version per vendor guidance [1], as well as rebuild and redeploy any affected applications as needed.



There are no other customer actions required. Any additional required actions or necessary information for customers regarding this concern will be announced via security bulletin.



[1] https://tanzu.vmware.com/security/cve-2022-22965”