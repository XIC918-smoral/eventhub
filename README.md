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
| eventhub_name | Specifies the name of the EventHub resource | `string` |  | Yes |
| namespace_name | Specifies the name of the EventHub Namespace | `string` |  | Yes |
| resource_group_name | The name of the resource group in which the EventHub's parent Namespace exists | `string` |  | Yes |
| partition_count | Specifies the current number of shards on the Event Hub | `number` |  | Yes |
| message_retention | Specifies the number of days to retain the events for this Event Hub. | `number` |  | Yes |
| sku | Defines which tier to use. Valid options are Basic, Standard, and Premium. Please not that setting this field to Premium will force the creation of a new resource and also requires setting zone_redundant to true | `string` |  | yes |
| capacity | Specifies the Capacity / Throughput Units for a Standard SKU namespace. Default capacity has a maximum of 2, but can be increased in blocks of 2 on a committed purchase basis | `number` | 2 | No |
| auto_inflate_enabled  | Is Auto Inflate enabled for the EventHub Namespace? | `bool` |  false | No |
| dedicated_cluster_id | Specifies the ID of the EventHub Dedicated Cluster where this Namespace should created | `string` | null | No |
| maximum_throughput_units |  Specifies the maximum number of throughput units when Auto Inflate is Enabled. Valid values range from 1 - 20 | `number` | null | No |
| vnet_name | The name of the virtual network | `string` |  | Yes |
| subnet_name | The variable for subnet name | `string` |  | Yes |
| enable_private_endpoint | Specifies the name of the EventHub resource | `string` |  | Yes |
| zone_redundant | Specifies if the EventHub Namespace should be Zone Redundant (created across Availability Zones) | `bool` | false | No |
| partition_count | Specifies the current number of shards on the Event Hub | `number` |  | Yes |
| message_retention | Specifies the number of days to retain the events for this Event Hub. | `number` |  | Yes |
| status | Specifies the status of the Event Hub resource. Possible values are Active, Disabled and SendDisabled. Defaults to Active | `string` | Active | No |
| tag_map | Map of Tags those we want to Add | `map(string)` |  | Yes |
| authorization_rule_name | Specifies the name of the EventHub Authorization Rule resource | `string` |  | Yes |
| listen | Does this Authorization Rule have permissions to Listen to the Event Hub? | `bool` | false | No |
| send | Does this Authorization Rule have permissions to Send to the Event Hub? | `bool` | false | No |
| manage | Does this Authorization Rule have permissions to Manage to the Event Hub? When this property is true - both listen and send must be too | `bool` | false | No |
| namespace_authorization_rule_name | Specifies the name of the Authorization Rule | `string` |  | yes |
| listen_namespace_authorization_rule | Does this Authorization Rule have permissions to Listen to the Event Hub? | `bool` | false | No |
| send_namespace_authorization_rule | Does this Authorization Rule have permissions to Send to the Event Hub?" | `bool` | false | No |
| manage_namespace_authorization_rule | Does this Authorization Rule have permissions to Manage to the Event Hub? When this property is true - both listen and send must be too | `bool` | false | No |
| consumer_group_name | Specifies the name of the EventHub Consumer Group resource | `string` |  | yes |
| user_metadata | Specifies the user metadata. | `string` | null | No |
