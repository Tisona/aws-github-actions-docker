# GitHub runners AWS Cloudformation template

AWS CloudFormation template that deploys a GitHub self hosted runners in Docker. This setup allows for running multiple instances of GitHub runners on a single EC2 instance.

## Features

* Auto-update runners
* Auto-register runners at startup
* Deregister runners at shutdown
* No Kubernetes needed

## VPC

Template integrated with [widdix](https://github.com/widdix/aws-cf-templates/tree/master/vpc) Cloudformation templates. You will need to create VPC first and pass VPC stack name in the parameters.

## SSM login

GitHub runner instance does not use ssh keys for incoming connections. Run `ssm start-session` instead.

## Security

This stack should be deployed in its own environment. Consider using AWS landing zone and separated AWS account for GitHub runners.