# nginx_role

Minimal, purist Ansible role to install and configure Nginx in an idempotent way.

Usage
-----

Include the role in your playbook:

```yaml
- hosts: web
  roles:
    - role: nginx_role
      vars:
        nginx_server_name: example.com
        nginx_doc_root: /var/www/example
```

Variables (defaults)
---------------------

- `nginx_package`: nginx
- `nginx_service`: nginx
- `nginx_user` / `nginx_group`: www-data
- `nginx_doc_root`: /var/www/html
- `nginx_http_port`: 80

Files and templates
-------------------

- `templates/nginx.conf.j2` — main config based on role variables
- `templates/index.html.j2` — simple index page

Handlers
--------

- `Restart nginx` — triggered when config changes
Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
