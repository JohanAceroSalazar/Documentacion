# ADR-001: Implementación de dominio de notificaciones

## Contexto
El sistema actual no contempla comunicación con usuarios.

## Problema
No hay forma de enviar alertas de vuelos, pagos o reservas.

## Decisión
Crear un nuevo dominio "notification" con:
- notification
- notification_type
- notification_channel

## Justificación
Permite mejorar experiencia del usuario y comunicación en tiempo real.

## Consecuencias
+ Mejor UX
+ Mayor complejidad en el sistema