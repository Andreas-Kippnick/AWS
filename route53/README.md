# Route53

## reusable delegation set

If you want to use the same group of AWS DNS-Servers for all of your domains you can use [CreateReusableDelegationSet](https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateReusableDelegationSet.html). But if you want to work with reusable delegation sets in cloudfromation you are faciung two problems:

- You can't create a reusable delegation set with cloudformation
- You can't assign a reusable delegation set using [AWS::Route53:HostedZone](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html)

The SOLUTION - Try to use my custom cloudformation ressources:


- [reusable-delegationset.yml](./reusable-delegationset.yml) will create a delegation set and return alos the DNS serves FQND, IPv4 and IPv6 adresses
- [custom-hostedzone-using-deligationset.yml](./custom-hostedzone-using-deligationset.yml) will use the delegation set id and create a Hosted Zone

This two CF-Templates helps also to implement white-lable name server see [more about white lable dns](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/white-label-name-servers.html)

