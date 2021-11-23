---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "spacelift_current_stack Data Source - terraform-provider-spacelift"
subcategory: ""
description: |-
  spacelift_current_stack is a data source that provides information about the current administrative stack if the run is executed within Spacelift by a stack or module. This allows clever tricks like attaching contexts or policies to the stack that manages them.
---

# spacelift_current_stack (Data Source)

`spacelift_current_stack` is a data source that provides information about the current administrative stack if the run is executed within Spacelift by a stack or module. This allows clever tricks like attaching contexts or policies to the stack that manages them.

## Example Usage

```terraform
data "spacelift_current_stack" "this" {}

resource "spacelift_environment_variable" "core-kubeconfig" {
  stack_id = data.spacelift_current_stack.this.id
  name     = "CHUNKY"
  value    = "bacon"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- **id** (String) The ID of this resource.

