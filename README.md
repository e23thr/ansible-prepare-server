# ansible-prepare-server (specific for ubuntu 20.x @12SEP2020)

## Prepare

1. Create a basic user in the host
2. Make user in sudo group
3. (Recommend) change /etc/sudoers to allow sudo without password by changing this line like below

```
%sudo ALL=(ALL) NOPASSWD: ALL
```

## Documents

1. [Ansible Document - Installation](https://docs.ansible.com/ansible/latest/installation_guide/)

2. [Ansible Document - User Guide](https://docs.ansible.com/ansible/latest/user_guide/index.html)

3. edit inventory to your needs

4. Run command

```
% ansible-playbook prepare-server.yml -i inventory
```
