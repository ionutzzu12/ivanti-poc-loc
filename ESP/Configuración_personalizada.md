---
title: Configuración personalizada
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene los siguientes temas:

- [**Definir una configuración personalizada**](./Configuración_personalizada.md)
- [**Ajustes de la configuración personalizada**](./Configuración_personalizada.md)

Licencia: Silver

**Disponible para:** iOS, macOS, Android, Windows

**Descripción**

Le permite importar y distribuir un archivo de configuración predefinido.

Los formatos de archivo de configuración válidos son los siguientes:

| **SO** | **Formatos de archivo de configuración válidos** |
| ------ | ------------------------------------------------ |
| iOS    | - .plist                                         |

- .mobileconfig
- .xml                                                                                |
  \| macOS   | \* .plist
- .mobileconfig                                                                                       |
  \| Android | .xml. Actualmente, esta característica solo admite los archivos de configuración .xml para dispositivos Zebra. |
  \| Windows | SyncML.                                                                                                        |

## Definir una configuración personalizada

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Seleccione **Configuraciones**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir**.
:::

:::WorkflowBlockItem
Escriba «personalizada» en el campo de búsqueda y, a continuación, haga clic en la configuración **Personalizada**.Aparecerá la página de detalles de la configuración personalizada.
:::

:::WorkflowBlockItem
Configure los ajustes en esta página. Consulte la tabla de la sección [**Ajustes de la configuración personalizada**](./Configuración_personalizada.md) para obtener ayuda acerca de los valores.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente** para configurar los ajustes de distribución.
:::

:::WorkflowBlockItem
(dispositivos macOS) Seleccione una opción adicional para el ajuste **¿A quién es aplicable esta configuración?** dependiendo de lo que desee que haga esta configuración:
:::

:::WorkflowBlockItem
- En todo el dispositivo (normalmente usado).
- Específico para el usuario (usuario actualmente registrado).
  Haga clic en **Hecho**.
:::
::::

## Ajustes de la configuración personalizada

| **Ajuste**     | Qué hacer                                                                                                                                                                                                                |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Nombre         | Introduzca un nombre que identifique a esta configuración.                                                                                                                                                               |
| Descripción    | Introduzca una descripción que explique la finalidad de esta configuración.                                                                                                                                              |
| Elegir OS      | Haga clic en el icono del SO para cargar un archivo de configuración que se corresponda con el icono seleccionado                                                                                                        |
| Elegir archivo | Esta opción aparecerá después de haber seleccionado un SO. Arrastre un archivo de la configuración al cuadro Arrastrar y soltar o haga clic en el botón **Elegir archivo** para seleccionar un archivo de configuración. |

## Configuración personalizada de CSP (solo Windows)

Solo puede crear una configuración CSP personalizada en dispositivos Windows. Cuando seleccione el sistema operativo Windows en la sección Elegir sistema operativo, obtendrá dos opciones: 

**Opción 1: archivo CSP XML**: seleccione esta opción y siga el mismo proceso mencionado para el ajuste **Seleccionar archivo** .

**Opción 2: nodo de esquema CSP OMA-URI personalizado**

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Seleccione la opción Nodo de esquema CSP OMA-URI personalizado de la lista. La sección Configuración CSP personalizada aparecerá en pantalla.
:::

:::WorkflowBlockItem
En **ACCIONES**, haga clic en el botón + para empezar a crear la configuración con diferentes campos OMA-URI.
:::

:::WorkflowBlockItem
En la pantalla aparece la ventana emergente **Agregar fila** que tiene los siguientes campos:
:::

:::WorkflowBlockItem
- Descripción: introduzca la información general sobre el ajuste
- OMA-URI: introduzca el OMA-URI que desea utilizar como ajuste
- Tipo de datos: seleccione un tipo de datos que utilizará para esta configuración: DATE, FLOAT, BASE64, NODE, XML, BINARY, CHARACTER, TIME, BOOLEAN, INTEGER
- Valor: introduzca un valor asociado al tipo de datos seleccionado
- Tipo de acceso: Añadir, Eliminar, Ejecutar, Reemplazar, Obtener
  Haga clic en **Guardar y Cerrar** para cerrar la ventana con los datos proporcionados. Haga clic en **Guardar y Añadir** otra para crear una nueva fila.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione el modo de distribución y haga clic en **Hecho**.
:::
::::

**Temas relacionados**

- [**Insertar SyncML en dispositivos mediante la configuración personalizada**](./Insertar_SyncML_en_dispositivos_mediante_la_configuración_personalizada.md)
