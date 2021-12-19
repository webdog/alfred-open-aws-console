# Alfred Open AWS Console in Browser

Opens up a subset of AWS Consoles in the browser based on the argument you pass. It then makes an opinion to where you want to be in that service dashboard.

For example, in CloudWatch, I am primary concerned with Log Groups, but the default URL for CloudWatch will drop into a dashboard, forcing another click. `ac cloudwatch` with Alfred instead navigates immediately to https://console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups

![gif-of-workflow-action](https://user-images.githubusercontent.com/960210/146687892-b6dd091c-81c6-42e0-99a8-fd4766d953a1.gif)

Note: Make sure you have a config file for AWS located in $HOME/.aws/config. I pull your default region from here, albeit not very intelligently, so YMMV.


Currently configured URLs (Note: As mentioned, the region parameter in the URL is sourced from the local aws config file located in your `$HOME/.aws/config` directory`)


| Service   |  URL  |
|---        |---    |
| EKS       |  https://console.aws.amazon.com/eks/home?region=us-east-1#/clusters     |   
| S3  |  https://console.aws.amazon.com/s3/home?region=us-east-1# |   
| VPC  | https://console.aws.amazon.com/vpc/home?region=us-east-1#vpcs:   |   
| EC2 | https://console.aws.amazon.com/ec2/home?region=us-east-1#Instances:instanceState=running |
| CloudTrail | https://console.aws.amazon.com/cloudtrail/home?region=us-east-1#/events?ReadOnly=false |
| CloudWatch | https://console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups |
| IAM | https://console.aws.amazon.com/iamv2/home#/roles |
