# ADR-003: Implementación de Liquibase

## Contexto
El DDL está en un solo script.

## Problema
No hay control de versiones.

## Decisión
Usar Liquibase con:
- changelog-master.xml
- changelogs por dominio

## Justificación
Permite versionamiento y despliegue controlado.

## Consecuencias
+ Control total de cambios
+ Auditoría