# PostgreSQL Ansible Role

This Ansible role manages the installation, configuration, and management of PostgreSQL databases. It provides a flexible and reusable way to deploy PostgreSQL on various systems.

## Requirements

- Ansible 2.9 or higher
- Supported operating systems: Ubuntu, CentOS, and Debian

## Role Variables

The following variables can be defined in `defaults/main.yml`:

- `postgresql_version`: The version of PostgreSQL to install (default: `13`).
- `postgresql_port`: The port on which PostgreSQL will listen (default: `5432`).
- `postgresql_db_name`: The name of the database to create (default: `mydb`).
- `postgresql_user`: The username for the PostgreSQL user (default: `myuser`).
- `postgresql_password`: The password for the PostgreSQL user (default: `mypassword`).

## Example Playbook

```yaml
- hosts: database
  roles:
    - postgresql
```

## Testing

To test this role, you can use the provided Molecule tests. Run the following command in the `molecule/default` directory:

```bash
molecule test
```

## License

MIT

## Author Information

This role was created in 2023 by [Your Name].

## Reflection

This role encapsulates best practices for managing PostgreSQL databases with Ansible, ensuring that installations are consistent and easily repeatable across different environments.