---
title: Delegar dispositivos
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Los espacios se utilizan para separar sus dispositivos en partes que se controlan independientemente. La pertenencia a los espacios se determina a partir de las reglas que se creen. La delegación de dispositivos permite al administrador global hacer una partición y administrar de manera independiente los dispositivos de un sistema de UEM. Cuando se delegan los dispositivos, el acceso a estos puede asignarse a un subconjunto de administradores delegados, con lo que se distribuyen las responsabilidades de los administradores.

Los dispositivos delegados pueden agruparse en grupos de dispositivos y se les pueden aplicar diferentes configuraciones personalizadas aplicadas sin que esto afecte a los dispositivos del espacio predeterminado u otros espacios.

## Crear reglas para delegar dispositivos

Las reglas que se definen para un espacio determinan qué dispositivos pertenecen a dicho espacio. Un dispositivo solo puede pertenecer a un espacio. Los dispositivos que no cumplan las reglas de los espacios que usted cree, pertenecerán automáticamente al espacio predeterminado.

1. Seleccione **Cualquiera** si desea que los dispositivos se incluyan en esta definición si cumplen cualquiera de las reglas.
2. Seleccione **Todas** si desea que los dispositivos solamente se incluyan en esta definición si cumplen todas las reglas.
3. Seleccione uno de los siguientes tipos de reglas de la lista desplegable:\* **Atributo personalizado de LDAP:** para las reglas basadas en atributos LDAP.
   - **SO**: para las reglas basadas en el sistema operativo del dispositivo.
   - **Grupo de usuarios**: para las reglas basadas en el grupo de usuarios un dispositivo (según se define en el servicio de administración dispositivo).
   - **Nombre de usuario**: para las reglas basadas en el nombre de usuario asociado con el dispositivo.
4. Defina los criterios para el tipo de regla seleccionada:- **Atributo personalizado de LDAP:&#x20;**&#x69;ntroduzca el nombre del atributo LDAP personalizado que se configuró en los ajustes de LDAP.
   - **Sistema operativo**: seleccione Android, iOS, macOS o Windows.
   - **Grupo de usuarios**: seleccione uno de los grupos de usuarios mostrados en la lista desplegable. Estos son los grupos de usuarios definidos en **Usuarios > Grupos de usuarios**.\* **Nombre de usuario**: escriba un nombre de usuario.
5. Para añadir otra regla para este espacio, haga clic en + junto a la regla anterior.
6. Haga clic en **Vista previa** para ver qué dispositivos se asignarán al espacio.
7. Haga clic en **Guardar** cuando esté satisfecho con los dispositivos del espacio.

Los dispositivos que no cumplan las reglas de un espacio serán automáticamente movidos al siguiente espacio en el que sí encajen. Si el dispositivo no cumple las reglas de un espacio existente, se moverá al espacio predeterminado. Por ejemplo, al eliminar a un usuario de un grupo de usuarios puede provocar que los dispositivos de ese usuario se muevan a un espacio diferente. Los cambios a un espacio diferente pueden resultar en cambios en las políticas y las configuraciones.
