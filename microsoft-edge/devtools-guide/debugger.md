---
description: Use el depurador para recorrer paso a paso y solucionar problemas del código.
title: 'Depurador: DevTools (EdgeHTML)'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, depuración, depuración, puntos de interrupción, relojes, trabajos de servicios, API de caché, almacenamiento Web, cookies
ms.custom: seodec18
ms.openlocfilehash: 722277618cd8d6d5d6dba4f2a8bd3a28b6466f77
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882922"
---
# Depurador: DevTools (EdgeHTML)

Use el **depurador** para desplazarse por el código, establecer relojes y puntos de interrupción, editar en vivo el código e inspeccionar las cachés. Pruebe y solucione el problema de su código de la siguiente manera:

- [Examinar](#resource-picker) y [Buscar](#file-search) código de los archivos de código fuente cargados
- [Controlar el flujo de ejecución](#toolbar) a medida que se avanza por el código
- [Administrar recursos de almacenamiento de páginas](./storage.md#cache-manager), incluidos los [trabajos de servicio y la caché](./service-workers.md), las [cookies](./storage.md#cookies-list) y el [almacenamiento web](./storage.md#local-and-session-storage-managers)  
- [Establecer puntos de interrupción y editar en vivo](#debug-window) el código a medida que se ejecuta
- [Seguimiento y edición de variables locales a](#watches) medida que se depura
- [Ocultar o Mostrar código asincrónico y código de biblioteca](#call-stack) de la pila de llamadas según sea necesario
- [Agregar puntos de interrupción especializados](#breakpoints) para XmlHttpRequests, eventos y [mutaciones Dom](#dom-breakpoints)

![El depurador de DevTools de Microsoft Edge](./media/debugger.png)

Hay tres formas de iniciar una sesión de depuración.

1. **Establecer un punto de interrupción.** Cuando la ejecución de tu código llega a él, entrarás en el depurador y podrás recorrer el código.
2. **Inicia una interrupción en el código.** Haga clic en el botón de la barra de herramientas [**romper**](#toolbar) (icono de*pausa* ) o `Ctrl+Shift+B` . El depurador se interrumpirá en el siguiente Resumen de ejecución.
3. **Establezca el comportamiento de la excepción.** Use el menú [**cambiar comportamiento de excepción**](#toolbar) ( `Ctrl+Shift+E` ) para interrumpir el depurador cuando el código inicie una excepción. De forma predeterminada, el depurador se establece para que *nunca se interrumpa en las excepciones*, pero se registran en la consola.

## Selector de recursos

A menudo, el primer paso de la depuración es establecer puntos de interrupción en el código que buscas para solucionar el problema. Puede encontrar todos los archivos de código cargados actualmente por la página desde el panel *selector de recursos* , incluidos los archivos *. html,. CSS* y *. js* .

 Al hacer clic en una entrada de archivo se abrirá una pestaña para ese archivo en la [ventana de depuración](#debug-window) y en negrita el texto del nombre de archivo para indicar que se trata de este (como el nombre de archivo de la *Guía de DevTools* está en la ilustración anterior). Después, puede establecer puntos de interrupción dentro de ese archivo desde la [ventana depuración](#debug-window).

![Selector de recursos de depurador](./media/debugger_resource_picker.png)

En el menú contextual del *selector de recursos* , también puede marcar un archivo como **código de biblioteca** (), lo que `Ctrl+L` le ofrece la opción de [omitir el código en el depurador](#debug-window) y [ocultarlo en el panel de la **pila de llamadas** ](#call-stack). Si hace clic de nuevo en (o `Ctrl+L` ), el archivo volverá a su valor anterior como código de *código* o de *biblioteca*.

### Búsqueda de archivos

Use el comando *Buscar en archivos* ( `Ctrl` + `Shift` + `F` ) si tiene una cadena específica de código que está tratando de buscar en el origen. La barra de herramientas proporciona diferentes opciones de búsqueda, incluidas las expresiones regulares. Al hacer clic en un resultado de búsqueda, la *ventana de depuración* se centra en el archivo y la línea especificados.

![Panel de búsqueda de archivos del depurador](./media/debugger_file_search.png)

## Ventana depuración

La *ventana depuración* es el lugar donde se establecen los puntos de interrupción, se recorre el código y se modifica en vivo el script mientras se depura. Haga clic a la izquierda de cualquier comando de script para agregar (o quitar) un **punto de interrupción**. Use el menú contextual o el panel [**puntos de interrupción**](#breakpoints) para *Agregar una condición* al punto de interrupción proporcionando una expresión lógica que hace que el depurador se interrumpa si evalúa *verdadero* en esa ubicación.

![Comandos de la ventana Depurar](./media/debugger_window.png)

Otras características de la ventana depuración incluyen controles para:

### 1. edición de código

Puede editar el JavaScript en vivo durante una sesión de depuración. Una vez que haya realizado los cambios, haga clic en <strong> Guardar </strong> ( `Ctrl+S` ) para probar los cambios la próxima vez que se ejecute la sección de código. Si tiene cambios de código sin guardar, aparecerá un asterisco (\ *) antes del nombre de archivo en la pestaña de la *ventana depuración* .

Haga clic en el botón **comparar documento con el original** para ver las diferencias de los cambios que ha realizado.

![Vista de diferencias del código editado en el depurador](./media/debugger_edit_code.png)

Ten en cuenta las siguientes limitaciones:

- La edición de script solo funciona en archivos *. js* externos (y no incrustados `<script>` en *. html*)
- Las modificaciones se guardan en memoria y se vacían al volver a cargar el documento, por lo que no podrá ejecutar modificaciones dentro de un `DOMContentLoaded` controlador, por ejemplo
- Por el momento, no hay ninguna forma (como una opción **Guardar como** ) para guardar las modificaciones en el disco desde el DevTools

### 2. formato de código

Use estos controles para dar formato al código de minified para que sea más legible mientras depura:

#### Impresión muy imprimida ( `Ctrl+Shift+P` ) 
Agrega saltos de línea y alineación de llave por convenciones de JavaScript. Incluso el código comprimido que se ha hecho más legible con esta opción puede tener la función, el selector y los nombres de variable que son muy diferentes al código fuente original. En estos casos, es posible que la opción [*conmutar mapas de origen*](#source-maps) esté disponible.

#### Ajuste de texto ( `Alt+W` )
Ajusta el código para que quepa dentro de los márgenes actuales de la ventana de depuración (eliminando la necesidad de desplazamiento horizontal).

### 3. ámbito del código

Puede indicar al depurador que omita determinados archivos con el botón **marcar como código de biblioteca** ( `Ctrl+L` ). De forma predeterminada, el botón de la barra de herramientas [**depurar solo mi código**](#toolbar) está activado, lo que significa que el depurador omitirá todos los archivos que se marquen como *código de biblioteca* y no aparecerán en la [pila de llamadas](#call-stack)del depurador. Si presiona el botón (**marcar como mi código**), `Ctrl+L` se quitará esta marca.

Para realizar un seguimiento de las bibliotecas en las sesiones de depuración, puede editar estos archivos para mantener una lista predeterminada o agregar caracteres comodín para un dominio o tipo de archivo:

```JavaScript
%APPDATA%\..\LocalLow\Microsoft\F12\header\MyCode.json and %APPDATA%\..\Local\Microsoft\F12\header\MyCode.json
```

#### Mapas de origen

Verá el botón **conmutar mapas de origen** habilitado para el código escrito en un idioma que se compila en JavaScript o CSS y que proporciona una asignación de *origen* (una asignación de archivo intermedio al origen original). Esta opción indica al depurador que presente el origen original que se utilizará para la depuración (en lugar del archivo compilado que *realmente* se ejecuta en el explorador).

El DevTools verificará si el compilador que generó el archivo JavaScript incluyó un comentario con el nombre del archivo de asignación. Por ejemplo, si un compilador ha comprimido *myfile.js* *myfile.min.js*, también puede generar un archivo de asignación, *myfile.min.js. map* e incluir un Comentario en el archivo comprimido como este:

```JavaScript
//# sourceMappingURL=myfile.min.js.map
```

![Menú contextual de pestaña archivo de depuración](./media/debug_file_contextmenu.png)

Si el DevTools no puede encontrar el mapa automáticamente, puede elegir un mapa de origen para el archivo. Haga clic con el botón secundario en la pestaña del archivo para buscar la opción **elegir mapa de origen** . 

## Barra de herramientas

Use la barra de *herramientas* de depuración para controlar cómo se recorre el código y qué código se debe recorrer o ignorar. Aquí también puede realizar una búsqueda de texto completo en los archivos de código para cadenas específicas.

![Barra de herramientas de depuración](./media/debugger_toolbar.png)

### 1. Continue ( `F5` )/Break ( `Ctrl+Shift+B` )
 **Continue** ( `F5` ) continúa la ejecución del código al siguiente punto de interrupción. Si mantiene pulsado, los `F5` saltos anteriores se moverán varias veces hasta que la suelte. 

 **Break** ( `Ctrl+Shift+B` ) se interrumpirá en el depurador después de ejecutar la instrucción Next.

### 2. función Step ( `F11` , `Ctrl+F10` , `Shift+F11` )
 Instrucciones **paso a paso** ( `F11` ) a la función a la que se llama. 

 **Paso a paso por paso** por `Ctrl+F10` la función que se llama. 

 **Paso a paso** ( `Shift+F11` ) sale de la función actual y de la función de llamada. 

 El depurador pasará a la siguiente instrucción si no está en una función cuando se usan estos comandos.

### 3. interrumpir en un nuevo trabajador ( `Ctrl+Shift+W` )
 Saltos en la creación de un nuevo [trabajo web](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers).

### 4. control de excepciones
**Cambiar comportamiento de excepción** ( `Ctrl+Shift+E` ) abre las opciones para cambiar la forma en que el depurador reacciona ante las excepciones. De forma predeterminada, el depurador omite las excepciones e inicia sesión en la [**consola**](./console.md). Puede elegir *interrumpir en todas las excepciones*o solo aquellas que no se controlan mediante `try...catch` instrucciones en el código (*interrumpir en excepciones no controladas*).

### 5. ver resultados de la búsqueda
(Actualmente deshabilitada). **Mostrar u ocultar resultados** activa o desactiva la visualización de los resultados de búsqueda [*Buscar en archivos*](#6-find-in-files-ctrlf) .

### 6. Buscar en archivos ( `Ctrl+F` )
 **Buscar en archivos** ( `Ctrl+F` ) ejecuta una búsqueda de texto en todos los archivos cargados dentro del [*selector de recursos*](#resource-picker). Si se encuentra el texto, se abre el primer archivo que coincide con la cadena de búsqueda. `Enter`O `F3` lo lleva a la siguiente coincidencia.

### 7. depurar solo mi código ( `Ctrl+J` )
 **Depurar solo mi código** ( `Ctrl+J` ) actúa como un botón de alternancia para incluir o excluir todos los archivos que se han marcado como [código de biblioteca](#3-code-scoping) a medida que avanza por el depurador.

### 8. conexión del depurador
**Desconectar o conectar depurador** es esencialmente el interruptor de encendido y apagado del depurador.

## Busca

Use el panel **relojes** para examinar un catálogo de todos los objetos y variables (**locales**), tanto en el ámbito local como en el global, disponibles para la instrucción que es el foco de la interrupción actual en el depurador.

![Panel relojes](./media/debugger_watches.png)

Puede realizar un seguimiento del valor de variables específicas a medida que pasan y salen de ámbito agregando un reloj (**Agregar inspección** `Ctrl+W` ) y modificando los valores modificables haciendo doble clic en él o seleccionando **Editar valor** en el *menú contextual*. Borre las inspecciones con los botones **eliminar** ( `Ctrl+D` ) o **eliminar todos** o en el menú contextual. 

## Detalles

El panel de *detalles* incluye las pestañas [**pila de llamadas**](#call-stack), [**puntos**](#breakpoints) de interrupción y [**puntos de interrupción Dom**](#dom-breakpoints) .

### Pila de llamadas

La pestaña **pila de llamadas** muestra la cadena de funciones que llevaron al punto de ejecución actual. La función actual aparece en la parte superior y las funciones de llamada se muestran debajo de él en orden inverso.

![Panel de pila de llamadas](./media/debugger_callstack.png)

El botón **Mostrar u ocultar Marcos** de la biblioteca ( `Ctrl+Shift+J` ) activa o desactiva la salida del [código](#3-code-scoping) de la biblioteca de la pila de llamadas. Use la opción de **código de biblioteca** ( `Ctrl+L` ) del *menú contextual* para marcar (o desmarcar) el origen del fotograma seleccionado como código de biblioteca. 

El botón **Mostrar u ocultar fotogramas asincrónicos** activa o desactiva la visualización de las raíces de las llamadas a funciones asincrónicas.

### Puntos de interrupción

En la pestaña **puntos de interrupción** puede administrar los puntos de interrupción y los puntos de seguimiento de eventos, incluyendo la configuración de condiciones, deshabilitarlos y eliminarlos.

![Pestaña puntos de interrupción](./media/debugger_breakpoints.png)

A continuación se muestra un resumen de los distintos tipos de puntos de interrupción que puede usar para la depuración.

Tipo de punto de interrupción | Descripción | Cómo configurarlo
:------------ | :------------ | :--------
**Punto** | Entra en el depurador justo antes de que se ejecute la línea de código especificada. Es más fácil establecer puntos de interrupción normales si tiene una instrucción por línea. | En la [ventana depuración](#debug-window), haga clic en el margen izquierdo junto a cualquier número de línea en el código. Aparece un punto rojo y se establece el punto de interrupción. Puede saltar al origen de cualquier punto de interrupción haciendo clic en su texto azul.
**Punto de interrupción condicional** | Se rompe si la condición especificada se evalúa como *verdadero*. Esto es esencialmente una `if(condition)` para irrumpir en el depurador.  | En la pestaña [puntos](#breakpoints) de interrupción, desplace el puntero sobre un punto de interrupción existente y haga clic en el botón "lápiz" (*agregue una condición a este punto de interrupción*), haga clic con el botón derecho en un punto de interrupción existente y seleccione **condición...** en el menú contextual. Especifique la condición "si" que se va a evaluar en la ubicación del punto de interrupción. 
**Punto de interrupción de XMLHttpRequest** (con condición opcional) | Se rompe cada vez que se ha cumplido una solicitud XMLHttpRequest (XHR). Puede inspeccionar el `response` objeto XHR desde el panel [**inspecciones**](#watches) . | En la pestaña [puntos de interrupción](#breakpoints) , haga clic en el botón de punto de *interrupción XMLHttpRequest* (círculo con flechas hacia arriba o hacia abajo). Puede convertirla en un *punto de interrupción condicional* según se describe anteriormente.
**Punto de seguimiento de evento** | Llamadas [`console.log()`](./console/console-api.md#logging-custom-messages) con una cadena especificada en respuesta a un evento específico. Use esto para las instrucciones de registro de consola temporales que no desea guardar directamente en el código del controlador de eventos. | En la pestaña [puntos de interrupción](#breakpoints) , haga clic en el botón punto de *seguimiento* (rombo con rayo). Seleccione un tipo de **evento** para el desencadenador y una instrucción de **seguimiento** para el registro.
**Punto de interrupción de evento** (con condición opcional) | Se rompe cada vez que se desencadena un evento especificado. | En la pestaña [puntos](#breakpoints) de interrupción, haga clic en el botón *punto de interrupción del evento* (círculo con rayo). Seleccione un tipo de **evento** para el desencadenador y, opcionalmente, especifique una instrucción de **condición** . 
**Punto de interrupción DOM** | Se rompe cada vez que se muta un elemento especificado de la página, como cuando se modifica su subárbol, cambian sus atributos o cuando se separa de DOM. | En la pestaña [elementos](./elements/dom-breakpoints.md) , haga clic con el botón derecho en un elemento de origen y seleccione entre las opciones de *puntos de interrupción Dom* . Use la pestaña [**puntos de interrupción Dom**](#dom-breakpoints) en los paneles *depurador* o *elementos* para administrar los puntos de interrupción. 

Los puntos de interrupción y los puntos de seguimiento condicionales tienen acceso a todas las variables locales y globales que se encuentran actualmente en el ámbito al entrar en el depurador.

### Puntos de interrupción DOM

Administre los puntos de interrupción de mutación de DOM en la pestaña de **puntos de interrupción Dom** , incluyendo la desactivación, la eliminación y el reenlace.  Los [puntos de interrupción de Dom se pueden establecer](./elements/dom-breakpoints.md) desde la *vista de árbol HTML* en el panel **elementos** .

![Pestaña puntos de interrupción DOM](./media/debugger_dom_breakpoints.png)

La pestaña *puntos de interrupción de Dom* en el **depurador** proporciona una funcionalidad equivalente a la pestaña *puntos de interrupción** en el panel **elementos** .

Más información sobre los diferentes tipos de [puntos de interrupción de Dom](./elements/dom-breakpoints.md).

## Abreviados

### Accesos directos de la barra de herramientas

Acción | Acceso directo
:------------ | :-------------
Buscar | `Ctrl` + `F`
Continuar (desde el punto de interrupción) | `F5` o `F8`
Avance rápido | Hold `F5` o `F8`
Continuar y actualizar | `Ctrl` + `Shift` + `F5`
Inter | `Ctrl` + `Shift` + `B`
Ir a | `F11`
Paso a paso por procedimientos | `F10`
Salir | `Shift` + `F11`
Interrumpir en un nuevo trabajador | `Ctrl` + `Shift` + `W`
Comportamiento de cambio de excepción (menú) | `Ctrl` + `Shift` + `E`
Depurar solo mi código | `Ctrl` + `J`

### Métodos abreviados del selector de recursos

Acción | Acceso directo
:------------ | :-------------
Marcar como mi código/código de biblioteca | `Ctrl` + `L`
Abrir archivo | `Ctrl` + `O`, `Ctrl` + `P`
Buscar en todos los archivos | `Ctrl` + `Shift` + `F`

### Accesos directos a la ventana depuración

Acción | Acceso directo
:------------ | :-------------
Quitar punto de interrupción | `F9`
Deshabilitar punto de interrupción | `Ctrl` + `F9`
Punto de interrupción condicional... | `Alt` + `F9`
Copiar | `Ctrl` + `C`
Guardar | `Ctrl` + `S`
Ir a la línea... | `Ctrl` + `G`
Mostrar la instrucción siguiente | `Alt` + `Num` + `*`
Ejecutar hasta el cursor | `Ctrl` + `F10`
Establecer instrucción siguiente | `Ctrl` + `Shift` + `F10`
Mostrar en el selector de archivos | `Ctrl` + `Alt` + `P`
Ir a definición en archivo | `Ctrl`+`D`
Buscar referencias en archivo | `Ctrl` + `Shift` + `D`
Impresión con sangría | `Ctrl` + `Shift` + `P`
Ajuste de texto | `Alt` + `W`
Marcar como mi código/código de biblioteca | `Ctrl` + `L`
Deshabilitar o habilitar las pestañas del editor. **Nota:** si usa el teclado para navegar en el depurador, no podrá salir del editor hasta que deshabilite la tabulación. | `Ctrl` + `M`

### Panel de accesos directos para los relojes

Acción | Acceso directo
:------------ | :-------------
Agregar inspección | `Ctrl` + `W`
Eliminar inspección | `Ctrl` + `D`

### Métodos abreviados para el panel detalles

| Acción                             | Acceso directo                 |
|:-----------------------------------|:-------------------------|
| Mostrar u ocultar marcos del código de la biblioteca | `Ctrl` + `Shift` + `J`   |
| Habilitar todos los puntos de interrupción             | `Ctrl` + `Shift` + `F11` |
