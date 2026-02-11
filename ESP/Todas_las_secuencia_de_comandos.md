---
title: Todas las secuencia de comandos
createdAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:09 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** dispositivos macOS

En la página **Administrador > Todas las secuencias de comandos**, Ivanti Neurons for MDM permite a los usuarios con la función de administración del sistema crear o cargar y administrar secuencias de comandos que se pueden utilizar en configuraciones y distribuir a dispositivos. Puede asociar atributos personalizados a las secuencia de comandos y asignar los valores resultantes a los dispositivos configurados. Utilice trazas de auditorías para ver los registros de los cambios de secuencia de comandos y los resultados de la ejecución.

Puede escribir una secuencia de comandos que configure cualquier configuración en los dispositivos. Por ejemplo, puede ejecutar secuencias de comandos que hagan lo siguiente:

- obligar a los usuarios de los dispositivos a cambiar sus contraseñas mensualmente;
- bloquear la pantalla después de 5 minutos de inactividad; o
- configurar una red Wi-Fi segura.

Esta sección contiene los siguientes temas:

- [**Añadir una secuencia de comandos**](./Todas_las_secuencia_de_comandos.md)
- [**Modificar una secuencia de comandos**](./Todas_las_secuencia_de_comandos.md)
- [**Usar variables de secuencia de comandos**](./Todas_las_secuencia_de_comandos.md)
- [**Probar una secuencia de comandos**](./Todas_las_secuencia_de_comandos.md)
- [**Verificar los resultados de ejecución de la secuencia de comandos**](./Todas_las_secuencia_de_comandos.md)

## Añadir una secuencia de comandos

Puede crear o cargar un repositorio de secuencia de comandos bash. Este repositorio se puede usar en una configuración, como [**Secuencia de comandos de Mobile@Work para macOS**](./Mobile@Work_para_macOS.md), para seleccionar una secuencia de comandos y distribuirlo para ejecutarlo en los dispositivos según la programación especificada en la configuración.

Por ejemplo, puede crear una secuencias de comandos de shell para su ejecución en dispositivos. Si fuera necesario, puede usar contenedores. La ejecución de archivos binarios desde una secuencia de comandos de shell no es compatible.

Ivanti le recomienda encarecidamente que pruebe las secuencias de comandos de shell antes de ejecutarlos en los dispositivos para garantizar su solidez y calidad. Ejecute su secuencia de comandos a nivel local y corrija los errores que se produzcan.

Procedimiento

1. Vaya a **Administración > Secuencias de comandos > Todas las secuencias de comandos**.
2. Haga clic en **+Añadir**.
3. Asigne un nombre a la secuencia de comandos y descríbala.
4. Seleccione uno de los siguientes **Tipos de secuencia de comandos**:\* **bash**
   - **zsh**
   - **python**
   - **swift**
5. Seleccione la casilla **Ejecutar como raíz** para ejecutar la secuencia de comandos como raíz en los dispositivos. De forma predeterminada, esta opción se encuentra deshabilitada.
6. En el **Editor de secuencias de comandos**, puede escribir, arrastrar y soltar o copiar y pegar una secuencia de comandos en el cuadro de texto.
7. Alternativamente, haga clic en **Importar código de una secuencia de comandos** para arrastrar y soltar un archivo de secuencia de comandos existente o haga clic en Elegir archivo para examinar y seleccionar el archivo de secuencia de comandos que va a cargar en Ivanti Neurons for MDM. Esto reemplazará cualquier secuencia de comandos que haya en el editor de secuencias de comandos. Esta acción no podrá deshacerse. Haga clic en **Importar**. El código de la secuencia de comandos cargado se mostrará en el editor de secuencias de comandos.
8. (Opcional) En la sección **Atributos personalizados disponibles**, seleccione uno o más atributos personalizados del dispositivo que aparecen para asociarlos con la secuencia de comandos. Estos se pueden utilizar para asignar los valores de ejecución de secuencia de comandos resultantes a los atributos personalizados del dispositivo de los dispositivos configurados. Haga clic en **Código de ejemplo para atributos personalizados** para ver un código de ejemplo que usa atributos personalizados en una secuencia de comandos.
9. Haga clic en **Guardar**.

Los nombres de atributos personalizados en la secuencia de comandos deben estar en minúsculas. Si se hace referencia a los atributos personalizados en cualquier secuencia de comandos, los atributos no se podrán eliminar. Cuando modifique un atributo personalizado (por ejemplo, su nombre) y si está asociado a una secuencia de comandos, deberá realizar los cambios correspondientes en las secuencia de comandos asociadas.

## Modificar una secuencia de comandos

