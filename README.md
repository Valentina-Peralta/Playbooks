# Colección de Playbooks de Ansible

Este repositorio contiene una colección de playbooks de Ansible destinados a automatizar diversas tareas en entornos de servidor. El objetivo es proporcionar una variedad de playbooks para simplificar la administración y configuración de sistemas.

## Playbook1: Instalación de Componentes en CentOS 7

El primer playbook de esta colección tiene como objetivo automatizar la instalación de varios componentes esenciales en un servidor CentOS 7. Los componentes que se instalan incluyen Python 3, pip3, Django, boto3 y Git.

- **Python 3 y pip3**: Se instala Python 3, que es necesario para muchas aplicaciones y herramientas en Python. También se instala pip3, que es el administrador de paquetes de Python 3.

- **Git**: Git es un sistema de control de versiones ampliamente utilizado para gestionar el código fuente y colaborar en proyectos de desarrollo de software.

- **Django**: Django es un marco de desarrollo web de Python que facilita la creación de aplicaciones web robustas y escalables.

- **boto3**: Boto3 es la biblioteca de Python de AWS (Amazon Web Services) que se utiliza para interactuar con los servicios de AWS desde aplicaciones Python.

#### Requisitos

Para utilizar este playbook y otros playbooks de esta colección, necesitas:

- Un servidor CentOS 7 con acceso SSH.
- Ansible instalado en tu máquina local desde la que ejecutarás los playbooks.
- `setuptools` instalado en tus servidores CentOS antes de ejecutar los playbooks, ya que muchos paquetes de Python, como `boto3` y `Django`, dependen de él.

## Playbook2: Configuración de Apache HTTPD

El segundo playbook en esta colección se enfoca en automatizar la configuración de un servidor Apache HTTPD en tus servidores. Los pasos que realiza este playbook incluyen:

- Instalación de Apache HTTPD en el servidor.
- Apertura de los puertos 80 (HTTP) y 443 (HTTPS) en el firewall.
- Recarga de la configuración del firewall.
- Inicio de Apache HTTPD.
- Verificación del estado de Apache HTTPD.

Este playbook es útil para establecer rápidamente un servidor web con Apache HTTPD y asegurarte de que los puertos necesarios estén abiertos y el servicio esté en funcionamiento.

#### Requisitos

Para utilizar este playbook, necesitas:

- Un servidor CentOS 7 con acceso SSH.
- Ansible instalado en tu máquina local desde la que ejecutarás los playbooks.

## Playbook3: Configuración de Nginx
Este playbook de Ansible automatiza la configuración de un servidor web Nginx en un sistema CentOS 7. Asegura que Nginx esté instalado, que el archivo `index.html.j2` se haya creado y configurado correctamente, y que el puerto 8080 esté abierto en el firewall.

### Instrucciones
Crear el Archivo `index.html.j2`

Debes crear un archivo llamado `index.html.j2` en  `templates`. Aquí hay un ejemplo de cómo podría ser el contenido del archivo `index.html.j2`:

```jinja2
<!DOCTYPE html>
<html>
<head>
    <title>Bienvenido a Ansible</title>
</head>
<body>
    <h1>Bienvenido a Ansible</h1>
    <p>Mi servidor es: {{ ansible_host }}</p>
</body>
</html>
```

## Playbook4: Instalación de SQLite3 y su paquete de desarrollo
Este playbook de Ansible está diseñado para instalar SQLite3 y su paquete de desarrollo en un servidor CentOS 7. SQLite es una base de datos ligera y ampliamente utilizada en aplicaciones y sistemas embebidos. La instalación del paquete de desarrollo es esencial para compilar aplicaciones que utilizan SQLite.
