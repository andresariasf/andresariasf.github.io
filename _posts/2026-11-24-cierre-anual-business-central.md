---
title: "Cierre anual en Business Central: guía práctica y checklist"
date: 2026-11-24 08:00:00 -0500
categories: [Business Central, Finanzas]
tags: [business central, cierre anual, cierre contable, contabilidad, finanzas]
description: "Guía práctica para preparar y ejecutar el cierre anual en Microsoft Dynamics 365 Business Central, desde las conciliaciones previas hasta el cierre del estado de resultados."
image:
  path: /assets/img/posts/cierre-anual-business-central.png
  alt: "Cierre anual en Microsoft Dynamics 365 Business Central"
---
Cierre anual en Business Central: guía práctica paso a paso

Se acerca el cierre del año y con él uno de los procesos más importantes para cualquier departamento financiero: el cierre contable anual.

Cuando trabajamos con Microsoft Dynamics 365 Business Central, es fácil pensar que el cierre consiste simplemente en cerrar los periodos contables y ejecutar el proceso de cierre del estado de resultados. Sin embargo, hay varias actividades que deberíamos completar antes de llegar a ese punto.

En este artículo quiero compartir un recorrido práctico por los principales puntos que deberíamos revisar antes de cerrar nuestro ejercicio en Business Central.

Antes de empezar: el cierre es un proceso, no un botón

Una de las primeras cosas que debemos tener claras es que cerrar el ejercicio fiscal y cerrar las cuentas de resultados son dos procesos diferentes.

Además, cerrar un ejercicio en Business Central no impide automáticamente que podamos registrar movimientos con fechas pertenecientes a ese año. Para controlar esto debemos utilizar las restricciones de fechas de registro.

Por eso, antes de ejecutar cualquier cierre, mi recomendación es trabajar sobre una pequeña lista de control.

Vamos a verla.

1. Revisar los periodos contables

Empecemos por lo básico.

Desde Periodos contables podemos comprobar:

Los periodos correspondientes al ejercicio actual.
La fecha de inicio del ejercicio.
Si los diferentes periodos están correctamente configurados.
Si ya tenemos creado el siguiente ejercicio.

Si todavía no tenemos creado el próximo año fiscal, podemos utilizar la acción Crear ejercicio.

Aunque normalmente trabajaremos con 12 periodos mensuales, Business Central permite utilizar otra estructura de periodos si nuestro ejercicio fiscal lo requiere.

Hasta aquí sencillo.

Pero todavía no debemos cerrar nada.

2. Revisar qué queda pendiente de registrar

Antes del cierre debemos asegurarnos de que se han registrado todas las operaciones que corresponden al ejercicio.

Por ejemplo:

Ventas

Revisaría principalmente:

Facturas de venta pendientes.
Abonos.
Pedidos entregados pero todavía no facturados.
Devoluciones.
Cobros pendientes de registrar o aplicar.
Compras

De forma similar:

Facturas de compra pendientes.
Abonos.
Pedidos recibidos pero todavía no facturados.
Devoluciones.
Pagos pendientes.
Gastos recibidos pero todavía no facturados.

Microsoft incluye precisamente el registro de documentos pendientes y la conciliación de cuentas por cobrar y pagar dentro de las actividades habituales del cierre de periodo.

Aquí tenemos una consideración importante:

una cosa es que el documento esté pendiente y otra que realmente deba registrarse en el ejercicio que estamos cerrando.

Esa decisión dependerá de las políticas contables de cada empresa.

3. Conciliar clientes y proveedores

Una vez registrados los documentos pendientes, debemos comprobar que nuestros submódulos coinciden con contabilidad.

Es decir:

Clientes → Cuentas por cobrar en contabilidad

y

Proveedores → Cuentas por pagar en contabilidad

Para esta revisión podemos apoyarnos en informes de antigüedad de deuda y movimientos por cuenta.

Si existe una diferencia, este es el momento de investigarla.

No deberíamos llegar al cierre definitivo con diferencias inexplicadas entre el módulo de clientes o proveedores y sus correspondientes cuentas de control.

4. Conciliar los bancos

Otro punto imprescindible.

