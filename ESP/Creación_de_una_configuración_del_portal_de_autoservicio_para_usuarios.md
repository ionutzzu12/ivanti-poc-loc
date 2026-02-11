---
title: Creación de una configuración del portal de autoservicio para usuarios
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Como usuario de la empresa, puede utilizar el portal de autoservicio para gestionar sus dispositivos y certificados. La pestaña Mis dispositivos muestra los dispositivos que ha registrado.

Puede realizar las siguientes tareas desde la pestaña Mis dispositivos:

- Bloquear
- Desbloquear
- Retirar
- Restablecer código de acceso de Aplicaciones seguras

Puede realizar las siguientes tareas desde la pestaña Mis certificados:

- Cargar certificado

Puede distribuir hasta un máximo de 100 archivos de configuración a la vez.

**Procedimiento**

1. Inicie sesión en el portal del administrador de Ivanti Neurons for MDM
2. Haga clic en **Añadir**.
3. Busque **Crear configuración de portal de autoservicio para usuarios**.
4. Haga clic en **Siguiente**.
5. Si no desea que esta configuración quede inmediatamente habilitada, deseleccione la opción **Habilitar esta configuración**.
6. Seleccione un nivel de distribución para la configuración:\* **Todos los dispositivos**: distribuir la configuración a todos los dispositivos disponibles. Para delegar configuraciones entre espacios, seleccione una de las siguientes opciones:- **No aplicar a los otros espacios**.
   - Para delegar configuraciones en los espacios, seleccione **Resumen de distribución**>**&#x20;Aplicar a todos los dispositivos en los espacios de otros dispositivos**.\* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores del espacio delegados editen la distribución para el espacio específico.
   - **Sin dispositivos** : seleccione esta configuración para la distribución en un momento posterior.
   - **Predeterminada** : se definen conjuntos específicos de grupos de dispositivos a los que se enviará esta configuración. Para delegar configuraciones entre espacios, seleccione una de las siguientes opciones:\* **No aplicar a los otros espacios**.
     - **Resumen de la distribución&#x20;**>**&#x20;Aplicar a los dispositivos de otros espacios**.\* Seleccione la casilla de verificación **Permitir que el administrador del espacio edite la distribución** para permitir que los administradores delegados del espacio editen la distribución para el espacio específico.
7. Si su servicio tiene espacios definidos, especifique si la configuración debe aplicarse a los demás espacios y la prioridad.
8. Haga clic en **Hecho**.

Para configuraciones que ejecutan un comando para el dispositivo en lugar de instalar un perfil en el dispositivo, los detalles de configuración no mostrarán la configuración como aplicada a ningún dispositivo.
