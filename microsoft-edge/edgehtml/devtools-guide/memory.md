---
description: Use el panel memoria para
title: 'DevTools: memoria'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, memoria, montón, GC, recolección de elementos no utilizados, retenciones de tamaño, Dominators
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5ad284f8072cc296743299ec9c4fb2037f8fd883
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236004"
---
# Memoria

Use el panel **memoria** para medir el uso de los recursos del sistema y Comparar instantáneas de montones en diferentes Estados de ejecución de código. Con ella, puedes hacer lo siguiente:

- [Representar el consumo de memoria de la página en tiempo real](#memory-usage-timeline) y tomar instantáneas del montón
- [Identificar problemas potenciales de memoria](#snapshot-summary) en el código, como objetos retenidos no adjuntos al Dom
- [Revisar los datos de uso de memoria](#snapshot-details) por tipo de objeto, recuento de instancias, tamaño y referencias para ayudar a aislar problemas
- [Aplicar filtros de datos de instantáneas](#filters) para reducir el ruido de información no accionable
- [Identificar el costo de memoria de un objeto específico](#object-references) y las referencias que lo mantienen activo
- [Comparar el montón en diferentes fases de su investigación](#snapshot-comparison) para localizar el origen de las pérdidas de memoria y otros problemas

![Panel de memoria de Microsoft Edge DevTools](./media/memory.png)


## Barra de herramientas

1. **Iniciar o detener la sesión de generación de perfiles (Ctrl + E)**: activar el generador de perfiles le permite realizar un seguimiento del uso de memoria y tomar instantáneas del montón.
2. **Importar sesión de generación de perfiles (Ctrl + O)**: cargue una sesión de diagnóstico de memoria de DevTools guardada.
3. **Exportar sesión de generación de perfiles (Ctrl + S)**: guardar la sesión de diagnóstico actual en el disco.
4. **Tomar instantánea de montón (Ctrl + Mayús + T)**: registrar asignaciones de memoria actuales para un punto de tiempo determinado.


## Escala de tiempo de uso de memoria

Los problemas de memoria pueden ser una causa importante de problemas de rendimiento, lo que hace que la página deje de responder y sea más atrasada a lo largo del tiempo.

El primer paso para analizar el uso de memoria de la página es [iniciar una sesión de generación de perfiles](#toolbar) con el fin de llevar instantáneas antes o después de que se reproduzcan los pasos que producen saturación de memoria o una pérdida de memoria sospechosa.

Al iniciar el generador de perfiles de memoria, verá un gráfico de memoria de proceso que le permite observar el conjunto de trabajo privado global (la cantidad de memoria consumida por la página) a lo largo del tiempo. El gráfico de memoria muestra una vista en vivo de la memoria de proceso de la pestaña, que incluye bytes privados, memoria nativa y el montón de JavaScript. 

![Escala de tiempo de uso de memoria](./media/memory_timeline.png)

 El gráfico le da una indicación de la tendencia de la memoria de la página que le permite juzgar Cuándo es adecuado [tomar una instantánea de montón](#toolbar) para compararla posteriormente, como cuando ve períodos de retención de memoria inesperada.

### Performance. Mark ()

Puede agregar marcas de **usuario** personalizadas a la escala de tiempo para ayudar a identificar eventos clave durante el curso de su sesión de análisis mediante una llamada al [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) método desde el código o la [**consola**](./console.md)de DevTools.

### Console. takeheapSnapshot ()

En ocasiones, es necesario tomar instantáneas en momentos específicos, como inmediatamente antes de una gran mutación del DOM. En estos casos, puede tomar instantáneas mediante programación con [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .

## Resumen de instantáneas

[Tomar una instantánea](#toolbar) generará un icono de resumen que indica el tamaño del montón de JavaScript en el momento en que se realizó la instantánea, junto con el número de objetos asignados y una captura de pantalla de la página. Puede seguir tomando instantáneas en cualquier momento mientras se ejecuta a través del escenario de usuario que requiere análisis. Las instantáneas generan mosaicos adicionales, cada uno de los cuales indica la diferencia en la memoria JavaScript de la instantánea anterior.

![Instantánea de montón](./media/memory_snapshot.png)

Al hacer clic en los valores del icono Resumen, se cambiará al panel con los [detalles de los datos de la instantánea](#snapshot-details). Los posibles [problemas de memoria se indican](#snapshot-details) con un icono de información azul ("i").

## Detalles de instantáneas

Los datos del panel *instantáneas* muestran los objetos creados por la página, junto con cualquier memoria asignada por Marcos de JavaScript que pueda estar consumiendo.

![Tabla detalles de instantáneas](./media/memory_details.png)

Las tres pestañas representan distintas vistas de los datos:

#### Tipos

Muestra el recuento de instancias y el tamaño total de los objetos del montón, agrupados por tipo de objeto. De forma predeterminada, se ordenan por recuento de instancias.

Al seleccionar un objeto en el panel *tipos* superiores, en la tabla [referencias de objetos](#object-references) del panel inferior se enumeran todos los objetos que apuntan a ese objeto.

#### Raíz

Muestra una vista jerárquica de las referencias secundarias para describir cómo los objetos se arraigan en el objeto global, lo que impide su recolección de elementos no utilizados.

De forma predeterminada, los nodos secundarios se ordenan por la columna tamaño retenido, con el tamaño más alto en la parte superior.

#### Dominators

Muestra una lista de objetos en el montón que tienen referencias exclusivas a otros objetos. Dominators se ordenan por tamaño retenido para indicar que los objetos que consumen la mayor cantidad de memoria son potencialmente más fáciles de liberar.

A continuación se explica cómo interpretar las columnas de los *tipos, las raíces* y las vistas de *Dominators* :

Columna | Descripción
:------------ | :-------------
Identificador (s) | Nombre que mejor identifica el objeto. Por ejemplo, para los elementos HTML, los detalles de la instantánea muestran el valor del atributo ID, si se usa alguno.
Tipo | Tipo de objeto (por ejemplo, *HTMLDivElement*).
Tamaño | Tamaño del objeto, sin incluir el tamaño de los objetos a los que se hace referencia.
Tamaño retenido | Tamaño de objeto más el tamaño de todos los objetos secundarios que no tienen otros elementos primarios. Por motivos prácticos, esta es la cantidad de memoria que retiene el objeto, por lo que si elimina el objeto, se reclama la cantidad de memoria especificada.
Número | Número de instancias de objetos. Este valor solo aparece en la vista tipos.

Al seleccionar un objeto en el panel superior de *Dominators* , en la tabla [referencias de objetos](#object-references) del panel inferior se enumeran todos los objetos que apuntan a ese objeto.

### Filtros

Puede ajustar aún más los datos de la tabla con lo siguiente:

![Filtrar por integradas e identificadores de objetos](./media/memory_filter.png)

1. **Filtro de identificador**: filtrar datos buscando un identificador de objeto concreto
2. **Agrupar por Dominator**: solo se muestran los objetos con referencias *exclusivas* a otros objetos en la vista de nivel superior de los objetos (esta es la vista predeterminada de la pestaña *Dominators* ).
3. **Filtro de incorporaciones/IDS**: de forma predeterminada, los [objetos integrados de JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) se incluyen en la lista. La lista de identificadores de objetos puede ser útil si hay varios objetos anónimos que deben diferenciarse.

Los *tipos, las raíces* y las vistas de *Dominators* tienen su propio filtro, por lo que el filtro no se conserva al cambiar a otra vista.

### Referencias a objetos

En las vistas [**tipos**](#types) y [**Dominators**](#dominators) , el panel inferior contiene una lista de **referencias de objeto** que muestra las referencias compartidas. Al elegir un objeto en el panel superior, esta lista muestra todos los objetos que apuntan a ese objeto, en otras palabras, los objetos que mantienen activos el objeto seleccionado.

Las referencias circulares se muestran con un asterisco (*) y la información sobre herramientas informativa, y no se pueden expandir. De lo contrario, impediría subir el árbol de referencia e identificar los objetos que están conservando la memoria.

Para identificar rápidamente los objetos equivalentes, marque la opción de filtro [*Mostrar identificadores de objeto*](#filters) para mostrar los identificadores de objeto junto a los nombres de objeto en la columna *identificador (s)* . Los objetos que tienen el mismo identificador son referencias compartidas.

### Comparación de instantáneas

Al hacer clic en una [ficha comparación de instantáneas](#snapshot-details) o en un vínculo de comparación en el [mosaico Resumen de instantánea](#snapshot-summary)  , aparecerá una diferencia de información entre las dos instantáneas. En el panel comparación, las vistas *Dominators, tipos* y *raíces* proporcionan los mismos [*detalles de instantánea*](#snapshot-details) que se verían para una única instantánea, con estos valores adicionales:

Columna | Descripción
:------------ | :-------------
Diferencia de tamaño. | Diferencia entre el tamaño del objeto en la instantánea actual y su tamaño en la instantánea anterior, sin incluir el tamaño de los objetos a los que se hace referencia.
Diferencias de tamaño retenida. | Diferencia entre el tamaño conservado del objeto en la instantánea actual y su tamaño retenido en la instantánea anterior. El tamaño retenido incluye el tamaño del objeto, además del tamaño de todos sus objetos secundarios, que no tienen otros elementos primarios. Por motivos prácticos, el tamaño retenido es la cantidad de memoria retenida por el objeto, por lo que si elimina el objeto, se reclama la cantidad de memoria especificada.

Puede usar la lista desplegable **ámbito** para filtrar la información diferencial entre instantáneas:

![Filtro de ámbito de las comparaciones de instantáneas](./media/memory_comparison_scope_filter.png)

- <strong>Objetos que quedan de la instantánea # <number></strong> : muestra las diferencias entre los objetos agregados al montón y que se han quitado del montón de la instantánea de línea base a la instantánea anterior. Por ejemplo, si el Resumen de instantánea muestra <em> + 205/-195 </em> en el recuento de objetos, este filtro mostrará los diez objetos que se han agregado pero no se han quitado.

- <strong>Los objetos agregados entre la instantánea # <number> y # <number></strong> : muestran todos los objetos agregados al montón desde la instantánea anterior.

- <strong>Todos los objetos de la instantánea # <number></strong> : muestra todos los objetos del montón (en otras palabras, una <em> vista sin filtrar </em> ).

De forma predeterminada, el filtro *Mostrar referencias no coincidentes* se aplica a la vista comparación para indicar referencias de objeto que no coinciden con el filtro de ámbito actual. Puede desactivarla en el menú desplegable:

![Filtro de referencias no coincidentes para comparaciones de instantáneas](./media/memory_comparison_matching_filter.png)


## Accesos directos

 Acción | Acceso directo
:------------ | :-------------
Iniciar o detener sesión de generación de perfiles  | `Ctrl` + `E`
Importar sesión de generación de perfiles | `Ctrl` + `O`
Exportar sesión de generación de perfiles | `Ctrl` + `S`
Tomar instantánea de montón | `Ctrl` + `Shift` + `T`

## Problemas conocidos

### Se produjo un error al iniciar la sesión de generación de perfiles

Si ve este mensaje de error: **se ha producido un error al iniciar la sesión de generación de perfiles** en la herramienta memoria, siga estos pasos para obtener una solución alternativa.

1. Presione `Windows Key`  +  `R` .

2. En el cuadro de diálogo Ejecutar, escriba **Services. msc**.
![problemas conocidos-1](./media/known_issues_1.PNG)

3. Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.
![problemas conocidos-2](./media/known_issues_2.PNG)

4. Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.
![problemas conocidos-3](./media/known_issues_3.PNG)

5. Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .

6. Ahora debería poder comenzar a crear perfiles. 
![problemas conocidos-4](./media/known_issues_4-memory.PNG)

¿Aún tiene problemas? Envíenos sus comentarios con el icono para **Enviar comentarios** . 

![problemas conocidos-5](./media/known_issues_5.PNG)
