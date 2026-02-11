---
title: Configuración mejorada de segmentación de red 5G
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM proporciona una configuración de segmentación de red 5G mejorada para configurar segmentaciones de red 5G para Android, lo que permite a los operadores de redes móviles asignar segmentos de red 5G dedicados, o "segmentos", para agrupar diferentes aplicaciones con necesidades similares, como baja latencia o alto ancho de banda, en un segmento específico para una mejor optimización de los recursos de la red. Esto permite que los administradores de MDM y los proveedores de red administren las porciones directamente para lograr un mejor rendimiento de la aplicación.

## Características principales

1\. **Red dedicada**: en lugar de que todas las aplicaciones compartan una única porción de red, la segmentación de red permite que distintas aplicaciones utilicen su propia porción de red adaptada a sus requisitos específicos.

2\. **Personalización**: El administrador puede configurar cómo se asignan las aplicaciones a segmentos de red específicos según sus requisitos individuales; por ejemplo, garantizar una baja latencia para aplicaciones de comunicación en tiempo real o un alto ancho de banda para servicios de transmisión como YouTube. Una porción diseñada para juegos de alto rendimiento puede priorizar una baja latencia, mientras que una para transmisión multimedia estaría optimizada para un alto ancho de banda.

3\. **Participación del socio**: esta característica a menudo requiere la colaboración con proveedores de red, que definen estas porciones de red e informan a los administradores de MDM sobre la lista de porciones y su importancia.

## Creación de una configuración mejorada de segmentación de red 5G

### Procedimiento

1\. **Agregar configuración**

- Vaya a **Configuraciones >> +Agregar**. Se muestra la página **Agregar configuración**.
- Introduzca **Segmentación de red mejorada** en la barra de búsqueda para configurar Segmentación de red mejorada. Se muestra la página **Crear configuración de segmentación de red mejorada**.
- Haga clic en **+Agregar descripción** para introducir una descripción de la configuración.

2\. **Configurar la aplicación**

- En **Configuración >> Catálogo de aplicaciones**, introduzca el nombre de la aplicación deseada.
- Haga clic en **Agregar manualmente** si la aplicación no está disponible en Play Store o App Store.
- Introduzca **ID de paquete** y seleccione el **segmento de red** adecuado en el menú desplegable.
- Seleccione la porción deseada en el menú desplegable **Seleccionar porción**.
- Haga clic en **Agregar**. La aplicación ahora aparecerá en **Configurar segmentos de red** debajo del segmento de red seleccionado.
- Para eliminar una aplicación, haga clic en **Eliminar** en la sección **Configurar porción de red**.

3\. **Distribuir configuración**

- Haga clic en **Siguiente**, seleccione o desmarque la casilla de verificación "**Habilitar esta configuración**", elija una opción de distribución (Todos los dispositivos, Sin dispositivos o Personalizada),
- Haga clic en **Listo** para completar la configuración.

## Configuración mejorada de segmentación de red para Lockdown y Kiosko

La creación de una configuración de segmentación de red 5G mejorada le permite configurar dispositivos para que funcionen de manera restringida, lo que garantiza que los usuarios solo tengan acceso a aplicaciones y configuraciones específicas.

En los siguientes bloqueos, hay una casilla de verificación "**Habilitar segmentación de red 5G**":

- **Perfil de trabajo**: En los dispositivos propiedad de los empleados con un perfil de trabajo configurado con Android Enterprise versión 12.0, la casilla de verificación "Habilitar segmentación de red 5G" se puede encontrar en**Ajustes de configuración > Configuración de bloqueo del perfil de trabajo**.
- **Dispositivo administrado con perfil de trabajo/Perfil de trabajo en dispositivos propiedad de la empresa**: En Dispositivo administrado con perfil de trabajo/Perfil de trabajo en dispositivos propiedad de la empresa con versiones de Android 12.0 tenemos la casilla de verificación "Habilitar segmentación de red 5G".

Esta es una configuración heredada que permite que los dispositivos utilicen la segmentación de red 5G. Su correlación con la nueva configuración de Segmentación de red 5G mejorada es la siguiente:

Si se aplica alguno de los bloqueos anteriores a un dispositivo y la opción *Habilitar segmentación de red 5G***no** está seleccionada, la configuración *Segmentación de red 5G mejorada* fallará con un error.

### Ejemplos

- **Caso 1**: Si el bloqueo del dispositivo no se distribuye y la configuración de segmentación de red mejorada se distribuye, se activará la configuración mejorada.
- **Caso 2**: Si el bloqueo del dispositivo está distribuido pero la casilla de verificación 5G no está seleccionada (falso), la configuración de red 5G mejorada generará un error.
- **Caso 3**: Si se distribuye primero la segmentación de red mejorada, seguida del bloqueo del dispositivo con la casilla de verificación habilitada, la configuración de la segmentación de red mejorada seguirá funcionando. De lo contrario, se producirá un error.

## Detalles de configuración:

- Si el bloqueo del dispositivo se distribuye y se envía/distribuye la configuración de segmentación de red mejorada, los usuarios deben asegurarse de que la casilla de verificación Habilitar segmentación de red 5G esté habilitada para evitar errores.
- Si la casilla de verificación no está habilitada y se envía la configuración, se generará un error en el dispositivo.
