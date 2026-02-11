---
title: Crear configuración en modo autónomo de una única aplicación
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

La configuración le permite asegurarse de que solo se ejecutan aplicaciones específicas en un dispositivo. Aunque el usuario intente iniciar una aplicación distinta, la configuración solo iniciará la aplicación específica.

Procedimiento

1. Vaya a **Configuraciones&#x20;**>**&#x20;Agregar&#x20;**>**&#x20;Modo autónomo de aplicación única**.
2. Siga las siguientes pautas para definir la aplicación y los ajustes relacionados.

| **Ajuste**                              | Qué hacer                                                                                                                                                                                                                           |
| --------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nombre**,                             | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                                          |
| **Descripción**                         | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                                                         |
| **Establecimiento de la configuración** | **Identificador de grupo**: (requerido) el identificador único del grupo. Si dos diccionarios contienen el mismo valor BundleIdentifier pero un valor TeamIdentifier distinto, se considerará un error y el perfil no se instalará. |
|                                         | **Identificador de Team**: (requerido) el identificador del equipo del desarrollador, que se usó cuando se firmó la aplicación.                                                                                                     |
| Haga clic en **Siguiente**.             |                                                                                                                                                                                                                                     |

4. En la pantalla **Distribución**, seleccione los grupos que recibirán esta configuración.
5. Haga clic en **Hecho**.
