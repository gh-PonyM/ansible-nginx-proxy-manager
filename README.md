# Role nginx_proxy_manager

Generated ansible role docker using docker compose for ansible-nginx-proxy-manager

## Installation

Install the role using `ansible-galaxy` using a `requirements.yml` file:

```yaml

roles:
- src: https://github.com/gh-PonyM/nginx_proxy_manager.git
  version: main
  name: nginx_proxy_manager
  scm: git
```

## docker-compose.yml template

The original [docker-compose.yml](docker-compose.yml) was transformed into an [ansible template](templates/docker-compose.yml)

## Defaults

Extracted from the original `docker-compose.yml` including environment configurations, the generated defaults are:

| Variable | default  | ENV | used by | is secret |
| -------- |----------|-----| ------- |-----------|
| `prmgr_db_sqlite_file` | /data/database.sqlite | `DB_SQLITE_FILE` | proxy_manager | False |
| `prmgr_disable_ipv6` | true | `DISABLE_IPV6` | proxy_manager | False |
| `prmgr_host_port_proxy_manager_443` | 443 | `host_port_proxy_manager_443` | proxy_manager | False |
| `prmgr_host_port_proxy_manager_80` | 80 | `host_port_proxy_manager_80` | proxy_manager | False |
| `prmgr_host_port_proxy_manager_81` | 81 | `host_port_proxy_manager_81` | proxy_manager | False |
| `prmgr_releases` | {'proxy_manager': 'latest'} | `None` | None | False |
