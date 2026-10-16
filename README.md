# Agenda Salones

Bot de WhatsApp que agenda, cancela y recuerda citas 24/7 para salones de belleza y consultorios odontológicos, con panel web de agenda, caja y comisiones.

![Agenda del día](01-agenda.png)

## Problema que resuelve

Los negocios pequeños pierden tiempo y clientes respondiendo WhatsApp a mano para agendar, y sufren inasistencias. Agenda Salones atiende a los clientes 24/7: muestra servicios y profesionales, ofrece horarios libres y agenda, cancela o reprograma la cita sin intervención humana.

## Funciones

- Bot de WhatsApp con menús interactivos y notas de voz (transcripción con IA).
- Recordatorios automáticos con botones Confirmar / Cancelar para reducir inasistencias.
- Recordatorio de retoque o control cuando se cumplen los días del servicio.
- Pausa del bot para que una persona tome la conversación.
- Panel web: agenda en tiempo real, caja diaria con cierre y cuadre, comisiones por profesional, clientes, servicios por categorías, bloqueos de horario y reportes de ventas.
- QR por profesional para compartir su link de agenda.
- Multi-negocio: cada negocio conecta su propio número de WhatsApp y sus datos quedan aislados.
- Variante para odontología con vocabulario propio, sin duplicar código.

## Así se ve

### Agendamiento por WhatsApp
![Conversación del bot](02-whatsapp.png)

### Flujo del bot en n8n
![Flujo en n8n](03-flujo-n8n.png)

### Caja diaria y comisiones
![Caja diaria](04-caja.png)

## Tecnologías

| Capa | Herramienta |
|---|---|
| Orquestación | n8n self-hosted en VPS con Docker |
| Mensajería | WhatsApp Cloud API de Meta |
| Base de datos | Supabase (PostgreSQL, autenticación, Row Level Security) |
| Pruebas | 172 verificaciones automatizadas en la base de datos |
| Panel web | React + Vite + Tailwind CSS |
| IA | OpenRouter (transcripción de audios e interpretación de respuestas) |
| Correos | Gmail API (cierres de caja y alertas) |

## Contenido de este repositorio

- `n8n/salones-bot.json`: flujo principal del bot, sin credenciales ni datos reales.
- Capturas del sistema funcionando con datos de prueba.

El código del panel web y la base de datos es privado. Este repositorio es una muestra del proyecto.

---

Desarrollado por **Carlos Solano** · Automatización con n8n e IA · Medellín, Colombia
