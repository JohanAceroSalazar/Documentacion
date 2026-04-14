# ADR-005: Contenerización del sistema

## Contexto
Se requiere despliegue reproducible.

## Problema
Difícil levantar entorno manualmente.

## Decisión
Usar Docker:
- PostgreSQL container
- Liquibase container

## Justificación
Portabilidad y facilidad de despliegue.

## Consecuencias
+ Entorno consistente
+ Fácil onboarding