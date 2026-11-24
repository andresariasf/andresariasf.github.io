---
title: "Cierre anual en Business Central: guía práctica y checklist"
date: 2026-11-24 08:00:00 -0500
categories: [Business Central, Finanzas]
tags: [business central, cierre anual, cierre contable, contabilidad, finanzas]
description: "Guía práctica para el cierre anual en Business Central: conciliaciones, inventario, costes, activos fijos, divisas y cierre del ejercicio."
image:
  path: /assets/img/posts/cierre-anual-business-central.png
  alt: "Cierre anual en Microsoft Dynamics 365 Business Central"
---

Se acerca el final del año y con él uno de los procesos más importantes para cualquier departamento financiero: **el cierre anual**.

Hace un par de años compartí con mi equipo una pequeña lista de puntos que debíamos tener presentes antes de comenzar un nuevo ejercicio en Microsoft Dynamics 365 Business Central. Incluía cosas tan sencillas, pero fáciles de olvidar, como crear los nuevos periodos contables, revisar las series numéricas, actualizar las listas de precios o limitar las fechas permitidas de registro.

Con el tiempo esa lista ha ido creciendo.

Cuando hablamos del cierre anual en Business Central, en realidad estamos hablando de **dos cosas diferentes**:

1. Preparar Business Central para comenzar a trabajar correctamente en el nuevo año.
2. Completar los procesos financieros necesarios para cerrar correctamente el ejercicio anterior.

Y dependiendo de nuestra empresa, tendremos que revisar inventario, producción, activos fijos, divisas, clientes, proveedores y otros procesos antes de cerrar definitivamente el año.

En este artículo comparto mi **checklist actualizado para el cierre anual en Business Central**.

---

## 1. Antes del cierre: preparar Business Central para el nuevo año

Empezaría por algunas configuraciones sencillas que pueden provocar problemas operativos desde el primer día del nuevo ejercicio si nadie las revisa.

### Series numéricas

Si utilizamos series diferentes o correlativas por año, debemos comprobar nuestras **Series numéricas**.

Por ejemplo:

```text
FAC-2026-00001
PED-2026-00001
ALB-2026-00001
```

Si la empresa necesita comenzar una nueva numeración en enero, no deberíamos esperar al primer documento del año para descubrir que la serie no está preparada.

Mi recomendación es revisar especialmente las series utilizadas para:

- Facturas.
- Abonos.
- Pedidos.
- Albaranes.
- Documentos registrados.
- Diarios.
- Activos fijos.

Y, obviamente, considerar cualquier requisito fiscal relacionado con la numeración de documentos en cada localización.

---

## 2. Crear el nuevo ejercicio

Desde **Periodos contables** debemos comprobar que tenemos creado el siguiente ejercicio.

Si todavía no existe:

**Periodos contables → Crear ejercicio**

Revisaremos:

- Fecha inicial.
- Número de periodos.
- Duración de los periodos.
- Fecha de comienzo del ejercicio.

Aunque habitualmente tendremos 12 periodos mensuales, Business Central permite trabajar con otras estructuras fiscales.

> No necesitamos esperar a cerrar el ejercicio anterior para crear el siguiente.
{: .prompt-tip }

De hecho, tener preparado el siguiente ejercicio forma parte de una buena preparación del cierre.

---

## 3. Periodos de inventario

Si utilizamos inventario, no debemos olvidarnos de los **Periodos inventario**.

Estos periodos permiten controlar hasta qué fecha pueden registrarse movimientos de producto.

Por tanto, debemos considerar:

- Hasta qué fecha permitiremos movimientos.
- Cuándo se realizará el inventario físico.
- Qué movimientos quedan pendientes.
- Cuándo cerramos definitivamente el periodo de inventario.

Especialmente en empresas con un volumen importante de operaciones de almacén, deberíamos coordinar esta fecha con compras, ventas, transferencias y producción.

---

