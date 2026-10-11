# Absolut360 Premium System

Base independiente del MVP de gestión comercial Absolut360.

## Incluye

- Prototipo web interactivo de resumen, POS, inventario, caja, historial, planes y licencias.
- Planes públicos: mensual **S/19.99**, trimestral **S/49.99** y anual **S/179.99**.
- Licencia única interna de **S/5,000**, asignable manualmente solo por superadministración.
- Datos demo guardados localmente en el navegador.
- Envoltura Android Capacitor y flujo de GitHub Actions para compilar un APK de prueba.

## Probar la web

Abre index.html en un navegador moderno. No requiere instalación ni dependencias.

## Obtener el APK

Cada push a main ejecuta el flujo **Build Android demo APK**. Al terminar correctamente, abre la ejecución en **Actions** y descarga el artefacto `absolut360-premium-debug-apk`. El ZIP incluye `app-debug.apk`. El artefacto dura 14 días.

Consulta [las instrucciones de Android](docs/android-apk.md).

## Límites

Esto es una demostración frontend, no un SaaS listo para producción. No incluye servidor, autenticación, aislamiento real entre empresas, sincronización, cobros, respaldos ni comprobantes fiscales. El almacenamiento local no es una barrera de seguridad y puede borrarse desde el navegador.

El APK de prueba usa datos locales, no procesa pagos y no es para ventas reales ni publicación en Play Store. No contiene código, secretos, credenciales, claves ni recursos propietarios recuperados del APK de referencia. La revisión directa del APK y del video sigue pendiente.

Consulta [el plan](docs/plan.md) y [el estado de revisión](docs/reference-review.md).