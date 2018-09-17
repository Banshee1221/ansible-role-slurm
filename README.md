# ansible-role-slurm

This role sets up a slurm cluster along with a database for slurm accounting.
If a database exists in your environment then it will try to use that.

ONLY MYSQL/MARIADB or compliant DBs are compatible.


## To use:

1. Have a "slurm" section to your ansible inventory.
2. Mark one of the slurm nodes with the variables `slurm_builder=True`, so that the role knows which node to build slurm on. This is also used for other things so ensure it's set in the slurm group.
3. Have a "database" section to your ansible inventory. If there is no database then DBD will not be deployed.
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