Para editar o eliminar una secuencia de comandos:

1. Vaya a **Administración > Secuencias de comandos > Todas las secuencias de comandos**.
2. En la columna **Acciones** de la secuencia de comandos, haga clic en el icono correspondiente para la acción de editar o eliminar.
3. Siga las instrucciones que aparecen en pantalla para completar la acción.

Cuando se cambia una secuencia de comandos (contenido, nombre, descripción), todas las configuraciones asociadas a la secuencia de comandos se redistriburán en los dispositivos.

## Usar variables de secuencia de comandos

Definir y almacenar entradas de secuencia de comandos como variables de entorno y de sustitución en el repositorio de secuencias de comandos. En la configuración de secuencias de comandos de Mobile\@Work para macOS, dependiendo de la secuencia de comandos que esté enlazado, las variables de secuencia de comandos relacionadas estarán disponibles para usarse según sea necesario. Esta característica requiere [**Mobile@Work para macOS**](./Mobile@Work_para_macOS.md) 1.71.0 hasta la versión más reciente compatible con Ivanti Neurons for MDM.

Use las variables para ejecutar una secuencia de comandos con valores diferentes cada vez que se ejecute. Por ejemplo, un administrador puede crear una secuencia de comandos para utilizar la variable de entorno $\{userEmailAddress} como variable de secuencia de comandos y asociarla a una configuración de secuencia de comandos de Mobile\@Work para macOS. Cuando la configuración se distribuye e instala en cada dispositivo de usuario, Ivanti Neurons for MDM envía una dirección de correo electrónico de usuario registrado diferente para que cada dispositivo realice ciertas acciones. El portal administrativo de Ivanti Neurons for MDM es compatible con variables personalizadas.

Para añadir una variable de secuencia de comandos:

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Administración > Secuencias de comandos > Todas las secuencias de comandos**.
:::

:::WorkflowBlockItem
En la sección Entrada de la secuencia de comandos, haga clic en **+ Añadir**.
:::

:::WorkflowBlockItem
En la página emergente Añadir entrada de secuencias de comandos - Variable de entorno, introduzca los siguientes detalles:
:::

:::WorkflowBlockItem
- Etiqueta que se mostrará: este texto se mostrará como una etiqueta en la página de configuración de la secuencia de comandos de Mobile\@Work para macOS. Por ejemplo, Introducir la carpeta del sistema operativo, Introducir el número de Apache, etc.
- Nombre de la variable de entorno: por ejemplo, JAVA\_HOME, OS\_VERSION, etc. Ivanti Neurons for MDM sustituye los valores de las variables de secuencia de comandos mientras envía los detalles de la configuración a un dispositivo de destino a la vez que los valores se mantienen en la base de datos.
- Valor predeterminado de la variable de entorno: por ejemplo, 1024, bin/java, $\{PhoneNumber}, y así sucesivamente. Las variables de entrada se utilizarían en la secuencia de comandos cargado o las editaría un administrador. Consulte también las siguientes notas.
  En el área Vista previa, revise cómo se mostrará el valor de la variable de entorno como entrada de secuencia de comandos en la página de configuración.
:::

:::WorkflowBlockItem
Haga clic en **Guardar**.
:::
::::

De este modo, solo la etiqueta y el valor por defecto estarán disponibles para la configuración y no el nombre de la variable de entorno, lo cual proporciona una capa de abstracción.

- El valor alfanumérico (por ejemplo, 1024, bin/java, root\@localhost) o los atributos de sistema (por ejemplo, $\{userFirstName}) son aceptables como valor de la variable de entorno.
- El valor de la variable de entorno se puede modificar o eliminar durante la implementación en la página de configuración.
- Si no se proporciona el valor de la variable de entorno, asegúrese de proporcionar un valor durante la implementación de la secuencia de comandos. De lo contrario, se trasladará el valor vacío a la secuencia de comandos.
- Después de distribuir e instalar una configuración de la secuencia de comandos en el dispositivo, la edición de las variables de entorno en la página Administrador > Todas las secuencias de comandos no afectará a las configuraciones existentes asociadas a la secuencia de comandos. Consulte también [**Configuración de la secuencia de comandos de Mobile@Work para macOS**](./Mobile@Work_para_macOS.md).

### Editar una variable de la secuencia de comandos

Para modificar una variable de la secuencia de comandos, haga clic en el icono de edición (lápiz) que hay junto a la variable y guarde los cambios.

Si la configuración de una secuencia de comandos se refiere a una secuencia de comandos que tiene variables de secuencia de comandos, la edición de la etiqueta de una variable de secuencia de comandos existente también se reflejará en la configuración de la secuencia de comandos. Sin embargo:

