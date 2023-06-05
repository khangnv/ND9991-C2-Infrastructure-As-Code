# References:

1. https://lucid.app/lucidchart/4c8af6b6-9c11-48e6-bc51-5f5988b89428/edit?invitationId=inv_92cad6d0-cbf7-4671-8a83-522fbd31c8de&page=0_0#

2. https://github.com/1Jayso/nd9991-c2-Infrastructure-as-Code-v1/tree/master/project_starter

3. https://github.com/Mike-Muasya/Infrastructure-as-Code/tree/master/project-IaC

4. https://github.com/abderrahimsoumer/nd9991-c2-Infrastructure-as-Code-v1/tree/master/udagram_project

# AWS config

`aws --version`
`aws configure`
`aws s3 ls`
`aws iam list-users`

## CloudFormation Stack

1. Create a templace file
2. Create stack
   `aws cloudformation create-stack --stack-name $1 --template-body file://$2  --parameters file://$3`
   `./create.sh MyFirstStack network.yml network-parameters.json`
3. Update stack
   `aws cloudformation update-stack --stack-name %1 --template-body file://%2  --parameters file://%3`
   `./update.sh MyFirstStack servers.yml server-parameters.json`
4. Describe stack
   `aws cloudformation describe-stacks --stack-name MyFirstStack`
5. Delete stack
   `aws cloudformation delete-stack --stack-name MyFirstStack`
