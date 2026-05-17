# Resumen del proyecto: automatizacion de Excel para maniobras

## Archivos revisados

- `ficha_maniobra_descarga_soya_37.pdf`: ejemplo de ficha de maniobra de descarga. Es la maniobra 37, producto soya, fecha 27/04/26, horario 17:30-20:30, 43.5 toneladas, pago total 3,480, 9 colaboradores, 380 por colaborador.
- `resumen_importes_recibidos_trabajadores.jpg`: tabla resumen de importes recibidos por trabajador, con total general de 10,930.
- `audio_01_intro_ejemplo_ficha_trabajadores.ogg`: introduccion. Explica que el archivo/imagen es un ejemplo de lo que se muestra a los trabajadores.
- `audio_02_calculo_pago_por_producto_y_horario.ogg`: explica como calcula cada maniobra.
- `audio_03_automatizar_excel_pagos_pendientes.ogg`: explica la necesidad principal de automatizacion.
- `audio_04_comentario_caminadora_audio_corto.ogg`: comentario corto sobre que esta en caminadora; no aporta casi al proyecto.
- `audio_05_vista_trabajadores_fecha_producto.ogg`: explica que los trabajadores ven una version resumida.
- `audio_06_regla_carlos_salas_y_reportes.ogg`: explica regla especial de Carlos Salas y reportes deseados.
- `audio_07_excel_maestro_confirmacion_requisitos.ogg`: confirma que quiere un Excel maestro con productos, tarifas y trabajadores para seleccionar datos al crear cada maniobra.
- `audio_08_carlos_salas_contar_maniobras_extra_manual.ogg`: aclara que si la regla de Carlos Salas complica, basta con mostrar cuantas maniobras tiene pendientes.
- `audio_09_resumen_deuda_y_maniobras_por_trabajador.ogg`: confirma que quiere ver cuanto debe y cuantas maniobras no ha pagado por trabajador, y tambien cuanto pago y en cuantas maniobras estuvo.
- `EJEMPLO LOBA.xlsx`: archivo de ejemplo con 2 hojas. `Criterios` contiene productos y tarifas por horario. `EJEMPLO` contiene fichas de maniobra con formato parecido al PDF y ejemplos de trabajadores/importes.

## Lo que necesita el Excel

Tu amigo quiere un Excel para controlar pagos de maniobras de descarga.

Cada maniobra debe registrar:

- Numero de maniobra.
- Fecha.
- Horario de descarga.
- Producto, por ejemplo soya o pasta de soya.
- Toneladas descargadas.
- Si fue dentro de horario laboral o fuera de horario laboral.
- Tarifa por tonelada segun producto y horario.
- Total de la maniobra.
- Trabajadores que participaron.
- Importe calculado por trabajador.
- Importe ajustado/redondeado manualmente si el resultado no queda comodo para pagar.
- Estado de pago: pagado o pendiente.
- Fecha de cobro, si aplica.

## Reglas entendidas

- Cada producto tiene dos tarifas: dentro de horario laboral y fuera de horario laboral.
- Ejemplo mencionado: pasta/soya se paga a 70 dentro de horario y 80 fuera de horario.
- El total se calcula multiplicando toneladas por tarifa.
- Ese total se divide entre el numero de trabajadores participantes.
- El numero de trabajadores cambia por maniobra, puede ser 5, 9, 12, etc.
- A veces el resultado se redondea o ajusta para que sea mas facil pagar.
- Carlos Salas tiene una regla interna: se le pagan 100 pesos extra por cada maniobra que haga. Si automatizar eso complica, basta con mostrar cuantas maniobras tiene pendientes para calcular ese extra manualmente.

## Automatizaciones que pide

- Poder marcar cada pago como pagado o pendiente.
- Tener una vista o boton que muestre solo lo pendiente.
- Sumar automaticamente cuanto se le debe a cada trabajador por maniobras pendientes.
- Mostrar cuantas maniobras pendientes tiene cada trabajador.
- Sumar automaticamente cuanto ya se le pago a cada trabajador.
- Mostrar cuantas maniobras pagadas/acumuladas tiene cada trabajador.
- Filtrar por mes.
- Ver acumulado global por trabajador.
- Evitar copiar y pegar manualmente datos para hacer tablas dinamicas.
- Generar una ficha resumida para trabajadores, ocultando calculos internos.

