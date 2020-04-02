---
layout: post
title:  "Actualizar dependencias Package.json"
date:   2018-02-24 00:13:00 -0400
categories: npm
---
Cuando tienes un proyecto que depende de paquetes **npm** y deseas actualizar todas las dependencias 
para obtener las últimas características y mejoras de estos paquetes en tu proyecto.

Por lo general actualizas manualmente cada paquete en tu archivo package.json o haces algún otro proceso que es bastante aburrido.

En este acticulo presentare como actualizarlo de una manera mas sencilla con **npm-check-updates**.

**npm-check-updates** es una utilidad que actualiza nuestro package.json con la última versión de todas las dependencias de nuestro proyecto.

### **Instalación**

**`npm install -g npm-check-updates`**

### Identificar las diferencias entre versiones

Para identificar las diferencias entre las versiones de nuestros paquetes simplemente basta con escribir el comando 
**ncu** dentro de nuestra carpeta del proyecto, obviamente aquí debe encontrarse el archivo **package.json**, así:

**`ncu`**

### Actualizar las dependencias de nuestro proyecto

Una vez sean identificadas los paquetes desactualizados, se debe ejecutar en comando **ncu -u**, ya que el anterior solo 
muestra datos informativos.

**`ncu -u`**

Luego de ejecutar el comando **npm-check-updates** actualizara las dependencias y realizara la actualización de nuestro **package.json**,
esto lo puede visualizar con un **git status**

### Instalación de paquetes actualizados

Como paso final solo nos quedaría instalar los paquetes actualizados.

**`npm install -d`**

Y así de simple hemos actualizado cada una de nuestras dependencias a su última versión.
