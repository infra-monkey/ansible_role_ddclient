# Overview
This role does description.
This role requires root permissions. It must be called as root. This needs to be managed at the ansible or playbook level.

# Variables

| Name  | Type | Required | Description |
| ----- | ---- | -------- | ----------- |
| ddclient_provider | string | yes | Name of the provider to use as described [here](https://ddclient.net/protocols.html). Use `custom` to provide settings manually |
| ddclient_login | string | yes | Your login to the dynamic dns service provider |
| ddclient_password | string | yes | Your password to the dynamic dns service provider |
| ddclient_domains | list(string) | yes | Domains or records to update with your dns service provider |
| ddclient_config | hash | no (requires `ddclient_provider: custom`) | Your custom configuration for the dynamic dns service provider |
| ddclient_config.protocol | string | no | Name of the protocol to use as described [here](https://ddclient.net/protocols.html). |
| ddclient_config.use_ssl | boolean | no (requires `ddclient >= 3.7`) | Set `ssl=yes` in the configuration for the dynamic dns service provider |
| ddclient_config.use_web | boolean | no | Set `use=web` in the configuration for the dynamic dns service provider |
| ddclient_config.web_url | string | no (requires `ddclient_config.use_web: true`) | Set the `web` parameter in the configuration for the dynamic dns service provider |
| ddclient_config.server | string | no | Set the `server` parameter in the configuration for the dynamic dns service provider |
| ddclient_config.zone | string | no | Set the `zone` parameter in the configuration for the dynamic dns service provider |

# Automatique Testing

This role is tested using Molecule against:
- Debian 11/12
