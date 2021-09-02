# aws_devops_engineering

## CLI

### CLI Skeleton

Export cli template.

	aws dynamodb create-table --generate-cli-skeleton > template.json

Run cli template.

	aws dynamodb create-table --cli-input-json file://template.json
	
### CLI Auto Prompt

Navigate thru command tree.

	aws --cli-auto-prompt

### CLI Wizard

Interactive wizard.

    aws dynamodb wizard new-table

### CLI Wait

To wait until an instance is running.

    aws ec2 wait instance-running --instance-ids i-1234567890abcdef0

## CodeBuild

### CodeBuild local

https://docs.aws.amazon.com/codebuild/latest/userguide/use-codebuild-agent.html

## References

https://aws.amazon.com/pt/devops/

https://web.devopstopologies.com/

https://bookshelf.vitalsource.com/#/

https://aws.amazon.com/pt/blogs/aws/new-for-aws-cloudformation-quickly-retry-stack-operations-from-the-point-of-failure/

https://github.com/aws-cloudformation/awesome-cloudformation

https://aws.amazon.com/pt/blogs/mt/introducing-aws-cloudformation-guard-2-0/

https://github.com/awslabs/git-secrets

https://d1.awsstatic.com/whitepapers/microservices-on-aws.pdf

https://gallery.ecr.aws/

https://aws.amazon.com/pt/bottlerocket/


