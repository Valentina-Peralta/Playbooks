# Colección de Playbooks de Ansible

Este repositorio contiene una colección de playbooks de Ansible destinados a automatizar diversas tareas en entornos de servidor. El objetivo es proporcionar una variedad de playbooks para simplificar la administración y configuración de sistemas.

## Playbook1: Instalación de Componentes en CentOS 7

El primer playbook de esta colección tiene como objetivo automatizar la instalación de varios componentes esenciales en un servidor CentOS 7. Los componentes que se instalan incluyen Python 3, pip3, Django, boto3 y Git.

### Componentes Instalados

- **Python 3 y pip3**: Se instala Python 3, que es necesario para muchas aplicaciones y herramientas en Python. También se instala pip3, que es el administrador de paquetes de Python 3.

- **Git**: Git es un sistema de control de versiones ampliamente utilizado para gestionar el código fuente y colaborar en proyectos de desarrollo de software.

- **Django**: Django es un marco de desarrollo web de Python que facilita la creación de aplicaciones web robustas y escalables.

- **boto3**: Boto3 es la biblioteca de Python de AWS (Amazon Web Services) que se utiliza para interactuar con los servicios de AWS desde aplicaciones Python.

### Requisitos

Para utilizar este playbook y otros playbooks de esta colección, necesitas:

- Un servidor CentOS 7 con acceso SSH.
- Ansible instalado en tu máquina local desde la que ejecutarás los playbooks.

### Uso

1. Asegúrate de que tu servidor CentOS 7 esté configurado en el inventario de Ansible.
2. Modifica los playbooks si es necesario (por ejemplo, si deseas agregar más tareas).
3. Ejecuta un playbook con el siguiente comando:

   ```shell
   ansible-playbook playbook1.yml
