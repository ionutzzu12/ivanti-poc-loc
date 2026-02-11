---
title: Preparación para la compatibilidad con un dispositivo de Android Enterprise
createdAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:03 GMT+0200 (Eastern European Standard Time)
---

Esta sección describe los requisitos de red mínimos para dispositivos de Android Enterprise. Los dispositivos Android generalmente no requieren que abra puertos de entrada en el cortafuegos para funcionar correctamente. No obstante, hay una serie de conexiones de salida que los administradores deben conocer cuando ajustan sus entornos de red para los dispositivos de Android Enterprise.

La lista de cambios en la red que figura en el siguiente cuadro no es exhaustiva y puede cambiar. Cubre los puntos finales conocidos para las versiones actuales y pasadas de las aplicaciones de gestión empresarial API y GMS.

Además de los puestos que se listan en la tabla siguiente, los dispositivos de Android Enterprise requieren acceso a Ivanti Neurons for MDM.

Para obtener información sobre los requisitos de los dispositivos Android Enterprise, consulte [**Requisitos de red para Android Enterprise**](https://support.google.com/work/android/answer/10513641?hl=en) de la Ayuda de Android Enterprise.

Google no proporciona IP específicas, por lo que debe permitir que su cortafuegos acepte conexiones salientes a todas las direcciones IP contenidas en el bloque IP que aparece en el ASN de Google de 15169 que se enumera aquí: [**http://bgp.he.net/AS15169#\_prefixes**](http://bgp.he.net/AS15169#_prefixes).

Las IP de los puntos de Google y los nodos de Edge no aparecen en los bloques AS15169. Consulte [**https://peering.google.com/**](https://peering.google.com/) para obtener más información sobre la red Edge de Google.
