 Check Ansible Version
========================
[![Build Status](https://travis-ci.org/chaos-bodensee/role-ansible_version.svg?branch=master)](https://travis-ci.org/chaos-bodensee/role-ansible_version)

 What is it doing?
--------------

This role check the ansible-playbook version and will fail, if it is to old.
This should help prevent bigger issues with to old ansible installations

 How to use?
-----------
This anisble role should be executet on ``localhost``.

### Example playbook:
**With ansible galaxy:**

```bash
# install role
ansible-galaxy install do1jlr.ansible_version
```

Example playbook:
```
---
- hosts: localhost
  roles:
  - do1jlr.ansible_version
```

**Without ansible galaxy:**

Add this role to your roles as ``ansible_version``. *Example:*
```bash
git clone https://github.com/chaos-bodensee/role-ansible_version.git roles/ansible_version
```

Your Playbook could look like this:
```ini
---
- name: check if ansible is not to old
  hosts: localhost
  tags:
   - default
  roles:
    - ansible_version
  gather_facts: no
```

 Modifications
------------

For possible modifications please have a look into the ``default`` Folder!


 Participation
-------------
This role is developed on [github](https://github.com/chaos-bodensee/role-ansible_version.git).
Feel free to add any Issues or PullRequests there. Thanks <3


### Testing

*This role is tested via travis-ci and docker. To test this role manual simply execute the ``.ansible-test.yml`` playbook inside this role.*
