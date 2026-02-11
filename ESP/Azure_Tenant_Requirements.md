---
title: Azure Tenant Requirements
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

En esta sección se describe cómo configurar Ivanti Neurons for MDM con Microsoft Azure Tenant.

## Requisitos

### Microsoft

Los clientes de Ivanti Neurons for MDM deben tener una suscripción válida a Microsoft Intune y asignar una licencia de Microsoft Intune a los usuarios de dispositivos.

### MobileIron

- Ivanti Neurons for MDM: Ivanti Neurons for MDM versión 75 hasta la última versión compatible con MobileIron.
- Licencias adicionales: el Cumplimiento de los dispositivos de Azure es una oferta Premium y está disponible para clientes de [**Secure UEM Premium**](https://www.mobileiron.com/en/pricing#) y Platinum. Una licencia Platinum es suficiente para los clientes existentes.
- Go para iOS (cliente) o Go para Android (cliente) versión 75.0 hasta la versión más reciente compatible con MobileIron.

### Compatibilidad con múltiples Ivanti Neurons for MDM

Si tiene varios Ivanti Neurons for MDM conectados al mismo arrendatario de Azure, desconéctese de todos los Ivanti Neurons for MDM o desactive la política de conformidad para la integración de conformidad de Entra ID desde un Ivanti Neurons for MDM específico (único) para que no cargue los datos del dispositivo en Azure.

Asegúrese de deshabilitar la política de cumplimiento antes de desconectar Ivanti Neurons for MDM.

## Proceso del administrador de Ivanti Neurons for MDM

El proceso desde la perspectiva del administrador de Ivanti Neurons for MDM es el siguiente:

1. El administrador aplica licencias de Intune a los usuarios de dispositivos. Consulte [**Aplicar la licencia de Intune a usuarios de dispositivos**](./Aplicar_la_licencia_de_Intune_a_usuarios_de_dispositivos.md).
2. El administrador inicia sesión en Azure Portal.
3. El administrador agrega MobileIron como socio de cumplimiento de Azure. Consulte [**Para añadir MobileIron como socio de cumplimiento**](./Para_añadir_MobileIron_como_socio_de_cumplimiento.md).
4. El administrador crea la directiva de Acceso condicional para las aplicaciones. Consulte [**Creación de una directiva de acceso condicional en Microsoft Endpoint Manager**](./Creación_de_una_directiva_de_acceso_condicional_en_Microsoft_Endpoint_Manager.md).
5. El administrador establece la conexión entre MobileIron y Azure. Consulte [**Conexión de Microsoft Azure con Ivanti Neurons for MDM**](./Conexión_de_Microsoft_Azure_con_Ivanti_Neurons_for_MDM.md).
6. El administrador crea la política de cumplimiento del dispositivo en Ivanti Neurons for MDM. Consulte [**Creación de una directiva de cumplimiento de los dispositivos de los socios**](./Creación_de_una_directiva_de_cumplimiento_de_los_dispositivos_de_los_socios.md).
7. La directiva de Acceso condicional entra en vigor. El acceso a las aplicaciones se concede o deniega en función de que el dispositivo sea o no compatible.Ivanti recomienda que el administrador ejecute pruebas en cada aplicación de Microsoft.