## 4. Revisar las fechas permitidas de registro

Este es uno de los controles más importantes.

Podemos establecer fechas generales desde **Configuración contabilidad** mediante:

- **Permitir registro desde**.
- **Permitir registro hasta**.

Adicionalmente podemos establecer fechas específicas por usuario desde **Configuración usuario**.

Esto nos permite, por ejemplo, que a partir del 1 de enero los usuarios registren únicamente en el nuevo ejercicio mientras que determinados usuarios de Finanzas conservan temporalmente acceso al ejercicio anterior para registrar ajustes.

> **Cerrar un ejercicio no bloquea automáticamente el registro sobre ese año.** El control de nuevas contabilizaciones debe complementarse con las fechas permitidas de registro.
{: .prompt-warning }

Por eso **Cerrar año** y **bloquear el registro** son dos conceptos que no debemos confundir.

---

## 5. Revisar las listas de precios

Este era uno de los puntos de mi checklist original y creo que sigue siendo muy válido.

Muchas empresas aprovechan el cambio de ejercicio para actualizar:

- Precios de venta.
- Precios de compra.
- Descuentos.
- Acuerdos comerciales.
- Tarifas por cliente.
- Tarifas por proveedor.

Si nuestras nuevas tarifas empiezan el **1 de enero**, deberían estar preparadas y validadas antes de esa fecha.

También debemos comprobar las fechas iniciales y finales de las listas existentes para evitar que una tarifa antigua siga aplicándose por error.

---

## 6. Registrar todo lo que realmente pertenece al ejercicio

Una vez preparada la operativa del nuevo año podemos centrarnos en el ejercicio que estamos cerrando.

Antes de ejecutar los procesos de cierre debemos revisar documentos y diarios pendientes.

### Ventas

- Facturas pendientes.
- Abonos.
- Entregas pendientes de facturación.
- Devoluciones.
- Cobros pendientes.
- Anticipos.

### Compras

- Facturas pendientes.
- Abonos.
- Recepciones pendientes de facturación.
- Devoluciones.
- Pagos pendientes.
- Servicios recibidos aún no facturados.

Después debemos conciliar:

**Clientes → Cuentas por cobrar**

**Proveedores → Cuentas por pagar**

La idea es sencilla: antes de cerrar, debemos conseguir que los submódulos y la contabilidad cuenten la misma historia.

---

## 7. Revisar Direct Posting y las cuentas de control

Este es un punto que incorporaría expresamente al checklist.

Debemos revisar las **cuentas de control** asociadas a procesos como:

- Clientes.
- Proveedores.
- Bancos.
- Inventario.
- Activos fijos.

En la medida de lo posible, deberíamos evitar contabilizaciones manuales directas sobre cuentas que deberían alimentarse mediante un submódulo.

¿Por qué?

Podemos terminar teniendo algo así:

```text
Saldo clientes              100.000
Cuenta contable clientes    105.000
                            -------
Diferencia                    5.000
```

Y entonces empieza el entretenido trabajo de descubrir de dónde vienen esos 5.000.

Por eso merece la pena revisar la configuración de **Direct Posting** y comprobar que las cuentas de control se utilizan de acuerdo con el diseño contable definido para la empresa.

No esperaría al 31 de diciembre para hacer esta validación.

---

## 8. Conciliaciones bancarias

Cada banco debería estar conciliado contra su correspondiente extracto.

Revisaría especialmente:

- Comisiones.
- Intereses.
- Transferencias en tránsito.
- Pagos todavía no aplicados.
- Cobros pendientes.
- Movimientos existentes en el banco pero todavía no registrados.

El objetivo debería ser:

> **Extracto bancario = Banco en Business Central = Contabilidad**
{: .prompt-info }

Si no coinciden, debemos poder explicar la diferencia.

---

## 9. Inventario: uno de los puntos más críticos

Si nuestra empresa trabaja con inventario, aquí debemos detenernos un poco más.

