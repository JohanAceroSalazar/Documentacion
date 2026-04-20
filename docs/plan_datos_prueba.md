# Plan de Datos de Prueba

## Objetivo
Definir los datos mínimos necesarios para validar la creación y funcionamiento de las tablas por dominio en la base de datos.

---

## Estrategia

Los datos se insertarán siguiendo el mismo orden de dependencias de los dominios:

1. Geografía
2. Aerolínea
3. Identidad
4. Seguridad
5. Clientes
6. Aeropuerto
7. Aeronaves
8. Vuelos
9. Ventas
10. Abordaje
11. Pagos
12. Facturación
13. Notificaciones

---

## Datos mínimos por dominio

### 1. Geografía
- 1 continente
- 1 país
- 1 estado
- 1 ciudad
- 1 distrito
- 1 dirección
- 1 zona horaria
- 1 moneda

---

### 2. Aerolínea
- 1 aerolínea asociada a país

---

### 3. Identidad
- 1 persona
- 1 tipo de documento
- 1 documento
- 1 contacto

---

### 4. Seguridad
- 1 estado de usuario
- 1 rol (ADMIN)
- 1 permiso
- 1 usuario
- asignación de rol

---

### 5. Clientes
- 1 cliente
- 1 programa de fidelización
- 1 cuenta de millas

---

### 6. Aeropuerto
- 1 aeropuerto
- 1 terminal
- 1 puerta

---

### 7. Aeronaves
- 1 fabricante
- 1 modelo
- 1 aeronave

---

### 8. Vuelos
- 1 vuelo
- 1 segmento

---

### 9. Ventas
- 1 reserva
- 1 ticket

---

### 10. Abordaje
- 1 check-in
- 1 boarding pass

---

### 11. Pagos
- 1 pago
- 1 transacción

---

### 12. Facturación
- 1 factura
- 1 línea de factura

---

### 13. Notificaciones
- 1 notificación
- 1 envío

---

## Ubicación de scripts

Cada dominio debe tener su propio archivo:
- `001-geography-inserts.sql`
- `002-airline-inserts.sql`
- etc.

---

## Validación

Después de insertar:
- Ejecutar SELECT por tabla
- Validar integridad de FK
- Validar constraints