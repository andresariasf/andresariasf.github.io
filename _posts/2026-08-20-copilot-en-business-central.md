---
title: "Copilot en Business Central: qué puede hacer hoy y cómo empezar a aprovecharlo"
date: 2026-08-20 09:00:00 -0500 
categories: [Business Central, Copilot]
tags: [business-central, copilot, ai, dynamics365]
description: Una mirada funcional y práctica a las principales capacidades de Copilot en Business Central, con ejemplos de ventas, finanzas, inventario y análisis de información.
image:
  path: /assets/img/posts/copilot-business-central.png
  alt: "Copilot en Business Central"
---

Cuando hablamos de Inteligencia Artificial aplicada a un ERP, es fácil imaginar un sistema capaz de resolverlo todo con una sola pregunta.

La realidad actual es más concreta y, para mí, también más interesante.

Copilot en Business Central no busca reemplazar el proceso de negocio ni tomar todas las decisiones por el usuario. Su objetivo es ayudar a consultar información, analizar datos, completar tareas y reducir parte del trabajo manual que normalmente realizamos dentro del sistema.

Esto cambia poco a poco la forma de trabajar con Business Central.

Ya no se trata únicamente de conocer dónde está cada página, qué filtro utilizar o qué campo completar. También podemos apoyarnos en Copilot para encontrar información, organizar datos, generar propuestas y avanzar más rápido dentro de un proceso.

En este artículo quiero revisar las capacidades que considero más relevantes, explicadas desde una perspectiva funcional y con ejemplos sencillos.

## Copilot no es una única funcionalidad

Lo primero que debemos entender es que Copilot en Business Central no es solamente una ventana de chat.

Business Central incorpora diferentes experiencias de IA dentro de la aplicación. Algunas son transversales y pueden ayudar a usuarios de distintas áreas. Otras están integradas en procesos concretos, como ventas, inventario, cuentas por pagar o conciliación bancaria.

Podemos agruparlas en tres niveles:

1. **Asistencia general**, para buscar, comprender y resumir información.
2. **Asistencia dentro del proceso**, para analizar datos o proponer contenido.
3. **Agentes**, para ejecutar procesos específicos con mayor autonomía y mantener al usuario dentro del flujo de revisión y control.

La diferencia es importante.

Copilot normalmente trabaja junto con el usuario: recibe una instrucción y genera una respuesta o propuesta. Un agente puede encargarse de una actividad más completa, por ejemplo, revisar solicitudes recibidas por correo y preparar una cotización para que una persona la valide.

<!-- IMAGEN 1: Vista general del chat de Copilot abierto dentro de Business Central -->

/assets/img/posts/copilot-bc-chat.png
_El chat permite buscar datos de la empresa y obtener orientación sobre el uso de Business Central._

## 1. Buscar información utilizando lenguaje natural

Uno de los escenarios más fáciles de entender es el chat de Copilot.

En lugar de navegar por varias páginas o aplicar filtros manualmente, el usuario puede formular una pregunta relacionada con la información disponible en Business Central.

Por ejemplo:

- Muéstrame los clientes con saldo vencido.
- Busca los pedidos de venta abiertos.
- ¿Dónde encuentro la configuración de dimensiones?
- ¿Cómo se registra una nota de crédito de compra?
- Muéstrame el artículo con número 1000.

Copilot puede buscar registros y proporcionar enlaces para abrir la información correspondiente. También puede ayudar a comprender campos, páginas, procesos y funcionalidades, incluyendo contenido de algunas extensiones instaladas.

Desde el punto de vista funcional, esto puede facilitar la adopción del ERP. Un usuario nuevo no siempre conoce el nombre exacto de una página o la ruta de navegación, pero sí sabe qué información necesita.

Copilot ayuda a reducir esa distancia entre la necesidad del usuario y la estructura del sistema.

### ¿Qué debemos considerar?

