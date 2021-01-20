[![Ansible Galaxy](https://raw.githubusercontent.com/roles-ansible/role_ansible-version/master/.github/galaxy.svg?sanitize=true)](https://galaxy.ansible.com/do1jlr/ansible_version/)  [![MIT License](https://raw.githubusercontent.com/roles-ansible/role_ansible-version/master/.github/license.svg?sanitize=true)](https://github.com/roles-ansible/role_ansible-version/blob/master/LICENSE)

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

```bash
# install role
ansible-galaxy install do1jlr.ansible_version
```

Example playbook:
```
---
- hosts: localhost
  roles:
  - { role: do1jlr.ansible_version, tags: [default,version,always], gather_facts: false }
```

**Without ansible galaxy:**

Add this role to your roles as ``ansible_version``. *Example:*
```bash
git clone https://github.com/roles-ansible/role_ansible-version.git roles/ansible_version
```

Your Playbook could look like this:
```ini
---
- name: check if ansible is not to old
  hosts: localhost
  tags:
    - default
    - version
    - always
  roles:
    - ansible_version
  gather_facts: false
```

 Modifications
------------

For possible modifications please have a look into the ``default`` Folder!


 Participation
-------------
This role is developed on [github](https://github.com/roles-ansible/role_ansible-version.git).
Feel free to add any Issues or PullRequests there. Thanks <3


 Testing
---------
This role is tested with [these github-action](https://github.com/search?q=topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of debian and ubuntu. Linting is tested via travis-ci and the official ansible github action.
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Ansible Lint check](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)
| [![Ansible check debian:stable](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:stable/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Astable%22) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:sid](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:sid/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Asid%22) | [ansible test with debian sid](https://github.com/marketplace/actions/check-ansible-debian-sid) |
| [![Ansible check debian:buster](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:buster/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Abuster%22) | [ansible test with debian buster](https://github.com/marketplace/actions/check-ansible-debian-buster) |
| [![Ansible check debian:stretch](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:stretch/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Astretch%22) | [ansible test with debian stretch](https://github.com/marketplace/actions/check-ansible-debian-stretch) |
| [![Ansible check ubuntu:latest](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:latest/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Alatest%22) | [ansible test with ubuntu latest](https://github.com/marketplace/actions/check-ansible-ubuntu-latest) |
| [![Ansible check ubuntu:bionic](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:bionic/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Abionic%22) | [ansible test with ubuntu bionic](https://github.com/marketplace/actions/check-ansible-ubuntu-bionic) |
| [![Ansible check ubuntu:trusty](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:trusty/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Atrusty%22) | [ansible test with ubuntu trusty](https://github.com/marketplace/actions/check-ansible-ubuntu-trusty) |
| [![Ansible check centos:centos7](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20centos:centos7/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+centos%3Acentos7%22) | [ansible test with ubuntu xenial](https://github.com/marketplace/actions/check-ansible-centos-centos7) |
| [![Ansible check centos:centos8](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20centos:centos8/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+centos%3Acentos8%22) | [ansible test with ubuntu xenial](https://github.com/marketplace/actions/check-ansible-centos-centos8) |
| [![Ansible check centos:latest](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20centos:latest/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+centos%3Alatest%22) | [ansible test with ubuntu xenial](https://github.com/marketplace/actions/check-ansible-centos-latest) |
