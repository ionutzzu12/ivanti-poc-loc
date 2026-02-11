---
title: Configurar el modo kiosco para Android
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Iniciar el modo kiosco de forma remota**](./Configurar_el_modo_kiosco_para_Android.md)
- [**Salir de modo kiosco**](./Configurar_el_modo_kiosco_para_Android.md)

Licencia: Silver

El modo kiosco para dispositivos Android le permite restringir el uso de un dispositivo a aplicaciones específicas. Puede utilizar el modo kiosco para configurar dispositivos para empleados que utilicen solo aplicaciones específicas para el trabajo.

Cuando prepare los dispositivos Android para el modo kiosco o el modo Propietario del dispositivo con el modo kiosco, tendrá que [**crear una lista de permitidos de aplicaciones**](./Configuración_del_control_de_aplicaciones__controle_qué_aplicaciones_pueden_instalarse_en_cada_dispositivo.md) que desee poner disponible para los usuarios en el Modo kiosco. Para dispositivos que empleen el modo Propietario del dispositivo, puede añadir aplicaciones a la lista de aplicaciones permitidas arratrándolas y soltándolas para ordenar las aplicaciones en el orden en que deben aparece en el selector del Modo kiosco cuando se configure la aplicación. Consulte [**Configuración de bloqueo y kiosco**](./Bloqueo_y_kiosco__modo_de_administrador_de_dispositivos_de_Android.md) para obtener más información.

**Requisitos previos**

Antes de configurar el modo kiosco para Android, asegúrese de haber realizado las siguientes tareas:

- Instalado Go en los dispositivos.
- Configurado el catálogo de la aplicación con las aplicaciones que la configuración del kiosco necesitará.
- Distribuido el catálogo de aplicaciones a los dispositivos que funcionarán en el modo kiosco.Los dispositivos SonimXP5S no son compatibles con el modo Kiosco.
- Instalado las aplicaciones que necesitará la configuración de su kiosco.
- (Opcional) Configurar [**Personalización de marca del kiosko de Android**](./Administrador___Personalización_de_marca_del_kiosko_de_Android.md).

El modo kiosko es compatible con Android 5.1 y 6.0. Los dispositivos que no sean Samsung Knox se deben colocar en modo Propietario del dispositivo para evitar el uso de aplicaciones no deseadas.

**Importante:** algunos dispositivos tienen funciones que pueden provocar que el dispositivo se salga de la pantalla o se cree un escape de cualquier otro tipo del modo kiosco. La función «People Edge» del Samsung Galaxy S6 Edge es un ejemplo de esta función. Recomendamos que un administrador desactive este tipo de funciones antes de implementar el dispositivo.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Haga clic en **Bloqueo y kiosco: modo de administrador de dispositivos de Android**.
4. En la pantalla **Crear ajustes**, complete al menos la sección **Ajustes del modo kiosco**.
5. En la pantalla **Distribución**, seleccione los grupos dispositivos que recibirán esta configuración.
6. Haga clic en **Hecho**.
7. Para dispositivos que no son Samsung, continúe con los siguientes pasos:1) Vaya a **Dispositivos&#x20;**>**Dispositivos**.
   2\) Seleccione los dispositivos que desea habilitar para el modo kiosco.
   3\) Seleccione **Acciones** > **Forzar ingreso**.
   4\) En los dispositivos, toque el botón **Modo Kiosco**.
   5\) Presione el botón **Inicio** en el dispositivo.
   6\) Si aparece el diálogo **Elegir selector**, pulse **Selector del kiosco Go** y seleccione **Siempre**. Este paso es necesario para garantizar que se utiliza el selector correcto para esta característica. De lo contrario, se pediría al usuario que seleccione un selector cualquiera.

## Iniciar el modo kiosco a distancia

**Procedimiento**

1. Vaya a **Dispositivos > Dispositivos**.
2. Añada la columna Modo kiosco a la pantalla.
3. Seleccione los dispositivos que tienen habilitado el modo kiosco, pero que no estén actualmente en modo kiosco.
4. Seleccione **Acciones > Entrar en modo kiosco**.

## Salir de modo kiosco

Puede salir del modo kiosco en el dispositivo si establece un código PIN en la configuración.

**Procedimiento**

1. Pulse el icono **Ajustes**.
2. Seleccione **Salir del modo kiosko**.
3. Pulse el campo **PIN del kiosco** cuando se le solicite.
4. Salga del PIN del kiosco.

Puede salir del modo kiosco en un dispositivo específico desde el portal:

**Procedimiento**

1. Vaya a **Dispositivos > Dispositivos**.
2. Muestre los detalles del dispositivo.
3. Seleccione **Acciones > Salir del modo kiosco**.

También puede utilizar los siguientes métodos para salir del modo kiosco:

- Eliminar la configuración
- Desactivar la configuración
- Quitar el grupo de dispositivos de la configuración
