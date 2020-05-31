Ansible Role: Template
=========

This Role used for install NoSQL database system [Couchbash](https://www.couchbase.com/)

## Requirements

Make sure these requirements need before the installation

| **Items**      | **Details** |
| ------------------| ------------------|
| Operating system | CentOS7.x Ubuntu18.04 AmazonLinux|
| Python version | Python2  |
| Python Components |    |
| Runtime |  |


## Related roles

This Role does not depend on other role variables in syntax, but it depend on other role before

```
  roles:
    - {role: role_common, tags: "role_common"}
    - {role: role_template, tags: "role_couchbase"}
```


## Variables

The main variables of this Role and how to use them are as follows:

| **Items**      | **Details** | **Format**  | **Need to assignment** |
| ------------------| ------------------|-----|-----|
| template_applications | True, False | Boolean | No |

notes: 

1. ×××××××
2. ×××××××

## Example

```
- name: Memcached
  hosts: all
  become: yes
  become_method: sudo 
  vars_files:
    - vars/main.yml 

  roles:
    - {role: role_common, tags: "role_common"}
    - {role: role_cloud, tags: "role_cloud"}
    - {role: role_template, tags: "role_template"}
```

## FAQ

1. Every role name must start with **role_**
2. Minimal dependence other roles
3. Variable must reasonable, and program syntax complete