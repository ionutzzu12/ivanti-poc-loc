---
title: Administración de aplicaciones de Windows
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Los usuarios pueden (Importar, configurar, programar, distribuir, actualizar y eliminar) el ciclo de vida completo de la aplicaciones de Windows. Los procesos de distribución y actualización de aplicaciones son compatibles a través de la consola MDM. Para obtener más información sobre cómo administrar aplicaciones de Windows y otras aplicaciones, consulte [**Configuración de aplicaciones**](./Configuración_de_aplicaciones.md), [**Datos sobre aplicaciones**](./Datos_sobre_aplicaciones.md) y [**Catálogo de aplicaciones**](./Catálogo_de_aplicaciones.md).

### Tipos de aplicaciones compatibles

- In-house (Compruebe las opciones en **Agregar una aplicación interna** de la sección [**Catálogo de aplicaciones**](./Catálogo_de_aplicaciones.md))
- MSB (Integración con Microsoft Store for Business)
- El almacenamiento público (a través de la integración nativa con Microsoft Store) de la región de Microsoft Store se puede ajustar en Aplicaciones > Ajustes del catálogo. Para obtener más información, consulte **Agregar una aplicación desde un almacén público** de la sección [**Catálogo de aplicaciones**](./Catálogo_de_aplicaciones.md).

### Extensiones de aplicaciones compatibles

- MSI
- MSIX
- APPX
- Agrupaciones de APPX
- EXE (a través de [**Ivanti Bridge**](./Ivanti_Bridge.md))

### Control de aplicaciones

La configuración de Control de aplicaciones controla la instalación de aplicaciones por dispositivo. Para obtener más información, consulte [**Configuración del control de aplicaciones: controle qué aplicaciones pueden instalarse en cada dispositivo**](./Configuración_del_control_de_aplicaciones__controle_qué_aplicaciones_pueden_instalarse_en_cada_dispositivo.md).

### Paquetes y dependencias

Las siguientes funciones están disponibles: 

