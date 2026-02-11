---
title: Configuración de los ajustes de la extensión de Safari
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

Ivanti Neurons for MDM permite gestionar las Extensiones de Safari en dispositivos iOS y macOS supervisados. Los administradores pueden gestionar eficazmente las extensiones de Safari para la navegación estándar y privada.

Disponible para:

- iOS 18.0 supervisado hasta la versión más reciente compatible con Ivanti Neurons for MDM.
- macOS 15.0 supervisado hasta la versión más reciente compatible con Ivanti Neurons for MDM.

**Procedimiento**

1. Vaya a **Configuraciones** > **+Añadir**.
2. Buscar y seleccionar la configuración de **Ajustes de extensión de Safari**.
3. Configure los ajustes de **Ajustes de extensión de Safari** según la tabla siguiente:| **Ajuste**                   | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
   \| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   \| Nombre                       | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
   \| Descripción                  | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
   \| ID de extensión              | Introduzca el identificador de extensión compuesto. Por ejemplo, "*Identificador (TeamIdentifier)*".Introduzca "\*" para todas las extensiones.Para generar esta cadena, utilice el signo de código *-dv \<path\_to\_appex>*. La extensión del navegador se encuentra en la carpeta plug-ins dentro del paquete de aplicaciones. El formato esperado es "*Identificador (TeamIdentifier)*". En el caso de las extensiones que no están disponibles en macOS, el desarrollador de la aplicación debe proporcionar esta información. |
   \| Estado de la extensión       | Seleccione una de las siguientes opciones:\* **Permitido**: el usuario puede activar o desactivar la extensión.
   - **Siempre activa**: la extensión está siempre "Activa" para el usuario.
   - **Siempre inactiva**: la extensión está siempre "Inactiva" para el usuario.                                                                                                                                                                                                                                                             |
     \| Estado de navegación privada | Seleccione una de las siguientes opciones:\* **Permitido**: el usuario puede activar o desactivar la extensión en la navegación privada.
   - **Siempre activa**: la extensión está siempre "Activa" para el usuario incluso durante la navegación privada.
   - **Siempre desactivada**: la extensión no estará disponible.                                                                                                                                                                                                              |
     \| Dominios permitidos          | Introduzca los valores de dominio o subdominio para dar acceso a la extensión Safari.Puede introducir múltiples valores de dominio o subdominio.La configuración del dominio permitido no se aplica en el dispositivo si introduce "\*" en el campo ID de extensión.                                                                                                                                                                                                                                                               |
     \| Dominios rechazados          | Introduzca los valores de dominio o subdominio para restringir el acceso a la extensión Safari.Puede introducir múltiples valores de dominio o subdominio.La configuración del dominio rechazado no se aplica en el dispositivo si introduce "\*" en el campo ID de extensión.                                                                                                                                                                                                                                                     |
4. Haga clic en **+Agregar** para agregar varias **Extensiones**.
5. Haga clic en **Siguiente** para configurar los ajustes de distribución.
6. Seleccione una de las opciones de distribución para configurar la configuración **Ajustes de extensión de Safari** . Para más información sobre la configuración de las opciones de distribución, consulte [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).
7. Haga clic en **Hecho**.
