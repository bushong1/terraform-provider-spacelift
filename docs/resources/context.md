---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "spacelift_context Resource - terraform-provider-spacelift"
subcategory: ""
description: |-
  spacelift_context represents a Spacelift context - a collection of configuration elements (either environment variables or mounted files) that can be administratively attached to multiple stacks (spacelift_stack) or modules (spacelift_module) using a context attachment (spacelift_context_attachment)`
---

# spacelift_context (Resource)

`spacelift_context` represents a Spacelift **context** - a collection of configuration elements (either environment variables or mounted files) that can be administratively attached to multiple stacks (`spacelift_stack`) or modules (`spacelift_module`) using a context attachment (`spacelift_context_attachment`)`

## Example Usage

```terraform
resource "spacelift_context" "prod-k8s-ie" {
  description = "Configuration details for the compute cluster in 🇮🇪"
  name        = "Production cluster (Ireland)"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String) Name of the context - should be unique in one account

### Optional

- **description** (String) Free-form context description for users
- **id** (String) The ID of this resource.
- **labels** (Set of String)

