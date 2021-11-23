---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "spacelift_webhook Data Source - terraform-provider-spacelift"
subcategory: ""
description: |-
  spacelift_webhook represents a webhook endpoint to which Spacelift sends the POST request about run state changes.
---

# spacelift_webhook (Data Source)

`spacelift_webhook` represents a webhook endpoint to which Spacelift sends the POST request about run state changes.

## Example Usage

```terraform
data "spacelift_webhook" "webhook" {
  webhook_id = spacelift_webhook.webhook.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **webhook_id** (String) ID of the webhook

### Optional

- **id** (String) The ID of this resource.
- **module_id** (String) ID of the stack which triggers the webhooks
- **stack_id** (String) ID of the stack which triggers the webhooks

### Read-Only

- **enabled** (Boolean) enables or disables sending webhooks
- **endpoint** (String) endpoint to send the POST request to
- **secret** (String) secret used to sign each POST request so you're able to verify that the request comes from us

