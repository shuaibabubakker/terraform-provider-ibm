---
subcategory: 'Event Notifications'
layout: 'ibm'
page_title: 'IBM : ibm_en_smtp_users'
description: |-
  List all the SMTP Users
---

# ibm_en_smtp_users

Provides a read-only data source for SMTP Users. You can then reference the fields of the data source in other resources within the same configuration using interpolation syntax.

## Example usage

```terraform
data "ibm_en_smtp_users" "smtp_config_users" {
  instance_guid = ibm_resource_instance.en_terraform_test_resource.guid
}
```

## Argument reference

Review the argument reference that you can specify for your data source.

- `instance_guid` - (Required, Forces new resource, String) Unique identifier for IBM Cloud Event Notifications instance.

- `search_key` - (Optional, String) Filter the SMTP Configuration by name.

- `smtp_id` - (Required, String) SMTP confg Id.

## Attribute reference

In addition to all argument references listed, you can access the following attribute references after your data source is created.

- `id` - The unique identifier of the `smtp_config_users`.

- `smtp_users` - (List) List of users.

  - `id` - (String) Autogenerated SMTP User ID.

  - `username` - (String) SMTP user name.

  - `description` - (String) SMTP User description.

  - `domain` - (String) Domain Name.

  - `smtp_config_id` - (String) SMTP confg Id.

  - `created_at` - (Stringr) Created time.

  - `updated_at` - (Stringr) Updated time.

- `total_count` - (Integer) Total number of SMTP Users.