Cada cuenta bancaria debería quedar conciliada contra su correspondiente extracto.

Desde Conciliación de cuentas bancarias podemos revisar y relacionar los movimientos del banco con los movimientos existentes en Business Central.

Especial atención a:

Comisiones bancarias.
Intereses.
Transferencias en tránsito.
Pagos todavía no aplicados.
Cobros pendientes.
Movimientos registrados por el banco que todavía no existen en Business Central.

El objetivo debería ser sencillo:

Banco + Business Central + Contabilidad deben contar la misma historia.

5. ¿Trabajamos con inventario?

Si la respuesta es sí, aquí tenemos uno de los puntos más importantes del cierre.

Antes de comprobar el valor final del inventario deberíamos revisar:

Inventario físico.
Diferencias de inventario.
Existencias negativas.
Productos sin coste.
Recepciones pendientes.
Envíos pendientes.
Transferencias.
Costes pendientes de ajustar.

Después de tener registrados correctamente los movimientos, debemos prestar especial atención a dos procesos:

Ajustar coste - Movimientos producto

y posteriormente:

Registrar coste inventario en contabilidad

El orden importa.

Primero necesitamos que los movimientos de inventario reflejen correctamente sus costes y después podemos trasladar esos valores a contabilidad.

Este ajuste de costes forma parte de la secuencia recomendada antes de validar definitivamente la valoración del inventario.

6. ¿Tenemos producción?

Si nuestra empresa trabaja con fabricación, añadimos algunas comprobaciones más.

Por ejemplo:

Órdenes de producción abiertas.
Consumos pendientes.
Salidas pendientes.
Capacidades y tiempos sin registrar.
Órdenes terminadas que todavía no hemos finalizado.
Trabajo en curso o WIP.
Desviaciones de producción.

¿Por qué es importante?

Porque registrar después un consumo, una capacidad o una salida podría modificar el coste de nuestros productos.

Por eso debemos terminar primero nuestros movimientos operativos y después ejecutar el ajuste de costes.

7. Activos fijos

Si utilizamos el módulo de activos fijos de Business Central, también debemos completar sus procesos antes del cierre.

Principalmente:

Registrar las altas y bajas pendientes.
Revisar adquisiciones.
Registrar posibles reclasificaciones.
Revisar mantenimiento.
Calcular la amortización hasta la fecha final del ejercicio.

Microsoft incluye entre las tareas de cierre la revisión de los ajustes, apreciaciones, amortizaciones y movimientos pendientes de activos fijos.

Una vez calculada la amortización, debemos revisar y registrar los movimientos generados.

8. ¿Utilizamos divisas?

Si tenemos clientes, proveedores o bancos en moneda extranjera, tendremos otro proceso importante.

Primero actualizamos los Tipos de cambio de divisa.

Después podemos ejecutar:

Ajustar tipos de cambio

Esto nos permitirá reconocer las diferencias correspondientes sobre los movimientos abiertos de clientes, proveedores y bancos.

La actualización de los tipos de cambio y su correspondiente ajuste es también una de las actividades que Microsoft contempla dentro del proceso habitual de cierre.

9. Provisiones, periodificaciones y ajustes

Llegados a este punto seguramente necesitaremos registrar determinados ajustes contables.

Por ejemplo:

Gastos devengados.
Ingresos devengados.
Gastos anticipados.
Provisiones.
Reclasificaciones.
Deterioros.
Ajustes identificados durante las conciliaciones.

Dependiendo del tipo de operación, podemos utilizar diarios generales o diarios periódicos para facilitar estos registros.

La idea es que cada ingreso o gasto quede reconocido en el ejercicio que realmente corresponde.

10. Revisar las dimensiones

Este es un punto que personalmente considero especialmente importante.

Podemos tener una contabilidad perfectamente cuadrada y, aun así, tener un problema con nuestras dimensiones.

Antes del cierre revisaría que nuestros movimientos tengan correctamente informadas las dimensiones utilizadas por la empresa:

Departamento.
Centro de coste.
Proyecto.
Sucursal.
Oficina.
País.
Línea de negocio.

¿Por qué?

Porque probablemente utilizaremos esas dimensiones posteriormente para analizar nuestro resultado.

