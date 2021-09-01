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

## References

https://aws.amazon.com/pt/devops/

https://web.devopstopologies.com/

https://bookshelf.vitalsource.com/#/

https://aws.amazon.com/pt/blogs/aws/new-for-aws-cloudformation-quickly-retry-stack-operations-from-the-point-of-failure/

https://github.com/aws-cloudformation/awesome-cloudformation

https://aws.amazon.com/pt/blogs/mt/introducing-aws-cloudformation-guard-2-0/

