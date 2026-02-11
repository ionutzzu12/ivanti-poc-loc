---
title: Configuración del certificado
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

La configuración del certificado identifica el certificado que se va a distribuir a los dispositivos. Los certificados permiten a los dispositivos establecer confianza con los servidores y los recursos de red. A partir de la versión 76 solo admitimos certificados v3.

Como administrador, ahora puede generar certificados Ivanti Neurons for MDM para el inicio de sesión con tarjeta inteligente e Id. de objetos del cliente (OID). Puede generar certificados para las siguientes opciones de autenticación:

- Autenticación de cliente - habilitada de modo predeterminado.
- IPSEC - opcional, el administrador puede habilitarlo.
- Inicio de sesión con tarjeta inteligente - opcional, el administrador puede habilitarlo.
- OID personalizados: opcional, el administrador puede habilitarlos.

Esta función es aplicable solo para las siguientes entidades de certificación:

- Entidad de Certificación local
- Entidad de certificación intermedia
- Entidad de certificación externa: configure las políticas de aplicación de la plantilla de CA en el servidor NDES para que admita IPSEC, Inicio de sesión con tarjeta inteligente y OID personalizados.
- Autoridad de certificación SCEP local

## Distribución de la configuración

A partir de la versión 91 de Ivanti Neurons for MDM, los administradores globales pueden delegar en los administradores de espacio la edición de la Configuración de certificados para todos los dispositivos y para la opción de distribución personalizada. Para los certificados generados dinámicamente, puede seleccionar opcionalmente la opción Permitir que esta configuración esté disponible en todos los espacios. Esta opción hace que la configuración de los certificados estén disponibles en todos los espacios y puedan utilizarse en Exchange, Wi-Fi, VPN, VPN por aplicación y cualquier otra configuración aplicable. Esta opción se puede usar en situaciones en las que solo es necesario configurar el certificado para distribuirlo en los dispositivos (en espacios no predeterminados) como parte de configuraciones asociadas y no como configuración individual.

Procedimiento

1. Introduzca un nombre en el campo Nombre.
2. Cargar el archivo del certificado.
3. Haga clic en **Siguiente**.
4. Seleccione la opción **Habilitar esta configuración**.
5. Seleccione una de las siguientes opciones de distribución:\* **Todos los dispositivos**. Seleccione una de las siguientes opciones:- **No aplicar a los otros espacios**.
   - **Aplicar a todos los dispositivos de otros espacios**.\* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores delegados del espacio editen la distribución para el espacio específico.
   - **Ningún dispositivo** (predeterminada)
   - **Personalizar**Seleccione una de las siguientes opciones:\* **No aplicar a los otros espacios**.
     - **Aplicar a todos los dispositivos de otros espacios**.\* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores delegados del espacio editen la distribución para el espacio específico.Independientemente de los espacios, la configuración del certificado puede configurarse en todos los espacios, distribuirse a todos los dispositivos y aplicarse a todos los dispositivos en otros espacios de dispositivos.
6. Haga clic en **Hecho**.

## Ajustes del certificado

Como administrador, puede configurar una autoridad de certificación local que no sea SCEP.

**Procedimiento**

1. Inicie sesión en el portal del administrador de Ivanti Neurons for MDM
2. Vaya a **Admin** > **Infraestructura** > **Gestión de certificados** > **Entidad de certificación**.
3. Haga clic en **+Añadir**. Las siguiente opciones están disponibles:\* **Crear la entidad de certificación local proporcionada por Ivanti Neurons for MDM**.
   - **Conecte el CA local de Ivanti Neurons for MDM con su CA existente**.
   - **Conectar con una autoridad de certificados de Cloud de confianza pública**.
   - **Conectar una autoridad de certificación SCEP local**.
   - **Conectar una autoridad de certificación distinta a SCEP local**.
4. Complete los siguientes campos según corresponda:

| **Ajuste**                    | Qué hacer                                                                 |
| ----------------------------- | ------------------------------------------------------------------------- |
| Nombre                        | Introduzca un nombre que identifique a esta configuración.                |
| URL                           | URL de la CA de OpenTrust que el administrador debe obtener de OpenTrust. |
| Contraseña                    | Introduzca la contraseña del certificado de autenticación                 |
| Certificado de autenticación  | Acepta el formato de archivo .p12 proporcionado por OpenTrust/ IDnomic.   |
| Cadena de certificados TLS CA | Acepta el formato de archivo PEM proporcionado por OpenTrust/ IDonomic.   |
| Haga clic en **Hecho**.       |                                                                           |

Después de configurar la autoridad de certificación no SCEP local, debe crear el certificado de identidad. Basándose en el ID del perfil, rellene todos los campos obligatorios para completar la configuración.

Se genera una notificación cuando falla la generación de Certificados CA SCEP debido a los siguientes dos motivos y se supera el tiempo de espera de la Fase 2:

1. No es posible alcanzar el conector
2. No es posible alcanzar el servidor de CA
