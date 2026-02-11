---
title: Excluir o distribuir aplicaciones
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Excluir o distribuir aplicaciones gestionadas de un dispositivo sin cambiar la configuración de distribución de aplicaciones internas y públicas en dispositivos iOS, macOS y Windows. Para todas las aplicaciones gestionadas, estas opciones están presentes en la columna **Acciones** de la sección **Aplicaciones disponibles** para todos los dispositivos.

### Permisos

Para excluir o distribuir una aplicación hacia o desde un dispositivo, es necesario disponer de las siguientes autorizaciones:

- Dispositivo de acceso en space (partición)
- Accede a las aplicaciones disponibles para el dispositivo.

## Excluir

La opción de exclusión de una app seleccionada desinstala y elimina del dispositivo los datos asociados. Siga el flujo de trabajo para excluir una aplicación que sea un prerrequisito. Una confirmación emergente indica que está excluyendo una aplicación prerrequisito, lo que resulta en la exclusión de la aplicación principal del dispositivo.

Si excluye aplicaciones internas con múltiples versiones, excluye todas las versiones de aplicaciones no distribuidas del dispositivo. Si excluye una aplicación del dispositivo, se elimina de Apps\@Work e Ivanti Go. Si excluye y elimina una aplicación del Catálogo de aplicaciones y la vuelve a añadir, la aplicación ya no permanecerá excluida para el dispositivo. Si excluye una aplicación gestionada del dispositivo, ésta deberá estar visible en la lista **Dispositivos** > **Dispositivos** > **Aplicaciones disponibles** para que el administrador pueda distribuir la aplicación después de excluirla.

## Distribuir

Cuando el administrador activa el comando **Enviar instalación** desde la aplicación, ésta no se instalará hasta que el administrador decida distribuirla desde las **Aplicaciones disponibles** del dispositivo. Aparece un nuevo mensaje de exclusión para los dispositivos que no reciben la aplicación. Cuando el administrador distribuye una aplicación disponible, la siguiente sincronización instala la aplicación distribuida en el dispositivo.
