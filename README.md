lighthouse
=========

This role install lighthouse and nginx.

## Requirements
-------

- Ansible >= 2.10
- Target host: Ubuntu 22.04 / 24.04
- Root/sudo access


## Role Variables
-------

| Variable | Default | Description |
|----------|---------|-------------|
| `lighthouse_version` | `master` | Branch or tag to checkout |
| `lighthouse_location_dir` | `/var/www/lighthouse` | Deployment directory for Lighthouse files |
| `nginx_config_file` | `/etc/nginx/nginx.conf` | Path to main Nginx configuration file |


## Dependencies
-------

None.


## Example Playbook
-------

```yaml
- hosts: lighthouse-servers
  become: true
  roles:
    - role: lighthouse-role
      lighthouse_vcs: "https://github.com/myorg/lighthouse.git"
      lighthouse_version: "v2.0.0"
      nginx_http_port: 8080
```

## License
-------

MIT

## Author Information
------------------

Viktor M.
