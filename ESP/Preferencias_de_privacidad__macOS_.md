---
title: Preferencias de privacidad (macOS)
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** macOS 10.14 o versiones más recientes compatibles.

Configurar qué aplicaciones tienen permitido obtener acceso a los servicios, archivos y recursos del sistema. Esta configuración controla la configuración de un dispositivo macOS en Preferencias del sistema > Seguridad y privacidad > Privacidad.

## Creación de una configuración de preferencias de privacidad

Procedure

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **privacidad** en el campo de búsqueda y, a continuación, haga clic en la configuración de las **Preferencias de privacidad**.
4. Asigne un nombre a la configuración y descríbala.
5. Vaya a una de las aplicaciones enumeradas en la página. Consulte la [**documentación de Apple**](https://developer.apple.com/documentation/devicemanagement/privacypreferencespolicycontrol/services) para ver información relacionada.1) Para macOS 10.14+, las aplicaciones y los ajustes disponibles para la configuración incluyen:\* Accesibilidad: especifica las políticas para la aplicación a través del subsistema de accesibilidad.
   - Libreta de direcciones: especifica las políticas para la información de contacto administrada por Contacts.app.
   - Eventos de Apple: especifica las políticas para la aplicación que envía los AppleEvents restringidos a otro proceso.
   - Calendario: especifica las políticas para la información del calendario administrado por Calendar.app.
   - Cámara: una cámara del sistema. El acceso a la cámara no puede darse en un perfil; solo puede denegarse.
   - Micrófono: un micrófono del sistema. El acceso al micrófono no puede darse en un perfil; solo puede denegarse.
   - Fotos: las fotos gestionadas por la aplicación Fotos en \~/Pictures/.photoslibrary.
   - Publicar un evento: especifica las políticas para que la aplicación utilice las API de CoreGraphics para enviar CGEvents al flujo de eventos del sistema.
   - Recordatorios: especifica las políticas para la información de los recordatorios administrados por la aplicación Recordatorios.
   - Política del sistema (todos los archivos): permite el acceso de la aplicación a todos los archivos protegidos, incluidos los archivos de administración del sistema.
   - Política del sistema (archivos de administración): permite a la aplicación acceder a algunos archivos utilizados en la administración del sistema.

:::Paragraph{listStyleType="decimal" listStart="2" indent="2"}
Para macOS 10.15+, las aplicaciones y los ajustes disponibles para la configuración incluyen:\* Uso de archivos: permite que la aplicación del Proveedor de archivos sepa cuándo está usando el usuario los archivos administrados por el Proveedor de archivos.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Escuchar eventos de todos los procesos: permite a la aplicación utilizar las API de CoreGraphics y HID para escuchar (recibir) eventos CGEvents y HID de todos los procesos. El acceso a estos eventos no puede darse en un perfil; solo puede denegarse. Desmarque la opción Permitido.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Acceso a la biblioteca multimedia: permite a la aplicación acceder a Apple Music, a la actividad de música y vídeo y a la biblioteca multimedia.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Captura de pantalla de la visualización del sistema: permite a la aplicación capturar (leer) el contenido de la visualización del sistema. El acceso a los contenidos no puede darse en un perfil; solo puede denegarse. Desmarque la opción Permitido.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Reconocer y enviar datos de voz a Apple: permite a la aplicación utilizar el sistema de reconocimiento de voz y enviar datos de voz a Apple.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Acceder a los archivos de la carpeta Escritorio del usuario: permite a la aplicación acceder a los archivos de la carpeta del escritorio del usuario.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Acceder a los archivos de la carpeta Documentos del usuario: permite a la aplicación acceder a los archivos de la carpeta Documentos del usuario.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Acceder a los archivos de la carpeta Descargas del usuario: permite a la aplicación acceder a los archivos de la carpeta Descargas del usuario.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Acceder a los archivos de los volúmenes de la red: permite a la aplicación acceder a los archivos de los volúmenes de la red.
:::

:::Paragraph{listStyleType="disc" indent="3"}
Acceder a los archivos de los volúmenes extraíbles: permite a la aplicación acceder a los archivos de los volúmenes extraíbles.
:::

6. Para cada aplicación que quiera configurar, haga clic en **Acciones > Añadir**.
7. Introduzca los valores para las siguientes claves de identidad:\* Identificador: nombre de los ajustes. Por ejemplo: «us.zoom.ZoomPresence».
   - Tipo de identificador: seleccione entre ID de paquete o Ruta. Por ejemplo: «Id. del paquete»
   - Requisito de código: especifique el valor de ID de paquete o ruta. Por ejemplo: «identifier "us.zoom.ZoomPresence" and anchor apple generic».
   - Código estático (Verdadero o Falso)
   - Permitido (Verdadero o Falso)
   - Comentar
8. Haga clic en **Guardar**.
9. (Opcional) En cualquier aplicación, haga clic en **Acciones > Eliminar** para eliminar cualquier ajuste de preferencias de privacidad existente.
10. Haga clic en **Siguiente** para configurar los ajustes de distribución.
11. Haga clic en **Hecho**.
