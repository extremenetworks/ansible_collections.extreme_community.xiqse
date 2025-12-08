# Ansible Collection - Extreme Networks Community - XIQ-SE

This collection provides Ansible modules and roles to manage ExtremeCloudIQ - Site Engine via GraphQL.

## Overview

This collection, currently in version 1.0.0, includes :

- **Module** :
  - `device_version` : Get the version of device via XIQ-SE API
  - `xiqse_mutation` : Executing a query type GraphQL mutation
  - `xiqse_query`: Executing a query type GraphQL query
  - `xiqse_site` : Allows site management within XIQ-SE
  - `xiqse_version` : Get the version of XIQ-SE

## Getting started

### Prerequisites

- **Ansible:** Version 2.9 or later.
- **Python:** The control node requires Python 3.x.

### Installation

Install the collection via Ansible Galaxy:

```bash
@TODO
```

You can also build it locally:

```bash
git clone https://github.com/extremenetworks/ansible_collections.extreme_community.xiqse
ansible-galaxy collection build
ansible-galaxy collection install extreme_community.xiqse-1.0.0.tar.gz
```

## Usage Examples

Find all our examples here with the environment configuration :

- @TODO

## Support

_The software is provided as-is and [Extreme Networks](http://www.extremenetworks.com/) has no obligation to provide maintenance, support, updates, enhancements, or modifications. Any support provided by [Extreme Networks](http://www.extremenetworks.com/) is at its sole discretion._

Issues and/or bug fixes may be reported on [The Hub](https://community.extremenetworks.com/).

## Want to contribute?

Fork this repository, make your changes, and submit a pull request. Or, follow the instructions described [here](https://extremeportal.force.com/ExtrArticleDetail?n=000007550).

>Be Extreme
