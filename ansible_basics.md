## 1) ¿Qué es Ansible? (2 ejemplos)
Herramienta de automatización e Infraestructura como Código que gestiona configuración y orquesta tareas vía SSH.
Ejemplos: (a) Desplegar y configurar servicios (NFS, web). (b) Aplicar hardening/actualizaciones de forma masiva y repetible.

## 2) ¿Qué es un playbook?
Archivo YAML que describe hosts, tareas, variables y handlers para alcanzar un estado deseado de forma reproducible e idempotente.

## 3) ¿Qué contiene un inventario?
Lista de hosts y grupos (con variables como `ansible_user`, `ansible_host`) en formato ini/yaml; puede ser estático o dinámico.

## 4) ¿Qué es un módulo? (ejemplo)
Componente que ejecuta una acción concreta en el host.
Ejemplo: `dnf` (instala paquetes en CentOS), `service` (gestiona servicios), `lineinfile` (edita líneas), `copy` (copia archivos).

## 5) Ventajas de Ansible
- Sin agentes: usa SSH.
- Idempotente y reproducible.
- Legible (YAML) y versionable (Git).
- Escalable por grupos de hosts; despliegues consistentes.
