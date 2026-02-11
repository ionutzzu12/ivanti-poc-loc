---
title: Director de la escuela
createdAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:08 GMT+0200 (Eastern European Standard Time)
---

## Licencia: Gold

**Aplicable a:** iOS 9.3+ supervisado

Apple School Manager es un servicio en la nube de Apple destinado a las instituciones educativas para brindarles servicios, incluida la compra de aplicaciones en Apps y libros de Apple, la inscripción de iPad a través de la inscripción de dispositivos de Apple y la creación de identificaciones de Apple administradas. Con la completa integración con Apple School Manager, la Ivanti Neurons for MDMsolución de UEM proporciona una forma de administrar completamente y sin interrupciones los iPads destinados a profesores y a estudiantes, con el fin de sacar provecho del ecosistema de School Manager y de las aplicaciones tales como Classroom.

Apple Books no es compatible.

## Configuración de School Manager

:::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Administrador > School Manager**.
:::

:::WorkflowBlockItem
Haga clic en la opción **Configurar Education** si está desactivada.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones:
:::

::::WorkflowBlockItem
- **Sincronice con la cuenta de Apple School Manager para importar información de la escuela**:1) Vaya a **Administrador > Apple > Inscripción de dispositivos** para descargar los archivos clave de su organización.
  2\) Cargue los archivos a su cuenta de Apple School Manager para generar sus claves de cifrado.
  3\) Descargue las claves de cifrado de Apple School Manager y cargue las claves en Ivanti Neurons for MDM (**Administración > Apple > Inscripción de dispositivos**).
  Las cuentas existentes del programa de inscripción de dispositivos de Apple se pueden reutilizar para Apple Education. Apple le dará la opción de actualizar su cuenta de Inscripción de dispositivos para incluir funciones de Education cuando acceda a Apple School Manager. Para ver las instrucciones sobre cómo actualizar, visite [**https://support.apple.com/en-in/HT206960**](https://support.apple.com/en-in/HT206960).
  Cuando se acepten las claves de cifrado, aparecerá el botón **Sincronizar ahora**.
  4\) Haga clic en **Sincronizar ahora** para comenzar a sincronizar los datos con Apple School Manager.
- **Importe datos desde archivos CSV**:::::WorkflowBlock

:::WorkflowBlockItem
Haga clic (opcional) e&#x6E;**&#x20;Descargar archivo ZIP de plantillas CSV** para descargar un archivo zip que contiene plantillas de todos los tipos de archivo.
:::

:::WorkflowBlockItem
Haga clic en **Seleccionar archivos**...
:::

:::WorkflowBlockItem
Añada los siguientes seis archivos CSV:
:::

:::WorkflowBlockItem
- Archivo de datos de los alumnos (students.csv)
- Archivo de datos de la lista (roster.csv)
- Archivo de datos del personal (staff.csv)
- Archivo de datos de las clases (classes.csv)
- Archivo de datos de los cursos (courses.csv)
- Archivo de datos de las localizaciones (locations.csv)Debe seleccionar los seis archivos CSV juntos cada vez antes de cargarlos.
  Haga clic en **Cargar**.
:::

:::WorkflowBlockItem
(Opcional) Si los archivos CSV tienen que modificarse, conserve todos los datos necesarios en los seis archivos que se cargaron previamente. Haga las modificaciones necesarias y vuelva a cargarlos de nuevo.
:::

:::Paragraph{indent="1"}
\::::
Busque los datos desde la pestaña **Clases** e **Individuos**.Los individuos (estudiantes y personal) también aparecen en la página **Usuarios** de Ivanti Neurons for MDM.
:::
::::

:::WorkflowBlockItem
Cree dos grupos de dispositivos para dispositivos que se usarán para la educación de estudiantes y de personal, tal y como se indica a continuación:1) Vaya a **Administrador > Atributos personalizados**.
2\) Cree atributos personalizados para los alumnos y el personal que vayan a usarse para crear grupos de dispositivos administrados dinámicamente.
3\) Vaya a **Dispositivos > Grupos de dispositivos**.
4\) Haga clic en **Añadir+**.
5\) Vaya creando los grupos de dispositivos administrados dinámicamente para alumnos y personal utilizando los atributos personalizados creados previamente como filtros.
:::

:::WorkflowBlockItem
Asigne los dispositivos registrados a los alumnos y el personal desde la página **Dispositivos** utilizando la opción **Acciones > Asignar al usuario**.
:::

:::WorkflowBlockItem
Cree una configuración para Líderes (personal) y Miembros (alumnos) añadiendo las cargas útiles en **Configuraciones >&#x20;**[**Education**](./Educación.md).
:::

:::WorkflowBlockItem
Distribuya las configuraciones para Líderes (personal) y Miembros (alumnos) a los grupos de dispositivos del personal y los alumnos.Esta distribución insertará las configuraciones e instalará los certificados en los dispositivos respectivos.
:::
:::::

En la página de **Administración > School Manager**, si no hay ningún valor para el nombre de la clase, se derivará del identificador de la fuente del sistema de clases y de los campos del identificador del curso. Estos campos son opcionales en Apple School Manager o el archivo CSV. No obstante, se recomienda introducir siempre un valor, ya que esta combinación se utiliza como identificador predeterminado cuando no hay ningún Nombre de clase.

## Insertar la aplicación Classroom para los profesores

Con la aplicación Classroom, los profesores (Líderes) pueden gestionar las siguientes situaciones:

::::WorkflowBlock
:::WorkflowBlockItem
- La capacidad de gestionar Classroom para controlar los iPad y las aplicaciones de forma remota.
- La capacidad de crear un grupo de clase.
- La capacidad de un profesor para ver los alumnos miembros de ese grupo.
- La capacidad de un profesor para enviar contenido a los alumnos en ese grupo.
- Restringir qué aplicaciones y contenido pueden ver los alumnos.
:::
::::

Puede enviar la aplicación de Aula desde la tienda de aplicaciones de Apple.

**Procedimiento**

1. Vaya a la página **Aplicaciones > App Catalog**.
2. Haga clic en el botón **+Agregar**.
3. Busque y seleccione la aplicación Classroom de Apple.
4. Haga clic en **Siguiente**.
5. Introduzca la categoría y la descripción.
6. Haga clic en **Siguiente**.
7. Distribuya la aplicación en el grupo de dispositivos de los profesores que había creado previamente.
8. Configure los ajustes de la aplicación en la página Configuraciones de aplicaciones.
9. Haga clic en **Hecho**.

## Desactivar School Manager

Si se desactiva School Manager, se borrarán todos los datos actuales. Tenga cuidado al hacerlo.

1. Vaya a **Administrador > School Manager**.
2. Haga clic en la opción **Configurar Education** si está activada.
3. Haga clic en **Sí**.
