# Documentación del Cambio CR-004-SOS911

## 1. Información general

| Campo | Información |
|---|---|
| **ID del cambio** | CR-004-SOS911 |
| **Proyecto** | SOS911 |
| **Tipo de cambio** | Funcional |
| **Prioridad** | Alta |
| **Fecha de solicitud** | 11/08/2026 |
| **Solicitante** | Product Owner |
| **Estado** | Cerrado |
| **Versión anterior** | v1.1.0 |
| **Nueva versión** | v1.2.0 |
| **Requisito asociado** | RF-026 |
| **Issue GitHub** | #4 |
| **Pull Request** | #25 |
| **Tag** | v1.2.0 |

---

## 2. Descripción del cambio

Se incorporó una funcionalidad de seguimiento en tiempo real del prestador de servicios asignado.

La funcionalidad permite al usuario consultar la ubicación aproximada del prestador durante su desplazamiento hacia el lugar de atención.

Además, el sistema permite visualizar información relacionada con el estado del servicio y el tiempo estimado de llegada (ETA), cuando esta información se encuentra disponible.

---

## 3. Motivo del cambio

El cambio fue solicitado con el propósito de mejorar la experiencia del usuario durante la atención del servicio.

La funcionalidad permite:

- Conocer la ubicación aproximada del prestador.
- Realizar seguimiento durante el desplazamiento.
- Consultar el estado actual del servicio.
- Obtener información sobre el tiempo estimado de llegada.
- Mejorar la transparencia durante la atención.
- Facilitar la comunicación entre usuario y prestador.

---

## 4. Situación anterior

Antes de implementar el cambio, el usuario podía solicitar un servicio y recibir información relacionada con el prestador asignado.

Sin embargo, no disponía de una funcionalidad que permitiera visualizar la ubicación del prestador durante su desplazamiento hacia el lugar de atención.

Por este motivo, se identificó la necesidad de incorporar un mecanismo de seguimiento mediante geolocalización.

---

## 5. Situación posterior al cambio

Después de implementar el cambio, el sistema permite iniciar el seguimiento cuando el prestador acepta el servicio y comienza su desplazamiento.

El prestador transmite periódicamente su ubicación mediante la aplicación móvil.

La API recibe y procesa la información, mientras que la aplicación del usuario consulta la posición y la muestra mediante un mapa.

El seguimiento finaliza cuando el servicio termina o es cancelado.

---

## 6. Requisito relacionado

### RF-026 – Seguimiento del prestador de servicios

El sistema deberá permitir al usuario visualizar la ubicación aproximada del prestador de servicios asignado durante su desplazamiento hacia el lugar de atención, mostrando además el estado del servicio y el tiempo estimado de llegada.

**Documento relacionado:**

`docs/requisitos/RF-026-seguimiento-prestador.md`

---

## 7. Flujo implementado

```text
Usuario solicita servicio
          ↓
Sistema asigna prestador
          ↓
Prestador acepta
          ↓
Se inicia seguimiento
          ↓
Prestador obtiene ubicación
          ↓
Aplicación envía ubicación
          ↓
API recibe ubicación
          ↓
Sistema actualiza posición
          ↓
Usuario consulta mapa
          ↓
Prestador llega al destino
          ↓
Finaliza seguimiento