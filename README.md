# Ansible Collection - Extreme Networks Community - XIQ-SE

This collection provides Ansible modules and roles to manage ExtremeCloudIQ - Site Engine via GraphQL.

## Overview

This collection provides modules and roles to interact with ExtremeCloudIQ – Site Engine (XIQ‑SE) over GraphQL.

Included modules:
- `xiqse_query`: Execute arbitrary GraphQL queries
- `xiqse_mutation`: Execute GraphQL mutations
- `xiqse_version`: Retrieve XIQ‑SE server version
- `xiqse_site`: Manage sites in XIQ‑SE
- `device_version`: Retrieve device firmware via XIQ‑SE

## Getting started

### Prerequisites

- `Ansible` >= `2.15.0` (aligned with `meta/runtime.yml`)
- Python 3.x on the control node
- Python packages: `requests`, `urllib3`

### Installation

Install from Galaxy:

```bash
ansible-galaxy collection install extreme_community.xiqse
```

Or build and install locally:

```bash
git clone https://github.com/extremenetworks/ansible_collections.extreme_community.xiqse
cd ansible_collections.extreme_community.xiqse
ansible-galaxy collection build
ansible-galaxy collection install extreme_community-xiqse-1.0.0.tar.gz
```

## Usage Examples

Query XIQ‑SE server version:

```yaml
- name: Get XIQ-SE version
  hosts: localhost
  gather_facts: false
  tasks:
    - name: Query version
      extreme_community.xiqse.xiqse_version:
        provider:
          host: "{{ xiqse_host }}"
          client_id: "{{ xiqse_client }}"
          client_secret: "{{ xiqse_secret }}"
      register: result

    - name: Show version
      ansible.builtin.debug:
        msg: "XIQ-SE version: {{ result.version }}"
```

Run a custom GraphQL query:

```yaml
- name: Run GraphQL query
  hosts: localhost
  gather_facts: false
  tasks:
    - name: Execute query
      extreme_community.xiqse.xiqse_query:
        query: |
          query {
            administration {
              serverInfo {
                uptime
                version
              }
            }
          }
        provider:
          host: "{{ xiqse_host }}"
          client_id: "{{ xiqse_client }}"
          client_secret: "{{ xiqse_secret }}"
      register: result

    - name: Display result
      ansible.builtin.debug:
        var: result
```

## Support

_The software is provided as-is and [Extreme Networks](http://www.extremenetworks.com/) has no obligation to provide maintenance, support, updates, enhancements, or modifications. Any support provided by [Extreme Networks](http://www.extremenetworks.com/) is at its sole discretion._

Issues and/or bug fixes may be reported on [The Hub](https://community.extremenetworks.com/).

## Want to contribute?

Fork this repository, make your changes, and submit a pull request. Or, follow the instructions described [here](https://extremeportal.force.com/ExtrArticleDetail?n=000007550).

>Be Extreme
