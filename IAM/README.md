# below is the command to run the cloudformation template
# parameters to change MyIAMUser and ParameterValue

aws cloudformation create-stack --stack-name IAMUserStack --template-body iam.yml \
--parameters ParameterKey=IAMUserName,ParameterValue=Test ParameterKey=IAMUserPassword,ParameterValue=MySecurePass123 \
--capabilities CAPABILITY_NAMED_IAM

# below is the command to delete cloudformation template
aws cloudformation delete-stack --stack-name IAMUserStack
