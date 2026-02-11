---
title: Apps@Work (iOS, Android, Windows y macOS)
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Apps\@Work es un escaparate de aplicaciones de empresa que facilita la distribución segura de software y aplicaciones. Apps\@work está disponible para dispositivos iOS, Android, macOS y Windows. La appstore corporativa Apps\@Work está integrada en los clientes Ivanti Go app y Mobile\@Work para iOS, Android y macOS. Para dispositivos Windows es una aplicación independiente nativa. Esta sección contiene los siguientes temas:

- [**Apps@Work de iOS**](./Apps@Work__iOS__Android__Windows_y_macOS_.md)
- [**Android Apps@Work**](./Apps@Work__iOS__Android__Windows_y_macOS_.md)
- [**macOS Apps@Work**](./Apps@Work__iOS__Android__Windows_y_macOS_.md)
- [**Windows Apps@Work**](./Apps@Work__iOS__Android__Windows_y_macOS_.md)

## Apps\@Work de iOS

La tienda de aplicaciones nativas de Apps\@work se despliega automáticamente con el cliente de Go. No es necesaria ninguna acción del administrador. La pestaña Apps\@work se muestra en la barra de tareas del cliente de Go. El usuario final puede acceder a esta pestaña para ver e instalar las aplicaciones aprobadas por la empresa. Para obtener más información, consulte [**Funciones de la tienda de aplicaciones de Apps@Work en iOS**](./Funciones_de_la_tienda_de_aplicaciones_de_Apps@Work_en_iOS.md).

Las notificaciones del usuario final de iOS Apps\@Work para actualizaciones de aplicaciones están habilitadas por defecto. Si desea cambiar los ajustes, consulte el tema **Notificaciones** en [**Ajustes del catálogo**](./Ajustes_del_catálogo.md).

## Clientes existentes con webclip de Apps\@Work para iOS

Los clientes que tienen desplegado webclip de Apps\@Work de iOS legado, no obtendrán por defecto el catálogo de aplicaciones nativas integrado. Si quiere transicionar al catálogo nativo de Apps\@Work de iOS y eliminar webclip de Apps\@work de los dispositivos, lleve a cabo los pasos siguientes:

### Enviar las configuraciones

El administrador debe enviar el Catálogo de aplicaciones para la configuración del cliente nativo de los dispositivos para que Apps\@Work esté disponible en la experiencia de la tienda de aplicaciones nativas desde la aplicación del cliente de Go. Para obtener más información, consulte [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).

**Procedimiento**

1. Iniciar sesión en el portal administrativo de Ivanti Neurons for MDM.
2. Vaya a **Configuraciones** > Filtrar y seleccionar **Servicios del cliente**. Se listan todas las configuraciones del cliente.
3. Seleccione **Catálogo de aplicaciones para el cliente nativo**. Se abre la página de configuración del Catálogo de aplicaciones del cliente nativo.
4. Haga clic en el icono **Editar distribución**. Se abre la página Editar distribución.
5. Seleccione una de las siguientes opciones:\* **Todos los dispositivos**
   - **Sin dispositivos**: si no quiere distribuir en ningún dispositivo
   - **Personalizar**: le permite seleccionar dispositivos, grupos de dispositivos, usuarios, grupos de usuarios
6. Después de distribuir la configuración, el usuario debe actualizar la versión del cliente de Go a 83 o superior. La pestaña de Apps\@Work ahora es visible en el cliente de Go app.La configuración no se puede enviar a los dispositivos que se han registrado mediante iReg porque el cliente de Go no está disponible en el dispositivo. Debe instalar el cliente de Go app para obtener el catálogo de aplicaciones nativas. Para obtener más información, consulte [**Registro de dispositivos (iOS, macOS y Android)**](./Registro_de_dispositivos__iOS__macOS_y_Android_.md).

## Eliminar webclip Apps\@Work de iOS

Para clientes que tienen Webclip de Apps\@Work distribuido en sus dispositivos y ya han migrado a la experiencia nativa da Apps\@Work, pueden eliminar webclip de Apps\@Work para iOS.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Filtrar la configuración: **Catálogo de aplicaciones de Apple**.
3. Haga clic en **Editar**.
4. Desde **Distribución** seleccione **Distribución a ningún dispositivo**.
5. Haga clic en **Guardar**.

## Android Apps\@Work

