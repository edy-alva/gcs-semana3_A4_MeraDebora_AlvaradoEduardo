# RF-026 – Seguimiento del Prestador de Servicios


## Casos de prueba

| ID | Caso de prueba | Resultado esperado | Resultado |
|---|---|---|---|
| CP-001 | Usuario solicita un servicio | La solicitud se registra correctamente | PASS |
| CP-002 | Prestador acepta el servicio | El sistema asigna el servicio al prestador | PASS |
| CP-003 | Se inicia el desplazamiento | El seguimiento se activa | PASS |
| CP-004 | Prestador cambia de ubicación | El mapa actualiza su posición | PASS |
| CP-005 | Usuario consulta ubicación | Se muestra la ubicación aproximada del prestador | PASS |
| CP-006 | Se pierde temporalmente GPS | Se muestra la última ubicación conocida | PASS |
| CP-007 | Prestador llega al destino | El sistema actualiza el estado del servicio | PASS |
| CP-008 | Servicio finalizado | El seguimiento deja de actualizarse | PASS |
| CP-009 | Usuario no autorizado intenta consultar ubicación | El sistema rechaza el acceso | PASS |
| CP-010 | Prestador cancela el servicio | Se detiene el seguimiento | PASS |


## Pruebas de seguridad

| ID | Prueba | Resultado esperado |
|---|---|---|
| SEG-001 | Acceder a ubicación sin autenticación | Acceso rechazado |
| SEG-002 | Usuario consulta ubicación de otro servicio | Acceso rechazado |
| SEG-003 | Consultar ubicación después de finalizar el servicio | Información no actualizada |
| SEG-004 | Transmitir información de ubicación | Comunicación protegida |
| SEG-005 | Manipular identificador del servicio | El sistema rechaza la solicitud no autorizada |