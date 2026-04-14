# ADR-002: Estrategia de roles y permisos

## Contexto
Existe estructura básica de roles.

## Problema
No hay jerarquía ni control granular avanzado.

## Decisión
Implementar RBAC completo:
- Roles predefinidos (ADMIN, AGENT, CUSTOMER)
- Permisos por módulo

## Justificación
Escalabilidad y seguridad.

## Consecuencias
+ Mayor control
- Más complejidad en gestión