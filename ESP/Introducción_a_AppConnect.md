---
title: Introducción a AppConnect
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

AppConnect es una función que coloca las aplicaciones en contenedores para proteger los datos en dispositivos iOS y Android. Cada aplicación compatible con AppConnect se convierte en un contenedor extraíble y seguro cuyos datos están cifrados y protegidos frente accesos no autorizados. Puesto que cada usuario emplea varias aplicaciones empresariales, cada contenedor está también conectado a contenedores de otras aplicaciones protegidas. Esta conexión permite a las aplicaciones compatibles con AppConnect compartir datos, como por ejemplo documentos. Ivanti Neurons for MDM emplea políticas para administrar las aplicaciones compatibles con AppConnect.

Para obtener más información acerca de AppConnect y cómo configurar e implementar aplicaciones de AppConnect, consulte la *Guía de AppConnect para Ivanti Neurons for MDM*.

## Estado de las aplicaciones seguras

En la página **Dispositivos > Dispositivos**, haga clic en un dispositivo para visualizar la págin&#x61;**&#x20;Información general**. En esta página, los usuarios pueden comprobar el estado de las aplicaciones seguras con la siguiente información:

- **Estado de las aplicaciones seguras** - indica si AppConnect está activado o desactivado.
- **Estado del cifrado de las aplicaciones seguras** - indica si el código de acceso de AppConnect está activado o desactivado.
- **Modo del cifrado de las aplicaciones seguras** - indica el modo del cifrado (como AES 256).

Además, estos campos se pueden usar:

- Como filtros (panel izquierdo) para limitar las entradas del dispositivo que se muestran cuando los usuarios están intentando encontrar/filtrar dispositivos.
- Como reglas cuando se crea un grupo de dispositivos administrados dinámicamente.
- Como filtros de distribución, que limitan los dispositivos donde se distribuirán las aplicaciones en función de las reglas definidas.

Para cada aplicación segura, los administrados pueden revisar la Política de contenedores y los estados de configuración (Instalado, Solicitado, Enviado o Pendiente de instalación) en la pestaña **Configuraciones** de la página de detalles del dispositivo.