- Un cambio en el valor por defecto de la variable de la secuencia de comandos no se reflejará en las configuraciones existentes.
- Un cambio en el valor por defecto de la variable de secuencia de comandos se reflejará en cualquier nueva configuración creada con la secuencia de comandos anterior.

### Borrar una variable de la secuencia de comandos

Para eliminar una variable de la secuencia de comandos, haga clic en el icono de eliminación (menos) que hay junto a la variable y confirme.

Una variable de secuencia de comandos recién creada, o la eliminación de una variable de secuencia de comandos existente, se reflejará incluso en una configuración ya existente.

## Probar una secuencia de comandos

Pruebe ejecutar una secuencia de comandos en la herramienta de depuración rápidamente antes de probarlo en un dispositivo y sin necesidad de guardar las secuencias de comandos. Esta característica requiere [**Mobile@Work para macOS**](./Mobile@Work_para_macOS.md) 1.67 hasta la versión más reciente que compatible con Ivanti Neurons for MDM.

Procedimiento

1. Vaya a **Administración > Secuencias de comandos > Todas las secuencias de comandos**.
2. En el Editor de secuencias de comandos, añada o importe una secuencias de comandos.
3. Si el abonado tiene varios espacios, seleccione uno de ellos.
4. En la sección Script de prueba, seleccione **macOS** como la plataforma.
5. En el campo de texto **Buscar dispositivos**, busque y seleccione el dispositivo en el que se puede probar la secuencia de comandos. El dispositivo se puede buscar por número de serie,nombre de usuario,nombre de dispositivo yversión del sistema operativo.
6. Haga clic en **Probar ahora**. De esta manera, se puede añadir, editar y eliminar una variable de entorno, y la secuencia de comandos se puede probar con ese estado (sin siquiera guardar los cambios realizados).
7. Espere a que la secuencia de comandos se inserte y ejecute en el dispositivo.
8. Revise los resultados de las pruebas publicadas en las secciones Entrada de secuencia de comandos (que contiene detalles de las variables de entorno), Salida de secuencia de comandos y Atributos personalizados. También se muestran los valores por defecto de las variables de entorno.

## Verificar los resultados de ejecución de la secuencia de comandos

Para ver los registros de los resultados de la ejecución de la secuencia de comandos:

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Dispositivos**.
:::

:::WorkflowBlockItem
Haga clic en el nombre del dispositivo.
:::

:::WorkflowBlockItem
Haga clic en la pestaña **Registros**.
:::

:::WorkflowBlockItem
En una línea que muestre la acción Ejecución de la secuencia de comandos, podrá verificar la siguiente información:
:::

:::WorkflowBlockItem
- Nombre de la secuencia de comandos en la columna Detalles.
- Estado de ejecución de la secuencia de comandos en la columna Estado.
- Fecha y hora de ejecución de la secuencia de comandos en la columna Fecha.
- Registros de ejecución de la secuencia de comandos (plist de registros de dispositivos) haciendo clic en el icono del ojo que hay debajo en la columna Acciones.
  Utilice filtros para mostrar las filas de **Ejecución de la secuencia de comandos**. Los registros de estas filas incluyen la salida (plist) de la salida estándar y el error estándar de las secuencias de comandos .
:::

:::WorkflowBlockItem
Utilice filtros para mostrar las filas de **Procesamiento de los resultados de la ejecución de la secuencia de comandos**. Los registros de estas líneas incluyen detalles (plist) de cómo se procesaron los resultados.

- Si una secuencia de comandos no tiene ningún atributo personalizado asociado, no habrá ningún resultado que procesar. Dichas secuencias de comandos no se mostrarán en la lista de filas filtradas.
- Si una secuencia de comandos tuviera atributos personalizados asociados con este y si estos tuvieran el formato esperado, entonces los atributos personalizados de los resultados se asignan y el estado se ve como Correcto. Puede verificar los atributos personalizados asignados y sus valores en la pestaña **Atributos**.
- Si una secuencia de comandos tenía atributos personalizados asociados y estaban en el formato esperado, los atributos personalizados de los resultados se asignarán y el estado se mostrará como «Error».
- Si el formato del resultado es correcto pero no todos los atributos personalizados asociados se envían en el resultado, el estado se mostrará como «Error».
- Si se envía una variable de secuencia de comandos con la secuencia de comandos, los registros de procesamiento de resultados de la ejecución de la secuencia de comandos incluirán detalles (plist) para la variable de secuencia de comandos.
:::
::::

Temas relacionados:

- [**Configuración de secuencia de comandos de Mobile@Work para macOS**](./Mobile@Work_para_macOS.md)
