# Taller – Obligatorio 2025 (Ansible)

## Topología
- **bastion** (controller) → ejecuta Ansible
- **ubuntu**  (192.168.1.100)
- **centos**  (192.168.1.200)
- Red interna: `192.168.1.0/24`

## Requisitos previos
- En **bastion**: Ansible instalado.
- Clave pública del bastion copiada a `ubuntu` y `centos` (usuario `ansible` con sudo NOPASSWD).
  ```bash
  ssh-keygen -t ed25519 -C bastion   # si no tenés clave
  ssh-copy-id ansible@192.168.1.100  # ubuntu
  ssh-copy-id ansible@192.168.1.200  # centos
