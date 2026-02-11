---
title: Móvil
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** iOS 7.0+ and watchOS 10.0+

Esta sección contiene los siguientes temas:

- [**Ajustes móviles para la APN predeterminada**](./Móvil.md)
- [**Ajustes móviles para APN de datos**](./Móvil.md)
- [**Controlar el acceso móvil durante la itinerancia**](./Móvil.md)
- [**Controlar el acceso móvil**](./Móvil.md)

La configuración móvil configura el perfil móvil para un dispositivo. Configure los ajustes de red móvil en dispositivos con iOS 7.0+ o watchOS 10.0+. Algunas empresas tienen contratos con sus operadores de telefonía móvil, que les otorgan acceso a un Nombre de punto de acceso (APN) exclusivo para acceder a la red remotamente o para planes de facturación especiales. Consulte con su operador de telefonía móvil para ver los parámetros de configuración.

- Los perfiles móviles solo se pueden instalar de uno en uno.
- No se puede instalar un perfil móvil si ya hay instalado un [**perfil APN**](./Configuración_de_APN.md).

Puede configurar los ajustes móviles para los siguientes tipos de APN desde el cuadro desplegable **Tipos de APN configurada**:

- APN predeterminada y de datos
- APN predeterminadas
- APN de datos

Para todas las configuraciones, introduzca un nombre que identifique la configuración y una descripción opcional.

## Ajustes móviles para la APN predeterminada

| **Ajustes de APN predeterminadas** | Qué hacer                                                                                                                                  |
| ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Nombre del APN                     | Introduzca en nombre para el punto de acceso correspondiente. Por lo general, el nombre lo define el operador que proporciona el servicio. |
| Tipo de autenticación APN          | (Opcional) Seleccione una de las siguientes opciones:\* CHAP (protocolo de autenticación por desafío mutuo)                                |

- PAP (protocolo de autenticación de contraseña) |
  \| Nombre de usuario                  | (Opcional) Introduzca un nombre de usuario que se utilizará para la autenticación.                                                                          |
  \| Contraseña                         | (Opcional) Introduzca una contraseña que se utilizará para la autenticación.                                                                                |

## Ajustes móviles para APN de datos

| **Ajustes de APN de datos** | Qué hacer                                                                                                                                  |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Nombre del APN              | Introduzca en nombre para el punto de acceso correspondiente. Por lo general, el nombre lo define el operador que proporciona el servicio. |
| Tipo de autenticación APN   | (Opcional) Seleccione una de las siguientes opciones:\* CHAP (protocolo de autenticación por desafío mutuo)                                |

- PAP (protocolo de autenticación de contraseña) |
  \| Nombre de usuario                                       | (Opcional) Introduzca un nombre de usuario que se utilizará para la autenticación.                                                                          |
  \| Contraseña                                              | (Opcional) Introduzca una contraseña que se utilizará para la autenticación.                                                                                |
  \| Servidor proxy                                          | Especifique el servidor proxy.                                                                                                                              |
  \| Puerto del servidor proxy                               | Especifique el puerto del servidor proxy.                                                                                                                   |
  \| 10.3+                                                   |                                                                                                                                                             |
  \| Máscara permitida del protocolo                         | Seleccione IPv4, IPv6 o ambos.                                                                                                                              |
  \| Máscara permitida del protocolo en itinerancia nacional | Seleccione IPv4, IPv6 o ambos.                                                                                                                              |
  \| Máscara permitida del protocolo en itinerancia          | Seleccione IPv4, IPv6 o ambos.                                                                                                                              |

## Controlar el acceso móvil durante la itinerancia

Se puede limitar el acceso de algunas o todas las aplicaciones administradas a los datos móviles mientras el dispositivo está en itinerancia.

**Procedimiento**

1. Vaya a la pestaña **Configuraciones** en el menú de navegación principal de Ivanti Neurons for MDM.
2. Haga clic en **+Añadir**.
3. Introduzca **Rojo** en el campo de búsqueda y luego haga clic en configuración de **Uso de la red**.
4. Seleccione la casilla **No permitir para todas las aplicaciones administradas** para bloquear que las aplicaciones administradas puedan acceder a los datos móviles durante la itinerancia o en todo momento.
5. Deje la casilla sin seleccionar para poder especificar las aplicaciones administradas por nombre o Id. de paquete que desea bloquear para que no reciban datos móviles.
6. Use los menús desplegables en el campo Aplicaciones para buscar una aplicación por su nombre o Id. de paquete.

## Controlar el acceso móvil

Se puede limitar el acceso de algunas o todas las aplicaciones administradas a los datos móviles en cualquier momento. Las aplicaciones se podrán seguir usando de forma limitada, pero no tendrán acceso a los datos móviles.

**Procedimiento**

1. Vaya a la pestaña **Configuraciones** en el menú de navegación principal de Ivanti Neurons for MDM.
2. Haga clic en **+Añadir**.
3. Introduzca **Rojo** en el campo de búsqueda y luego haga clic en configuración de **Uso de la red**.
4. Seleccione la casilla **No permitir para todas las aplicaciones administradas** para bloquear que las aplicaciones administradas puedan acceder a los datos móviles en cualquier momento.
5. Opcionalmente, también puede dejar la casilla sin seleccionar para poder especificar las aplicaciones administradas que desea bloquear para que no reciban datos móviles.
6. Use los menús desplegables en el campo Aplicaciones para buscar una aplicación por su nombre o Id. de paquete.
