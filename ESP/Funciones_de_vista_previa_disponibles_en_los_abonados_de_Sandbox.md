---
title: Funciones de vista previa disponibles en los abonados de Sandbox
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Esta sección enumera las funciones disponibles actualmente **SOLO** en la instancia sandbox de Ivanti Neurons for MDM. Las instancias sandbox de Ivanti Neurons for MDM están disponibles por defecto para los usuarios de Enterprise. Puede acceder a estas funciones desde la instancia sandbox de N-MDM y proporcionar cualquier comentario que tenga sobre las mismas.

Si necesita acceder a la instancia sandbox, póngase en contacto con [**Ivanti Sales**](https://www.ivanti.com/lp/contact-us).

## Versiones

Esta sección contiene las funciones exclusivas del entorno aislado para las siguientes versiones:

- [**Versión actual: R118**](./Funciones_de_vista_previa_disponibles_en_los_abonados_de_Sandbox.md)\* [**Atestación de Claves de Acceso de Apple**](./Funciones_de_vista_previa_disponibles_en_los_abonados_de_Sandbox.md)
  - [**Configuración de restricciones de Apple:**](./Funciones_de_vista_previa_disponibles_en_los_abonados_de_Sandbox.md)

## Versión actual: R118

### Atestación de Claves de Acceso de Apple

Utilice la configuración de Attestation de Passkey para configurar el dispositivo de manera que permita la atestación empresarial WebAuthn para ciertas claves de acceso.

Las claves de acceso se crean en dispositivos gestionados, y SecurityPasskeyAttestation utiliza una credencial gestionada por la empresa para atestiguar la clave de acceso con un certificado corporativo. Las credenciales admitidas incluyen SCEP, ACME y credenciales de identidad.

La atestación de clave de acceso admite lo siguiente:

- Versiones mínimas de sistemas operativos soportados: macOS 14
- Métodos de inscripción compatibles: inscripción de dispositivos
- Las cuentas de Apple administradas son necesarias para controlar la sincronización de claves de acceso.
- Se puede usar junto con Access Management de ABM.

La carga útil de la clave de acceso da error en Mac. Los activos del certificado no están alojados en un endpoint autenticado.

Al crear una configuración de clave de acceso, primero debe crear una configuración de certificado de identidad y vincularla a la configuración de clave de acceso. Además, proporcione los detalles siguientes en la sección Configuración de Security Passkey Attestation.

| **Campo**                                                                                | **Descripción**                                                                                                                                                                                    |
| ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre                                                                                   | Nombre de la clave de acceso.                                                                                                                                                                      |
| Descripción                                                                              | Cualquier información acerca de la configuración.                                                                                                                                                  |
| Referencia de identidad de atestación\* La clave de identidad de atestación es extraíble | Proporcione la referencia de identidad del activo que ha creado para vincularla a la Configuración de clave de acceso.Seleccione esta opción para confirmar si la clave de identidad es extraíble. |
| Partes dependientes                                                                      | Introduzca los detalles de los dominios autenticados.                                                                                                                                              |

### Configuración de restricciones de Apple:

**Mejora en la configuración de restricciones**: La interfaz de usuario de la página de **Configuración de restricciones** tiene un aspecto renovado para las **Configuraciones de restricciones de Apple**, con los cambios siguientes:

- Anteriormente, los administradores debían configurar las restricciones de iOS y macOS por separado. Ahora, los administradores pueden acceder a **Configuraciones** > **+Agregar** y seleccionar **Restricciones de Apple**. Además, ahora los administradores pueden seleccionar el **Tipo de plataforma** en la lista desplegable para agregarla a una nueva Restricción de Apple.
- El panel **Configuración de restricciones** ahora segrega múltiples configuraciones bajo pestañas relevantes, como **Funcionalidad del Dispositivo**, **Aplicaciones**, **Seguridad y Privacidad**, entre otras. Si Apple introduce una nueva restricción, esta se incorporará automáticamente en la pestaña correspondiente.
- El panel **Ajustes de restricciones** ahora permite a los administradores forzar los ajustes seleccionados a los dispositivos mediante el botón de alternancia de **Forzar al dispositivo**.
