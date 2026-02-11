---
title: Cuentas administradas de Google Play (cuentas con Android Enterprise)
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

Licencia: Silver

Las cuentas administradas de Google Play son necesarias para habilitar el uso y configuración de dispositivos con Android Enterprise. Ya no es necesario que use Google Apps Directory Sync (GADS) o las cuentas de Google para registrar los dispositivos.

**Importante:** si ya ha configurado Android Enterprise, primero debe retirar esos dispositivos para poder usar esta función.

## Configurar Android Enterprise

**Procedimiento**

1. Inicie sesión en el portal de Ivanti Neurons for MDM.
2. Vaya a **Administrador > Google > Android Enterprise**.
3. En **Cuenta de Google Play administrada**, haga clic en **Autorizar Google** para mostrar la página de Google Play for Work.
4. Haga clic en **Comenzar**.\* Introduzca el nombre de su empresa.
   - Acepte el acuerdo de Android Enterprise.
5. Haga clic en **Confirmar**.
6. Haga clic en **Completar registro**.

Cuando Android Enterprise esté configurado mediante las cuentas de Google Play, hay un límite en el número de dispositivos que se pueden inscribir por usuario. Para superar esta limitación, cuando cree un nuevo usuario, seleccione la opción **Cuenta de dispositivo con Android Enterprise** para activar que se asigne automáticamente una Cuenta de dispositivo Google a las inscripciones de dispositivos administrados en el trabajo con Android Enterprise vinculadas a esta cuenta.

Las cuentas de dispositivos están previstas para implementaciones de tipo COSU (un solo uso), como por ejemplo con el modo Kiosco. Es posible que los usuarios con cuentas de dispositivos tengan acceso limitado a Google Play.

De vez en cuando, una cuenta administrada de Google Play o su token caduca por diferentes motivos, como la caducidad del token de autenticación o la cuenta o empresa que se va a borrar. En dichas situaciones, los servicios de Google Play notificarán al cliente con una acción de retransmisión que hará que el cliente reaprovisione el dispositivo eliminando la cuenta existente y añadiendo una cuenta con un token nuevo obtenido del servidor de UEM.

En esos casos, no se puede reaprovisionar la cuenta porque la cuenta anterior no se ha podido eliminar o porque se han producido demasiados intentos de reaprovisionamiento. Al usuario se le notifica para que vuelva a empezar de nuevo retirando el cliente o restableciendo los valores de fábrica del dispositivo, según sea el caso, en función de si el dispositivo está en modo perfil de trabajo o en modo dispositivo administrado.
