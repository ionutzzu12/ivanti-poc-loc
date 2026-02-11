---
title: Preferencia de identidad
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** macOS 10.12 o versiones más recientes compatibles.

Identifique un elemento de Preferencia de identidad en la llave del usuario que haga referencia a una carga útil de la identidad incluida en el mismo perfil.

En dispositivos macOS, la Preferencia de identidad le permite elegir una identidad (par clave-valor) que desee usar con un sitio web. Una vez que haya insertado una Preferencia de identidad (que consiste en la URL y la identidad) en el dispositivo, aparecerá en **Acceso a la llave > Todos los elementos** (el «Tipo» será «Preferencia de identidad»). La próxima vez que intente conectarse a esa URL desde Safari, el dispositivo presentará el certificado configurado.

Ivanti Neurons for MDM crea una configuración predeterminada de preferencia de la identidad del sistema con una carga útil para la URL de AppStore y el certificado que se utilizará.

Mientras el usuario accede al App Catalog de macOS con Safari en macOS 10.12 y versiones posteriores, recibirá un mensaje pidiendo la contraseña del sistema para almacenar en el caché el certificado de identidad. Los usuarios deben seleccionar "Permitir siempre" la primera vez que les aparezca para evitar que salga el mismo mensaje posteriormente mientras acceden al App Catalog de macOS.

Safari con versiones de macOS previas a la 10.12 y otros navegadores mostrarán mensajes del certificado y la contraseña del sistema mientras se accede al App Catalog de macOS en una sesión nueva con un explorador desde dispositivos macOS.

## Crear la configuración de una preferencia de identidad

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **preferencia** en el campo de búsqueda y, a continuación, haga clic en la configuración de las **Preferencia de identidad**.
4. Asigne un nombre a la configuración y descríbala.
5. En la sección Ajuste de la configuración, en el campo **Nombre**, introduzca una Id. de correo electrónico, un hombre de host de DNS o un nombre que identifique de forma exclusiva al servicio.
6. En el campo **UUID del certificado**, seleccione un certificado.
7. Haga clic en **Siguiente** para configurar los ajustes de distribución.
8. Haga clic en **Listo**.

**Temas relacionados:**

- [**Preferencia de certificado**](./Preferencia_de_certificado.md)
