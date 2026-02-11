---
title: Actualizaciones de software
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:**

•Dispositivos supervisados iOS 10.3+ y tvOS 12.0+

•Dispositivos macOS

•Dispositivos Windows 10

Cree y distribuya reglas para las actualizaciones del SO.

Esta sección contiene los siguientes temas:

- [**Configurar actualizaciones de software para dispositivos iOS/tvOS**](./Actualizaciones_de_software.md)
- [**Configuración de las actualizaciones de software para los dispositivos No-DEP y DEP macOS**](./Actualizaciones_de_software.md)
- [**Configurar actualizaciones de software para dispositivos Windows**](./Actualizaciones_de_software.md)
- [**Aplicación de actualizaciones de software mediante gestión declarativa de dispositivos**](./Actualizaciones_de_software.md)

## Configurar actualizaciones de software para dispositivos iOS/tvOS

**Procedimiento**

Para permitir que a los dispositivos iOS/tvOS se les envíen actualizaciones del SO si están en modo supervisado:

1. Vaya a **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Haga clic en **Actualizaciones del software**.
4. Haga clic en **iOS/tvOS** para ver la sección Ajustes de la configuración.
5. Seleccione la opción **Permitir que las actualizaciones del SO se instalen automáticamente en dispositivos supervisados**.
6. Seleccione una de las siguientes opciones:\* Actualizar a la última versión
   - Actualizar a una versión específica: por ejemplo, introduzca el número de versión de iOS como 11.3.0.
7. Seleccione una de las siguientes acciones de instalación:\* Predeterminada
   - Solo descarga
   - Instalar lo antes posible
8. Seleccione las siguientes opciones de hora a la que deben producirse las actualizaciones:\* Hora de inicio
   - Hora de fin
   - Zona horaria
9. Haga clic en **Siguiente**.
10. Seleccione la opción **Habilitar esta configuración**.
11. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
    - Ningún dispositivo (predeterminada)
    - Personalizada
12. Haga clic en **Hecho**.

- Al instalar una versión específica de una actualización del SO para dispositivos iOS, debe seleccionar una versión que esté disponible para el dispositivo. Si selecciona una versión no válida o que no esté disponible, se ignorarán las actualizaciones de software del dispositivo.
- Si el dispositivo tiene un código de acceso, después de que MDM envíe la actualización al dispositivo, este pone en cola la actualización y se pide al usuario que introduzca su código de acceso para iniciar la instalación.
- Habilite `enforcedSoftwareUpdateDelay` en [**Restricciones de iOS**](./Restricciones_de_iOS.md) para asegurarse de que el análisis manual de los dispositivos en busca de actualizaciones de software no eliminará las versiones específicas que ha descargado esta configuración.

## Configuración de las actualizaciones de software para los dispositivos No-DEP y DEP macOS

El perfil de Inscripción de dispositivos forma parte de Apple Business Manager, que permite que los clientes puedan comprar dispositivos en grandes cantidades e inscribirlos automáticamente en MDM durante la activación. Para obtener información, consulte [**Inscripción de dispositivos**](./Inscripción_de_dispositivos.md).

El procedimiento siguiente le ayuda a enviar actualizaciones de SO a dispositivos de macOS con DEP y sin DEP.

**Procedimiento**

1. Vaya a **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Haga clic en **Actualizaciones del software**.
4. Haga clic en **macOS** para ver la sección Ajustes de la configuración.
5. Seleccione la opción **Habilitar actualizaciones de software de macOS**.
6. Seleccione el tipo de actualizaciones para el dispositivo. Para cada una de estas actualizaciones, también puede seleccionar actualizaciones que no requieran reiniciarse.\* Actualizaciones del OS
   - Actualizaciones críticas
   - Actualizaciones de los datos de configuración
   - Actualización del firmware
   - Actualizaciones no críticasEl administrador puede gestionar (instalar/ programar) las actualizaciones no críticas de MacOS activando la opción **Habilitar actualizaciones no críticas**. Esta opción está desactivada por defecto para los abonados existentes y la debe activar el administrador explícitamente después de la actualización, si es necesario.En **Actualización de OS**, los Administradores pueden actualizar el dispositivo a una versión específica de macOS.Todas las actualizaciones de macOS pueden configurarse con acciones como las siguientes:\* Predeterminada
     - Solo notificar
     - Instalar más tarde
     - Instalar el reinicio forzado
     - Solo descarga
     - Instalar lo antes posible
   - PrioridadPredeterminado: bajoValores posibles: bajo, alto
   - Aplazamientos de usuarios máximosPosibles valores: enteroEs compatible solo cuando se selecciona la opción Instalar más adelante.
