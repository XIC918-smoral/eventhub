Azure Network Terraform module
=====================================

Terraform versions
------------------
Terraform 1.1.7

Usage
------
```hcl

provider "azurerm" {
  features {}
}

module "eventhub" {
  source                   = "https://Millennial-Mobile-App@dev.azure.com/Millennial-Mobile-App/Platform/_git/Platform"
  namespace_name           = "_"
  resource_group_location  = "_"
  resource_group_name      = "_"
  sku                      = "_"
  capacity                 = "_"
  auto_inflate_enabled     = "_"
  dedicated_cluster_id     = "_"
  maximum_throughput_units = "_"
  zone_redundant           = "_"
  vnet_name                = "_"
  subnet_name              = "_"
  existing_subnet_id       = "_"
  enable_private_endpoint  = "_"


  eventhub_name     = "_"
  partition_count   = "_"
  message_retention = "_"
  status            = "_"

  tag_map = "_"

  authorization_rule_name = "_"
  listen                  = "_"
  send                    = "_"
  manage                  = "_"

  namespace_authorization_rule_name   = "_"
  listen_namespace_authorization_rule = "_"
  send_namespace_authorization_rule   = "_"
  manage_namespace_authorization_rule = "_"


  consumer_group_name = "_"
  user_metadata       = "_"
}

```

Tags
----
* Tags are assigned to resources with name variable as prefix.
* Additial tags can be assigned by tags variables as defined above.

Resources
------
| Name | Type |
|------|------|
| [azurerm_resource_group](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/resource_group) | resource |
| [azurerm_eventhub](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/eventhub) | resource |



Inputs
------
| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| name | Specifies the name of the EventHub resource | `string` |  | Yes |
| namespace_name | Specifies the name of the EventHub Namespace | `string` |  | Yes |
| resource_group_name | The name of the resource group in which the EventHub's parent Namespace exists | `string` |  | Yes |
| partition_count | Specifies the current number of shards on the Event Hub | `number` |  | Yes |
| message_retention | Specifies the number of days to retain the events for this Event Hub. | `number` |  | Yes |
| capture_description | A capture_description block | `string` |  | No |
| status | Specifies the status of the Event Hub resource | `string` | Active | No |
| interval_in_seconds  | Specifies the time interval in seconds at which the capture will happen. Values can be between 60 and 900 seconds | `number` |  300 | No |
| size_limit_in_bytes | Specifies the amount of data built up in your EventHub before a Capture Operation occurs. Value should be between 10485760 and 524288000 bytes | `number` | 314572800 | No |
| skip_empty_archives | Specifies if empty files should not be emitted if no events occur during the Capture time window | `bool` | false | No |
| vnet_name | The name of the virtual network | `string` |  | Yes |
| subnet_name | The name of the virtual network | `string` |  | Yes |
| name | Specifies the name of the EventHub resource | `string` |  | Yes |
| name | Specifies the name of the EventHub resource | `string` |  | Yes |
