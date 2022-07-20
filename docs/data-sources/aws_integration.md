---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "spacelift_aws_integration Data Source - terraform-provider-spacelift"
subcategory: ""
description: |-
  spacelift_aws_integration represents an integration with an AWS account. This integration is account-level and needs to be explicitly attached to individual stacks in order to take effect.
  Note: when assuming credentials for shared workers, Spacelift will use $accountName-$integrationID@$stackID-suffix or $accountName-$integrationID@$moduleID-$suffix as external ID https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html and $runID@$stackID@$accountName truncated to 64 characters as session ID https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole,$suffix will be read or write.
---

# spacelift_aws_integration (Data Source)

`spacelift_aws_integration` represents an integration with an AWS account. This integration is account-level and needs to be explicitly attached to individual stacks in order to take effect.

Note: when assuming credentials for **shared workers**, Spacelift will use `$accountName-$integrationID@$stackID-suffix` or `$accountName-$integrationID@$moduleID-$suffix` as [external ID](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html) and `$runID@$stackID@$accountName` truncated to 64 characters as [session ID](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole),$suffix will be `read` or `write`.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `integration_id` (String) immutable ID of the integration

### Read-Only

- `duration_seconds` (Number) Duration in seconds for which the assumed role credentials should be valid
- `external_id` (String) Custom external ID (works only for private workers).
- `generate_credentials_in_worker` (Boolean) Generate AWS credentials in the private worker
- `id` (String) The ID of this resource.
- `labels` (Set of String)
- `name` (String) Name of the AWS integration
- `role_arn` (String) ARN of the AWS IAM role to attach
- `space_id` (String) ID (slug) of the space the integration is in

