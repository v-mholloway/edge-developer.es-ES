---
description: Usar la línea de comandos de consola para interactuar con una página en ejecución
title: DevTools-consola-línea de comandos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, línea de comandos de consola
ms.custom: seodec18
ms.openlocfilehash: c661736e5ea264f60279c89cfa0f9c55361d2288
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574657"
---
# Línea de comandos de consola

Use la línea de comandos de consola para ver y cambiar los valores de una página y ejecutar código de depuración sobre la marcha, todo ello aprovechando la finalización de código automático de Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) . 

Solo tienes que introducir cualquier JavaScript válido en la línea de comandos y pulsar `Enter` para ejecutar. Para la entrada de varias líneas `Shift+Enter` , agregue un salto de línea. Use las `Up` `Down` teclas de dirección para desplazarse por los comandos de consola anteriores que especificó durante la sesión de DevTools actual. Además de JavaScript estándar y la [API de consola](./console-api.md), la consola también admite los siguientes comandos para:

 - [Selección de objetos DOM](#dom-selectors)
 - [Inspeccionar propiedades de objetos](#object-inspection)
 - [Buscar todos los agentes de escucha de eventos en un objeto dado](#event-listeners)

La secuencia de comandos escrita en la línea de comandos se ejecuta en el [ámbito global](/scripting/javascript/advanced/variable-scope-javascript) de la ventana seleccionada en ese momento, a menos que la página se haya pausado en un punto de interrupción. Los comandos de consola introducidos mientras la página está en pausa se ejecutarán en el [ámbito local](/scripting/javascript/advanced/variable-scope-javascript) de la función actual dentro de la pila de llamadas.

La consola tiene un menú desplegable de ejecución de **destino** justo encima del área de salida de la consola. La selección predeterminada es el documento de nivel superior, **_top**. Los iframes en el documento o las extensiones que se ejecutan también aparecerán como opciones, lo que le permite ejecutar comandos de forma alternativa dentro de esos ámbitos.

## Selectores de DOM
Estos selectores de consola proporcionan abreviaciones sencillas para acceder rápidamente a los objetos dentro del DOM:

### $ (*Cadena de selector CSS*)
Devuelve el primer elemento del documento que coincide con el [selector CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) (o el grupo de selectores separados por comas) especificado. Abreviatura de [Document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).

Ejemplo: Abra la consola y escriba `$('#main')` para devolver el objeto div con `id='main'` en esta página.

![Ejemplo de uso del selector "$"](../media/console_cmd_$.png)

### $ $ (*Cadena de selector CSS*)
Devuelve una matriz de elementos dentro del documento que coincide con el [selector CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) especificado (o la cadena de selectores separados por comas). Abreviatura de [Document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).

Ejemplo: Abra la consola y escriba `$$('.container')` para devolver todos los objetos div con `class='container'` en esta página.

![Ejemplo de uso del selector $ $ '](../media/console_cmd_$$.png)

### $0, $1, $2,...
Devuelve los últimos elementos seleccionados en el panel [**elementos**](../elements.md) , donde `$0` representa el elemento seleccionado actualmente, `$1` y así sucesivamente.

Ejemplo: Abra DevTools en la pestaña **elementos** , presione `CTRL + B` para activar la herramienta **Seleccionar elemento** y haga clic en un área de esta página con el mouse. Ahora abra la consola y escriba `$0` para devolver el elemento en el que acaba de hacer clic.

![Ejemplo de uso del selector ' $0 '](../media/console_cmd_$0.png)

### $x (*expresión XPath*)
Devuelve una matriz de elementos coincidentes con la expresión [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) especificada. 

Ejemplo: Abra la consola y escriba `$x('//script[@defer]')` para devolver todos los `<script>` elementos de esta página que contienen un `defer` atributo.

![Ejemplo de uso del selector ' $x '](../media/console_cmd_$x.png)

## Inspección de objetos

Estos comandos proporcionan formas rápidas de inspeccionar las propiedades de un objeto. El objeto especificado debe definirse en el espacio de nombres global o en el ámbito actual del depurador.

### DIR (*objeto*)
Devuelve una lista de las propiedades del objeto especificado en vista de árbol.

Ejemplo: Abra la consola y escriba `dir(document)` para ver las propiedades del objeto de documento que representa esta página.

![Ejemplo de uso del método ' dir '](../media/console_cmd_dir.png)

### Keys (*objeto*)
Devuelve una matriz de nombres de propiedad adjuntos al objeto especificado.

Ejemplo: Abra la consola y escriba `keys(window)` para devolver todas las propiedades definidas en el objeto de ventana global.

![Ejemplo de uso del método ' Keys '](../media/console_cmd_keys.png)

### Values (*Object*)
Devuelve una matriz de valores de propiedad asociada al objeto especificado.

Ejemplo: Abra la consola y escriba `values(window)` para devolver los valores de todas las propiedades (claves) definidas en el objeto de ventana global.

![Ejemplo de uso del método ' Values '](../media/console_cmd_values.png)

## Detectores de eventos

Este comando le permite inspeccionar los agentes de escucha de eventos registrados en un objeto determinado. El objeto especificado debe definirse en el espacio de nombres global o en el ámbito actual del depurador.

### getEventListeners (*objeto*)
Devuelve un objeto que contiene una clave para cada tipo de evento registrado en el objeto dado. El valor de cada clave es una matriz de agentes de escucha de eventos y su información relacionada. 

Ejemplo: Abra la consola y escriba `getEventListeners(document)` para ver todas las escuchas de eventos registradas en el objeto de documento de esta página.

![Ejemplo de uso del método ' getEventListeners '](../media/console_cmd_getEventListeners.png)