La tienda de aplicaciones nativas de Apps\@work se despliega automáticamente con el cliente de MI Go. No es necesaria ninguna acción del administrador. La pestaña Apps\@work se muestra en la barra de tareas del cliente de Mi Go. El usuario final puede acceder a esta pestaña para ver e instalar las aplicaciones aprobadas por la empresa. Para obtener más información, consulte [**Administrador- Android Enterprise**](./Administrador-_Android_Enterprise.md).

## macOS Apps\@Work

MacOs Apps\@work está integrado en el cliente de Mobile\@Work de macOS. Después de registrar el dispositivo en Ivanti Neurons for MDM. el cliente cambiará y se mostrará como Apps\@Work. Para nuevos abonados, la configuración de webclic del catálogo de aplicaciones de Apple no se enviará a dispositivos de macOS. En caso necesario, el administrador puede distribuir la configuración de webclip de Apps\@work en los dispositivos macOS. Para obtener más información, consulte [**Configuración de dispositivos macOS**](./Configuración_de_dispositivos_macOS.md).

### Distribución de aplicaciones para macOS

- Ivanti es compatible con la distribución de aplicaciones de macOS a través del protocolo de Apple MDM y usando la aplicación de Mobile\@Work. Los administradores pueden optar por utilizar uno o ambos de los siguientes enfoques:
  - Protocolo MSM de Apple: Los administradores pueden cargar únicamente formatos PKG específicos (formato de distribución) como aplicaciones internas y también pueden distribuir aplicaciones desde Mac App Store (se incluye el soporte para licencias de Apps and Books de Apple). Sin embargo, este enfoque no permite que los administradores distribuyan DMG y otros formatos PKG.
  - Aplicación Mobile\@Work para macOS: Como una manera de distribuir aplicaciones a los usuarios, los administradores pueden utilizar la aplicación MobileIron Packager (MIP) para convertir cualquier archivo PKG, DMG o .app a un archivo MIP. Cargue el archivo MIP en Ivanti Neurons for MDM como si se tratase de una aplicación interna
    Puede descargar la utilidad desde el [**sitio de descargas de software**](https://support.mobileiron.com/mi/mobileatwork-macos/current/).
- Los administradores pueden utilizar Mobile\@Work para distribuir aplicaciones internas que están en formato DMG, PKG o .app. Para las aplicaciones que solo están disponibles en Mac App Store, los administradores pueden continuar usando las prestaciones de MDM, que incluyen las prestaciones de las licencias de Apps and Books de Apple. Para obtener más información, consulte [**Configuración de dispositivos macOS**](./Configuración_de_dispositivos_macOS.md).

## Windows Apps\@Work

Apps\@Work es una aplicación nativa independiente que se puede descargar desde Microsoft Store o se puede enviar directamente desde Ivanti Neurons for MDM. Permite el uso de aplicaciones públicas e internas de Windows en dispositivos de Windows 10+ en Ivanti Neurons for MDM. Apps\@Work se instala en segundo plano en dispositivos compatibles de Windows 10+.

Para obtener más información, consulte [**Configuración de aplicaciones**](./Configuración_de_aplicaciones.md).

### Uso de Windows Apps\@Work

Apps\@Work permite el uso de aplicaciones públicas e internas de Windows en dispositivos de Windows 10 en Ivanti Neurons for MDM. Apps\@Work se instala en segundo plano en dispositivos compatibles de Windows 10.

**Certificado de autenticación de Apps\@Work**

Para usar la Autenticación de certificados con Windows Apps\@Work:

1. Vaya a **Administrador**\*\*>**Windows**>\*\***Certificado de autenticación de Apps\@Work**.
2. Ajustar como **OCTIVADO**.
   Si se ajusta como **DESACTIVADO**, se fuerza el uso del nombre de usuario y la contraseña.

SAML no es compatible con Apps\@Work para Windows.

Para configurar una aplicación para Apps\@Work:

1. Seleccione una aplicación de Windows.
2. Haga clic en la pestaña **Configuración de la aplicación**.
3. Haga clic en **Instalar en el dispositivo**.La configuración de aplicaciones Windows internas se puede establecer en la marca de instalación silenciosa o instalarse usando Apps\@Work. Las aplicaciones públicas no se pueden establecer en una instalación silenciosa.
4. Opcionalmente, también puede decidir si mostrar u ocultar aplicaciones en el catálogo de [**Apps@Work.Esta**](mailto\:Apps@Work.Esta) opción se aplica solo a las aplicaciones internas.
5. Haga clic en la pestaña **Promoción**.Actualmente Apps\@Work no es compatible con la promoción de banners, así que las opciones disponibles son **Destacado** y **No destacado**.para las aplicaciones públicas, solo aparece la opción **Promoción**.