Antes de cerrar revisaría:

- Inventario físico.
- Diferencias de inventario.
- Inventario negativo.
- Productos sin coste.
- Recepciones pendientes.
- Envíos pendientes.
- Transferencias.
- Costes indirectos.
- Aplicaciones de movimientos.
- Movimientos pendientes de ajustar.

Después debemos ejecutar los procesos de coste correspondientes.

### Ajustar coste - Movimientos producto

Primero debemos asegurarnos de que los costes están correctamente propagados entre los movimientos relacionados.

Después ejecutaremos:

### Registrar coste inventario en contabilidad

Esto permite trasladar hacia contabilidad las diferencias de coste pendientes.

Una secuencia práctica sería:

```text
Movimientos
     ↓
Inventario físico
     ↓
Ajuste de diferencias
     ↓
Adjust Cost - Item Entries
     ↓
Post Inventory Cost to G/L
     ↓
Inventory Valuation
     ↓
Conciliación Inventory vs G/L
```

El orden es importante. No queremos reconciliar el inventario para modificar sus costes inmediatamente después.

---

## 10. Si tenemos producción, todavía no hemos terminado

Si utilizamos Manufacturing, revisaría además:

- Órdenes de producción abiertas.
- Consumos pendientes.
- Outputs pendientes.
- Capacidades.
- Tiempos.
- Órdenes terminadas pero todavía abiertas.
- WIP.
- Desviaciones de producción.

Esto es especialmente importante antes del ajuste definitivo de costes.

Un consumo, una capacidad o un output pendiente puede terminar modificando el coste del producto que creíamos cerrado.

Por ello, finalizaría primero los movimientos operativos que correspondan y después continuaría con el ajuste definitivo de costes.

---

## 11. Ejecutar la depreciación de activos fijos

Este era otro punto de mi checklist original.

Si utilizamos **Activos fijos**, debemos revisar:

- Altas.
- Bajas.
- Adquisiciones.
- Mantenimiento.
- Libros de amortización.
- Activos totalmente amortizados.
- Activos que deberían haberse dado de baja.

Después ejecutaremos **Calcular amortización** hasta la fecha final correspondiente y registraremos los movimientos generados.

---

## 12. Ajustar tipos de cambio

Otro proceso que dependerá de nuestra empresa.

Si tenemos operaciones en moneda extranjera debemos revisar primero nuestros **Tipos de cambio divisa**.

Después podremos ejecutar **Ajustar tipos de cambio**, prestando especial atención a movimientos abiertos de:

- Clientes.
- Proveedores.
- Bancos.

Antes de registrar el ajuste conviene comprobar la fecha, los tipos de cambio utilizados y las cuentas configuradas para las pérdidas y ganancias por diferencias de cambio.

---

## 13. Provisiones, periodificaciones y otros ajustes

No todo llegará a través de una factura.

Tenemos que considerar posibles:

- Provisiones.
- Gastos devengados.
- Ingresos devengados.
- Gastos anticipados.
- Deterioros.
- Reclasificaciones.
- Ajustes identificados durante las conciliaciones.
- Ajustes de auditoría.

El objetivo es que los ingresos y gastos queden reconocidos en el ejercicio que realmente corresponde.

---

## 14. Revisar dimensiones

Este es un punto que añadiría expresamente a mi checklist actual.

Quizás nuestro Balance y Estado de Resultados sean correctos, pero ¿qué ocurre con nuestro análisis?

Revisaría las dimensiones importantes para la empresa, por ejemplo:

- Departamento.
- Centro de coste.
- Proyecto.
- Sucursal.
- Oficina.
- País.
- Línea de negocio.

Especialmente buscaría movimientos **sin dimensión, con dimensiones incorrectas o con combinaciones no esperadas**.

En mi experiencia, descubrir esto después de presentar los informes de gestión es bastante peor que detectarlo durante el cierre.

