# V5: Requerimientos de Comunicación a través de la red

## Objetivo de Control

Los controles enumerados en esta categoría tienen por objetivo asegurar la confidencialidad e integridad de la información intercambiada entre la aplicación móvil y los servicios del servidor. Como mínimo se deben utilizar canales seguros y cifrados utilizando el protocolo TLS con las configuraciones apropiadas. En el nivel 2 se establecen medidas en profundidad como fijación de certificados SSL.

## Requerimientos de Verificación de Seguridad

| # | MSTG-ID | Descripción | L1 | L2 |
| --- | --- | --- | --- | --- |
| **5.1** | MSTG‑NETWORK‑1 | La información es enviada cifrada utilizando TLS. El canal seguro es usado consistentemente en la aplicación. | ✓ | ✓ |
| **5.2** | MSTG‑NETWORK‑2 | Las configuraciones del protocolo TLS siguen las mejores prácticas de la industria, o lo hacen lo mejor posible en caso de que el sistema operativo del dispositivo no soporte los estándares recomendados. | ✓ | ✓ |
| **5.3** | MSTG‑NETWORK‑3 | La aplicación verifica el certificado X.509 del sistema remoto al establecer el canal seguro y sólo se aceptan certificados firmados por una CA de confianza. | ✓ | ✓ |
| **5.4** | MSTG‑NETWORK‑4 | La aplicación utiliza su propio almacén de certificados o realiza _pinning_ del certificado o la clave pública del servidor. Bajo ningún concepto establecerá conexiones con servidores que ofrecen otros certificados o claves, incluso si están firmados por una CA de confianza. |   | ✓ |
| **5.5** | MSTG‑NETWORK‑5 | La aplicación no depende de un único canal de comunicaciones inseguro (email o SMS) para operaciones críticas como registro de usuarios o recuperación de cuentas. |  | ✓ |
| **5.6** | MSTG‑NETWORK‑6 | La aplicación sólo depende de bibliotecas de conectividad y seguridad actualizadas. |  | ✓ |

<div style="page-break-after: always;">
</div>

## Referencias

La Guía de Pruebas de Seguridad Móvil de OWASP proporciona instrucciones detalladas para verificar los requisitos listados en esta sección.

- Android - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05g-Testing-Network-Communication.md>
- iOS - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06g-Testing-Network-Communication.md>

Para más información, ver también:

- OWASP Top 10 Móvil: M3 (Comunicación Insegura) - <https://www.owasp.org/index.php/Mobile_Top_10_2016-M3-Insecure_Communication>
- CWE 319 (Transmisión en Claro de Información Sensible) - <https://cwe.mitre.org/data/definitions/319.html>
- CWE 295 (Validación Inapropiada de Certificados) - <https://cwe.mitre.org/data/definitions/295.html>
