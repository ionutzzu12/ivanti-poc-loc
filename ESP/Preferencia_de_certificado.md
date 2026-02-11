---
title: Preferencia de certificado
createdAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:06 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** macOS 10.12 o versiones más recientes compatibles.

Identifique un elemento de Preferencia de certificado en la llave del usuario que haga referencia a una carga útil del certificado incluida en el mismo perfil.

Esta función se utiliza para enlaza un certificado a una dirección de correo electrónico o a una URL. Después de enlazar un certificado a una dirección de correo electrónico, la aplicación Mail lo usará para esa cuenta de correo electrónico. Si el Certificado SSL para un sitio web no es de confianza, al añadir una preferencia de Certificado se garantizará que en el explorador no aparece un mensaje de advertencia cuando se intenta acceder al sitio web.

## Creación de la configuración de una preferencia de certificado

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **preferencia** en el campo de búsqueda y, a continuación, haga clic en la configuración de las **Preferencia de certificado**.
4. Asigne un nombre a la configuración y descríbala.
5. Dentro de la sección Ajuste de la configuración, en el campo **Nombre**, introduzca una Id. de correo electrónico o el nombre para el que se solicita un certificado preferido.
6. En el campo **UUID del certificado**, seleccione un certificado.
7. Haga clic en **Siguiente** para configurar los ajustes de distribución.
8. Haga clic en **Listo**.

**Temas relacionados:**

- [**Preferencia de identidad**](./Preferencia_de_identidad.md)
