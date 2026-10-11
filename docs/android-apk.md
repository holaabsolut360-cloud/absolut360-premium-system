# APK de prueba para Android

## Generación automática

El flujo de GitHub Actions compila un APK de depuración cuando hay un push a main. También admite ejecución manual desde la pestaña Actions mediante “Build Android demo APK” y “Run workflow”.

Al finalizar, descarga el archivo del bloque Artifacts de esa ejecución:

- Artefacto: absolut360-premium-debug-apk
- APK: app-debug.apk

El artefacto expira a los 14 días. Para instalarlo, descarga el ZIP, extrae el APK y ábrelo en el dispositivo Android. Android puede pedir autorización para instalar desde esa fuente.

## Alcance de la app

Es una envoltura Capacitor de la demostración web actual. Los datos se guardan localmente en el dispositivo. No hay autenticación real, servidor, sincronización multiempresa, pagos ni comprobantes fiscales. No usar con ventas reales ni guardar información sensible.

## Firma

El APK generado es una build debug firmada con la clave temporal de depuración del proceso Android/Gradle. Sirve para pruebas y no para publicar en Play Store. La publicación requiere una clave de firma propia y resguardada en GitHub Secrets, junto con una revisión de privacidad, seguridad y cumplimiento.