Copilot no debería utilizarse como sustituto de los permisos ni de la correcta configuración del sistema. La experiencia hereda los permisos del usuario, por lo que no debería acceder a información que esa persona no puede consultar dentro de Business Central.

Tampoco debemos asumir que cada respuesta será perfecta. El usuario sigue siendo responsable de revisar la información y abrir el registro para validar el contexto.

## 2. Analizar listas sin salir de Business Central

Business Central ya permite aplicar filtros, ordenar columnas, guardar vistas y utilizar el modo de análisis.

Copilot añade una forma más natural de iniciar ese análisis.

Imaginemos que estamos revisando los movimientos de clientes y queremos identificar:

- Los clientes con mayor saldo.
- Las ventas agrupadas por región.
- Los artículos con más unidades vendidas.
- Los pedidos abiertos por vendedor.
- Los importes agrupados por mes.

En lugar de construir manualmente toda la vista, podemos describir el resultado esperado. Copilot puede proponer una vista con agrupaciones, filtros, totales y tablas dinámicas dentro del modo de análisis.

Esto no convierte a Business Central en una plataforma completa de Business Intelligence, ni reemplaza necesariamente a Power BI. El valor está en resolver análisis operativos directamente sobre la lista en la que ya estamos trabajando.

Por ejemplo, una persona responsable de cuentas por cobrar podría entrar a los movimientos de clientes y solicitar una vista que agrupe los saldos pendientes por cliente y fecha de vencimiento.

El resultado sería un punto de partida que después puede ajustarse funcionalmente.

<!-- IMAGEN 2: Lista de movimientos o clientes con una pestaña de análisis generada con Copilot -->

/assets/img/posts/copilot-bc-analisis.png
_Copilot puede ayudar a transformar una lista en una vista de análisis con filtros, agrupaciones y totales._

### ¿Dónde aporta valor?

Esta capacidad es especialmente útil cuando:

- El usuario conoce la pregunta, pero no domina el modo de análisis.
- Se necesita una revisión rápida antes de exportar datos.
- El análisis es operativo y no requiere un modelo semántico complejo.
- Se quiere permanecer dentro de Business Central.

Técnicamente, la experiencia trabaja sobre la información disponible en la lista. Por lo tanto, la calidad del resultado también depende de los campos que la página expone y de la calidad de los datos registrados.

## 3. Resumir clientes, proveedores y documentos

Una ficha de cliente puede contener datos generales, saldos, movimientos, documentos abiertos, estadísticas y diferentes cuadros informativos.

Para una persona que entra por primera vez al registro, revisar toda esa información puede tomar tiempo.

La función de resumen de Copilot busca reducir ese esfuerzo. Copilot presenta los puntos relevantes de un registro junto con enlaces que permiten ir al detalle.

Pensemos en un responsable de ventas que abre la ficha de un cliente antes de una llamada.

En lugar de recorrer todos los campos, podría obtener rápidamente un resumen con la información más importante para su rol. Luego podrá entrar al pedido, movimiento o documento relacionado para validar el dato.

Lo importante es entender que el resumen no crea una nueva fuente de información. Organiza y presenta información existente para facilitar su lectura.

<!-- IMAGEN 3: Ficha de cliente o proveedor con el resumen de Copilot visible -->

/assets/img/posts/copilot-bc-resumen.png
_Los resúmenes ayudan a identificar rápidamente los datos relevantes de un registro._

### Consideración funcional

Un resumen es útil para comprender el contexto, pero no sustituye la revisión del documento original.

Si el usuario necesita aprobar una transacción, realizar un registro contable o tomar una decisión financiera, debe abrir el detalle y comprobar la información.

Copilot acelera la lectura. La responsabilidad del proceso continúa en el usuario.

## 4. Completar campos con menos trabajo manual

Otra capacidad interesante es el autocompletado.

Cuando un usuario crea o modifica un registro, Copilot puede generar sugerencias para completar determinados campos. Las sugerencias pueden basarse en datos de la empresa, contenido generado por IA o, en ciertos escenarios, información pública encontrada en la web.