## Audios con partes dudosas

- `audio_01_intro_ejemplo_ficha_trabajadores.ogg`: se entiende la idea general, pero algunas frases iniciales no son claras por ruido/cansancio.
- `audio_04_comentario_caminadora_audio_corto.ogg`: no parece relevante al Excel.
- `audio_05_vista_trabajadores_fecha_producto.ogg`: hay una frase dudosa donde parece decir que muestra "version resumida"; lo seguro es que los trabajadores solo ven fecha, hora, producto, toneladas/importe y no todo el calculo.
- `audio_06_regla_carlos_salas_y_reportes.ogg`: la idea principal se entiende bien: Carlos Salas recibe 100 extra por maniobra y quiere reportes de pendientes/pagado por persona.

## Conclusion

Si se puede hacer. Lo ideal seria crear un archivo Excel con hojas para:

- Catalogo de productos y tarifas.
- Catalogo de trabajadores.
- Registro de maniobras.
- Detalle de trabajadores por maniobra.
- Pagos pendientes.
- Resumen mensual.
- Resumen global.
- Ficha imprimible o exportable para trabajadores.

## Confirmacion del audio nuevo

La idea mas clara es hacer un Excel maestro:

- Hoja de productos y tarifas.
- Hoja de trabajadores.
- Registro para crear una nueva maniobra seleccionando producto, horario y trabajadores.
- Si se selecciona soya u otro producto, Excel debe traer automaticamente su tarifa segun si fue dentro o fuera del horario laboral.
- El calculo sugerido puede salir automatico, pero el importe final que se muestra/paga puede editarse manualmente.
- Debe haber una casilla o marca de pagado.
- Debe mostrar pendientes por trabajador: cuanto se debe y cuantas maniobras no se han pagado.
- Debe mostrar historial/resumen por trabajador: cuanto se pago y en cuantas maniobras estuvo.
- Debe poder filtrarse por mes o por rango de fechas.

## Revision del archivo EJEMPLO LOBA.xlsx

El archivo ya trae una base util:

- Hoja `Criterios`: productos y tarifas.
  - MAIZ: 50 dentro de horario, 60 fuera.
  - SORGO: 50 dentro de horario, 60 fuera.
  - SOYA: 60 dentro de horario, 70 fuera.
  - SALVADO: 40 dentro de horario, 50 fuera.
  - DDG: 50 dentro de horario, 60 fuera.
  - ROLADO: 40 dentro de horario, 50 fuera.
  - Calcio: 40 dentro de horario, 50 fuera.
- Hoja `EJEMPLO`: trae dos fichas de maniobra ya armadas.
  - Maniobra 41: fecha 05/05/2026, sorgo, 19.5 toneladas, 7 colaboradores.
  - Maniobra 42: fecha 06/05/2026, maiz, 37 toneladas, 7 colaboradores.
- El formato ya parece pensado para imprimir o firmar.
- El importe recibido por trabajador esta capturado manualmente, que coincide con lo que explico el cliente.
- Faltan hojas/tablas de control para poder sacar pendientes, pagados y resumen por trabajador.

Con este archivo si se puede construir lo que pide. Lo recomendable es convertirlo en un Excel maestro con tablas de captura y reportes, manteniendo una hoja de ficha imprimible como la que ya tiene.

## Archivo generado

Se creo `EJEMPLO LOBA - automatizado.xlsx` trabajando sobre `EJEMPLO LOBA.xlsx`.

Incluye:

- `Inicio`: guia corta de uso.
- `Criterios`: productos y tarifas editables.
- `Trabajadores`: lista editable de trabajadores y extra de referencia.
- `Maniobras`: registro principal con total por maniobra.
- `Detalle_Pagos`: control por trabajador, importe manual, extra manual, pagado o pendiente.
- `Pendientes`: suma cuanto se debe por trabajador y cuantas maniobras pendientes tiene.
- `Resumen`: resumen por trabajador con filtro por fechas.
- `Ficha`: hoja imprimible tipo PDF para seleccionar una maniobra y mostrar participantes/importes.
- `EJEMPLO`: hoja original conservada como referencia.