7. Seleccione las siguientes opciones de hora a la que deben producirse las actualizaciones:\* Hora de inicio
   - Hora de fin
   - Zona horaria
8. Haga clic en **Siguiente**.
9. Seleccione la opción **Habilitar esta configuración**.
10. Seleccione una de las siguientes opciones de distribución:\* Todos los dispositivos
    - Ningún dispositivo (predeterminada)
    - Personalizada
11. Haga clic en **Hecho**.

## Configurar actualizaciones de software para dispositivos Windows

**Procedimiento**

Para configurar su calendario de actualizaciones de la instalación de Windows:

::::WorkflowBlock
:::WorkflowBlockItem
Vaya a **Configuraciones**.
:::

:::WorkflowBlockItem
Haga clic en **+Añadir**.
:::

:::WorkflowBlockItem
Haga clic en **Actualizaciones del software**.
:::

:::WorkflowBlockItem
Haga clic en **Windows** para ver la sección Ajustes de la configuración.
:::

:::WorkflowBlockItem
Introduzca las siguientes opciones dependiendo de la versión de sus dispositivos Windows.
:::

:::WorkflowBlockItem
Haga clic en **Siguiente**.
:::

:::WorkflowBlockItem
Seleccione la opción **Habilitar esta configuración**.
:::

:::WorkflowBlockItem
Seleccione una de las siguientes opciones de distribución:
:::

:::WorkflowBlockItem
- Todos los dispositivos
- Ningún dispositivo (predeterminada)
- Personalizada
  Haga clic en **Hecho**.
:::
::::

### Actualizaciones del software para dispositivos Windows 10+

- Fuentes de la actualización - Seleccione una de las siguientes fuentes:
  - WSUS para la empresa
  - Microsoft Update y/o WSUS para la empresa
    Fuente de actualización de controladores
- Mostrar fuente de actualización
- Otra fuente de actualización
- Fuente de actualización de la calidad
- URL para el servidor WSUS de la empresa
- Alternar servidor de actualización de Microsoft de Intranet
- Permitir actualizaciones de 'editores de confianza' - Limite las fuentes de las actualizaciones solamente a los editores de confianza.
- Estrategia de actualización automática - Seleccione una de las siguientes opciones del menú desplegable.
- Día programado de la instalación - Establezca la frecuencia de las actualizaciones.
- Hora programada de la instalación - Seleccione una hora a la que se instalarán las actualizaciones.
- Permitir que se descarguen automáticamente las actualizaciones mediante conexiones de uso medido - Activar o desactivar la opción.
- No permitir que las políticas de postergación de actualizaciones generen escaneos frente a Windows Update - Activar o desactivar la opción.
- Fecha límite de reinicio establecido - Seleccione el número de días para el reinicio de la fecha límite.
- Posponer fecha límite de reinicio establecido - Seleccione el número de días para posponer el reinicio de la fecha límite.
- Calendario de transiciones del reinicio establecido - Seleccione el número de días para el reinicio del calendario de transiciones.
- Actualizar/rellenar las URL de contenido vacías.
- Límite de descargas de la aplicación en operadores móviles - Seleccione una de las siguientes opciones:\* No ignorar el límite de descargas MO para aplicaciones y sus actualizaciones
  - Ignorar el límite de descargas de MO (es decir, permitir la descarga ilimitada) para las aplicaciones y sus actualizaciones
