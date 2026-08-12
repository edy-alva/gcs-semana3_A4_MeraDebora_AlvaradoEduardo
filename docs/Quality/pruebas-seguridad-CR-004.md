# RF-026 – Seguimiento del Prestador de Servicios

## Pruebas de seguridad

| ID | Prueba | Resultado esperado |
|---|---|---|
| SEG-001 | Acceder a ubicación sin autenticación | Acceso rechazado |
| SEG-002 | Usuario consulta ubicación de otro servicio | Acceso rechazado |
| SEG-003 | Consultar ubicación después de finalizar el servicio | Información no actualizada |
| SEG-004 | Transmitir información de ubicación | Comunicación protegida |
| SEG-005 | Manipular identificador del servicio | El sistema rechaza la solicitud no autorizada |