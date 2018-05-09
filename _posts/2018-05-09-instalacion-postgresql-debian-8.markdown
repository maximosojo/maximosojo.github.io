---
layout: post
title:  "Instalación y configuración PostgreSQL"
date:   2018-05-09 10:24:00 -0400
categories: postgres
---
En este articulo se explica como realizar la instalación y configuración de base de datos PostgreSQL en Debian.

PostgreSQL, es un gestor de base de datos relacional, la primera versión del código fue público el 1 de agosto de 1996, liberado bajo la licencia BSD y desarrollado por “PostgreSQL Global Development Group”.

### Pasos de instalación:

**Actualización de paquetes**

**`sudo apt-get update`**

**Instalación**

**`sudo apt-get install postgresql-9.4 postgresql-client-9.4`**

### Pasos de configuración inicial:

Lo primero que se tiene que hacer es cambiarle la contraseña al usuario ‘postgres’ que se crea luego de haber instalado el paquete:

**`passwd postgres`**

Acceda a la consola de administración de PostgreSQL para cambiar la contraseña del usuario ‘postgres’ con los siguientes comandos:

**`su postgres
postgres@server:~$ psql postgres
postgres=# ALTER ROLE postgres PASSWORD 'CONTRASENA_DEL_USUARIO';`**
