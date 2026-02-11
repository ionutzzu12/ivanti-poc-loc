---
title: Active Directory (macOS)
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** macOS 10.9 o versiones más recientes compatibles.

Configure opciones avanzadas para enlazar los dispositivos macOS con un dominio de Active Directory (AD) a fin de que puedan acceder a los servicios de software que dependen de Active Directory para la autenticación y seguridad.

Esta sección contiene los siguientes temas:

- [**Creación de una configuración de Active Directory**](./Active_Directory__macOS_.md)
- [**Ajustes de Active Directory**](./Active_Directory__macOS_.md)

## Creación de una configuración de Active Directory

Procedimiento

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **privacidad** en el campo de búsqueda y, a continuación, haga clic en la configuración de **Active Directory**
4. Asigne un nombre a la configuración y descríbala.
5. Introduzca los ajustes tal y como se describe en la siguiente tabla de ajustes de Active Directory.
6. Haga clic en **Siguiente** para configurar los ajustes de distribución.
7. Haga clic en **Hecho**.

## Ajustes de Active Directory

| **Ajuste**                          | **Qué hacer**                                                                                                  |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| Ajustes de Active Directory: Básico |                                                                                                                |
| Nombre de host                      | (Obligatorio) Introduzca el nombre de host, que es el dominio de Active Directory al que desea unirse.         |
| Nombre de usuario                   | Introduzca el nombre de usuario de la cuenta utilizada para unirse al dominio.                                 |
| Contraseña                          | Introduzca la contraseña de la cuenta utilizada para unirse al dominio.                                        |
| Unidad organizativa de AD           | Introduzca la unidad organizativa (UO) donde se va a añadir el objeto de equipo que se une.                    |
| Estilo de montaje de AD             | Seleccione una de las siguientes opciones para indicar el protocolo de red doméstica que desea utilizar:\* AFP |

- SMB                                                                                         |
  \| Ajustes de Active Directory: Avanzado                                            |                                                                                                                                                                                                             |
  \| Activar la clave ADCreateMobileAccountAtLogin                                    | Activa o desactiva la clave ADCreateMobileAccountAtLogin.Opción adicional: Crear una cuenta móvil al iniciar sesión.                                                                                        |
  \| Activar la clave ADWarnUserBeforeCreatingMA                                      | Activa o desactiva la clave ADWarnUserBeforeCreatingMA.Opción adicional: Avisar al usuario antes de crear una cuenta móvil.                                                                                 |
  \| Activar la clave ADForceHomeLocal                                                | Activa o desactiva la clave ADForceHomeLocal.Opción adicional: Forzar el directorio principal local.                                                                                                        |
  \| Activar la clave ADUseWindowsUNCPath                                             | Activa o desactiva la clave ADUseWindowsUNCPath.Opción adicional: Usar la ruta de acceso UNC en AD para derivar la ubicación principal.                                                                     |
  \| Activar la clave ADAllowMultiDomainAuth                                          | Activa o desactiva la clave ADAllowMultiDomainAuth.Opción adicional: Permitir la autenticación desde cualquier dominio del bosque.                                                                          |
  \| Shell de usuario predeterminado                                                  | Introduzca el shell de usuario predeterminado, como /bin/bash.                                                                                                                                              |
  \| Asignar UID de usuario al atributo                                               | Seleccione esta opción para asignar el UID de usuario al atributo especificado.                                                                                                                             |
  \| Asignar GID de usuario al atributo                                               | Seleccione esta opción para asignar el GID de usuario al atributo especificado.                                                                                                                             |
  \| Asignar GID de grupo al atributo                                                 | Seleccione esta opción para asignar el GID de grupo al atributo especificado.                                                                                                                               |
  \| Servidor de dominio preferido                                                    | Seleccione este servidor de dominio como preferido.                                                                                                                                                         |
  \| Convención de espacio de nombres                                                 | Seleccione una de las siguientes convenciones de nombres de la cuenta de usuario:\* Dominio (predeterminado)
- Bosque                                                                                        |
  \| Firma de paquetes                                                                | Seleccione una de las siguientes opciones de firma de paquetes:\* Permitir (predeterminado)
- Desactivar
- Requerir                                                                                          |
  \| Cifrado de paquetes                                                              | Seleccione una de las siguientes opciones de cifrado de paquetes:\* Permitir (predeterminado)
- Desactivar
- Requerir
- SSL                                                                                  |
  \| Permitir la administración por parte de grupos especificados de Active Directory | Seleccione esta opción para permitir la administración por parte de grupos especificados de Active Directory.Haga clic en **Añadir** para añadir uno o más grupos.                                          |
  \| Restringir DNS dinámico                                                          | Seleccione esta opción para restringir las actualizaciones dinámicas de DNS a las interfaces especificadas (por ejemplo, en0, en1, etc.).Haga clic en **Añadir** para añadir uno o más nombres de interfaz. |
  \| Cambiar el intervalo de contraseñas                                              | Especifique la frecuencia (en días) con la que se requiere un cambio de la contraseña de la cuenta de confianza del equipo. El valor cero está desactivado.                                                 |
