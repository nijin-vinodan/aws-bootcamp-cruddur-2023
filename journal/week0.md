# Week 0 — Billing and Architecture

# Meeting Notes
1. Walked through user personas on what we are trying to build.
2. Information about Well Architected Framework, TOGAF Framework, 4C 

# Architecture
1. Use Lucid Chart with aws icons to create the architecture diagram
2. Create a conceptual diagram (napkin design) > Logical diagram > Physical diagram (Actual aws components)

# Main Notes
1. We can use AWS services from their site and we can also use aws-cli to do it programmatically. 

# Create IAM Users
1. By default when we create an AWS account, we get a root user.
2. Using root account, we can create and provide access to many users using IAM (Identity Access Management)
3. When create IAM users, we add them to a group with policies(Group has list of permissible services which those users can have access to)
    i. For eg. In a project, you want only certain set of users who can have access to DynamoDB, whereas others can have access to Amplify
4. We can set up an alias for our AWS Account ID
5. Set up MFA.
6. For an user, generate access keys to download **Access key ID** and **Secret access key**

# Set Up Budgets in AWS
1. Search for Budgets in Global Search.
2. It is important to set up budgets.
3. For a free tier, we can have only 2 free budgets. 

# Accessing AWS through CLI

## Inbuilt aws-cli
By default, within aws site, there is a cli. We can use it to directly interact.
Note : 
1. The console icon is present in the header.
2. Some regions don't have inbuilt aws-cli.

## Local System
Alternatively, we can install aws-cli in our Terminal/VS Code in our machine. 

Follow the commands here to install aws-cli in MAC.
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

After installing, configure aws in the terminal using the following command
``` 
> aws configure

```
Provide Access Key ID, Secret Access key.

To verify you have logged in, try the following command
```aws sts get-caller-identity```

It will output the following details. Verify whether it corresponds to your aws details
```
{
    "UserId": "MMMMMMMMMMMMMMMMMMMM",
    "Account": "NNNNNNNNNNNNN",
    "Arn": "arn:aws:iam::MMMMMMMMMMMM:user/MMMMM"
}
```

To view any CLI comments, refer the aws-cli comman