---

## 15. Ejecutar los informes antes de cerrar

Antes de utilizar **Cerrar año**, guardaría una fotografía financiera de cómo estamos llegando al cierre.

Como mínimo revisaría:

- Balance de comprobación.
- Balance de situación.
- Estado de resultados.
- Antigüedad de clientes.
- Antigüedad de proveedores.
- Saldos bancarios.
- Valoración de inventario.
- Conciliación Inventory - G/L.
- Activos fijos.
- Análisis por dimensiones.

Y comprobaría nuevamente:

```text
AR           ↔ G/L
AP           ↔ G/L
Banks        ↔ G/L
Inventory    ↔ G/L
Fixed Assets ↔ G/L
```

No es suficiente con que el balance cuadre. Los submódulos deben explicar el saldo de sus correspondientes cuentas de control.

---

## 16. Antes de cerrar: ¿por qué no probarlo en Sandbox?

Esta es una recomendación que considero especialmente útil.

Si:

- Es nuestro primer cierre en Business Central.
- Acabamos de implementar la solución.
- Hemos modificado Posting Groups.
- Cambiamos nuestro Chart of Accounts.
- Tenemos personalizaciones relacionadas con contabilidad.
- Nunca hemos ejecutado **Close Income Statement**.

haría primero una prueba en **Sandbox**.

Esto nos permite comprobar:

- Qué movimientos genera el cierre.
- Qué cuenta recibe el resultado.
- Cómo se comportan nuestras dimensiones.
- El impacto de nuestras personalizaciones.
- Los informes posteriores al cierre.

> Personalmente, prefiero descubrir una sorpresa en Sandbox que durante el cierre real.
{: .prompt-tip }

---

## 17. Ahora sí: cerrar el ejercicio

Una vez conciliados y aprobados nuestros números podemos ejecutar:

**Periodos contables → Cerrar año**

Debemos tener clara una característica importante:

> **Una vez cerrado el ejercicio, no podemos volver a abrirlo mediante la funcionalidad estándar.**
{: .prompt-warning }

Por eso no deberíamos ejecutar este paso hasta haber terminado nuestras validaciones.

Cerrar el ejercicio tampoco significa que automáticamente hayamos bloqueado toda contabilización posterior. Para ello debemos seguir controlando las fechas permitidas de registro.

---

## 18. Asiento de regularización: Close Income Statement

Este era otro de los procesos incluidos en mi lista original.

Cerrar el ejercicio y cerrar el Estado de Resultados **no son lo mismo**.

Después del cierre debemos ejecutar:

**Cerrar estado de resultados / Close Income Statement**

El proceso toma las cuentas configuradas como **Income Statement** y genera los movimientos necesarios para cancelar sus saldos y trasladar el resultado a la cuenta correspondiente de patrimonio.

La secuencia sería:

```text
Cerrar ejercicio
        ↓
Close Income Statement
        ↓
Generación del diario
        ↓
REVISAR
        ↓
Registrar
```

He puesto **REVISAR** en mayúsculas por una razón.

No registraría el diario sin validar previamente:

- Cuenta de resultados acumulados.
- Importes.
- Dimensiones.
- Fecha.
- Número de documento.

---

## 19. ¿Qué ocurre si Auditoría solicita un ajuste?

Puede ocurrir que Auditoría solicite un ajuste correspondiente al ejercicio anterior cuando ya hemos ejecutado **Cerrar año**.

Cerrar el ejercicio no significa necesariamente que sea imposible registrar un ajuste con fecha del año anterior. Si las fechas permitidas de registro lo permiten, determinados usuarios pueden contabilizar dichos ajustes.

Después tendremos que volver a ejecutar **Close Income Statement** para trasladar también el impacto del nuevo movimiento.

Por tanto:

> **Cerrar año no significa bloquear año.**
{: .prompt-info }

