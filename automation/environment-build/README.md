# Automated Environment Build

This document describes how you can automatically build the static web site environment via Amazon CloudFront and Amazon S3.

## Edit and deploy the CloudFront site in cloudfront-s3-website.yml 

You should only need to change the parameter for WorkshopHostname.  Once that is complete run a command similar to the following but change the stackname

> Stack takes about 20 minutes
```
### DO NOT FORGET TO CHANGE THE STACK NAME
aws cloudformation create-stack --stack-name MY-Workshop --template-body file://cloudfront-s3-website.yaml
```