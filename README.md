# Resource for SSM Automation


## Step 1 - Create Automation Role

Within the ./cloudformation directory there is the AutomationServiceRole.yml which serves as starter template for creating your SSM Automation Service Role. You will need to add additional IAM permissions for any additional service your automation will interact with. From there you will need to give your user (role used to login and set the SSM automation) access to pass the SSM Automation role you are creationg.


> **Note:** If you run an automation workflow that invokes other services by using an AWS Identity and Access Management (IAM) service role, be aware that the service role must be configured with permission to invoke those services. This requirement applies to all AWS Automation documents (AWS-* documents) such as the AWS-ConfigureS3BucketLogging, AWS-CreateDynamoDBBackup, and AWS-RestartEC2Instance documents, to name a few. This requirement also applies to any custom Automation documents you create that invoke other AWS services by using actions that call other services. For example, if you use the aws:executeAwsApi, aws:createStack, or aws:copyImage actions, then you must configure the service role with permission to invoke those services. You can enable permissions to other AWS services by adding an IAM inline policy to the role.
