 Check Ansible Version
========================

 What is it doing?
--------------

This role check the ansible-playbook version and will fail, if it is to old.
This should help prevent bigger issues with to old ansible installations

 How to use?
-----------
This anisble role should be executet on ``localhost``.

### Example playbook:
**With ansible galaxy:**


**Without ansible galaxy:**
Add this role to your roles as ``ansible_version``.
```bash
git clone https://github.com/chaos-bodensee/role-ansible_version.git roles/ansible_version
```

Your Playbook could look like this:
```ini
---
- name: secure access to toolbox gateway
  hosts: localhost
  tags:
   - default
  roles:
    - ansible_version
```

 Modifications
------------

For possible modifications please have a look into the ``default`` Folder!
