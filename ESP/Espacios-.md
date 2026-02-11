---
title: Espacios
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

Licencia: Silver

Los espacios se emplean para aislar un sistema de administración unificada de puntos de conexión (UEM, Unified Endpoint Management) en entidades administradas de forma independiente para poder llevar a cabo una administración delegada. Los espacios pueden crearse para reflejar una jerarquía organizativa. Ivanti Neurons for MDM admite la delegación a nivel único con una entidad administrativa central definida como espacio predeterminado y una cantidad de entidades administrativas subordinadas denominadas espacios delegados. Todos los sistemas de UEM se crean con un espacio predeterminado.

La página Spaces y las opciones asociadas están ocultas para los abonados convergentes que tienen acceso a Ivanti Neurons for UEM y Ivanti Neurons for MDM.

Los espacios permiten la administración delegada de los siguientes componentes del sistema. Actualmente, los usuarios y los grupos de usuarios no pueden delegarse.

- Dispositivos
- Configuraciones
- Políticas
- Grupos de dispositivos
- Aplicaciones
- Un App Catalog
- Un token de Apps and Books de Apple

Cuando un administrador inicia sesión en el portal de administración de Ivanti Neurons for MDM en un abonado con al menos un único espacio delegado, al administrador se le presenta la ventana emergente de promoción para iniciar sesión en el portal de administrador. La ventana emergente de promoción no se mostrará tras la creación de un espacio delegado ni durante el inicio de sesión si ya se ha creado un espacio delegado.

## Funciones para administradores globales y de espacios delegados

Al usuario administrador con las funciones necesarias para acceder al espacio predeterminado se le denomina Administrador global. El acceso al espacio predeterminado puede ser de solo lectura o de lectura y escritura. El administrador global con las funciones administrativas necesarias puede crear espacios delegados y asignar administradores delegados para administrarlos. Puede asignarse un administrador delegado para administrar uno o más espacios delegados.

Los espacios a los que puede acceder un administrador en concreto se enumeran en el selector de espacios desplegable, situado en la esquina superior izquierda de las pestañas Dispositivos y Aplicaciones. Para ver y administrar un espacio, utilice el menú desplegable para cambiar al espacio deseado.

Un administrador global puede ver y controlar todos los espacios delegados, además del espacio predeterminado. Un administrador delegado puede ver y controlar solamente los espacios que le ha asignado el administrador global. Un administrador global posee el control central de los espacios delegados, mientras que un administrador delegado tiene la autonomía para administrar los espacios que se le han delegado. Este nivel de autonomía viene determinado en función de si la delegación se ha heredado o se ha copiado desde el espacio predeterminado.

A continuación se enumeran las diferentes funciones del usuario y las tareas que pueden realizar:

### Aplicación heredada en un espacio delegado

- Se heredan las puntuaciones u opiniones existentes en el momento de la delegación y son visibles para los usuarios del espacio delegado, incluido el nombre de usuario del autor.
- El administrador delegado no puede eliminar puntuaciones/opiniones de una aplicación heredada.
- El administrador delegado puede exportar puntuaciones/opiniones de una aplicación heredada.
- Los usuarios de los espacios delegados pueden añadir puntuaciones/opiniones a una aplicación heredada.
- Los usuarios de los espacios delegados pueden ver las puntuaciones/opiniones añadidas por usuarios en los espacios delegados, incluido el nombre de usuario del autor.

### Aplicación en un espacio delegado (añadido, no heredado)

- Solamente un administrador global puede activar o desactivar las opiniones en **Aplicaciones > Ajustes del catálogo > Puntuaciones y opiniones**.
- Los usuarios de un espacio delegado pueden añadir puntuaciones/opiniones.
- Un administrador delegado puede eliminar opiniones añadidas por usuarios en el mismo espacio delegado.
- Los usuarios de otros espacios delegados, incluido el predeterminado, no podrán ver las puntuaciones u opiniones añadidas por usuarios de todos los espacios delegados.
- El administrador delegado puede exportar las opiniones añadidas por todos los usuarios, incluidos los nombres de usuario.

### Aplicación delegada en un espacio predeterminado

- El administrador global puede eliminar las puntuaciones o revisiones añadidas por un usuario en un espacio delegado.
- El administrador global puede exportar todas las puntuaciones o revisiones, incluidas aquellas añadidas por usuarios en los espacios delegados.
- Los usuarios de un espacio predeterminado pueden ver las puntuaciones u opiniones añadidas por usuarios en los espacios delegados, incluido el nombre de usuario.

## Prioridad de un espacio delegado

El espacio predeterminado de un sistema de UEM tiene siempre el nivel más bajo de prioridad. El administrador global establece la prioridad de un espacio delegado relativo a otro espacio delegado. Esta prioridad puede cambiarse en cualquier momento. Los espacios delegados se enumeran por orden en niveles de mayor a menor prioridad en la página de espacios, situada en la pestaña Administrador del Portal de administración.

## Delegación mediante herencia o copia

Un concepto clave de la administración delegada es si un componente del sistema se ha heredado o copiado desde el espacio predeterminado.
