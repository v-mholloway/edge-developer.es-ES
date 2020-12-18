---
description: Use el panel elementos para inspeccionar el HTML, CSS, DOM y la accesibilidad de la página.
title: Elementos DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, elementos, HTML, CSS, puntos de interrupción de Dom, eventos, accesibilidad
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 14052bc40b9f94e628f0b575ede6c1ca8ccf179a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236013"
---
# Elementos

El panel **elementos** le ayuda a:

* [Identificar y modificar elementos en el árbol HTML](#html-tree-view) de la página actual
* [Inspeccionar y modificar CSS](./elements/styles.md) en la página, incluidos los pseudo-Estados y los pseudo-elementos
* [Comprender el diseño CSS y la cascada de estilos](./elements/computed.md) que se producen en la página
* [Realizar un seguimiento de los controladores de eventos no fiables](./elements/events.md) para poder depurarlos
* [Establecer puntos de interrupción de depuración para cambios visuales inesperados](./elements/dom-breakpoints.md) para saltar al código que los causa
* [Obtener información detallada sobre las fuentes usadas en la página](./elements/fonts.md) y desde dónde se están cargando
* [Ver la página desde el punto de vista de un lector de pantalla](./elements/accessibility.md) para comprobar y probar la accesibilidad 
* [Revisar una diferencia continuada de los cambios de CSS](./elements/changes.md) que realiza mientras depura la interfaz de usuario de la página

## Vista de árbol HTML

![Panel de elementos de DevTools de Microsoft Edge](./media/elements.png)

1. Use la herramienta **Select Element** ( `Ctrl+B` ) para localizar un elemento en la **vista de árbol HTML** haciendo clic en él en la página.

2. Use la herramienta de **resaltado de elementos** ( `Ctrl+Shift+L` ) para localizar un elemento en la página moviendo el puntero sobre él en la **vista de árbol HTML**.

3. Abra la herramienta **selector de colores** ( `Ctrl+K` ) para ver una lista de los colores que se usan en la página actual. Al hacer clic en un color de la lista encontrará más detalles (matiz, saturación, luminosidad, alfa). El *selector de colores* también se abre al hacer clic en el cuadrado coloreado junto a un valor de color en el panel **estilos** , lo que permite editar el color de un elemento de página y ver inmediatamente los resultados.

4. El botón de **accesibilidad Tree** ( `Ctrl+Shift+A` ) abrirá el panel [árbol de accesibilidad](./elements/accessibility.md) , que muestra la estructura de la página tal como aparecería ante una tecnología de asistencia, como la Screenreader de [narrador de Windows](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) .

5. También puede **encontrar** ( `Ctrl+F` ) un elemento en la vista de árbol HTML buscando el nombre de la etiqueta, los atributos o el contenido de texto.

### Editar elementos

Puede editar un elemento haciendo clic con el botón secundario en la vista de árbol HTML y seleccionando **Editar como HTML** en el menú contextual. El menú contextual también proporciona opciones para eliminar, cortar, copiar, pegar, establecer pseudoclase de CSS (*: activo*, *: foco*, *: suspender*, *: visitado*) y agregar atributos. Otra forma de modificar un atributo o su valor es hacer doble clic en él desde la vista de árbol HTML.

![Menú contextual de vista de árbol HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> Editar el árbol HTML no afecta al marcado de origen subyacente. Si actualiza la página, revertirá los cambios y representará solo el diseño determinado por el origen de la página. Puede **copiar** el código HTML modificado en el portapapeles haciendo clic con el botón secundario en el elemento deseado (o el `html` elemento global, si quiere que toda la página) Abra el menú contextual. (Las opciones de**cortar** y **pegar** también están disponibles).

En el panel [estilos](./elements/styles.md) , también puede Agregar, eliminar o modificar los pseudo-Estados CSS y los pseudo-elementos.

## Paneles de herramientas

Una vez que haya seleccionado un elemento de página de interés, puede usar los paneles de herramientas para inspeccionar más los distintos estilos y propiedades de accesibilidad, ver sus agentes de escucha de eventos y establecer puntos de interrupción de mutación de DOM.

![Paneles de herramientas en el panel elementos](./media/elements_toolpanes.png)

1. [**Estilos**](./elements/styles.md): estilos aplicados actualmente organizados por hoja de estilos

2. [**Calculado**](./elements/computed.md): estilos aplicados actualmente organizados por atributos CSS

3. [**Eventos**](./elements/events.md): agentes de escucha de eventos registrados en el elemento actual y elementos antecesores

4. [**Puntos de interrupción Dom**](./elements/dom-breakpoints.md): puntos de interrupción de mutación Dom 

5. [**Fuentes**](./elements/fonts.md): fuentes aplicadas actualmente para un elemento seleccionado

6. [**Accesibilidad**](./elements/accessibility.md): propiedades de accesibilidad

7. [**Cambios**](./elements/changes.md): cambios de CSS realizados durante la sesión de diagnóstico  

## Accesos directos

| Acción               | Acceso directo               |
|:---------------------|:-----------------------|
| Panel elementos       | `Ctrl` + `1`           |
| Resaltado de elementos | `Ctrl` + `Shift` + `L` |
| Seleccionar elemento       | `Ctrl` + `B`           |
| Selector de colores         | `Ctrl` + `K`           |
| Árbol de accesibilidad   | `Ctrl` + `Shift` + `A` |
