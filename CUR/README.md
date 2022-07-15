# Cost and usage report (CUR)

The template [cost-and-usage-report.yml](./cost-and-usage-report.yml) will create an S3 bucket, a CUR and also an athena environment that you are able to query your CUR using SQL.

IMPORTANT: You must run this template at the master payer account (aka manageman account or also called payer account) in the us-east-1 region because only in this region the CUR can be created. And than you have to wait 24 hours

 I have taken the CloudFromation template which will be [provided](https://docs.aws.amazon.com/cur/latest/userguide/use-athena-cf.html)  by AWS and modified it a bit. The benefit is that you just have to run one stack and all will be in place. CUR, S3 and Athena including Glue.