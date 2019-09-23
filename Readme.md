### This repo is to provide an example CloudFormation template that can be provided to AWS Customers that want to allow Read-Only Access or Full Access to the Well-Architected Tool (WAT) within their account to an external AWS account using an IAM cross-account role.

### Instructions:
Provide the [included CloudFormation template](./Cfn-template-WAR-ReadOnly-Cross-Account.template) to the party that wants to provide external access to the Well-Architected Tool in their account.

The following parameters are needed:
* **AccountName** [String]: Friendly name of the external AWS account that will be given access to the Well-Architected Tool.
* **ExternalAccountID** [Number]: 12-digit external AWS account ID that will be given access to the Well-Architected Tool.
* **WellArchitectedAccessLevel** [Pull-Down Option]: Permissions the IAM Role allows to the WAT.  Available options are ReadOnly, FullAccess.  The template utilizes these two AWS Managed Policies for the Well-Architected Tool service.

Once the CloudFormation Stack is complete, one of the Stack output fields is a URL the external party can use to federate via switch-roles into the account the template is deployed in with the specified level of access to the AWS Well-Architected Tool.

Reference:
* https://docs.aws.amazon.com/wellarchitected/latest/userguide/auth-and-access-control.html
* https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_cross-account-with-roles.html
