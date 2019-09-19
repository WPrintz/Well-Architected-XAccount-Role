This repo is to provide an example CloudFormation template that can be provided to AWS Customers that want to allow Read-Only Access or Full Access to the Well-Architected Tool (WAT) within their account to an external AWS account.

The following parameters are needed:
* AccountName = Friendly name of the external AWS account that will be given access to the Well-Architected Tool.
* ExternalAccountID = 12-digit external AWS account ID that will be given access to the Well-Architected Tool.
* WellArchitectedAccessLevel = Access Level to the WAT.  Available options are ReadOnly, FullAccess.
