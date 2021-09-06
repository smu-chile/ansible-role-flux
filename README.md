Role Name
=========

Role to create a flux deployment on a kubernetes cluster



Role Variables
--------------

```
    - "{{ FLUX_GIT_URL }}"
    - "{{ FLUX_GIT_BRANCH }}"
    - "{{ FLUX_GIT_PATH }}"
    - "{{ FLUX_GIT_EMAIL }}"
    - "{{ FLUX_GIT_IMAGE_VERSION }}"
    - "{{ FLUX_SSH_DEPLOY_PUBLIC_KEY }}"
    - "{{ FLUX_SSH_DEPLOY_PRIVATE_KEY }}"
```

Example Playbook
----------------


```
- hosts: "{{ lookup('env','BASTION_IP') }}"
  become: no
  remote_user: "ubuntu"
    - role: flux
      FLUX_GIT_URL: "{{ lookup('env', 'FLUX_GIT_URL') }}"
      FLUX_GIT_BRANCH: "{{ lookup('env', 'FLUX_GIT_BRANCH') }}"
      FLUX_GIT_PATH: "{{ lookup('env', 'FLUX_GIT_PATH' )}}"
      FLUX_GIT_EMAIL: "{{ lookup('env', 'FLUX_GIT_EMAIL' )}}"
      FLUX_GIT_IMAGE_VERSION: "{{ lookup('env', 'FLUX_GIT_IMAGE_VERSION' )}}"
      FLUX_SSH_DEPLOY_PUBLIC_KEY: "{{ lookup('env', 'SSH_DEPLOY_PUBLIC_KEY') }}"
      FLUX_SSH_DEPLOY_PRIVATE_KEY: "{{ lookup('env', 'SSH_DEPLOY_PRIVATE_KEY') }}"
```

License
-------

BSD

Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)