Una vez terminados los ajustes de auditoría, sí recomendaría restringir definitivamente las fechas permitidas de registro.

---

## Mi checklist final de cierre anual

Después de unir mi lista original con estas recomendaciones, este sería actualmente mi checklist.

### Preparar el nuevo año

- [ ] Revisar **Series numéricas**.
- [ ] Crear el nuevo **Ejercicio contable**.
- [ ] Revisar **Periodos inventario**.
- [ ] Revisar **Fechas permitidas de registro**.
- [ ] Actualizar **Listas de precios**.
- [ ] Revisar configuraciones con vigencia por fecha.

### Preparar el cierre

- [ ] Registrar documentos pendientes.
- [ ] Conciliar clientes.
- [ ] Conciliar proveedores.
- [ ] Conciliar bancos.
- [ ] Revisar cuentas de control y **Direct Posting**.
- [ ] Realizar inventario físico.
- [ ] Revisar inventario negativo.
- [ ] Revisar órdenes de producción y WIP.
- [ ] Ejecutar **Adjust Cost - Item Entries**.
- [ ] Ejecutar **Post Inventory Cost to G/L**.
- [ ] Conciliar Inventory vs G/L.
- [ ] Calcular depreciaciones.
- [ ] Ajustar tipos de cambio.
- [ ] Registrar provisiones y periodificaciones.
- [ ] Revisar dimensiones.
- [ ] Generar y revisar los informes financieros.

### Ejecutar el cierre

- [ ] Realizar una prueba en **Sandbox**, cuando aplique.
- [ ] Obtener la aprobación financiera.
- [ ] Ejecutar **Cerrar año**.
- [ ] Ejecutar **Close Income Statement**.
- [ ] Revisar el diario generado.
- [ ] Registrar el asiento.
- [ ] Registrar posibles ajustes de auditoría.
- [ ] Reejecutar el cierre de resultados si hubo ajustes.
- [ ] Restringir definitivamente las fechas de registro.
- [ ] Archivar los informes utilizados para validar el cierre.

---

## Para terminar

Cuando escribí aquella primera lista para mi equipo tenía apenas unos cuantos puntos.

Y en realidad me sigue gustando aquella idea porque resume bastante bien cómo deberíamos afrontar un cierre anual en Business Central:

**no esperar al último día para descubrir lo que nos faltaba preparar.**

El cierre anual no comienza cuando hacemos clic en **Cerrar año**.

Comienza bastante antes revisando nuestras series, periodos, fechas, documentos pendientes, conciliaciones, inventario, costes, activos, divisas y dimensiones.

Si tuviera que resumir todo este artículo en una sola secuencia sería:

> **Preparar → Registrar → Conciliar → Ajustar → Validar → Cerrar → Bloquear**
{: .prompt-tip }

Seguramente cada empresa añadirá algunos puntos más a esta lista dependiendo de sus procesos, industria y localización.

**¿Qué otro punto añadirías tú a este checklist de cierre anual en Business Central?**

---

## Referencias

Para preparar y actualizar este checklist he contrastado mi experiencia con documentación oficial de Microsoft y distintas guías especializadas sobre cierres de ejercicio en Business Central:

- [Close Years and Periods - Microsoft Learn](https://learn.microsoft.com/en-us/dynamics365/business-central/year-close-years-periods)
- [Close the Books - Microsoft Learn](https://learn.microsoft.com/en-us/dynamics365/business-central/year-close-books)
- [Business Central Year-End Close Checklist - ERP Software Blog](https://erpsoftwareblog.com/2026/11/business-central-year-end-close-checklist/)
- [How to Close a Fiscal Year in Business Central - Forvis Mazars](https://www.forvismazars.us/forsights/2025/11/how-to-close-a-fiscal-year-in-business-central)
- [Year-End ERP Checklist for Dynamics Business Central - HBS](https://www.hbs.net/blog/erp-year-end-prep-dynamics-business-central)
