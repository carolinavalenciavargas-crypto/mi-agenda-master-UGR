# Mi agenda · Máster UGR

Agenda adaptable a ordenador y móvil, sin dependencias de producción. Incluye 224 sesiones de 19 asignaturas extraídas de `Calendario UGR.pdf` (21/09/2026–26/05/2027), con sesiones de 16:30–18:30 y 18:30–20:30 según el documento. Conserva la excepción del 27/10/2026 (EGVCSR / EGGSI) y los periodos de vacaciones.

## Ejecutar

Desde este directorio:

```sh
python3 -m http.server 8000 --bind 0.0.0.0
```

Abrir la aplicación en un navegador servido por HTTP. No necesita instalación, base de datos ni credenciales.

## Funciones

- Calendario mensual, semanal y diario, filtro por asignatura y búsqueda.
- Registro manual de trabajos, seminarios, foros, exposiciones y entregas de PRADO.
- Crear, editar y eliminar actividades y clases; marcar actividades completadas.
- Adjuntar y descargar documentos (5 MB máximo por archivo, sujetos al espacio local).
- Recordatorios en pantalla y notificaciones con autorización mientras la página esté abierta. Horario de entregas de Granada (`Europe/Madrid`). No hay avisos con la aplicación cerrada.
- Exportar/importar copia JSON con actividades y documentos para trasladarla a otro dispositivo.

Los datos se guardan en `localStorage`, por navegador y origen. No existe sincronización entre dispositivos ni conexión automática a PRADO. El PDF aporta horarios de clases, no fechas de entregas. Usa copias de seguridad antes de borrar datos del navegador. La fuente web es opcional; hay una alternativa local sans-serif.

## Validación

```sh
node --check app.js
node --check data.js
```

Comprobar en navegador las vistas, la edición, la persistencia tras recargar, documentos y copia de seguridad.