- Límite de descargas de actualizaciones en operadores móviles - Seleccione una de las siguientes opciones:\* No ignorar el límite de descargas MO para actualizaciones del OS
  - Ignorar el límite de descargas de MO (es decir, permitir la descarga ilimitada) para las actualizaciones del OS
- Gestionar versiones preliminares - Seleccione una de las siguientes opciones:\* Desactivar versiones preliminares
  - Desactivar versiones preliminares una vez que se haga público el próximo lanzamiento
  - Activar versiones preliminares
- Reiniciar automáticamente el calendario de notificaciones de advertencias para las actualizaciones - Seleccione los minutos que se tardará en reiniciar automáticamente las notificaciones de advertencias.
- Reiniciar el recordatorio de advertencias - Seleccione las horas para establecer el reinicio del recordatorio de advertencias.
- Calendario de actualizaciones automáticas - Seleccione la frecuencia de las actualizaciones automáticas.
- Reiniciar automáticamente las notificaciones para las actualizaciones - Active el reinicio automático de las notificaciones para las actualizaciones.
- Versión del producto: introduzca la versión del producto que aparece en la página de versiones de Actualización de Windows (URL: aka.ms/WindowsTargetVersioninfo). Por ejemplo, "Windows 11" o "11" o "Windows 10".
- Versión de destino: introduzca la versión de destino en la página de versión de actualización de Windows.
- Inicio de horas activas: si activa esta opción, el PC no se reiniciará automáticamente tras las actualizaciones durante las horas activas. El PC intentará reiniciarse fuera de las horas activas.
- Fin de horas activas: si activa esta opción, el PC no se reiniciará automáticamente tras las actualizaciones durante las horas activas. Un PC intentará reiniciarse fuera de las horas activas.
- Rango máximo de horas activas: active esta opción para indicar el número máximo de horas desde la hora de inicio en que los usuarios pueden establecer sus horas activas.
- Sin notificaciones de actualización durante las horas activas: las opciones de notificación de actualización son las siguientes.\* Notificaciones predeterminadas de actualización de Windows
  - Desactivar todas las notificaciones, menos las advertencias de reinicio
  - Desactivar todas las notificaciones, incluidas las advertencias de reinicio
- Desactivar actualizaciones de controladores: active esta opción para excluir los controladores con actualizaciones de calidad de Windows. Si desactiva o no configura esta opción, Windows Update incluirá actualizaciones con una clasificación de controladores.
- Plazo de actualizaciones de calidad: el número de días antes de que las actualizaciones de calidad se instalen automáticamente en los dispositivos es independiente de las horas activas.
- Periodo de gracia límite para actualizaciones de calidad: el número mínimo de días desde la instalación de la actualización hasta el reinicio automático para actualizaciones de calidad.
- Periodo de gracia límite para actualizaciones de funciones: número de días que transcurren hasta que las actualizaciones de funciones se implementan automáticamente en los dispositivos, independientemente de las horas activas.
- Periodo de gracia límite para actualizaciones de funciones: número mínimo de días que transcurren hasta que las actualizaciones de funciones se implementan automáticamente en los dispositivos, independientemente de las horas activas.
- No reiniciar automáticamente hasta el final del periodo de gracia: cuando se activa, los dispositivos no se reiniciarán automáticamente fuera de las horas activas hasta que el plazo y el periodo de gracia hayan pasado, incluso si una actualización está lista para reiniciarse. Cuando está desactivado, se puede intentar llevar a cabo un reinicio automático fuera de las horas activas si la actualización está disponible para el reinicio antes de la fecha límite.

### Actualizaciones de software para dispositivos pre Windows 10.0.14393

Los siguientes ajustes no funcionarán si la opción Restricción de telemetría está desactivada en el dispositivo:

- Pausar cambios de versión/actualizaciones - Active esta opción para retrasar los cambios a una fecha posterior
- Aplazar actualizaciones durante - Elija esta opción para retrasar las actualizaciones hasta cuatro semanas
- Aplazar cambios de versión - Active esta opción para aplazar los cambios de versión
- Aplazar cambios de versión durante - Elija esta opción para retrasar hasta 8 meses

