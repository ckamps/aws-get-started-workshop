# Automated Static Web Deployments

This document describes how you can automatically deploy static website content via AWS CodePipeline and AWS CodeBuild.

## 1. Ensure CloudFront and S3 are configured

See the [Automated Environment Build](../environment-build/README.md) for details on building our your static web hosting environment.

## 2. Create a CodePipeline pipeline 

In this one you will probably want to change the first 5 parameters.  ProjectName should match whatever you put for WorkshopHostname in the cloudfront-s3-website.yaml. Set the `CloudFrontDistroId` to the distribution ID generated from the first stack.

> Stack completes in about 1-2 minutes  
```
### DO NOT FORGET TO CHANGE THE STACK NAME
aws cloudformation create-stack --stack-name MY-Website-Pipeline --template-body file://pipeline.yaml --capabilities CAPABILITY_NAMED_IAM
```

If you check the Build Pipeline and Build logs you should see files successfully copied to your S3 bucket.  

## 3. Test

### Test simple commit and merge workflow

### Test pull request (PR) workflow

### Test feature branch workflow