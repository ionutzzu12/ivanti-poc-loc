---
title: Grupos de usuarios
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Crear un grupo de usuarios administrado dinámicamente**](./Grupos_de_usuarios.md)
- [**Crear un grupo de usuarios administrado manualmente**](./Grupos_de_usuarios.md)
- [**Creación de un grupo de usuarios a partir de uno de los grupos de usuarios duplicados**](./Grupos_de_usuarios.md)
- [**Crear un grupo de usuarios mediante la carga de archivos CSV**](./Grupos_de_usuarios.md)

Cree un grupo de usuarios para poder asignar aplicaciones y [**roles**](./Funciones_del_usuario.md) a múltiples usuarios. Por ejemplo, puede necesitar crear un grupo de administradores si desea que todos los administradores de un departamento sean administradores de las aplicaciones y el contenido.

Puede crear un grupo de usuarios para administrarlo con uno de los siguientes métodos:

- **Administrado dinámicamente (lo más común):** se añaden/eliminan dinámicamente usuarios locales y de LDAP en un grupo según ciertas reglas y/o atributos.
- **Administrado manualmente (finalidad limitada):** añada/elimine manualmente usuarios en un grupo. Los grupos administrados manualmente solo se recomiendan para pruebas que requieran menos permisos.

Puede introducir texto en el campo **Buscar** para ver una lista de todos los grupos de usuarios cuyos nombres empiezan por el texto introducido.

- Los resultados de la búsqueda aparecen como una lista de posibles coincidencias en tiempo real mientras se introduce texto.
- Seleccione el nombre del grupo de usuarios deseado de la lista de posibles coincidencias para las acciones posteriores.
- La coincidencia de la búsqueda no distingue entre mayúsculas y minúsculas.

## Crear un grupo de usuarios administrado dinámicamente

El siguiente procedimiento no es aplicable a grupos de usuarios dinámicos.

**Procedimiento**

1. Haga clic en **+Añadir**.
2. Introduzca un nombre para el grupo de usuarios en el campo **Nombre**.
3. (Opcional) Haga clic en **Añadir descripción** para añadir una descripción para el grupo de usuarios.
4. Haga clic en la opción **Administrado dinámicamente (lo más común)**.
5. Establezca reglas o atributos según sus requisitos. La siguientes reglas corresponden a las opciones disponibles:\* Atributo personalizado de LDAP
   - msExchPoliciesIncluded
   - msExchMailboxGrid
   - mailNickname
     Atributo predeterminado de LDAP
   - samAccountName
   - userPrincipalName
     Atributo predeterminado del usuario
   - email\_address
   - distinguished\_name
   - last\_name
   - display\_name
   - first\_name
   - Grupo de usuarios
   - Atributo personalizado del usuario
     DN del grupo de usuarios
   * GUID del grupo de usuarios
   * Nombre del grupo de usuarios
6. Para cada regla, seleccione entre los usuarios locales y LDAP. Puede incluir o excluir un subgrupo utilizando los criterios de filtrado del **Grupo de usuarios**.
7. Añada más reglas haciendo clic en el icono más (+).Puede establecer filtros condicionales para seleccionar los que cumplan con **CUALQUIERA&#x20;**&#x6F; **TODAS** las reglas añadidas.
8. Cree un grupo de reglas haciendo clic en el icono jerárquico que hay junto al icono más (+).
9. Revise las reglas y atributos del grupo de usuarios en la consulta de texto que se muestra bajo la elecciones de las reglas.
10. En la sección **Resultados**, revise los detalles del (de los) usuario(s) que coinciden con los criterios configurados. Cuando añada o modifique una regla o un atributo, observará que se muestran los usuarios que coinciden, si es que existen:
11. Haga clic en **Guardar&#x20;**&#x70;ara guardar el grupo de usuarios configurado.

## Crear un grupo de usuarios administrado manualmente

1. Haga clic en **+Añadir**.
2. Introduzca un nombre de grupo.
3. (Opcional) Haga clic en **Añadir descripción** para añadir una descripción.
4. Seleccione la opción **Administrado manualmente (finalidad limitada)**.
5. En el campo **Buscar usuarios**, escriba la dirección de correo electrónico de cada usuario que vaya a incluir en el grupo.A medida que escribe, se encontrará y se mostrarán los usuarios que coincidan, si es que existen.
6. Seleccione los usuarios que desee añadir al grupo. Puede buscar y añadir más usuarios según sea necesario.
7. Haga clic en **Guardar**.Puede crear un grupo de usuarios administrados manualmente y, después, añadir este grupo a otro grupo de usuarios administrado dinámicamente. En tal escenario, editar el grupo de usuarios administrado manualmente no rompe la regla del grupo de usuarios administrados dinámicamente. No podrá eliminar un grupo de usuarios administrado manualmente si se agrega a un grupo de usuarios administrado dinámicamente.

## Creación de un grupo de usuarios a partir de uno de los grupos de usuarios duplicados

