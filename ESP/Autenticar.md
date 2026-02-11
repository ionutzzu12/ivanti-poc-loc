---
title: Autenticar
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:**

- macOS 10.13 y versiones más recientes compatibles.
- Windows 10 y versiones más recientes compatibles.

Utilice la configuración de Authenticate para proporcionar una autenticación sin contraseña para los servicios de inicio de sesión en la nube o de sobremesa. Cada dispositivo tendrá una sola configuración de Authenticate.

**Requisitos previos**

- Se requiere una licencia Zero Sign-On.
- Ivanti Neurons for MDM debe registrarse en Access (el perfil de Access debe estar configurado).
- Después de ajustar la configuración de Authenticate, no podrá anular el registro del perfil de Acceso, ya que la configuración de Authenticate hará referencia a este.
- Si el perfil de Access tiene algún cambio, redistribuya la configuración de Authenticate a los dispositivos macOS. Para los dispositivos Windows, copie y use los nuevos valores de CLI en las nuevas aplicaciones.

## Crear una configuración de Authenticate

Procedure

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **auth** en el campo de búsqueda y, a continuación, haga clic en la configuración de **Authenticate**.
4. Asigne un nombre a la configuración y descríbala.
5. Seleccione un **Certificado de identidad de escritorio** de la lista desplegable.
6. Seleccione una o ambas de las siguientes opciones del sistema operativo:\* macOS
   - Windows
7. Para macOS:1) En la región de Datos personalizados, pulse **+ Añadir** para añadir claves y valores de cadena para los datos personalizados que se insertarán a los dispositivos.
   2\) Haga clic en **Siguiente** para configurar los ajustes de distribución.
   3\) Haga clic en **Hecho**.
8. En los dispositivos Windows 10, esta configuración ayuda a generar argumentos de línea de comandos para la aplicación MSI de Authenticator para Windows de la siguiente manera:1) Pulse **Hecho** para completar la configuración de Authenticate.
   2\) Desde la página **Configuraciones**, vea la configuración de Authenticate para copiar el texto de la línea de comandos que se muestra. Este texto es necesario cuando se distribuye la aplicación Authenticate a dispositivos Windows.

Cuando la configuración de Authenticate se aplica a los dispositivos Windows, la configuración permanece en estado «Instalación pendiente». Puede ignorar esto, ya que la funcionalidad no se verá afectada.
