---
title: Filtros de distribución
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Configurar los filtros de distribución**](./Filtros_de_distribución.md)
- [**Configurar los filtros de distribución para el administrador delegado**](./Filtros_de_distribución.md)

Utilice filtros de distribución para limitar las aplicaciones disponibles para instalar. Los filtros de distribución le permiten visualizar solamente las aplicaciones del catálogo de aplicaciones que sean aplicables al dispositivo.

**Licencia**: Silver

Estos son los filtros que están disponibles de forma predeterminada:

- **Aplicaciones compatibles con la versión corporativa de Android**: limita la distribución de aplicaciones únicamente a los dispositivos compatibles con la versión corporativa de Android.
- **Aplicaciones solo para iPad**: limita la distribución de aplicaciones solamente a dispositivos iPad.
- **Aplicaciones solo para iPhone**: limita la distribución de aplicaciones solamente a dispositivos iPhone.

## Configurar los filtros de distribución

1. Vaya a **Aplicaciones > Filtro de distribución**.Aquí aparecerán los filtros predeterminados de aplicaciones y cualquier filtro de aplicación que se haya creado.
2. Haga clic en **+Añadir** para acceder al diálogo **Crear filtro de distribución**.
3. Introduzca un nombre y una descripción en los campos adecuados.
4. Seleccione las definiciones de reglas. Estas reglas se pueden crear usando los operadores correspondientes, como «contiene», «es menor que», «es mayor que», «está en el intervalo de», «es igual a» y «no es igual a». Las reglas se pueden anidar juntas utilizando las opciones CUALQUIERA (O) o TODOS (Y). Los filtros de distribución de aplicaciones son los siguientes:\* Acceso bloqueado
   - Compatible con APNS
   - Dispositivo administrado de Android con perfil profesional
   - Android for Work habilitado
   - Dispositivos Android administrados en el trabajo (Propietario del dispositivo) habilitados
   - Perfil de trabajo de Android en el Dispositivo propiedad de la empresa habilitado
   - Último ingreso del cliente
   - Registrado con el cliente
   - Cumplimiento
   - Medida de cumplimiento bloqueada
   - Nombre del país actual
   - MMC actual
   - MNC actual
   - Atributo personalizado del dispositivo
   - Atributo personalizado de LDAP
   - Atributo personalizado del usuario
   - Atributos personalizados IDP
   - Tipo de dispositivo
   - Nombre del país de origen
   - MCC de origen
   - MNC de origen
   - IMEI
   - IMEI2 (solo en dispositivos Android con doble puerto SIM y aplicable para dispositivos Android 8.0 o superior)
   - Modo pantalla completa
   - Fabricante
   - Versión de SO
   - Propiedad
   - N.º de teléfono
   - Itinerancia
   - Estado de Secure Apps
   - Supervisado
   - Sentry bloqueado
   - Inscripción de usuarios inscritos
   - Inscrito en la Inscripción de dispositivos automatizada
5. Haga clic en **Crear filtro de distribución**.
6. Si fuera necesario, seleccione un filtro personalizado para actualizar.1) Haga clic en **Editar** para visualizar la página **Actualizar filtro de distribución**.
   2\) Introduzca un nombre y una descripción en los campos adecuados.
   3\) Utilice los menús desplegables para definir reglas para el filtro.
   4\) Haga clic en **Crear filtro de distribución**.
7. Seleccione una aplicación.
8. En la página Detalles de la aplicación, seleccione la pestaña **Distribución**.
9. Haga clic en **Editar**.
10. Elija una opción de distribución de aplicaciones:\* **A todo el mundo**
    - **A nadie**
    - **Personalizado**La sección de Filtro de distribución solo es visible si se selecciona **Todas las personas** o la opción de distribución **Personalizada**.
11. Elija una opción del filtro distribución:1) Introduzca un nombre de filtro en **Buscar los filtros de distribución existentes**... Para encontrar un filtro que ya se haya creado.
    2\) Haga clic en **+Añadir filtro de distribución** para añadir un filtro nuevo.

Los filtros de distribución se pueden crear o asignar a una aplicación antes de añadirla al catálogo. Los cambios realizados en los filtros de distribución afectarán a la distribución de las aplicaciones que estén usando dicho filtro (en todos los espacios).

Cuando se configura el filtro y si el **Permitir la instalación de aplicaciones en dispositivos M1 al momento de la distribución** está habilitado, el resultado llena los dispositivos macOS M1. La aplicación iOS VPP estará disponible para todos los dispositivos mac si **Permitir la instalación de aplicaciones en dispositivos M1 al momento de la distribución** está habilitado y el filtro de distribución está en **Todos** o **Personalizado**. Los filtros de distribución de atributos relacionados con macOS no son compatibles con las aplicaciones de iOS.

## Configurar los filtros de distribución para el administrador delegado

El administrador delegado puede administrar y editar los filtros creados que se añadieron a las aplicaciones individuales durante el proceso de distribución en el espacio delegado. No obstante, el administrador delegado no puede usar los filtros de distribución creados en un espacio predeterminado en cualquier otro espacio, pero sí puede usarlos para las aplicaciones delegadas.

El administrador delegado puede crear, administrar y editar filtros de distribución en espacios específicos a los que tengan acceso. El filtro de distribución está disponible solamente en el espacio en el que se creó. Los filtros de distribución de las aplicaciones no se pueden delegar.  

Cuando un administrador delegado con una función de administración de aplicaciones y del sistema añade una aplicación utilizando un filtro de distribución en un espacio delegado, podrá ver los detalles de aquellos dispositivos que estén en su espacio y de los dispositivos de otros espacios.

Los usuarios con funciones de Administración del sistema o Solo lectura del sistema no podrán crear, actualizar ni eliminar filtros de distribución en ningún espacio.

Es posible que el administrador delegado con función de administrador de aplicaciones y contenido no tenga acceso al filtro de distribución. Por eso, no podrá:

- Crear aplicaciones utilizando filtros de distribución. Esto ocurrirá cuando usted haya iniciado sesión como administrador delegado y añada una aplicación.
- El administrador delegado con función de solo lectura del sistema o superior sí podrá añadir aplicaciones con un filtro de distribución. El administrador delegado sin una función de administración del sistema podrá añadir aplicaciones sin un filtro de distribución.

El administrador delegado puede filtrar el estado de delegación en el App Catalog seleccionando las siguientes opciones:

- Delegada
- No delegada
