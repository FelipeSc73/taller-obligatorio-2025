**Tarea 3**

# Usuarios (Ubuntu)
ansible ubuntu -m command -a "getent passwd"

# Memoria (todos)
ansible linux  -m command -a "free -h"

# chrony en CentOS
ansible centos -b -m dnf -a "name=chrony state=present"
ansible centos -b -m service -a "name=chronyd state=started enabled=yes"
ansible centos -m command -a "systemctl status chronyd --no-pager"


**Tarea 4**
ansible-playbook playbooks/nfs_setup.yml
# Validación
ansible centos -m command -a "exportfs -v"
ansible centos -m command -a "ss -tulpn | grep 2049"
ansible centos -m command -a "cat /etc/exports"

ansible-playbook playbooks/hardening.yml
# Validación
ansible ubuntu -m command -a "ufw status verbose"
ansible ubuntu -m command -a "grep -E 'PasswordAuthentication|PermitRootLogin|PubkeyAuthentication' /etc/ssh/sshd_config"
ansible ubuntu -m command -a "systemctl status fail2ban --no-pager"