Pensemos en la creación de un nuevo artículo.

Normalmente debemos completar manualmente datos como:

- Descripción.
- Categoría.
- Unidad de medida.
- Dimensiones.
- Información comercial.
- Otros atributos relevantes.

Copilot puede proponer valores para algunos campos y permitir que el usuario decida qué conservar.

El punto clave está en la palabra **proponer**.

La IA puede reducir la digitación, pero los valores deben revisarse antes de incorporarlos al maestro. Una sugerencia incorrecta en una ficha de artículo puede impactar compras, ventas, inventario, contabilización o análisis posteriores.

<!-- IMAGEN 4: Ficha de artículo con sugerencias de autocompletado -->

/assets/img/posts/copilot-bc-autocompletar.png
_El usuario conserva el control y decide cuáles sugerencias incorporar al registro._

### Consideración técnica

La documentación de Microsoft indica que el autocompletado puede utilizarse en páginas de tipo ficha y documento, como artículos y pedidos de venta, y también puede extenderse a páginas personalizadas.

Esto abre un escenario interesante para partners y desarrolladores AL.

No todo tiene que resolverse con una aplicación externa. Algunas experiencias de IA pueden incorporarse dentro de la interfaz y del proceso normal de Business Central.

## 5. Crear líneas de venta a partir de una solicitud

Este es uno de los ejemplos que mejor permite conectar Copilot con un proceso comercial real.

Imaginemos que un cliente envía un mensaje como este:

> Necesito 10 unidades de la silla ejecutiva negra, 4 escritorios de 120 centímetros y 2 lámparas para oficina.

Tradicionalmente, el usuario debe interpretar el texto, buscar cada artículo y agregar las líneas a la cotización o al pedido.

Con las sugerencias de líneas de venta, el usuario puede escribir unas palabras, pegar una conversación o cargar un archivo. Copilot analiza el contenido e intenta identificar los artículos que coinciden para proponer las líneas del documento.

El resultado no debería registrarse automáticamente sin revisión.

El usuario debe validar:

- El cliente.
- El artículo identificado.
- La variante.
- La unidad de medida.
- La cantidad.
- La disponibilidad.
- El precio y los descuentos.
- Las fechas solicitadas.

Esta validación es especialmente importante cuando existen descripciones similares, referencias comerciales del cliente, sustitutos o unidades de medida diferentes.

<!-- IMAGEN 5: Cotización de venta con la ventana de sugerencias de líneas -->

/assets/img/posts/copilot-bc-lineas-venta.png
_Copilot interpreta la solicitud y propone artículos para incorporarlos a la cotización o al pedido._

### ¿Dónde está el valor?

El valor no está únicamente en ahorrar algunos segundos al ingresar una línea.

La capacidad permite convertir información no estructurada, como un correo o una conversación, en una propuesta estructurada dentro del ERP.

Ese puente entre lenguaje natural y documento empresarial es uno de los escenarios donde la IA puede generar un impacto más visible.

## 6. Generar textos de marketing para artículos

La generación de textos de marketing fue una de las primeras experiencias visibles de Copilot en Business Central.

A partir de la información de la ficha del artículo, Copilot puede proponer una descripción comercial tomando en cuenta atributos y preferencias de tono.

Por ejemplo, si tenemos un artículo con información técnica como material, color, dimensiones y categoría, Copilot puede convertir esos datos en un texto más atractivo para un catálogo o una tienda en línea.

El usuario puede revisar y ajustar el contenido antes de publicarlo.

Cuando se utiliza la integración de Shopify con Business Central, el texto puede incorporarse al flujo de publicación del producto en la tienda.

<!-- IMAGEN 6: Ficha de artículo y ventana de creación de texto de marketing -->

/assets/img/posts/copilot-bc-marketing.png
_Copilot convierte atributos del artículo en una propuesta de descripción comercial._

Este escenario es sencillo, pero muestra algo importante: Business Central no contiene únicamente información contable. También puede convertirse en la fuente de datos para procesos comerciales, canales digitales y experiencias de cliente.

