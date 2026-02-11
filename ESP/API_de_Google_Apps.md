---
title: API de Google Apps
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

Es posible que los clientes de Google que utilizan Inicio de sesión único (SSO) para autenticar el acceso de los usuarios a los servicios de Google Apps no puedan usar Exchange para conectar a los usuarios al correo electrónico, los contactos y el calendario debido a las limitaciones en el protocolo que impiden que los dispositivos activados mediante SSO se conecten a servicios de autenticación externos. Este servicio puede controlar esto creando y administrando con seguridad las contraseñas de las cuentas para la conectividad ActiveSync.

**Requisitos previos**

Antes de intentar configurar la función de la API de Google Apps, necesita tener:

- Acceso de administrador a una cuenta en [**https://console.developers.google.com/**](https://console.developers.google.com/).
- Acceso de administrador a una cuenta en [**https://admin.google.com**](https://admin.google.com).

## Activar la función de la API de Google Apps

Procedimiento

1. Seleccione **Administrador > Google > API de Google Apps**.
2. Haga clic en **Paso 1: Google Dev**en la parte inferior del rectángulo de la izquierda, donde dice 1.
3. Aparecerá la página "Paso 1: Google Dev".
   Siga las instrucciones que aparecen en la página "Paso 1: Google Dev" y haga clic en **Hecho**.
4. Haga clic en **Paso 2: Google Admin&#x20;**&#x65;n la parte inferior del rectángulo central, donde dice 2.
5. Aparecerá la página "Paso 2: Google Admin".
   Siga las instrucciones que aparecen en la página "Paso 2: Google Admin" y haga clic en **Hecho**.
6. Introduzca el nombre de usuario de Google Admin en el campo **Introduzca el nombre de usuario de Google Admin** del rectángulo de la derecha, donde dice 3.
7. En ese mismo rectángulo, haga clic en **Elegir archivo** para cargar el archivo JSON que descargó en el paso 1.
8. Haga clic en **Guardar**.
9. Si no puede ver la página del API de Google Apps, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):
   - Administración del sistema
   - Solo lectura del sistema
