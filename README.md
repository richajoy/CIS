Purpose
--------
This is an ansible playbook for automatically applying CIS Security Benchmarks to a system running Red Hat Enterprise Linux 7.

What are these benchmarks?

The Center for Internet Security publishes security benchmarks for various systems. Refer to the CIS site as the authoritative site for anything regarding these benchmarks. 

What does this playbook do?

The playbook will attempt to configure your system to meet as many of the CIS security benchmarks as possible based on [CIS RedHat Enterprise Linux 7 Benchmark v2.1.1 - 01-31-2017 ](https://community.cisecurity.org/collab/public/index.php).Any benchmarks marked as "not implemented" will be skipped.

Dependencies
------------

Ansible > 2.2

Usage:
------

- Update the hosts inventory file before execution.

ansible-playbook -i hosts cis_main.yml

Tags
----
Many tags are available for precise control of what is and is not changed.

Some examples of using tags:

```
    # Audit and patch the site
    ansible-playbook site.yml -t auditd
```
 
