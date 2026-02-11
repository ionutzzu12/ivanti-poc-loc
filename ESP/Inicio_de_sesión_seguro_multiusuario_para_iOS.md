---
title: Inicio de sesión seguro multiusuario para iOS
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

El clip web multiusuario permite a los usuarios entrar y salir de los dispositivos iOS registrados en Ivanti Neurons for MDM. Cuando un usuario inicia sesión por primera vez, los perfiles, aplicaciones y configuraciones que están asociadas con ese usuario se insertarán en el dispositivo. Cuando haya terminado su trabajo, puede abrir el clip web y seleccionar la función «cerrar sesión», que asigna el dispositivo al usuario Nadie y elimina los perfiles, aplicaciones y configuraciones asociadas al usuario que inició sesión originalmente, siempre que las configuraciones y aplicaciones no se distribuyan al usuario Nadie. Después de cerrar sesión, el clip web se reinicia para que el siguiente usuario pueda iniciar sesión y recibir sus configuraciones, aplicaciones y políticas personalizadas. No es necesaria la supervisión del dispositivo para utilizar la función de inicio de sesión seguro multiusuario. Consulte el artículo de la base de conocimientos de la Asistencia técnica de [**Ivanti Neurons for MDM: inicio de sesión seguro multiusuario para iOS**](https://forums.ivanti.com/s/article/MobileIron-Cloud-Multi-user-secure-sign-in-for-iOS-5948), para ver más detalles sobre la función de inicio de sesión multiusuario.

**Aplicable a:** dispositivos iOS (no aplicable a los dispositivos con Inscripción de usuarios)

Esta sección contiene los siguientes temas:

- [**Credenciales admitidas**](./Inicio_de_sesión_seguro_multiusuario_para_iOS.md)
- [**Comprender el concepto de usuario «Nadie»**](./Inicio_de_sesión_seguro_multiusuario_para_iOS.md)
- [**Iniciar sesión en un dispositivo**](./Inicio_de_sesión_seguro_multiusuario_para_iOS.md)
- [**Cerrar sesión en un dispositivo**](./Inicio_de_sesión_seguro_multiusuario_para_iOS.md)

## Credenciales admitidas

Se deben usar el nombre de usuario y la contraseña para acceder al clip web seguro multiusuario. El registro basado en PIN no es compatible con el clip web seguro multiusuario.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuraciones**.
:::

:::WorkflowBlockItem
Haga clic en **Inicio de sesión seguro multiusuario para iOS**. Es posible que tenga que utilizar la función de búsqueda para encontrarla si hay varias páginas de configuraciones. No se accede a esta configuración seleccionando **+Añadir**.
:::

:::WorkflowBlockItem
Haga clic en **Editar distribución** o en el icono asociado para distribuir el clip web al Grupo de dispositivos apropiado.

::Image[]{src="Resources/Images/74EditDistribution.png" signedSrc="Resources/Images/74EditDistribution.png" size="25" caption alt isUploading="false" sha initialPath="Resources/Images/74EditDistribution.png" githubPath="Resources/Images/74EditDistribution.png" position="flex-start"}

Si desea distribuirlo a un Grupo de usuarios, puede crear un Grupo de dispositivos dinámico que esté vinculado a un Grupo de usuarios.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones de distribución, recordando que siempre debe distribuir el clip web al usuario Nadie o al grupo de dispositivos con el que el usuario Nadie está asociado. Esto no ocurre por defecto, así que asegúrese de distribuirlo al usuario Nadie.
:::

:::WorkflowBlockItem
- Todos los dispositivos
- Ningún dispositivo (predeterminada)
- Personalizada
  Haga clic en **Guardar**.
:::
::::

## Comprender el concepto *de usuario «Nadie»*

Cuando un dispositivo ha cerrado sesión a través del clip web, permanece inscrito en Ivanti Neurons for MDM con un usuario especial llamado el «usuario Nadie». Si desea eliminar aplicaciones y configuraciones del dispositivo cuando un usuario cierre la sesión, debe asegurarse de que esas aplicaciones y configuraciones no se distribuyan al usuario Nadie. Si desea que determinadas configuraciones, como la de Wi-Fi, permanezcan en el dispositivo cuando un usuario cierre la sesión del clip web de inicio de sesión seguro, debe asegurarse de que esas configuraciones también se distribuyan al usuario Nadie.

::Image[]{src="Resources/Images/74Nobody.png" signedSrc="Resources/Images/74Nobody.png" size="35" caption alt isUploading="false" sha initialPath="Resources/Images/74Nobody.png" githubPath="Resources/Images/74Nobody.png" position="flex-start"}

Esto significa que debe prestar atención a los Grupos de usuarios y Grupos de dispositivos a los que distribuye aplicaciones y configuraciones. Si está distribuyendo una aplicación a Todos y quiere que se elimine cuando un usuario cierre la sesión del dispositivo, entonces lo mejor es crear un Grupo de usuarios que no incluya al usuario Nadie. Los atributos personalizados facilitan la creación de un grupo de usuarios que sen «multiusuarios», y otro grupo de usuarios que consista solo en el usuario Nadie. Puede crear un atributo de usuario desde Administrador > Sistema > Atributos llamado «Propietario multiusuario» y luego asignar el valor de «Sí» o «Verdadero» al usuario Nadie. A continuación, puede crear grupos de usuarios y grupos de dispositivos en función del valor del atributo.

## Iniciar sesión en un dispositivo

El usuario puede iniciar sesión en un dispositivo iOS y asignarse a sí mismo el dispositivo. Después de iniciar sesión, todas las aplicaciones, políticas, configuraciones y certificados pertinentes se insertarán en el dispositivo.

Por motivos de seguridad, el usuario del IDP debe volver a autorenticarse cada vez que inicie sesión, incluso si ya ha iniciado sesión en el dispositivo.

## Cerrar sesión en un dispositivo

El usuario puede cerrar sesión en su dispositivo iOS después de haberlo usado. Después de cerrar sesión, las aplicaciones, políticas, configuraciones y certificados se eliminarán del dispositivo, dejándolo en el mismo estado en el que estaba antes de que el usuario iniciara sesión. Después, el dispositivo estará disponible para que otro usuario inicie sesión.

Cierre la sesión de todas las aplicaciones de Microsoft antes de cerrar la sesión de Multi-user Web Clip.
