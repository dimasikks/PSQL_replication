# Automatically PostgreSQL replication with 2 or more servers 

### To start FULL installation - configure all vars/main.yml, invenotry.yml files and hosts in init.yml, then make sure that your user is a member of sudo group.

After that use following command:
```bash
ansible-playbook init.yml
```

### Before start, you can check replication mode at your servers. For that configure all vars/main.yml and invenotry.yml files

After that use following command:
```bash
ansible-playbook init.yml --tags postgresql_replication_master
```

### Also, after reading the names of the roles, you can perform the necessary tasks separately using tags without starting the entire playbook

E.G. For install postgres:
```bash
ansible-playbook init.yml --tags postgresql_install
```

E.G. For configure replication only at master server:
```bash
ansible-playbook init.yml --tags postgresql_replication_master
```
