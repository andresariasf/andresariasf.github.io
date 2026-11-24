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

Por 
