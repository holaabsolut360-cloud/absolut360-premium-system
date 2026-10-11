# Plan MVP — Absolut360 Premium System

## Alcance

Crear un producto con identidad comercial, diseño, código y datos propios. El APK de AlToke será una referencia funcional observada mediante uso autorizado. No extraer ni reutilizar código, credenciales, tokens, llaves, endpoints privados ni recursos protegidos.

## Módulos

1. SaaS multiempresa, sucursales, usuarios y roles.
2. POS con catálogo, carrito, pagos, comprobante e historial.
3. Inventario con SKU, precios, costos, existencias por sucursal y movimientos.
4. Caja con apertura, entradas/salidas justificadas, conciliación y cierre.
5. Historial auditable de ventas, caja, stock y administración.
6. Planes públicos: mensual S/19.99, trimestral S/49.99, anual S/179.99.
7. Licencia única interna S/5,000, asignada manualmente solo por superadministrador.

## Modelo sugerido

Tenant, Branch, User, Membership, Product, StockBalance, StockMovement, Sale, SaleLine, Payment, CashSession, CashMovement, Subscription, LicenseGrant y AuditEvent.

Los datos de negocio deben llevar tenant_id. El servidor valida membresía y permisos en cada operación; ocultar controles de interfaz no protege datos. Guardar dinero en céntimos PEN. Registrar anulaciones mediante eventos compensatorios, sin borrar ventas originales.

## Etapas

- Fundación: elegir backend/base de datos, autenticación, empresas, sucursales, roles y migraciones.
- Ciclo POS: catálogo y stock → caja abierta → venta y pago → actualización atómica → comprobante → historial.
- Administración: suscripciones, empresas y concesión auditada de licencia interna.
- Operación segura: respaldos, monitoreo, revisión de permisos, pruebas de aislamiento, requisitos tributarios peruanos y despliegue.

## Decisiones pendientes

Backend y alojamiento, modo offline, impuestos y comprobantes, pagos, integración tributaria, impresoras/lectores y reglas de renovación. El prototipo inicial no implementa estos servicios.