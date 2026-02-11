---
title: Configurar un perfil de MDM en macOS
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

La configuración de MDM en macOS define los límites del acceso de Ivanti Neurons for MDM. Las configuraciones de MDM en macOS se aprovisionan individualmente para los dispositivos aprovisionados uno a uno.

Procedimiento

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a **Configuraciones**.
3. Seleccione la configuración de MDM de macOS que desea editar.
4. Haga clic en el icono del lápiz (editar) para editar la configuración.
5. Siga las siguientes pautas para realizar los cambios:

| **Ajuste**                                                                         | Qué hacer                                                                                                                                                                                                                                                                                                                                                                    |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Permitir bloqueo del dispositivo y eliminación de contraseña                       | Deje esta opción sin seleccionar para evitar que se aplique una configuración de cumplimiento del código de acceso.                                                                                                                                                                                                                                                          |
| Permitir borrado del dispositivo                                                   | Deje esta opción sin seleccionar para evitar que se aplique una acción de borrado del dispositivo.                                                                                                                                                                                                                                                                           |
| Permitir consulta de información de red (números de teléfono/SIM, direcciones MAC) | Deje esta opción sin seleccionar para que el dispositivo no envíe informes con información sobre redes.Si esta opción queda sin seleccionar, en la vista Lista de dispositivos y la vista Detalles de dispositivos aparecerá N/A en la información de redes que se deje de notificar. Además, la política de itinerancia no se podrá aplicar en los dispositivos afectados.  |
| **Contraseña de eliminación del perfil**                                           |                                                                                                                                                                                                                                                                                                                                                                              |
| Contraseña para eliminar el perfil                                                 | Especifique una contraseña. Se indicará al usuario que debe introducir la contraseña para eliminar un perfil del dispositivo.                                                                                                                                                                                                                                                |
| Haga clic en **Hecho**.                                                            |                                                                                                                                                                                                                                                                                                                                                                              |

Los cambios se aplican solo a los dispositivos que se aprovisionen después de hacer el cambio.
