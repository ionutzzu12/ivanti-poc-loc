---
title: Preguntas más frecuentes
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

Esta sección lista algunas de las preguntas frecuentes más comunes que puede tener cuando utiliza dispositivos de ChromeOS en Ivanti Neurons for MDM.

- ¿En qué se diferencia la gestión de Chromebook con la de otros SO?
- A partir de ahora, Google solo permite la distribución de configuraciones basadas en grupo de usuarios de LDAP y el administrador debe asegurarse cuando trabaje con configuraciones o aplicaciones, que la distribución se basa en grupos de usuarios de LDAP. Los grupos de usuarios locales y los grupos de dispositivos no son compatibles con la gestión de dispositivos de ChromeOS.
  ¿Qué licencia necesito con Ivanti para administrar los dispositivos de ChromeOS?
- Los dispositivos de ChromeOS deben tener licencias como Chrome Enterprise Upgrade o Chrome Education Upgrade. Estos se puede obtener de vendedores, como parte del hardware o como licencias independientes. Consulte la documentación de Google para obtener más información. Para empezar a usar la gestión de dispositivos de Chrome, es necesaria una licencia de UEM (Gestión de puntos terminales unificados) segura con Ivanti.
  ¿Estará disponible la solución Mobile Threat Defense (MTD) o una similar? ¿Necesito una licencia distinta para MTD?
- Esto no está disponible actualmente en el producto. Consulte las limitaciones actuales. Proporcionaremos más información sobre los cambios en la funcionalidad a través de las Preguntas frecuentes y los anuncios de versiones.
  ¿Por qué la pestaña de configuraciones y aplicaciones no tiene detalles como en otros dispositivos?
- Pues que las configuraciones se distribuyen a los Grupos de usuarios y no se aplican según el usuario activo, actualmente, las configuraciones no se muestran en los detalles del dispositivo. Las aplicaciones siguen la misma lógica de distribución y tienen el mismo límite. Proporcionaremos más información sobre los cambios en estas limitaciones a través de las Preguntas frecuentes y los anuncios de versiones.
  ¿Cuántas configuraciones son compatibles actualmente con ChromeOS?
- Con ChromeOS, hemos reducido el número de iconos de configuración disponibles así como las tareas de administración asociadas con la configuración. Nos referimos a esta configuración como "ChromeOS Blueprint". ChromeOS Blueprint es compatible con unas 700 configuraciones en estos dispositivos. Consulte la documentación de Google para las opciones de configuración.
  ¿Con qué facilidad se gestiona una configuración para todos los dispositivos?
- Los administradores pueden sencillamente clonar una configuración existente y modificarla (en caso necesario) para sus grupos de usuarios respectivos. No necesita empezar de cero.
  ¿Cómo agregado la configuración VPN a los dispositivos de Chrome?
- Esto se puede hacer mediante las aplicaciones de Android, no utilizando la VPN nativa.
  ¿Las acciones de dispositivos como Retirar y Borrar funcionan en estos dispositivos?
- Chromebooks en Enterprise siempre se gestionan con una empresa y los datos de tales dispositivos se consideran totalmente empresariales. Teniendo esto en cuenta:
  - Retirar está bloqueado
  - Borrar está permitido
  - Se permite Bloquear
  - Se permite Desbloquear
  - Otras acciones: no son compatibles

:::Paragraph{indent="1"}
¿Qué Chromebooks, en términos de hardware son compatibles con Ivanti?
:::

- Se espera que los dispositivos compatibles con las soluciones de administración de dispositivos en la nube de Google sean compatibles con Ivanti. Ivanti actualmente no publica una lista de hardware específico compatible con la solución de Ivanti.
  ¿Qué versión de Chrome OS es compatible?
- Google Cloud solo es compatible con la versión estable más reciente de ChromeOS y la compatibilidad con Ivanti sigue el modelo compatible con Google debido a la naturaleza de las integraciones backend.
  ¿Puede listar los límites actuales, puesto que se trata del primer lanzamiento de esta función?

Con la nueva compatibilidad con Chrome OS, nos estamos esforzando por proporcionar funciones que nuestros clientes esperan con ganas. A continuación hay algunos límites que los administradores deben observar:

- Las extensiones de Chrome OS (aplicaciones del explorador) actualmente no son compatibles (como "aplicaciones") para su distribución.
- Configuración de aplicaciones administradas para aplicaciones de Android no es compatible en la actualidad.
- La API de configuración Wi-Fi se publicó recientemente y actualmente no es compatible.
- Actualmente no es compatible la distribución de certificados.
- Actualmente no hay compatibilidad para distribuir la aplicación de Android con Ivanti Go (antes conocido como MobileIron Go).
- La aplicación de Ivanti Tunnel (VPN) actualmente no es compatible.
- Spaces y la delegación de espacio actualmente no son compatibles.
- La solución de Mobile Threat Defense actualmente no es compatible.
- La solución Zero Sign-on de Ivanti es compatible en estos dispositivos, categorizada como dispositivos sin administrar.
- Las acciones de política no son totalmente compatibles.
