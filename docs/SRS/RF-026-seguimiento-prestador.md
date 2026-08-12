# RF-026 – Seguimiento del Prestador de Servicios

## 1. Información general

| Campo | Información |
|---|---|
| **ID del requisito** | RF-026 |
| **Nombre** | Seguimiento del prestador de servicios |
| **Proyecto** | SOS911 |
| **Tipo** | Requisito funcional |
| **Prioridad** | Alta |
| **Estado** | Aprobado |
| **Versión** | 1.0 |
| **Fecha de creación** | 11/08/2026 |
| **Solicitud de cambio asociada** | CR-004-SOS911 |

---

## 2. Descripción

El sistema deberá permitir al usuario realizar el seguimiento del prestador de servicios asignado durante su desplazamiento hacia el lugar de atención.

La funcionalidad deberá mostrar la ubicación aproximada del prestador mediante información de geolocalización, el estado actual del servicio y el tiempo estimado de llegada.

---

## 3. Objetivo

Proporcionar al usuario información actualizada sobre el desplazamiento del prestador de servicios, permitiendo conocer su ubicación aproximada y el estado del servicio solicitado.

---

## 4. Justificación

Actualmente, el usuario puede solicitar un servicio técnico y conocer información relacionada con la solicitud y el prestador asignado.

Sin embargo, no dispone de información sobre la ubicación del prestador durante su desplazamiento hacia el lugar de atención.

La incorporación de esta funcionalidad permitirá mejorar la experiencia del usuario, proporcionar mayor transparencia durante la atención y facilitar el seguimiento del servicio solicitado.

---

## 5. Actores involucrados

| Actor | Responsabilidad |
|---|---|
| **Usuario** | Consultar la ubicación y estado del prestador asignado. |
| **Prestador de servicios** | Compartir periódicamente su ubicación durante el desplazamiento. |
| **Aplicación móvil** | Capturar y mostrar la información de ubicación. |
| **API REST** | Recibir, procesar y proporcionar la información de ubicación. |
| **Sistema** | Controlar el inicio, actualización y finalización del seguimiento. |

---

## 6. Precondiciones

Para que el seguimiento pueda iniciarse se deberán cumplir las siguientes condiciones:

1. El usuario debe haber solicitado un servicio.
2. El sistema debe haber asignado un prestador.
3. El prestador debe haber aceptado la solicitud.
4. El dispositivo del prestador debe disponer de permisos de ubicación.
5. El servicio de geolocalización debe encontrarse disponible.
6. El prestador debe encontrarse en estado de desplazamiento hacia el lugar de atención.

---

## 7. Flujo principal

El funcionamiento esperado será el siguiente:

```text
Usuario solicita servicio
          ↓
Sistema asigna prestador
          ↓
Prestador acepta servicio
          ↓
Sistema inicia seguimiento
          ↓
Prestador obtiene ubicación
          ↓
Aplicación envía ubicación a la API
          ↓
API procesa y almacena la ubicación
          ↓
Usuario consulta seguimiento
          ↓
Aplicación muestra ubicación aproximada
          ↓
Prestador continúa desplazamiento
          ↓
Sistema actualiza ubicación
          ↓
Prestador llega al destino
          ↓
Sistema finaliza seguimiento