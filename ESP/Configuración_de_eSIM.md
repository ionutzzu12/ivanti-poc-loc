---
title: Configuración de eSIM
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

La configuración de la eSIM configura la red celular en los dispositivos con el comando RefreshCellularPlans. Los administradores deben obtener la URL del operador de la eSIM antes de asignar la red celular al dispositivo.

Aplicable a: iOS, iPadOS y Windows 11

Procedimiento para dispositivos iOS y iPadOS

1. Vaya a Configuraciones > **+Agregar.**
2. Escriba eSIM en el campo de búsqueda y, a continuación, haga clic en la configuración de eSIM.
3. Introduzca un Nombre y Descripción de la configuración.
4. Haga clic eniOS/iPadOS
5. Escriba la URL del Operador.
6. Haga clic en Siguiente.
7. Seleccione la opción Habilitar esta configuración.
8. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
   - Ningún dispositivo (predeterminada)
   - personalizada
9. Haga clic en Hecho.

Procedimiento para dispositivos Windows 11

1. Vaya a Configuraciones > **+Agregar.**
2. Escriba eSIM en el campo de búsqueda y, a continuación, haga clic en la configuración de eSIM.
3. Introduzca un Nombre y Descripción de la configuración.
4. En la sección Elegir SO, haga clic en Windows.
5. En la sección Configuración, escriba la URL del operador en el cuadro de texto Nombre del servidor (en formato FQDN).\* ¿Es un servidor de detección? Seleccione esta opción para marcar el servidor como detectable.
   - Habilitación automática: seleccione esta opción para habilitar el perfil en el dispositivo una vez descargado.
6. Haga clic en Siguiente.
7. Seleccione la opción Habilitar esta configuración.
8. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
   - Ningún dispositivo (predeterminada)
   - personalizada
9. Haga clic en Hecho.

Restablecer eSIM a estado de fábrica (solo para dispositivos Windows 11)

Esta opción está disponible en la sección Detalles del dispositivo de todos los dispositivos. Al hacer clic en esta opción se eliminan todos los perfiles eSIM descargados en el dispositivo.

**Notas importantes: Aplicable solo para la configuración de eSIM de Windows**

- Cuando se borra y vuelve a inscribir un dispositivo Ivanti Neurons for MDM , el registro antiguo de este dispositivo (con el estado como Borrado) se debe eliminar de la página Dispositivos para evitar problemas de aprovisionamiento con la configuración de eSIM en este dispositivo vuelto a inscribir.
- Al volver a enviar la misma configuración a un dispositivo que ya ha descargado los perfiles, no se pueden descargar nuevamente los perfiles. Si el administrador desea que el dispositivo descargue los perfiles nuevamente, primero restablezca el módulo eSIM al estado de fábrica y luego se recomienda enviar/reenviar la configuración de eSIM.
- Cuando se aprovisiona correctamente una configuración de eSIM en un dispositivo, antes de retirar el dispositivo, el administrador debe realizar la acción de borrado de eSIM para garantizar que los perfiles de eSIM descargados se borren del dispositivo.
- La eliminación de la configuración de eSIM solo eliminará la configuración del dispositivo. Si se detectaron, descargaron y activaron perfiles eSIM en el dispositivo, dichos dispositivos permanecerán activos hasta que se realice un borrado de eSIM.
- Al realizar una acción de borrado de eSIM se eliminan todos los perfiles de eSIM descargados del dispositivo. No obstante, la configuración de eSIM que está en estado Instalado permanece intacta en el dispositivo. Para eliminar la configuración del dispositivo, el administrador debe no distribuir la configuración ESIM.