No queremos descubrir después del cierre que el resultado contable es correcto, pero que no podemos analizar adecuadamente dónde se produjo ese resultado.

11. Revisar nuestros informes financieros

Antes de cerrar definitivamente el ejercicio es el momento de generar nuestros informes.

Como mínimo revisaría:

Balance de comprobación.
Balance de situación.
Estado de resultados.
Antigüedad de clientes.
Antigüedad de proveedores.
Valoración de inventario.
Información de activos fijos.
Análisis por dimensiones.

Business Central contempla precisamente la ejecución de informes financieros como parte de las tareas de cierre de periodo.

Aquí podemos hacernos algunas preguntas sencillas:

¿Coinciden los submódulos con contabilidad?

¿Hay variaciones importantes frente al año anterior?

¿El resultado tiene sentido respecto al negocio?

¿Tenemos movimientos sin las dimensiones esperadas?

Si todo está correcto, podemos avanzar.

12. Ahora sí: cerrar el ejercicio

Una vez realizadas nuestras revisiones:

Periodos contables → Cerrar año

Con esta acción marcamos los periodos correspondientes al ejercicio como cerrados.

Pero cuidado con un punto importante:

Una vez cerrado el ejercicio, no podremos volver a abrirlo mediante la funcionalidad estándar.

Por eso debemos ejecutar este paso únicamente cuando nuestras validaciones hayan terminado.

13. Cerrar el estado de resultados

Ahora todavía nos falta un paso.

Tenemos que trasladar el resultado del ejercicio a nuestro patrimonio.

Para ello utilizamos el proceso:

Cerrar estado de resultados

El proceso trabaja sobre las cuentas configuradas como tipo Estado de resultados, genera los movimientos necesarios para cerrar sus saldos y permite trasladar el resultado a la cuenta correspondiente de patrimonio.

Normalmente indicaremos:

Fecha de cierre.
Diario.
Sección o lote.
Cuenta de resultados acumulados.
Tratamiento de dimensiones.

Una vez ejecutado el proceso, tendremos las líneas correspondientes en nuestro diario.

Mi recomendación: no registrarlas directamente sin revisarlas.

Primero validemos los importes y dimensiones. Después registramos.

¿Y si aparece un ajuste después?

Puede ocurrir.

Por ejemplo, el auditor solicita un ajuste correspondiente al ejercicio anterior cuando nosotros ya lo hemos cerrado.

Cerrar el ejercicio no significa que sea imposible registrar un movimiento con una fecha de ese año.

Si nuestras fechas permitidas de registro lo permiten, podemos contabilizar ajustes posteriores. Business Central identifica estos movimientos como correspondientes al año anterior.

Después del ajuste tendremos que volver a ejecutar Cerrar estado de resultados para trasladar su impacto correspondiente.

Mi checklist de cierre

Si tuviera que resumir todo el proceso, utilizaría esta lista:

 Crear el nuevo ejercicio.
 Registrar documentos pendientes.
 Conciliar clientes.
 Conciliar proveedores.
 Conciliar bancos.
 Realizar inventario físico.
 Revisar movimientos de inventario.
 Revisar producción y WIP.
 Ajustar costes.
 Registrar costes de inventario en contabilidad.
 Calcular las amortizaciones.
 Ajustar los tipos de cambio.
 Registrar provisiones y periodificaciones.
 Revisar dimensiones.
 Conciliar submódulos contra contabilidad.
 Revisar informes financieros.
 Cerrar el ejercicio.
 Cerrar el estado de resultados.
 Registrar el asiento de cierre.
 Restringir las fechas permitidas de registro.
Para terminar

El cierre anual en Business Central no tiene por qué ser un proceso complicado.

La clave, desde mi punto de vista, está en no verlo únicamente como un proceso contable.

Ventas, compras, bancos, inventario, producción, activos fijos y dimensiones pueden terminar impactando nuestro cierre.

Por eso una buena planificación, acompañada de una lista de comprobación, puede evitarnos muchas sorpresas cuando lleguemos al último paso.

Y recuerda: primero conciliamos, después validamos y solo entonces cerramos.
