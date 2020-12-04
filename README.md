# ansible-prepare-server (specific for ubuntu 20.x @04DEC2020)

## Prepare

1. Create a basic user in the host
2. Make user in sudo group
3. (Recommend) change /etc/sudoers to allow sudo without password by changing this line like below

```
%sudo ALL=(ALL) NOPASSWD: ALL
```

4. Upload your SSL to your user

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

| parameter                   | description                                                       |
| --------------------------- | ----------------------------------------------------------------- |
| **remote_user**             | normal user to be use as sudoers                                  |
| **letsencrypt_email**       | email to create let's encrypt certificate                         |
| **domain_name**             | main domain name for this server                                  |
| **jenkins_prefix**          | uri prefix for jenkins                                            |
| **jenkins_resource_domain** | resource domain for jenkins                                       |
| **more_domains**            | list of domains that can be configure with virtual host and https |

---

## Useful command

| command                                        | description                          |
| ---------------------------------------------- | ------------------------------------ |
| sudo timedatectl list-timezones                | List time zones                      |
| sudo timedatectl set-timezone <your_time_zone> | set system timezone ie. Asia/Bangkok |
