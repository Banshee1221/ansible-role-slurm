# ansible-role-slurm

**REQUIRES ANSIBLE 2.7+**

This role sets up a slurm cluster along with a database for slurm accounting.
If a database exists in your environment then it will try to use that.

ONLY MYSQL/MARIADB or compliant DBs are compatible.


## To use:

1. Have a "slurm" section to your ansible inventory.
2. Mark one of the slurm nodes with the variable `slurm_builder=True`, so that the role knows which node to build slurm on. This is also used for other things so ensure it's set in the slurm group.
3. Mark the headnode with the variable `headnode=True`, so as to avoid deploying the slurm daemon there. *THIS ROLE ONLY SUPPORTS ON HEADNODE AS OF NOW, THINGS WILL BREAK WITH MORE*
4. Create a playbook that includes this role. E.g.:
   ```shell
   - hosts: all
     become: true
     gather_facts: false
     pre_tasks:
     - name: Install python2 for Ansible
       raw: bash -c "test -e /usr/bin/python || (apt -qqy update && apt install -qqy python-minimal)"
       register: output
       changed_when: output.stdout != ""
     - name: Gathering Facts
       setup:
     roles:
       - role: ansible-role-slurm
   ```