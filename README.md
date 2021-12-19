# Alfred Open AWS Console in Browser

Opens up a subset of AWS Consoles in the browser based on the argument you pass. It then makes an opinion to where you want to be in that service dashboard.

For example, in CloudWatch, I am primary concerned with Log Groups, but the default URL for CloudWatch will drop into a dashboard, forcing another click.

`ac cloudwatch` instead navigates immediately to https://console.aws.amazon.com/cloudwatch/home?region=us-east-1#logsV2:log-groups


Note: Make sure you have a config file for AWS located in $HOME/.aws/config. I pull your default region from here, albeit not very intelligently, so YMMV.
