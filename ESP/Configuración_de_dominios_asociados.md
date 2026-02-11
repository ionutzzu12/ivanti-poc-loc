---
title: Configuración de dominios asociados
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

**Licencia**: Gold

La configuración de dominios asociados es un diccionario que asigna las aplicaciones a sus dominios asociados. Los dominios asociados se pueden usar con funciones como AppSSO extensible, enlaces universales y Autorrellenado de contraseñas.

Los ajustes de los dominios asociados son los siguientes:

| **Ajuste**                     | Qué hacer                                                                                                                                                                                                                                                                      |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Nombre                         | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                                                                                     |
| Identificador de la aplicación | (Requerido) El identificador de la aplicación con el que asociar los dominios.                                                                                                                                                                                                 |
| Dominios asociados             | (Requerido) Los dominios con los que asociar la aplicación. Cada cadena de texto tiene el formato "service\:domain". Los dominios deben ser nombres de host totalmente cualificados, como [**www.ejemplo.com**](http://www.ejemplo.com).                                       |
| Habilitar la descarga directa  | Si es cierto, los datos de este dominio se descargarán directamente en lugar de utilizar un CDN. El valor de derechos para este dominio se debe ajustar como service\:domain?mode=managed o se ignorará el valor. Disponible en macOS 11 y posterior.**Predeterminado**: falso |
