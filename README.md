# Ellucian Wgetrc File Installer

[![Build Status](https://travis-ci.org/ChristopherDavenport/ansible-role-ellucian-wgetrc.svg?branch=master)](https://travis-ci.org/ChristopherDavenport/ansible-role-ellucian-wgetrc)

## Dependencies

None

## Role Variables

`ellucian_wgetrc_users` really is a list with names unless you have custom
home paths.

`ellucian_wgetrc_http_user` user is by default banner, but can be changed.

`ellucian_wgetrc_http_password` is the password for accessing Ellucian Solution
Manager

`ellucian_wgetrc_auth_no_challenge` is just a config setting, should not
be changed.

```yaml

# ellucian_wgetrc_users:
    # - name:
    #   group:
    #   path:

ellucian_wgetrc_http_user: banner
# ellucian_wgetrc_http_password:
ellucian_wgetrc_auth_no_challenge: "on"

```

## Example Playbook

```yaml
- hosts: servers
  vars:
    ellucian_wgetrc_users:
      - name: banner
    ellucian_wgetrc_http_password: examplePass
  roles:
     - ChristopherDavenport.ellucian-wgetrc
```
