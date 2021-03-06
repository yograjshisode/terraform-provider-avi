---
layout: "avi"
page_title: "Avi: avi_alertsyslogconfig"
sidebar_current: "docs-avi-resource-alertsyslogconfig"
description: |-
  Creates and manages Avi AlertSyslogConfig.
---

# avi_alertsyslogconfig

The AlertSyslogConfig resource allows the creation and management of Avi AlertSyslogConfig

## Example Usage

```hcl
resource "avi_alertsyslogconfig" "foo" {
    name = "terraform-example-foo"
    tenant_ref = "/api/tenant/?name=admin"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) A user-friendly name of the syslog notification.
* `description` - (Optional) User defined description for alert syslog config.
* `syslog_servers` - (Optional) The list of syslog servers.
* `tenant_ref` - (Optional) It is a reference to an object of type tenant.


### Timeouts

The `timeouts` block allows you to specify [timeouts](https://www.terraform.io/docs/configuration/resources.html#timeouts) for certain actions:

* `create` - (Defaults to 40 mins) Used when creating the AMI
* `update` - (Defaults to 40 mins) Used when updating the AMI
* `delete` - (Defaults to 90 mins) Used when deregistering the AMI

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `uuid` -  Unique object identifier of the object.

