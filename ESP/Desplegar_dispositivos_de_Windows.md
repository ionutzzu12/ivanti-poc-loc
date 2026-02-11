---
title: Desplegar dispositivos de Windows
createdAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:04 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Información general**](./Desplegar_dispositivos_de_Windows.md)
- [**Administración de dispositivos**](./Desplegar_dispositivos_de_Windows.md)
- [**Inscripción y registro de dispositivos Windows**](./Desplegar_dispositivos_de_Windows.md)
- [**Administración de actualización de Windows**](./Desplegar_dispositivos_de_Windows.md)
- [**Distribución y administración de aplicaciones**](./Desplegar_dispositivos_de_Windows.md)
- [**Control de aplicaciones**](./Desplegar_dispositivos_de_Windows.md)
- [**Configuración del administrador de dispositivos Windows**](./Desplegar_dispositivos_de_Windows.md)
- [**Conformidad de los dispositivos de Windows**](./Desplegar_dispositivos_de_Windows.md)
- [**Inventario de aplicaciones y hardware de Windows**](./Desplegar_dispositivos_de_Windows.md)

## Información general

Ivanti Neurons for MDM le ayuda a administrar todos los equipos portátiles y de escritorio de Windows, incluida la administración del ciclo de vida de los dispositivos HoloLens 2 end-end: desde configuración, inscripción, aprovisionamiento, seguridad, aplicación, administración, monitorización, actualización de software y SO, hasta la retirada.

## Administración de dispositivos

Dispositivos Windows compatibles:

- Windows PC 10+
- Microsoft HoleLens 2

Para obtener más información sobre las funciones de Administración de dispositivos y de informes, consulte [**Dispositivos**](./Dispositivos.md)

## Inscripción y registro de dispositivos Windows

Ivanti Neurons for MDM es compatible con todos los métodos de registro de dispositivos estándar para dispositivos de Windows:

- Registro manual
- Inscripción en masa
- a través de SCCM y de Ivanti EPM
- Windows Autopilot
- Registro Entra ID

Para obtener más información sobre métodos de registro, consulte [**Uso de Microsoft Azure**](./Uso_de_Microsoft_Azure.md)

Para obtener información sobre compatibilidad multiusuario, consulte [**Compatibilidad con varios usuario para dispositivos de Windows**](./Uso_de_Microsoft_Azure.md).

## Administración de actualización de Windows

- Configuración y programación de las actualizaciones de Windows: para configurar y programar las actualizaciones de Windows, cree una configuración mediante Configuración - [**Actualizaciones de software**](./Actualizaciones_de_software.md).
- Windows Update Management: puede ver y aprobar las actualizaciones notificadas por los dispositivos Windows que desee actualizar mediante Windows Update Management. Mediante esta característica, puede evitar que las actualizaciones innecesarias o no probadas se instalen en los dispositivos. Para obtener más información, consulte [**Administración de actualización de Windows**](Windows_Update_Management.htm).

## Distribución y administración de aplicaciones

Los usuarios pueden administrar ciclos de vida de aplicaciones completos (Importar, configuración, programar, distribución, actualizar y eliminación) de las aplicaciones de Windows.

Tipos de aplicaciones compatibles: 

- Interno
- MSB
- Almacenamiento público

Extensiones de aplicaciones compatibles:

- MSI
- MSIX
- APPX
- Agrupaciones de APPX
- EXE (Bridge)

Para obtener más información sobre cómo administrar las aplicaciones de Windows, consulte [**Configuración de aplicaciones**](./Configuración_de_aplicaciones.md). Para automatizar las actualizaciones de las aplicaciones, consulte [**Programación de aplicaciones Windows**](./Programación_de_aplicaciones_Windows.md) y [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).

## Control de aplicaciones

La configuración del control de aplicaciones le permite categorizar las aplicaciones como lista de permitidos o lista de bloqueados a nivel de dispositivo. Las aplicaciones que ya estén instaladas no serán visibles y no podrán iniciarse. Las aplicaciones seguirán siendo visibles en la App Store, pero no se podrán descargar ni iniciar. Cualquier dispositivo al que se distribuya esta configuración de Control de aplicaciones la empleará e ignorará cualquier otro ajuste de Políticas de aplicaciones permitidas. La configuración de control de aplicaciones sustituye a cualquier política relacionada con la aplicación que haga referencia a las mismas aplicaciones en los dispositivos de destino.

Para obtener más información, consulte [**Configuración del control de aplicaciones: controle qué aplicaciones pueden instalarse en cada dispositivo**](./Configuración_del_control_de_aplicaciones__controle_qué_aplicaciones_pueden_instalarse_en_cada_dispositivo.md).

