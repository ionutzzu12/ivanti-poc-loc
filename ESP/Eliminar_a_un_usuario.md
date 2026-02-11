---
title: Eliminar a un usuario
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Qué ocurre cuando se elimina a un usuario local**](./Eliminar_a_un_usuario.md)
- [**¿Qué ocurre con los usuarios de LDAP?**](./Eliminar_a_un_usuario.md)

**Procedimiento**

1. Vaya a **Usuarios > Usuarios.**
2. Seleccione la entrada del usuario.
3. Haga clic en **Acciones** (arriba a la derecha).
4. Seleccione **Eliminar**.

Cuando un administrador de Ivanti Neurons for MDM o un administrador asociado intenta eliminar a un administrador socio, Ivanti Neurons for MDM muestra un mensaje que indica que un administrador asociado debe llevar a cabo esta operación en el Portal del proveedor de servicios.

Si un usuario tiene algunos dispositivos asociados a su cuenta, primero debe retirar y eliminar los dispositivos y luego eliminar el usuario. Si el usuario no tiene dispositivos, la información del usuario se puede eliminar cuando se elimina el usuario.

## Qué ocurre cuando se elimina a un usuario local

- Toda la información relacionada con un usuario eliminado se elimina también del sistema.
- Se retiran los dispositivos asociados con el usuario.
- Se mantiene el contenido cargado por el usuario.
- No se permiten más registros de dispositivos para la cuenta del usuario.

## ¿Qué ocurre con los usuarios de LDAP?

- Si el servidor LDAP se ha desactivado, el usuario LDAP no puede eliminarse permanentemente. La siguiente sincronización de datos LDAP restaurará a un usuario LDAP eliminado.
- Si el servidor o grupo LDAP se ha eliminado, los usuarios LDAP se convierten en usuarios locales y sí pueden eliminarse.
- Cuando se elimina un usuario desde LDAP, no se eliminará de la nube. El estado de sincronización cambiará a "NO\_SYNC", pero no se eliminará el usuario.
