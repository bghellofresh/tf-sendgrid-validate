# Sendgrid Validate

This module creates a valid sendgrid setup for a given domain, id and domainkey.

## Usage

```
module "sendgrid" {
  source             = "./modules/sendgrid"
  domain             = "domain-without-http"
  zone_id            = "zoneid"
  sendgrid_domainkey = "xxxxxxx"
  sendgrid_id        = "0000000"
}
```

*NOTE* after validation completes you have to run `terraform destroy` for this configuration to remove the setup. There is a companion module called `tf-sendgrid` that provides a production ready setup of sendgrid.

# Creates

This creates 15 records in AWS Route 53 according to the sendgrid spec.
