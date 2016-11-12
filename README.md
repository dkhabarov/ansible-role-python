# ansible-role-base-bootstrap
Устанавливает python, если того нету в системе. При базовом провижене роль должна отрабавать ранее всех остальных.

requirements.yml:
```yaml
---
- src: https://github.com/dkhabarov/ansible-role-base-bootstrap.git
  name: dkhabarov.ansible-role-base-bootstrap
```
Установка:

```shell
ansible-galaxy install -r requirement.yml -f
```

Пример плейбука:

```yaml
---
- name: apply common configuration
  user: root
  hosts: all
  gather_facts: False
  roles:
    - dkhabarov.ansible-role-base-bootstrap
```

provision!
