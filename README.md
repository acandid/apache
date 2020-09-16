 apache
=======

Install and configuring the Apache SSL on RHEL/CentOS, Debian 9,10 and Ubuntu 20.04

- Install the necessary packages;
- Configure apache, vhost and ssl

Requirements
------------

- The SELinux and firewall settings are not considered to be a concern of this role.

Role Variables
--------------

Necessary changes to defaults / main.yml

| Variable                                     | Default                       | Comments                                                                     |
| :---                                         | :---                          | :---                                                    
| `apache_docroot`                             | '/var/www/html'               | Path to the document root (directory containing html files)
|                                              |                               |
| `apache_failover_domain`                     |                               | Inform your domain
|                                              |                               |


Dependencies
------------

No dependencies.

Installing Certificates
-----------------------

It is necessary to exchange the certificates below for your certificates

```
├── files
│   ├── almircandido.com_ca
│   ├── almircandido.com.crt
│   └── almircandido.com.key

```

Playbook Example
----------------

```
---
- hosts: apache
  become: yes
  roles:
    - /path/acandid.apache
...
```

Inventory Example
-----------------

```
[apache]
debian
ubuntu
redhat
centos

```

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://br.linkedin.com/in/almircandido
