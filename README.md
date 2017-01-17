# ansible-role-python
Устанавливает python, если того нету в системе. При базовом провижене роль должна отрабавать ранее всех остальных.

requirements.yml:
```yaml
---
- src: https://github.com/dkhabarov/ansible-role-python.git
  name: dkhabarov.ansible-role-python
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
    - dkhabarov.ansible-role-python
```

provision!
