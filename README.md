# Pocket ID Terraform Provider

Manage the users, groups, OIDC clients and settings of your [Pocket ID](https://github.com/pocket-id/pocket-id) instance as code with Terraform or OpenTofu.

## Setup

You need Terraform 1.5 or later, or OpenTofu 1.6 or later, and an API key of your Pocket ID instance.

```hcl
terraform {
  required_providers {
    pocketid = {
      source  = "pocket-id/pocketid"
      version = "~> 2.6"
    }
  }
}

provider "pocketid" {
  base_url  = "https://id.example.com"
  api_token = var.pocketid_api_token
}
```

The provider also reads `POCKETID_BASE_URL` and `POCKETID_API_TOKEN` from the environment.

### Moving from `trozz/pocketid`

The provider was previously published as `trozz/pocketid`. Change the `source` in `required_providers` to `pocket-id/pocketid` and replace the provider in your state:

```sh
terraform state replace-provider trozz/pocketid pocket-id/pocketid
```

## Quick start

### Create an OIDC client

```hcl
resource "pocketid_client" "web_app" {
  name = "My Web Application"
  callback_urls = [
    "https://app.example.com/callback",
    "http://localhost:3000/callback"
  ]
  is_public    = false
  pkce_enabled = true
}

output "client_id" {
  value = pocketid_client.web_app.id
}

output "client_secret" {
  value     = pocketid_client.web_app.client_secret
  sensitive = true
}
```

### Create groups and users

```hcl
resource "pocketid_group" "developers" {
  name          = "developers"
  friendly_name = "Development Team"
}

resource "pocketid_user" "john_doe" {
  username   = "johndoe"
  email      = "john@example.com"
  first_name = "John"
  last_name  = "Doe"
  groups     = [pocketid_group.developers.id]
}
```

Users sign in with passkeys, so they register one themselves in Pocket ID, for example with a `pocketid_one_time_access_token`.

## Resources and data sources

| Resources | Data sources |
| --- | --- |
| `pocketid_application_config` | `pocketid_application_config` |
| `pocketid_client` | `pocketid_client`, `pocketid_clients` |
| `pocketid_group` | `pocketid_group`, `pocketid_groups` |
| `pocketid_ldap_sync` | |
| `pocketid_one_time_access_token` | |
| `pocketid_scim_service_provider` | |
| `pocketid_user` | `pocketid_user`, `pocketid_users` |

Visit the [documentation](https://registry.terraform.io/providers/pocket-id/pocketid/latest/docs) for all their arguments.

## Examples

- [Basic client](examples/basic-client): the minimal configuration for an OIDC client
- [Single-page application with PKCE](examples/spa-with-pkce): a public client for a browser app
- [User and group management](examples/user-management): users, groups and their memberships
- [Complete](examples/complete): clients, groups and users together with the data sources that read them
- [Resources](examples/resources) and [data sources](examples/data-sources): an example for each, also shown in the documentation

## Contribute

You're very welcome to contribute to Pocket ID! Please follow the [contribution guide](https://github.com/pocket-id/.github/blob/main/CONTRIBUTING.md) to get started. See [AGENTS.md](AGENTS.md) for how to build, test and lint the provider.
