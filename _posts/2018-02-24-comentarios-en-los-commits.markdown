---
layout: post
title:  "Comentarios en los commits!"
date:   2018-02-24 00:13:00 -0400
categories: git
---
Este manual corto lo elaboré con el propósito de mostrar un formato para los comentarios de nuestros commits, que nos ayude en la navegación y nos de un idea al primer vistazo de los cambios realizados dentro del los mismos.

Este formato lo pueden aplicar a cualquier proyecto, bien sea personal o de terceros, la idea es implementarlo en los que tienen actualmente, de esta manera ir visualizando las mejoras de lectura de los commits y asu vez tener proyectos muy profesionales.

La estructura del mensaje a reactar en el commit es la siguiente:

**`<type>(<scope>): <subject>`**

**Type:**
En el tipo de commit, podemos elegir de las siguientes opciones.

* **`feat:`** Una nueva funcionalidad.

* **`fix:`** Cuando se va a subir alguna corrección.

* **`docs:`** Solo para los cambios en los documentos.

* **`style:`** Estos es cuando el cambio no afecta el código o la funcionalidad (Espacios en blanco, formato, punto y coma, etc), solo la estructura.

* **`refactor:`** Es cuando el cambió en el código no corrige un error o agrega una nueva funcionalidad. Mejora en el código.


**Scope:**
Es el ámbito donde se realizó en cambio, config, web-server, index, modulo, etc.

**Subject:**
Contiene la descripción de cambio, se debe de utilizar en tiempo presente, máximo 100 caracteres.

### Ejemplos de implementación:

**`feat(assets): se integran los assets para redes sociales.`**

**`fix(Signin): se corrige inicio de sesión con facebook`**