## Configuración del administrador de dispositivos Windows

La compatibilidad para Windows 10+ PC y Microsoft HoloLens 2 incluye las capacidades siguientes:

- [**Registro de dispositivos (PC con Windows 10+ y Microsoft HoloLens 2)**](./Registro_de_dispositivos__PC_con_Windows_10__y_Microsoft_HoloLens_2_.md)
- [**Configuración del código de acceso**](./Configuración_del_código_de_acceso.md)
- [**Configuración de Exchange**](./Configuración_de_Exchange.md)
- [**Configuraciones**](./Configuraciones.md)
- [**Dispositivos**](./Dispositivos.md)
- [**Aplicaciones**](./Aplicaciones.md)
- [**Programación de aplicaciones Windows**](./Programación_de_aplicaciones_Windows.md)
- [**Configuración del control de aplicaciones: controle qué aplicaciones pueden instalarse en cada dispositivo**](./Configuración_del_control_de_aplicaciones__controle_qué_aplicaciones_pueden_instalarse_en_cada_dispositivo.md)
- [**Administración de actualización de Windows**](Windows_Update_Management.htm)
- [**Estado del dispositivo que notifica desde Ivanti Neurons for MDM a Azure**](./Estado_del_dispositivo_que_notifica_desde_Ivanti_Neurons_for_MDM_a_Azure.md)
- [**Configuración de los perfiles de Windows Autopilot**](./Configuración_de_los_perfiles_de_Windows_Autopilot.md)
- [**Insertar SyncML en dispositivos mediante la configuración personalizada**](./Insertar_SyncML_en_dispositivos_mediante_la_configuración_personalizada.md)
- [**Políticas**](./Políticas.md)
- Restricciones de Windows
- Certificados de identidad
- Windows Hello para empresas
- Perfiles de Wi-Fi y de VPN

Las configuraciones que se han distribuido a los dispositivos de HoloLens que no son compatibles con este tipo de dispositivo, no se notificarán como configuraciones distribuidas en la pestaña Configuración en los Detalles del dispositivo.

Funciones de Windows (compatible solo para PC de Windows):

- [**Ivanti Bridge**](./Ivanti_Bridge.md)
- [**Configuración del BIOS de Windows**](./Configuración_del_BIOS_de_Windows.md)
- [**BitLocker de Windows**](./BitLocker_de_Windows.md)
- [**Configuración del kiosco de Windows**](./Configuración_del_kiosco_de_Windows.md)
- [**Configuración de la licencia de Windows**](./Configuración_de_la_licencia_de_Windows.md)
- [**Configuración de la integración de servidores EMA**](./Configuración_de_la_integración_de_servidores_EMA.md)
- [**Ajustes de la impresora**](./Ajustes_de_la_impresora.md)
- [**Configuración para eliminar el «bloatware»**](./Configuración_para_eliminar_el_«bloatware».md)
- [**Explorador ADMX (GPO)**](./Explorador_ADMX__GPO_.md)

## Conformidad de los dispositivos de Windows

Ivanti Neurons for MDM se puede configurar con Microsoft Azure para una inscripción perfecta de los usuarios en sus dispositivos de escritorio de Windows y tabletas con Windows 10+. Para configurar la integración del abonado de Azure para habilitar el Cumplimiento de dispositivos, consulte [**Uso de Microsoft Azure**](./Uso_de_Microsoft_Azure.md).

## Inventario de aplicaciones y hardware de Windows

**Inventario de aplicaciones de Windows**

El Inventario de aplicaciones es una lista de aplicaciones detectadas en los dispositivos inscritos. Utilice esta página para obtener información sobre las aplicaciones que se están utilizando en los dispositivos inscritos. Para obtener más información, consulte [**Inventario de aplicaciones**](./Inventario_de_aplicaciones.md).

El inventario de aplicaciones muestra las aplicaciones Win32 o de Win32 Store en un dispositivo si la configuración de privacidad del mismo permite la recopilación de información para todas las aplicaciones del dispositivo.

**Configuración de los intervalos del inventario de aplicaciones**

Puede establecer intervalos de recopilación de inventario de aplicaciones de Windows 10 para varios inventarios de tipos de origen de aplicaciones. Los intervalos se usan cuando la política de privacidad se ha ajustado para que se obtengan todas las aplicaciones del dispositivo.

Para obtener más información, consulte [**Configuración de los intervalos del inventario de aplicaciones**](./Configuración_de_los_intervalos_del_inventario_de_aplicaciones.md).

**Inventario de hardware de Windows**
