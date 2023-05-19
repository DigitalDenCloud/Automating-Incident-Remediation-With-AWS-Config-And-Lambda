<br />

![Architecture Diagram](Architecture.png)
  <h1 align="center">Automating Incident Remediation with AWS Config and Lambda</h1>
  <p align="center">
    <br />
    Configure a solution to automatically remediate an incident where a security group's inbound rules no longer conforms with the desired configuration
  </p>
</p>

### More Information
------------------
- [Blog](https://blog.digitalden.cloud/automating-incident-remediation-with-aws-config-and-lambda-9efc077b72e9)
- [Lab](https://youtu.be/VgxpkKJrWpY)

### Project date
------------------
16.05-2023

### Tech Stack
------------------
- AWS Identity and Access Management (IAM)
- AWS Config
- AWS Lambda
- AWS CloudWatch

### Project Description
-----------------
1. Utilized AWS Config: Configured AWS Config to monitor changes to specific resources in my AWS account, specifically the EC2 security group settings. AWS Config tracks changes and maintains a configuration history for the resources.

2. Defined Desired Configuration: Defined the desired configuration for the EC2 security groups, specifying which inbound ports should be open and which should not. This configuration represents the desired state of the security groups.

3. Security Concern Identification: AWS Config continuously monitors the EC2 security group settings and detects any changes that deviate from the desired configuration. It flags these changes as potential security concerns.

4. AWS Lambda Integration: To automate the remediation process, I integrated AWS Config with AWS Lambda. AWS Lambda allows you to execute custom code in response to specific events. In this case, I created Lambda functions to handle security incidents triggered by AWS Config.

5. Remediation Actions: When AWS Config detects a security incident, such as someone modifying a security group's inbound rules, it triggers the associated Lambda function. The Lambda function then takes remediation actions to bring the security group back into compliance with the desired configuration. For example, it could revoke unauthorized access or revert to the previously approved configuration.

### Objectives
-----------------
- [x] Create IAM roles to grant AWS services access to other AWS services.
- [x] Enable AWS Config to monitor resources in my AWS account.
- [x] Create a Lambda function and import function code.
- [x] Create and enable a custom AWS Config rule that uses my Lambda function.
- [x] Test the behaviour of an AWS Config rule to ensure it works as intended.
- [x] Analyse Amazon CloudWatch logs to audit when AWS Config rules are invoked.
