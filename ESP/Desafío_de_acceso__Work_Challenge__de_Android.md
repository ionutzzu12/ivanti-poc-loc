---
title: Desafío de acceso (Work Challenge) de Android
createdAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
updatedAt: Wed Feb 11 2026 17:29:05 GMT+0200 (Eastern European Standard Time)
---

Esta sección contiene el siguiente tema:

- [**Crear una configuración del Desafío de acceso (Work Challenge) de Android:**](./Desafío_de_acceso__Work_Challenge__de_Android.md)
- [**Ajustes del establecimiento de la configuración**](./Desafío_de_acceso__Work_Challenge__de_Android.md)

**Licencia**: Silver

La configuración del Desafío de acceso (Work Challenge) de Android define las contraseñas seguras para que los usuarios accedan a los datos y las aplicaciones del Perfil de trabajo. Requiere el perfil de trabajo de Android Enterprise.

Notas sobre la implementación:

- Los administradores pueden aplicar una política de contraseña del dispositivo y otra política de contraseña del perfil de trabajo de forma independiente.
- Ivanti Neurons for MDM no enviará esta configuración a los clientes con una versión anterior a Android 7.0 porque tales dispositivos no admiten esta característica.
  Ivanti Neurons for MDM solo envía esta configuración a los dispositivos con un perfil de trabajo empresarial Android.

## Crear una configuración del Desafío de acceso (Work Challenge) de Android:

**Procedimiento**

1. Haga clic en **Configuraciones**.
2. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/U6DZaRCOhB4SHlN8pvBaC_r43workchallenge001.png" alt caption}
   Haga clic en **+Añadir**.
3. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/uOl7lzAHI5nQiqviYudT4_r43workchallenge002.jpg" alt caption}
   Escriba "work" ("trabajo") en el campo de búsqueda.
4. Seleccione la configuración **Desafío de acceso (Work Challenge) de Android**.
5. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/hQtWtgYU0W3rjtV5N5uyA_r44workchallenge003.png" alt caption}
   Introduzca un nombre para la configuración y, si lo desea, una descripción.
6. Utilice los campos de Ajustes de la configuración para crear la configuración. Consulte [**Ajustes del establecimiento de la configuración**](./Desafío_de_acceso__Work_Challenge__de_Android.md) para ver detalles sobre los ajustes.
7. Haga clic en **Siguiente ->**.
8. :inlineImage[]{src="https://archbee-image-uploads-qa.s3.amazonaws.com/yzXkkCTORWlcwRG_AVHKZ/kcqA31riKbHP9hF3GwoVy_r43workchallenge004.png" alt caption}
   Habilite la configuración si fuera necesario.
9. Configure los ajustes de distribución para todos los dispositivos, ningún dispositivo o un conjunto personalizado
10. Haga clic en **Hecho**.

## Ajustes del establecimiento de la configuración

| **Ajuste**                                                  | **Qué hacer**                                                                                                                                        |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nombre                                                      | Introduzca un nombre que identifique a esta configuración.                                                                                           |
| Descripción                                                 | Introduzca una descripción que explique la finalidad de esta configuración.                                                                          |
| Activar cualquier método de bloqueo                         | Permitir que el usuario elija cualquier método de bloqueo, incluido el desbloqueo mediante patrón. Anula cualquier otro ajuste del código de acceso. |
| Longitud mínima del código de acceso                        | Seleccione una longitud mínima del código de acceso, de 4 a 16 caracteres.                                                                           |
| Permitir valores simples                                    | Habilite esta opción para permitir que el código de acceso tenga secuencias de caracteres repetidos, ascendentes o descendentes.                     |
| Requerir valor alfanumérico                                 | Habilite esta opción para requerir que el código de acceso tenga al menos una letra y un número.                                                     |
| Características de caracteres complejos y tipo de elementos | Configure los requisitos de los caracteres complejos y los tipos de elemento, que varían entre:\* Ninguno                                            |

- Un carácter no alfanumérico como mínimo
- 2 caracteres no alfanuméricos como mínimo
- 3 caracteres no alfanuméricos como mínimo
- 4 caracteres no alfanuméricos como mínimo |
  \| Desbloqueo de huella digital                                | Habilite esta opción para permitir que los usuarios desbloqueen sus dispositivos con su huella digital.                                                                                                                                                                                |
  \| Antigüedad máxima del código de acceso                      | Configure una antigüedad máxima para la contraseña, desde ninguna hasta 730 días.                                                                                                                                                                                                      |
  \| Autobloqueo                                                 | Seleccione un período de tiempo después del cual el dispositivo se autobloquea. Los períodos de tiempo varían de nunca a quince minutos.                                                                                                                                               |
  \| Historial del código de acceso                              | Especifique el número de códigos de acceso exclusivos necesarios antes de que se permita volver a usar el código de acceso, que varía de ninguno a 50 códigoa de acceso.                                                                                                               |
  \| Número máximo de intentos erróneos                          | Seleccione el número máximo de intentos erróneos. **ADVERTENCIA: Ivanti Neurons para MDM borra los dispositivos para los que el usuario supera el número máximo de intentos de contraseña.**                                                                                           |
