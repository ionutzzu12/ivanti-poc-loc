---
title: Transparencia del certificado
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

**Aplicable a:** iOS 12.1.1, macOS 10.14.2, tvOS 12.1.1, watchOS 10.0+, visionOS 1.1+ y versiones más recientes compatibles.

Controla que se cumpla la transparencia del certificado, que solo puede aparecer en el perfil del dispositivo. Puede incluir múltiples certificados y desactivar dominios según sea necesario.

## Creación de la configuración de la transparencia del certificado

**Procedimiento**

1. Seleccione **Configuraciones**.
2. Haga clic en **+Añadir**.
3. Escriba **certificado** en el campo de búsqueda y, a continuación, haga clic en la configuración de la **Transparencia del certificado**.
4. Introduzca un nombre y describa la configuración.
5. Especifique los **Dominios que se desactivarán**. Haga clic en **+ Añadir dominio** para añadir más de un dominio. Se puede usar un punto inicial para hacer coincidir subdominios, no obstante, una regla de coincidencia de dominios no debe coincidir con todos los dominios de un dominio de nivel superior. Por ejemplo, están permitidos «.ejemplo.com» y «.example.co.uk», mientras que «.com» y «.co.uk» no están permitidos. No se admiten los dominios de comodines.
6. Especifique el **Hash del certificado**después de seleccionar un algoritmo (SHA 256). Haga clic en **+ Añadir&#x20;**&#x70;ara añadir más de un hash del certificado.
7. Haga clic en **Siguiente** para configurar los ajustes de distribución.
8. Haga clic en **Hecho**.

Para generar los datos especificados por la clave hash en el diccionario subjectPublicKeyInfo, utilice el siguiente comando para un certificado cifrado con PEM:

`openssl x509 -pubkey -in example_certificate.pem -inform pem | openssl pkey -pubin - outform der | openssl dgst -sha256 -binary | base64`

Si su certificado está codificado mediante DER, use el siguiente comando:

`openssl x509 -pubkey -in example_certificate.der -inform der | openssl pkey -pubin - outform der | openssl dgst -sha256 -binary | base64`