1. Las aplicaciones de Windows se puede establecer como requisitos previos para todos los tipos de aplicaciones. Para obtener información sobre cómo configurar los requisitos previos de las aplicaciones, consulte [**Instalar dependencias de aplicaciones**](./Instalar_dependencias_de_aplicaciones.md).
2. Los grupos APPX y APPX Dependencias de aplicaciones y Otras dependencias de paquetes. En la página [**Ver Detalles de la aplicación**](./Ver_Detalles_de_la_aplicación-.md), revise la sección **Dependencias de la aplicación y otros paquetes** .
3. Las aplicaciones de Win32 son compatibles con el código de producto correcto (MSI) y líneas de comandos y variables. [**Aquí**](https://learn.microsoft.com/en-us/windows/win32/msi/command-line-options) se puede encontrar una lista de opciones de línea de comandos comunes.

### Secuencias de comandos

Las secuencias de comandos son compatibles a través del cliente de Ivanti Bridge. Para obtener más información sobre cómo configurar las Secuencias de comandos, consulte el [**Ivanti Bridge**](./Ivanti_Bridge.md)

Después de instalar Ivanti Bridge en los dispositivos, las secuencias de comandos se pueden distribuir de la siguiente manera:

- En el nivel de dispositivo con las secuencias de comandos y las acciones a través de la Acción de Ivanti Bridge
- A través de la configuración de Ivanti Bridge (vaya a Configuraciones > Bridge)

### Secuencias de comandos y archivos previos a la instalación o posteriores

**Para archivos .exe y .MSI**

Puede configurar las secuencias de comandos de instalación tras PowerShell, secuencias de comandos de registro y archivos ejecutables de Windows (.exe) y descargar otros tipos de archivos para aplicaciones de Windows en el nivel de Detalles de aplicaciones.

Cuando se agrega un nuevo script o archivo anterior o posterior a la instalación, aparece la pantalla de Ivanti Bridge. Puede adjuntar el script o el archivo, agregar el argumento del script, además de proporcionar una ubicación de destino para los archivos. El script de preinstalación se debe ejecutar de manera correcta en el dispositivo antes de enviar el comando de instalación de la aplicación al dispositivo. Los scripts de pre y postinstalación y los archivos se ejecutarán/instalarán en el mismo orden en que se cargaron en la consola. Si falla la descarga o la instalación del script de preinstalación, no se puede continuar con la instalación de la aplicación.

Si falla el script tras la instalación, puede ver los errores en la página de Detalles del dispositivo, en la sección Registros del dispositivo. Además, no puede revertir los scripts/archivos descargados y ejecutables instalados antes de la instalación, en caso de que fallen las acciones después de la instalación.

Puede reordenar los scripts y archivos de preinstalación o postinstalación utilizando la opción Priorizar scripts y archivos. Esta opción solo estará disponible si hay al menos dos o más scripts o archivos disponibles. Con esta opción, puede arrastrar y soltar los archivos o scripts dentro de sus respectivas secciones previas o posteriores, y no de una sección a otra.

### Comportamiento de instalación y configuraciones

Las aplicaciones de Windows son compatibles con la siguientes funciones:

- Instalaciones silenciosas
- [**Programación de aplicaciones Windows**](./Programación_de_aplicaciones_Windows.md)
- Opciones de reinicio

Para obtener más información sobre las opciones de comportamientos de instalación, consulte [**Configuración de aplicaciones**](./Configuración_de_aplicaciones.md)

Las aplicaciones MSI y EXE (instaladas mediante Bridge) admiten instalaciones con sesiones MDM sin usuario.

Por ejemplo, en los siguientes casos:

- El dispositivo se reinició y aun no ha iniciado sesión ningún usuario
- El usuario que ha cerrado sesión de Windows
- El dispositivo se inscribió en modo Autopilot sin usuario (Implementación y aprovisionamiento automático)
- Las aplicaciones se instalan a nivel de dispositivo

Permite la instalación de aplicaciones de MSI de maneras más eficientes, por ejemplo, durante la inscripción en Autopilot o por la noche, cuando nadie está trabajando en el dispositivo Windows. Cuando se usa un reembalaje sencillo para EXE en MSI, se puede instalar, pero no se puede actualizar ni eliminar. El paquete MSI real tiene una conexión con CSP. Se instalarán otros tipos de aplicaciones después de que el usuario inicie sesión.

### Tunnel for Windows (por VPN de aplicación)

Tunnel es una aplicación nativa y autónoma de Windows. Actualmente está disponible en Microsoft Store para distribución a dispositivos. Crea una configuración de VPN por aplicación. Es necesario desplegar Sentry. Para configurar la aplicación de Tunnel, vaya a **Configuraciones** > **+Agregar** > Buscar Tunnel (seleccione las Configuraciones que sean compatibles con los dispositivos Windows). Seleccione el perfil Sentry y configure los ajustes para comenzar a usar el protocolo de túnel en los datos de la aplicación mediante Sentry. Para establecer un servidor de Sentry, vaya a **Admin** > **Infraestructura** > **Sentry**.

### Inventario de aplicaciones

El Inventario de aplicaciones y software instalado en la flota de dispositivos Windows se puede monitorizar en dos niveles:

- Para comprobar las aplicaciones instaladas en todos los dispositivos, vaya a **Dispositivos** > **Inventario de aplicaciones**
- Para comprobar el inventario a nivel de dispositivo, vaya a Dispositivos > seleccione un dispositivo > haga clic en Aplicaciones instaladas

Los administradores pueden establecer los intervalos de recopilación del inventario de aplicaciones de Windows. Vaya a Administrador > Windows > Intervalos del inventario de aplicaciones Los intervalos se usan cuando la política de privacidad se ha ajustado para que se obtengan todas las aplicaciones del dispositivo. Para configurar la Configuración de privacidad, vaya a Configuraciones > +Agregar > busque Privacidad > Seleccione Recopilar el inventario de todas las aplicaciones del dispositivo. Seleccione los tipos de aplicaciones que desee recopilar.

### Catálogo de aplicaciones corporativas (Apps\@Work)
