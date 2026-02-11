---
title: Configuración para eliminar el «bloatware»
createdAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:07 GMT+0200 (Eastern European Standard Time)
---

La configuración para eliminar el «bloatware» le permite seleccionar la lista de aplicaciones instaladas en dispositivos que deben eliminarse obligatoriamente. Para esta configuración, es un requisito previo tener una configuración de Bridge. Vaya a [**Bridge**](./Ivanti_Bridge.md) para obtener más detalles.

Para ejecutar o desinstalar aplicaciones:

1. En la pestaña **Configuración**, haga clic en **+Añadir**.
2. Seleccione la configuración de **Eliminar el «bloatware»**. Aparecerá la página **Configuración para eliminar el «bloatware»**.
3. En el campo **Nombre**, introduzca un nombre adecuado para la configuración.
4. Haga clic en el enlace +**Añadir descripción** para añadir una descripción de la configuración. Este campo es opcional.
5. En la sección **Ajuste de la configuración**, seleccione las aplicaciones que deben eliminarse o desinstalarse. Como alternativa, también puede buscar una aplicación en el campo de búsqueda mediante el nombre de la aplicación que aparece en la lista de aplicaciones de escritorio.Antes de crear la configuración para **eliminar el bloatware**, debe recuperar las aplicaciones en **Aplicaciones > Aplicaciones de escritorio > Recuperar aplicaciones.** De lo contrario, no habrá aplicaciones disponibles para buscar o elegir cuando se cree la configuración para **eliminar el bloatware**.Se pueden eliminar los tipos de archivo .appx, .appxbundles, .xap y .msi, pero no los .exe.
6. En las opciones avanzadas, configure las siguientes opciones:|                                                       |                                                                                                        |
   \| ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
   \| Opción                                                | Descripción                                                                                            |
   \| **Ejecutar esta configuración cada**                  | Establezca la duración del intervalo (en minutos) después de la cual debe ejecutarse la configuración. |
   \| **Ejecutar al iniciar sesión**                        | Seleccione esta casilla para ejecutar la configuración cuando se inicie sesión.                        |
   \| **Anular el reinicio forzoso tras la desinstalación** | Seleccione esta casilla para evitar un reinicio obligatorio después de desinstalar la aplicación.      |
