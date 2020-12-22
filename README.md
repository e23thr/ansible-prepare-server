# ansible-prepare-server (specific for ubuntu 20.x @04DEC2020)

## Prepare

1. prepare dns for all ssl_domains
2. Copy ssh public key to the server

## Documents

1. [Ansible Document - Installation](https://docs.ansible.com/ansible/latest/installation_guide/)

2. [Ansible Document - User Guide](https://docs.ansible.com/ansible/latest/user_guide/index.html)

3. edit inventory to your needs

4. Run command

```
% ansible-playbook prepare-server.yml -i inventory
```

---

## Inventory file

| parameter             | description                                                       |
| --------------------- | ----------------------------------------------------------------- |
| **letsencrypt_email** | email to create let's encrypt certificate                         |
| **ssl_domains**       | list of domains that can be configure with virtual host and https |

---

## Useful command

| command                                             | description                                                     |
| --------------------------------------------------- | --------------------------------------------------------------- |
| ssh-copy-id -i ~/.ssh/id_rsa.pub root@remote-server | copy public ssh key to server for remote shell without password |
| sudo timedatectl list-timezones                     | List time zones                                                 |
| sudo timedatectl set-timezone <your_time_zone>      | set system timezone ie. Asia/Bangkok                            |
