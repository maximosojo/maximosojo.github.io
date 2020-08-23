---
layout: post
title:  "Guía de Ingeniera de Software"
date:   2020-08-23 19:39:00 -0400
categories: develop
---

Esta guía describe en parte los estándares y las mejores prácticas recomendadas para el desarrollo de software. Estos estándares están destinados a mantener la calidad del producto y proporcionar coherencia entre las bases de código para que sea más fácil para todos los ingenieros aprender nuevas partes del sistema. Este último objetivo es importante para animar a todos a que se sientan cómodos buceando en todas las partes del sistema, como suele ser necesario al depurar.

Es importante recordar que todas las situaciones son únicas, por lo que las reglas no deben seguirse a ciegas. Sin embargo, estas pautas representan las mejores prácticas que se acuerdan por el equipo. Si cree que es necesario apartarse de ellos, está bien, pero esté preparado para explicar por qué.

## El repositorio

Estas pautas cubren la denominación, la estructura y los procesos de los repositorios.

### #1: calidad FCS todo el tiempo

En general, utilice la rama "master" para el desarrollo. El desarrollo no debe estar en curso en las ramas de lanzamiento. "maestro" debe ser calidad FCS todo el tiempo. Los entregables deben ser siempre de la calidad suficiente para enviarse a un primer cliente, FCS (primer envío al cliente).

Cuando se trabaja en funciones grandes, es tentador utilizar ramas de desarrollo que eventualmente se integran en master. De hecho, esto a veces es necesario. Sin embargo, debe evitarse cuando sea posible, ya que significa que las personas están ejecutando ramas de desarrollo en lugar de "master", lo que puede conducir a una espiral de muerte de calidad (QDS) ya que menos personas ejecutan el árbol de la línea principal. Siempre que sea posible, considere si los proyectos más grandes se pueden dividir en partes de tamaño razonable que puedan integrarse individualmente en el "maestro" sin romper la funcionalidad existente. Esto le permite continuar desarrollando en "maestro" sin dejar de ser capaz de comprometerse con frecuencia.

Tenga en cuenta que el hecho de que un repositorio esté en github no significa que sus problemas se rastreen allí. Eso se decide por proyecto.

### #2: README.md

Cada repositorio debe tener en su raíz un archivo README.md (Markdown) que describe el repositorio y cubre:

* El nombre del Proyecto, API u otros componentes contenidos en el repositorio y una breve descripción de lo que hacen el texto estándar para hacer referencia a la contribución y las pautas de seguimiento de problemas del proyecto.
* Propietarios del proyecto.
* Las configuraciones de estilo y liberias ccs utilizadas, cualquier comprobación adicional previa a la confirmación y cualquier destino útil no estándar de Makefile.
* Alguna descripción general de la estructura del proyecto, que puede incluir descripciones de los subcomponentes, estructura de directorio y principios básicos de diseño
* Flujo de trabajo de desarrollo básico: cómo ejecutar el código y empezar a jugar con él
* Se recomienda encarecidamente comenzar con la plantilla en este repositorio.

### #3: CHANGELOG.md

Cada repositorio debe tener en su raíz un archivo CHANGELOG.md (Markdown) que registre los cambios y cubre:

* Nuevas funcionalidades integradas.
* Registro de librerias para cumplir con requerimientos de código.
* Actualización de módulos criticos del sistema o compomentes compartidos.
* Revisión de bugs encontrados o reportados.
* Cualquier información relevante para el equipo de desarrollo.

El formato se basa en [Keep a Changelog]( http://keepachangelog.com/en/1.0.0/ )

## El código

Estas pautas cubren la denominación, la estructura y los procesos a la hora de registras nuevo código.

### #1: Comentar y documentar

Considere agregar un comentario de bloque en la parte superior de cada archivo que describa en un mensaje el componente que se implementa en el archivo. Por ejemplo:

    /**
     * profile.js: Perfil
     *
     * Visualización de información asociada al perfil de los usuarios.
     */


Considere agregar un comentario de bloque en la parte superior de cada método registrado, que describa en un mensaje el funcionamiento del mismo. Por ejemplo:

    /**
     * Registro de usuarios, con llamado desde API.
     */     
     async register(req, res) {

     }

Para subsistemas no triviales, considere agregar una declaración de Gran Teoría que describe lo que hace el componente, la interfaz externa y los detalles internos.