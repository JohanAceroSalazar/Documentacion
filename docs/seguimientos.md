# Seguimiento del Proyecto

## Estado general
Proyecto en desarrollo de base de datos estructurada por dominios.

---

## Progreso por dominio

| Dominio              | Estado       | Observaciones |
|----------------------|--------------|--------------|
| Geografía            | ✅ Completo  | OK |
| Aerolínea            | ✅ Completo  | OK |
| Identidad            | ✅ Completo  | OK |
| Seguridad            | ✅ Completo  | OK |
| Clientes             | ✅ Completo  | OK |
| Aeropuerto           | ✅ Completo  | OK |
| Aeronaves            | ✅ Completo  | OK |
| Vuelos               | ✅ Completo  | OK |
| Ventas               | ✅ Completo  | OK |
| Abordaje             | ✅ Completo  | OK |
| Pagos                | ✅ Completo  | OK |
| Facturación          | ✅ Completo  | OK |
| Notificaciones       | ✅ Completo  | OK |

---

## Problemas encontrados

- Orden de ejecución de FK entre dominios
- Dependencias cruzadas entre tablas
- Validación de constraints

---

## Soluciones aplicadas

- Separación por dominios
- Creación ordenada de tablas
- Uso de Liquibase para control de cambios

---

## Próximos pasos

- Crear inserts de prueba
- Validar integridad completa
- Crear roles y permisos (DCL)
- Probar eliminación de tablas en orden correcto

---

## Notas

- Mantener consistencia en nombres
- No modificar estructura sin control de versiones
- Validar cada dominio antes de continuar