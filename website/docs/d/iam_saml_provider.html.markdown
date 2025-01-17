---
subcategory: "IAM"
layout: "aws"
page_title: "AWS: aws_saml_provider"
description: |-
  Get information on an IAM SAML provider.
---

# Data Source: aws_saml_provider

This data source can be used to fetch information about a specific
IAM SAML provider. This will allow you to easily retrieve the metadata
document of an existing SAML provider.

## Example Usage

```hcl
data "aws_iam_saml_provider" "example" {
  arn = "arn:aws:iam::123456789:saml-provider/myprovider"
}
```

## Argument Reference

* `arn` - (Required) The ARN assigned by AWS for the provider.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `create_date` - Creation date of the SAML provider in RFC1123 format, e.g. `Mon, 02 Jan 2006 15:04:05 MST`.
* `name` - The name of the provider.
* `saml_metadata_document` - The XML document generated by an identity provider that supports SAML 2.0.
* `tags` - The tags attached to the SAML provider.
* `valid_until` - The expiration date and time for the SAML provider in RFC1123 format, e.g. `Mon, 02 Jan 2007 15:04:05 MST`.
