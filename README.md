# ansible-role-gitea

An Ansible role to install [Gitea](https://gitea.io/en-us/) on Linux.

## Requirements

None.

## Role Variables

* gitea_version = The version of Gitea to install.
* gitea_arch = The processor architecture that should be installed.
* gitea_user = The Gitea user to create and use for the service.
* gitea_database_backend = The databsae back-end to use. The default is "sqlite". This will only modify the systemd service file for dependency services.
    * mssql
    * mysql
    * postgres
    * sqlite3 (Default)
* gitea_cache_backend = The cache back-end to use for.
    * memcache
    * memory (Default)
    * redis

## Dependencies

None.

## Example Playbook

```
---
- hosts: gitea_server
  roles:
    - ansible-role-gitea
```

## License

Apache v2.0
