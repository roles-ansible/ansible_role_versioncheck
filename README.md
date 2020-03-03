[![Build Status](https://travis-ci.org/roles-ansible/role_ansible-version.svg?branch=master)](https://travis-ci.org/roles-ansible/role_ansible-version)

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
  - do1jlr.ansible_version
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
  roles:
    - ansible_version
  gather_facts: no
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
| [![Travis Build Status](https://travis-ci.org/roles-ansible/role_ansible-version.svg?branch=master)](https://travis-ci.org/roles-ansible/role_ansible-version) | [.travis.yml](https://github.com/roles-ansible/role_ansible-version/blob/master/.travis.yml) |
| [![Ansible Lint check](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)
| [![Ansible check debian:stable](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:stable/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Astable%22) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:sid](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:sid/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Asid%22) | [ansible test with debian sid](https://github.com/marketplace/actions/check-ansible-debian-sid) |
| [![Ansible check debian:buster](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:buster/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Abuster%22) | [ansible test with debian buster](https://github.com/marketplace/actions/check-ansible-debian-buster) |
| [![Ansible check debian:jessie](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:jessie/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Ajessie%22) | [ansible test with debian jessie](https://github.com/marketplace/actions/check-ansible-debian-jessie) |
| [![Ansible check debian:stretch](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20debian:stretch/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+debian%3Astretch%22) | [ansible test with debian stretch](https://github.com/marketplace/actions/check-ansible-debian-stretch) |
| [![Ansible check ubuntu:latest](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:latest/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Alatest%22) | [ansible test with ubuntu latest](https://github.com/marketplace/actions/check-ansible-ubuntu-latest) |
| [![Ansible check ubuntu:bionic](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:bionic/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Abionic%22) | [ansible test with ubuntu bionic](https://github.com/marketplace/actions/check-ansible-ubuntu-bionic) |
| [![Ansible check ubuntu:disco](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:disco/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Adisco%22) | [ansible test with ubuntu disco](https://github.com/marketplace/actions/check-ansible-ubuntu-disco) |
| [![Ansible check ubuntu:eoan](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:eoan/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Aeoan%22) | [ansible test with ubuntu eoan](https://github.com/marketplace/actions/check-ansible-ubuntu-eoan) |
| [![Ansible check ubuntu:focal](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:focal/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Afocal%22) | [ansible test with ubuntu focal](https://github.com/marketplace/actions/check-ansible-ubuntu-focal) |
| [![Ansible check ubuntu:trusty](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:trusty/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Atrusty%22) | [ansible test with ubuntu trusty](https://github.com/marketplace/actions/check-ansible-ubuntu-trusty) |
| [![Ansible check ubuntu:xenial](https://github.com/roles-ansible/role_ansible-version/workflows/Ansible%20check%20ubuntu:xenial/badge.svg)](https://github.com/roles-ansible/role_ansible-version/actions?query=workflow%3A%22Ansible+check+ubuntu%3Axenial%22) | [ansible test with ubuntu xenial](https://github.com/marketplace/actions/check-ansible-ubuntu-xenial) |
