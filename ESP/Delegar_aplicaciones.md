---
title: Delegar aplicaciones
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

La delegación de aplicaciones permite a un administrador global dividir y administrar independientemente aplicaciones en Ivanti Neurons for MDM. El administrador global puede obtener y distribuir de manera centralizada las aplicaciones públicas e internas a la vez que mantiene la separación y el control proporcionado por los espacios delegados.

Al distribuir de manera central una aplicación, el administrador global puede predefinir el comportamiento de la administración de la aplicación por medio de configuraciones de las aplicaciones, así como mediante las reglas de distribución de las aplicaciones. La aplicación puede delegarse y ponerse disponible en el App Catalog del espacio delegado.

De esta forma, la aplicación delegada se distribuye a los usuarios con dispositivos en un espacio delegado determinado. Cuando se delegan las aplicaciones, el acceso a estas puede asignarse a un subconjunto de administradores delegados, con lo que se distribuyen las responsabilidades de los administradores.

La delegación de una aplicación requiere que se definan, en primer lugar, uno o más espacios delegados. Cuando una aplicación se delega, se asignará a todos los espacios. El espacio de delegación de aplicaciones se clasifica en:

- Espacio predeterminado
- Espacios delegados

## Añadir una aplicación a un espacio delegado

Las aplicaciones pueden ser añadidas a un espacio delegado por un administrador delegado o global. La aplicación aparecerá solo en el App Catalog de los espacios delegados a los que se haya añadido. Si añade una aplicación previamente delegada desde el espacio predeterminado a un espacio delegado, esto generará un error. En este caso, la herencia de la aplicación deberá desactivarse primero en el espacio predeterminado para que pueda añadirse a un espacio delegado. Para obtener más información, consulte **Añadir una configuración** en [**Trabajar con configuraciones**](./Trabajar_con_configuraciones.md).

## Distribución de la aplicación en un espacio delegado

Cuando se delega una aplicación desde el espacio predeterminado, se heredan sus reglas de distribución. Esta aplicación se distribuirá a todos los dispositivos asignados al espacio delegado que cumplan las reglas de distribución de la aplicación.

Los administradores globales pueden delegar en los administradores de espacio la edición del Certificado de identidad generado dinámicamente para todos los dispositivos y para la opción de distribución personalizada.

Los cambios en la distribución son aplicables sólo al espacio específico. Todos los demás espacios siguen heredando la configuración de distribución espacial predeterminada.

Ajustes de aprobación de aplicaciones para aplicaciones Android: no se admite la configuración de aprobación de aplicaciones por espacio para aplicaciones de Android. Las aplicaciones aprobadas en el espacio personalizado surten efecto en todos los espacios.

Aplicaciones de catálogo Android existentes: en los abonados en los que ya se han añadido aplicaciones públicas de Android en el espacio predeterminado, las aplicaciones deben anularse para que esa aplicación pública pueda añadirse en otro espacio no predeterminado.
