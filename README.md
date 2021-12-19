# Alfred Open AWS Console in Browser

Opens up a subset of AWS Consoles in the browser based on the argument you pass. It then makes an opinion to where you want to be in that service dashboard.

For example, in CloudWatch, I am primary concerned with Log Groups, but the default URL for CloudWatch will drop into a dashboard, forcing another click. `ac cloudwatch` with Alfred instead navigates immediately to https://console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups

![gif-of-workflow-action](https://user-images.githubusercontent.com/960210/146687892-b6dd091c-81c6-42e0-99a8-fd4766d953a1.gif)

Note: Make sure you have a config file for AWS located in $HOME/.aws/config. I pull your default region from here, albeit not very intelligently, so YMMV.


Currently configured URLs (Note: As mentioned, the region parameter in the URL is sourced from the local aws config file located in your `$HOME/.aws/config` directory`)


| Service   |  URL  | Description |
|---        |---    |---          |
| EKS       |  https://console.aws.amazon.com/eks/home?region=us-east-1#/clusters     | Opens up to your EKS Clusters view   |
| S3  |  https://console.aws.amazon.com/s3/home?region=us-east-1# |  Opens up to the general S3 Dashboard |
| VPC  | https://console.aws.amazon.com/vpc/home?region=us-east-1#vpcs:   |   Opens up to the list of VPCs in the region |
| EC2 | https://console.aws.amazon.com/ec2/home?region=us-east-1#Instances:instanceState=running | Opens up to the EC2 dashboard, showing running instances |
| CloudTrail | https://console.aws.amazon.com/cloudtrail/home?region=us-east-1#/events?ReadOnly=false | Opens up to the CloudTrail `events` page, instead of the dashboard |
| CloudWatch | https://console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups | Opens up CloudWatch Log Groups, instead of the general CloudWatch dashboard |
| IAM | https://console.aws.amazon.com/iamv2/home#/roles | Opens up to the IAM Roles, instead of the general IAM dashboard |
