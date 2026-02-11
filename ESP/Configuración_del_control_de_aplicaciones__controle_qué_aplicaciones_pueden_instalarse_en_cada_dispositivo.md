---
title: Configuración del control de aplicaciones: controle qué aplicaciones pueden instalarse en cada dispositivo
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

La configuración del control de aplicaciones le permite categorizar las aplicaciones como lista de permitidos o lista de bloqueados a nivel de dispositivo. Las aplicaciones que ya estén instaladas no serán visibles y no podrán iniciarse. Las aplicaciones seguirán siendo visibles en la App Store, pero no se podrán descargar ni iniciar. Cualquier dispositivo al que se distribuya esta configuración la empleará e ignorará cualquier otro ajuste de Políticas de aplicaciones permitidas. Esta configuración sustituye a cualquier política relacionada con la aplicación que haga referencia a las mismas aplicaciones en los dispositivos de destino.

Esta configuración sustituye a cualquier política relacionada con la aplicación que haga referencia a las mismas aplicaciones en los dispositivos de destino. Para dispositivos Windows 10, las restricciones se dan a nivel del dispositivo, de modo que una configuración es la única forma de aplicar las reglas de la aplicación.

La configuración del control de aplicaciones le permite crear dos tipos de listas:

- **Lista de permitidos:** solo permite aquellas aplicaciones que se añadan de manera explícita a esta lista. No se podrá instalar ninguna otra aplicación en los dispositivos.
- **Lista de bloqueados:** No permitir la instalación de aplicaciones específicas en dispositivos.

**Dispositivos compatibles**

Puede utilizar la configuración del control de aplicaciones para poner en lista de bloqueados o en lista de permitidos diferentes aplicaciones en los siguientes dispositivos:

- Android Work Profile en dispositivos propiedad de la empresa
- Solo iOS 9.3+ supervisados
- tvOS 11+
- Windows

## Crear la configuración del control de aplicaciones

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Introduzca **Control de Aplicaciones** en el campo resultante **Elegir configuración** y luego seleccione la configuración de **Control de aplicaciones**.
4. Introduzca un nombre y una descripción para la configuración.
5. Seleccione un SO y continúe más abajo en la sección que corresponda a su SO.

### Android Work Profile en dispositivos propiedad de la empresa

Los usuarios pueden añadir hasta 50 ID de aplicaciones al grupo de la lista de permitidos o de la lista de bloqueados.

**Procedimiento**

1. Seleccione **Crear una lista de permitidos para aplicaciones personales** o **Crear una lista de bloqueados para aplicaciones personales** para añadir la lista de aplicaciones correspondientes para que se incluyan en la lista de permitidos o la lista de bloqueados.
2. Introduzca la ID de la aplicación (com.example.com) y haga clic en Añadir.
3. Haga clic en **Siguiente** y elija una opción de distribución.
4. Haga clic en **Hecho**.

### Dispositivos iOS 9.3 supervisados

**Procedimiento**

::::WorkflowBlock
:::WorkflowBlockItem
Elija si desea crear una lista de permitidos o una lista de bloqueados.
:::

:::WorkflowBlockItem
Haga clic en **Añadir aplicaciones**.
:::

:::WorkflowBlockItem
Elija las aplicaciones que desea poner en la lista de permitidos o la lista de bloqueados haciendo clic en una o en las dos pestañas siguientes:
:::

:::WorkflowBlockItem
- Haga clic en **Añadir por búsqueda** para buscar y elegir aplicaciones desde la App Store o App Catalog.
- Haga clic en **Añadir manualmente** para elegir las aplicaciones introduciendo la Id. de paquete de Apple (empieza por "com.apple") solo para las aplicaciones del sistema Apple.
  Haga clic en la pestaña **Lista de permitidos** o **Lista de bloqueados** para ver la lista de aplicaciones elegidas que se pondrán en la lista de permitidos o la lista de bloqueados.
:::

:::WorkflowBlockItem
(Opcional) Seleccione la opción **Incluir todos los clips web**.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente** y, a continuación, elija una opción de distribución.
:::

:::WorkflowBlockItem
Haga clic en **Hecho**.
:::
::::

### Dispositivos Windows

**Procedimiento**

1. Seleccione **Permitido** o **No Permitido** para añadir la lista de aplicaciones apropiadas a la lista de permitidos o a la lista de bloqueados.
2. En la sección **Definición de reglas**, seleccione el **tipo de aplicación** de la lista.
3. Introduzca un nombre de identificador en el **cuadro Identificador de la aplicación** para buscar una aplicación específica. También puede utilizar el enlace **Buscar aplicaciones** para abrir un nuevo diálogo y buscar identificadores de aplicaciones específicos de Windows.
4. (Opcional) Introduzca alguna descripción sobre la aplicación en el cuadro **Descripción de la aplicación**.
5. Utilice el enlace **+Añadir** para añadir más definiciones de reglas para poner las aplicaciones en la lista de permitidos o en la lista de bloqueados.
6. Haga clic en **Siguiente** y elija una opción de distribución.
7. Haga clic en **Hecho**.