### Actualizaciones de software para dispositivos Windows 10.0.14393+

- Sucursal desde la que se instalan las actualizaciones: permite al administrador de TI establecer la sucursal desde la que un dispositivo recibe las actualizaciones. La rama para instalar actualizaciones desde el campo contiene las opciones siguientes:
  - Windows Insider - Rápido
  - Windows Insider - Lento
  - Publicar versión de Windows Insider
  - Cana semestral (Dirigido)
  - Cana semestral
  - Vista previa de las actualizaciones de calidad
  - Canal Canary
    Actualizaciones de características (actualizaciones): solo compatibles con Windows Professional, Windows Enterprise y Windows Education.
  - Pausar actualizaciones
  - Aplazar durante - Elija esta opción para retrasar hasta 180 días.
    Actualizaciones de calidad (actualizaciones): solo compatibles con Windows Professional, Windows Enterprise y Windows Education.
  - Pausar actualizaciones
  - Aplazar durante - Elija esta opción para retrasar hasta 30 días.

### Actualizaciones de software para dispositivos Windows 10.0.17083+

- Destacar actualizaciones:
  - Período de desinstalación de actualizaciones destacadas - Seleccione el número de días que se tardará en desinstalar una actualización destacada.

### Actualizaciones de software para dispositivos Windows 10.0.17763+

- Desactivar el acceso a «Pausar actualizaciones» por los usuarios
- Desactivar el acceso a UXWU por los usuarios (escaneo, descarga e instalación de Windows Update)
- Actualizar nivel de notificación - Seleccione una de las siguientes opciones:\* Usar las notificaciones predeterminadas de Windows Update
  - Desactivar todas las notificaciones, menos las advertencias de reinicio
  - Desactivar todas las notificaciones, incluidas las advertencias de reinicio
- Destacar actualizaciones:\* Fecha límite anterior al reinicio automático para la instalación de actualizaciones - Seleccione el número de días para la fecha límite anterior al reinicio automático para la instalación de actualizaciones.
  - Fecha límite de reinicio establecido - Seleccione el número de días para la fecha límite del reinicio establecido.
  - Posponer fecha límite de reinicio establecido - Seleccione el número de días para posponer el reinicio de la fecha límite.
  - Calendario de transiciones del reinicio establecido - Seleccione el número de días para el reinicio del calendario de transiciones.

## Aplicación de actualizaciones de software mediante DDM

El administrador puede imponer la instalación de Actualizaciones de software en dispositivos iOS, macOS y iPadOS mediante DDM.

Compatible con:

- iOS 17+
- iPadOS 17+
- macOS 14+

**Procedimiento**

1. Cree una configuración **Aplicación de Cumplimiento de Actualizaciones de Software** desde la sección Configuraciones.
2. Realice una comprobación forzada para asegurarse de que la configuración de actualización de software forzada está instalada en el dispositivo.

Cuando abra el dispositivo, debería ver una notificación sobre las actualizaciones de software necesarias con detalles como el número de versión, la fecha límite, etc.

Si no desea imponer la actualización del software, debe establecer la opción de distribución de la configuración en **Ninguno**.

### Distribución de predicados para una configuración de aplicación de actualizaciones de software

1. Cree una configuración de forzar actualizaciones de Software.
2. Configure el interruptor de palanca “Activación con predicados” en ON y use el botón para incluir los predicados (según sea necesario).

::Image[]{src="Resources/Images/predicates.png" signedSrc="Resources/Images/predicates.png" size="77" caption alt isUploading="false" sha initialPath="Resources/Images/predicates.png" githubPath="Resources/Images/predicates.png" position="flex-start"}

Para editar o eliminar un predicado, vaya a **Administrador** > **Apple** > **Predicados**. En esta página encontrará la lista de predicados disponibles. Haga clic en **Editar** para realizar cualquier cambio en el predicado existente y guardarlo. Del mismo modo, para eliminar un predicado existente, selecciónelo y haga clic en **Eliminar**.

No puede eliminar un predicado si está asociado a alguna configuración.