## 7. Apoyar la conciliación bancaria

La conciliación bancaria es un proceso frecuente y, en algunos escenarios, intensivo en revisión manual.

Business Central ya dispone de reglas para emparejar automáticamente las líneas del extracto bancario con los movimientos bancarios. Sin embargo, pueden quedar líneas pendientes cuando las fechas, descripciones o agrupaciones no coinciden de forma directa.

Copilot complementa ese emparejamiento automático.

Por ejemplo, un cliente puede realizar un solo pago para cancelar varias facturas. En Business Central existen varios movimientos, pero en el extracto aparece una sola línea bancaria.

Copilot puede analizar fechas, importes y descripciones para proponer una coincidencia entre esa línea del banco y varios movimientos del sistema.

Para las líneas que siguen sin coincidencia, también puede sugerir una cuenta contable basándose en la descripción de la transacción y en los nombres de las cuentas.

Un cargo con una descripción relacionada con combustible, por ejemplo, podría generar una propuesta hacia una cuenta asociada con transporte.

<!-- IMAGEN 7: Conciliación bancaria con las propuestas de coincidencia de Copilot -->

/assets/img/posts/copilot-bc-conciliacion.png
_Las coincidencias propuestas deben revisarse antes de conservarlas o contabilizarlas._

### Lo que más me gusta de este enfoque

Copilot no elimina el control financiero.

Las propuestas se muestran para revisión y el usuario puede conservarlas, modificarlas o descartarlas. El proceso mantiene a la persona responsable dentro de la decisión.

Desde una perspectiva funcional, esto es fundamental. En un ERP, la automatización debe reducir trabajo sin perder trazabilidad ni control.

> Esta capacidad puede estar sujeta a versión, idioma, región y estado preliminar. Conviene validar su disponibilidad en cada ambiente antes de incluirla dentro del diseño definitivo del proceso.
{: .prompt-tip }

## 8. Sugerir artículos sustitutos

En ventas o servicio, un artículo sin inventario puede detener el proceso mientras alguien busca una alternativa.

Copilot puede analizar la información de los productos y proponer artículos sustitutos cuando el artículo original no está disponible o fue descontinuado.

El usuario puede revisar la propuesta considerando:

- Características del artículo.
- Disponibilidad.
- Precio.
- Unidad de medida.
- Compatibilidad comercial o técnica.
- Condiciones acordadas con el cliente.

Esta funcionalidad no debería reemplazar la definición de una estrategia de sustitución ni las reglas comerciales de la empresa.

Sí puede ayudar a encontrar alternativas y mantener el pedido en movimiento.

<!-- IMAGEN 8: Ficha o pedido mostrando una propuesta de artículo sustituto -->

/assets/img/posts/copilot-bc-sustitutos.png
_Copilot puede apoyar la búsqueda de alternativas cuando un artículo no está disponible._

## De Copilot a los agentes

Hasta aquí hemos hablado principalmente de experiencias donde el usuario inicia la acción y revisa una propuesta.

El siguiente nivel son los agentes.

Un ejemplo es el agente de pedidos de venta. Puede monitorear solicitudes recibidas por correo, identificar al contacto, interpretar los productos solicitados y preparar una cotización para revisión. Si el cliente confirma la cotización, el proceso puede continuar con la conversión a pedido.

En cuentas por pagar, el agente correspondiente puede monitorear facturas de proveedores, extraer información, buscar coincidencias con pedidos y recepciones, proponer cuentas para líneas sin coincidencia y dirigir excepciones para revisión.

Esto no significa que todo deba automatizarse.

Antes de implementar un agente, deberíamos definir:

- Qué evento inicia el proceso.
- Qué datos debe interpretar.
- Qué reglas de negocio debe respetar.
- Qué excepciones requieren intervención.
- Qué acciones puede realizar.
- En qué punto se necesita aprobación.
- Cómo se mantiene la trazabilidad.

