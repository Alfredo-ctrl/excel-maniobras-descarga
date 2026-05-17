# Excel maestro para maniobras de descarga

Proyecto de Excel para registrar maniobras de descarga, trabajadores, pagos pendientes y pagos realizados.

## Archivos

- `archivos/EJEMPLO LOBA - limpio para usar.xlsx`: version limpia, lista para empezar a capturar datos reales.
- `archivos/EJEMPLO LOBA - version con datos de prueba.xlsx`: version con los datos de ejemplo originales para revisar como funciona.
- `resumen_requisitos_automatizacion_excel.md`: resumen de lo que pidio el cliente y como se resolvio.

## Que hace el Excel

- Permite editar productos y tarifas.
- Permite editar trabajadores.
- Registra maniobras de descarga.
- Calcula total por maniobra.
- Controla pagos por trabajador.
- Permite marcar pagos como `Si` o `No` en la columna `Pagado?`.
- Muestra pendientes por trabajador.
- Muestra resumen de pagos por rango de fechas.
- Genera una ficha imprimible para firma.

## Uso recomendado

1. Abrir `EJEMPLO LOBA - limpio para usar.xlsx`.
2. Actualizar la hoja `Criterios` con productos y tarifas reales.
3. Actualizar la hoja `Trabajadores` con la lista real.
4. Capturar cada descarga en `Maniobras`.
5. Capturar los trabajadores de cada maniobra en `Detalle_Pagos`.
6. Marcar `Pagado?` como `Si` o `No`.
7. Revisar `Pendientes`, `Resumen` y `Ficha`.

La version con datos de prueba solo sirve para mostrar el funcionamiento.