Desde el Neurons for MDM 118 portal del Administrador se muestra el número de grupos de usuarios duplicados y el número de GUID correspondiente para identificar los grupos duplicados cuando se selecciona el atributo “Nombre del grupo de usuarios” en el creador de reglas. Además, una tabla bajo esta regla muestra la lista de los grupos de usuarios duplicados y sus detalles, como el Nombre del Grupo de Usuarios, el GUID, la Fuente y el nombre distinguido (DN).

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Inicie sesión en el portal del administrador de Ivanti Neurons for MDM
:::

:::WorkflowBlockItem
Vaya a **Usuarios**, **Grupos de usuarios**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir**. Se abre el asistente para crear un grupo de usuarios.

1. Especifique el nombre en el campo **Nombre**.
2. Seleccione **Nombre del grupo de usuarios** en el generador de reglas, seleccione **es igual a**, seleccione *uno* de los nombres de grupo duplicados.
3. Haga clic en el icono **+** para añadir más reglas.
4. Seleccione **Grupo de usuarios GUID**, **es igual a**.
5. Copie y pegue el GUID de la tabla que muestra la lista de nombres de grupos de usuarios duplicados y GUIDs. El resultado muestra los usuarios asociados que se añadirán al nuevo grupo.
6. Haga clic en **Guardar**. Los usuarios de la lista se añaden ahora al nuevo grupo de usuarios que ha creado.
:::
::::

Si no puede realizar las tareas en la página **Grupos de usuarios**, puede ser que no tenga los permisos necesarios. Necesita tener una de las siguientes [**funciones**](./Funciones_del_usuario.md):

- Administración del sistema
- Administración de usuarios

## Crear un grupo de usuarios mediante la carga de archivos CSV

La función recién agregada permite a los administradores crear grupos de usuarios y agregar usuarios a los grupos creados mediante un archivo CSV.

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Inicie sesión en el portal del administrador de Ivanti Neurons for MDM
:::

:::WorkflowBlockItem
Vaya a **Usuarios**, **Grupos de usuarios**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir**.
:::

:::WorkflowBlockItem
Seleccione **Importar grupos de usuarios desde CSV**. Se abre el asistente de importación de grupos de usuarios.

1. En la sección Descargar CSV, haga clic en **Descargar plantilla CSV** para descargar la plantilla CSV. Con la plantilla, puede editar el archivo para crear grupos de usuarios y agregar usuarios a los grupos de usuarios nuevos/existentes.
2. Después de editar y guardar el archivo CSV, haga clic en **Elegir un archivo** para cargar el archivo CSV.
3. Haga clic en **Cargar**. Aparecerá una confirmación si se ha cargado correctamente.
:::
::::

| Propiedad                            | Descripción                                                                                                                                     |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Límite del tamaño del archivo CSV    | El tamaño máximo del archivo CSV para importar está limitado a 2 MB.                                                                            |
| Requisitos de formato de archivo CSV | Los archivos CSV deben contener exactamente 2 columnas: accountUid y groupName.\* Tanto el valor accountUid como el groupName son obligatorios. |

- Los registros que no cumplan con estos criterios se descartarán durante la importación.Los administradores pueden descargar un archivo CSV de muestra desde la sección de importación como referencia. |
  \| Gestión de errores durante la importación | Si se producen errores o fallos durante la importación CSV, se generará un archivo de error.\* Ahora los administradores pueden descargar este archivo de error para revisar las filas de CSV fallidas y comprender los motivos del error.
- El archivo de error incluye la fila CSV específica que falló y proporciona una explicación del error.       |
  \| Condiciones de importación correctas      | La importación de usuarios a grupos de usuarios solo se realiza correctamente cuando el grupo de usuarios es local y se administra manualmente.\* El usuario debe existir en el sistema para que la importación se realice correctamente.                                                                                                                |

### Condiciones para crear un grupo de usuarios y agregar un usuario con un archivo CSV de muestra

Detalles del archivo CSV de muestra

**accountUid**: [**test\_user\_1@org.com**](mailto\:test_user_1@org.com)

**groupName**: test\_group\_1

| Condiciones                       | Descripción                                                                                                                                                                                                                                                               |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Grupo existente                   | Si el grupo test\_group\_1 ya existe, el usuario [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) se asociará con el grupo.                                                                                                                                       |
| Grupo inexistente                 | Si el grupo test\_group\_1 no existe, se creará un nuevo grupo con el nombre test\_group\_1 y el usuario [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) se asociará con el grupo.                                                                               |
| Grupo no local                    | Si el grupo test\_group\_1 existe pero no es un grupo local, este registro se incluirá en el archivo CSV de error con el motivo "El grupo no es local".                                                                                                                   |
| Grupo no administrado manualmente | Si el grupo test\_group\_1 existe pero no es un grupo administrado manualmente, este registro se incluirá en el archivo CSV de error con el motivo "El grupo no es un grupo administrado manualmente".                                                                    |
| Usuario inexistente               | Si el usuario [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) no existe, este registro se incluirá en el archivo CSV de error con el motivo "Usuario no encontrado".                                                                                             |
| Usuario o grupo inexistente       | Si tanto el usuario [**test\_user\_1@org.com**](mailto\:test_user_1@org.com) como el grupo test\_group\_1 no existen, se creará un nuevo grupo con el nombre test\_group\_1 y este registro se incluirá en el archivo CSV de error con el motivo "Usuario no encontrado". |
