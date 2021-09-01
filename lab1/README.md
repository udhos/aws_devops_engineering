
```
keyPair=$(aws ec2 describe-key-pairs --output text --query KeyPairs[*].KeyName)

# Create stack
aws cloudformation create-stack --stack-name AWSStudent-Lab1 \
	--parameters ParameterKey=KeyName,ParameterValue=$keyPair \
	ParameterKey=InstanceType,ParameterValue=t2.micro \
	--template-body file://simple-infrastructure.yaml

# Describe stack
aws cloudformation describe-stacks --stack-name AWSStudent-Lab1

# Detect drift
aws cloudformation describe-stack-resource-drifts --stack-name AWSStudent-Lab1 --stack-resource-drift-status-filters MODIFIED DELETED

# Create change set
aws cloudformation create-change-set --stack-name AWSStudent-Lab1 \
	--change-set-name Lab1ChangeSet \
	--parameters ParameterKey=InstanceType,ParameterValue=t2.micro \
	ParameterKey=KeyName,ParameterValue=$keyPair \
	--template-body file://simple-infrastructure-CS.yaml

# Describe change set
aws cloudformation describe-change-set --stack-name AWSStudent-Lab1 --change-set-name Lab1ChangeSet

# Execute change set
aws cloudformation execute-change-set --stack-name AWSStudent-Lab1 --change-set-name Lab1ChangeSet

# If execution of change set fails:
# 1. Fix template
# 2. Delete change set
# 3. Create new change set
# 4. Execute new change set

```

