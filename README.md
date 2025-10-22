# PostgreSQL Ansible Role

This repository contains an Ansible role for managing PostgreSQL databases. The role is designed to simplify the installation, configuration, and management of PostgreSQL on various systems.

## Table of Contents

- [Requirements](#requirements)
- [Role Variables](#role-variables)
- [Example Playbook](#example-playbook)
- [Testing](#testing)
- [License](#license)
- [Author Information](#author-information)
- [Reflection](#reflection)

## Requirements

- Ansible 2.9 or higher
- Supported operating systems: Ubuntu, CentOS, and Debian

## Role Variables

The following variables can be defined in `roles/postgresql/defaults/main.yml`:

- `postgresql_version`: The version of PostgreSQL to install (default: `13`)
- `postgresql_port`: The port on which PostgreSQL will listen (default: `5432`)
- `postgresql_db_name`: The name of the database to create (default: `mydb`)
- `postgresql_user`: The username for the PostgreSQL user (default: `myuser`)
- `postgresql_password`: The password for the PostgreSQL user (default: `mypassword`)

## Example Playbook

```yaml
- hosts: database_servers
  roles:
    - postgresql
```

## Testing

To test the role, navigate to the `roles/postgresql/tests` directory and run:

```bash
ansible-playbook test.yml -i inventory
```

## License

This project is licensed under the MIT License.

## Author Information

Created by [Your Name](https://github.com/yourusername).

## Reflection

This role was created to streamline the process of managing PostgreSQL databases using Ansible. It provides a reusable and configurable way to deploy PostgreSQL across different environments.