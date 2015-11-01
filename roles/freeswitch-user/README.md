Role Name
========

This role use to create user for target remote and design for freeswitch ( I'm Candidate ) not recommend for general usage.

Requirements
------------

- Openssl because i use openssl to generate password. 



Role Variables
--------------

You can define variable from top playbook as below. 

- username: username you want to install  
- name: description of this user
- password: user password *** NOTE *** when you not specify this value playbook will generate password for you
  that you want to grep from log by you own ( log you can found at this root playbook name 'ansible-work.log' 
- ssh_key: automatic deploy ssh-key  

```
    users:
      - username: fsuser
        name: freeswitch users
        home_dir: "/opt/freeswitch/"
        password: "123456"
        ssh_key:
            - "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC9bQslGDiJ7cObX07HnWxeBMJxBoG5y0ernnJW6U5eC8bk8hlebGJTdluYDBsa3UpJaIDOo44putydcP02ZNQ32L9YDZlpfmBCB0QZRgAI5bBiOL/3DyteDyLqkz1AAcfG6DduyAm1bt/2zXVzxnExaUYedhNyLuSlyY/FXW1oN9RKvwfCO8y/omgjYk08MwmAZ1H3qH6AQkeMZpWPmVNRhDBpfSP8VOE8Nvubkt/UJZAZ8MgSEkRzyDHRL/HSJ1dUSnbJ3MmF8UeKaYifxWvLJoxOh+I5yIQ6ZGmgboq3YOXppr4Rm+1xN8c9lLSIhOlYrMUEq8ywq4MiKYVv65Nr udomsak@localhost.localdomain"

      - username: fsuser2
        name: freeswitch users
        home_dir: "/opt/freeswitch2/"
        password: "123456"
        ssh_key:
            - "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC9bQslGDiJ7cObX07HnWxeBMJxBoG5y0ernnJW6U5eC8bk8hlebGJTdluYDBsa3UpJaIDOo44putydcP02ZNQ32L9YDZlpfmBCB0QZRgAI5bBiOL/3DyteDyLqkz1AAcfG6DduyAm1bt/2zXVzxnExaUYedhNyLuSlyY/FXW1oN9RKvwfCO8y/omgjYk08MwmAZ1H3qH6AQkeMZpWPmVNRhDBpfSP8VOE8Nvubkt/UJZAZ8MgSEkRzyDHRL/HSJ1dUSnbJ3MmF8UeKaYifxWvLJoxOh+I5yIQ6ZGmgboq3YOXppr4Rm+1xN8c9lLSIhOlYrMUEq8ywq4MiKYVv65Nr udomsak@localhost.localdomain"


```



Dependencies
------------

- NONE


License
-------

- NONE

Author Information
------------------

Udomsak Chundang  <udomsak.chundang@gmail.com>