<!-- IMAGEN 9: Diagrama simple Correo → Agente → Business Central → Revisión del usuario -->

/assets/img/posts/copilot-bc-agente.png
_Un agente puede avanzar el proceso, pero las reglas, excepciones y revisiones deben diseñarse previamente._

## Consideraciones antes de utilizar Copilot

Copilot no debe evaluarse únicamente desde una demostración.

Antes de llevarlo a un proceso real, recomiendo revisar al menos cinco aspectos.

### Disponibilidad

No todas las capacidades están disponibles en todas las versiones, regiones o idiomas. Algunas pueden encontrarse en versión preliminar.

### Datos

La calidad de las propuestas depende del contexto y de los datos disponibles. Maestros incompletos, descripciones poco claras o clasificaciones inconsistentes pueden afectar los resultados.

### Permisos

Copilot hereda los permisos del usuario. La seguridad de Business Central sigue siendo la base para determinar qué información puede consultar cada persona.

### Revisión humana

Las respuestas y sugerencias deben validarse, especialmente cuando afectan documentos comerciales, registros financieros o datos maestros.

### Proceso

La IA no corrige por sí sola un proceso mal definido. Antes de automatizar, debemos comprender las reglas, responsables, excepciones y controles del negocio.

## Una precisión importante: IA en Business Central no siempre significa Copilot

Business Central también dispone de capacidades basadas en modelos predictivos, como la previsión de ventas e inventario, la predicción de pagos atrasados y el análisis de flujo de caja.

Estas funciones también utilizan inteligencia artificial, pero no todas pertenecen a las experiencias de Copilot generativo.

La distinción es relevante:

- Las funciones predictivas utilizan datos históricos para estimar un resultado futuro.
- Copilot generativo interpreta lenguaje, crea contenido, resume información o genera propuestas.
- Los agentes pueden avanzar actividades específicas con mayor autonomía.

Todas forman parte de la evolución de Business Central, pero resuelven necesidades distintas.

## ¿Copilot reemplaza la configuración o el desarrollo?

No.

Copilot puede reducir tareas manuales y hacer que algunas funciones sean más accesibles, pero no reemplaza:

- El análisis del proceso.
- La configuración funcional.
- El modelo de permisos.
- Las dimensiones.
- Los grupos contables.
- Las reglas de inventario.
- Los flujos de aprobación.
- Las integraciones.
- Los desarrollos necesarios para cubrir requerimientos específicos.

Desde una perspectiva técnica, algunas capacidades de Copilot también pueden trabajar con contenido personalizado. Microsoft permite extender experiencias de IA mediante las herramientas de desarrollo de Business Central y conectar soluciones mediante Copilot Studio.

Esto no significa que cada necesidad requiera desarrollo.

Como en cualquier implementación, primero deberíamos revisar si el escenario se resuelve con estándar, configuración, Power Platform, una extensión AL o un agente.

La IA añade una nueva alternativa a la arquitectura, pero no elimina las decisiones de diseño.

## Reflexión final

Copilot en Business Central ya no es únicamente una idea futura.

Hoy puede ayudar a buscar datos, analizar listas, resumir registros, completar campos, preparar documentos comerciales, generar textos, apoyar conciliaciones y proponer alternativas de inventario.

Al mismo tiempo, debemos mantener expectativas realistas.

Copilot trabaja mejor cuando encuentra procesos claros, datos consistentes, permisos correctamente definidos y usuarios que revisan las propuestas antes de convertirlas en acciones.

Para mí, ahí está el verdadero valor.

No se trata solo de agregar Inteligencia Artificial al ERP. Se trata de utilizarla en el punto correcto del proceso para reducir trabajo manual, facilitar la adopción y permitir que las personas dediquen más tiempo a analizar, decidir y aportar valor.

Este es apenas el comienzo. En los siguientes artículos revisaré escenarios concretos y mostraré cómo estas capacidades pueden aplicarse dentro de procesos reales de Business Central.
