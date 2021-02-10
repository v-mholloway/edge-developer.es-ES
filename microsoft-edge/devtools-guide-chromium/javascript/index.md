---
description: Aprende a usar Microsoft Edge DevTools para buscar y corregir errores de JavaScript.
title: Introducción a la depuración de JavaScript en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325954"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# Introducción a la depuración de JavaScript en Microsoft Edge DevTools  

Este artículo le enseña el flujo de trabajo básico para depurar cualquier problema de JavaScript en DevTools.  

## Paso 1: Reproducir el error  

Encontrar una serie de acciones que reproduzcan de forma coherente un error siempre es el primer paso para la depuración.  

1.  Elija **Abrir demostración.**  Espera `Control` \(Windows, Linux\) o \(macOS\) y abre la `Command` demostración en una nueva pestaña del explorador.  
    
    [Demostración abierta][OpenDebugJSDemo]  
    
1.  Escriba `5` en el cuadro de texto Número **1.**  
1.  Escriba `1` en el cuadro de texto Número **2.**  
1.  Elija **Agregar número 1 y Número 2.**  La etiqueta debajo del botón indica `5 + 1 = 51` .  El resultado debe ser `6` .  A continuación, corrija el error de adición que es el error.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 da como resultado 51, pero debe ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` da como `51` resultado , pero debe ser `6`  
    :::image-end:::  
    
## Paso 2: Familiarizarse con la interfaz de usuario del panel Orígenes  

DevTools proporciona muchas herramientas diferentes para diferentes tareas.  Entre las distintas tareas se incluyen el cambio de CSS, la generación de perfiles de rendimiento de la carga de páginas y la supervisión de solicitudes de red.  El **** panel Orígenes es donde se depura JavaScript.  

1.  Abre DevTools presionando `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  Este acceso directo abre el panel **Consola.**  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Panel de consola" lightbox="../media/javascript-console-empty.msft.png":::
       La **herramienta consola**  
    :::image-end:::  
    
1.  Elija la **herramienta Orígenes.**  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Panel Orígenes" lightbox="../media/javascript-sources-sections.msft.png":::
       Panel **Orígenes**  
    :::image-end:::  
    
La **interfaz de** usuario del panel Orígenes tiene tres partes.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Las 3 partes de la interfaz de usuario del panel Orígenes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   Las 3 partes de la interfaz de usuario **del** panel Orígenes  
:::image-end:::  

1.  El **panel Navegador de** archivos \(Sección 1 de la figura anterior\).  Todos los archivos que solicita la página web se enumeran aquí.  
1.  El **panel Editor** de código \(Sección 2 de la figura anterior\).  Después de seleccionar un archivo en el panel Navegador **de** archivos, el contenido de ese archivo se muestra aquí.  
1.  El **panel depuración de JavaScript** \(Sección 3 de la figura anterior\).  Varias herramientas para inspeccionar el JavaScript de la página web.  Si la ventana de DevTools es ancha, este panel se muestra a la derecha del **panel Editor de** código.  
    
## Paso 3: Pausar el código con un punto de interrupción  

Un método común para depurar este tipo de problema es insertar varias instrucciones en el código y, a continuación, inspeccionar los valores a medida que `console.log()` se ejecuta el script.  Por ejemplo:  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

El `console.log()` método puede realizar el trabajo, pero los puntos de **interrupción** lo hacen más rápido.  Un punto de interrupción le permite pausar el código en medio del tiempo de ejecución y examinar todos los valores en ese momento.  Los puntos de interrupción tienen algunas ventajas sobre el `console.log()` método:  

*   With `console.log()` , you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.  Con los puntos de interrupción, puede pausar el código relevante sin saber cómo está estructurado el código.  
*   En las `console.log()` instrucciones, debe especificar explícitamente cada valor que desee inspeccionar.  Con los puntos de interrupción, DevTools muestra los valores de todas las variables en ese momento en el tiempo.  A veces, las variables que afectan al código están ocultas y ocultas.  
    
En resumen, los puntos de interrupción pueden ayudarle a encontrar y corregir errores más rápido que el `console.log()` método.  

Si retroces y piensa en cómo funciona la aplicación, puedes hacer una suposición informada de que la suma incorrecta \( \) se calcula en el agente de escucha de eventos asociado con el botón Agregar número 1 y Número `5 + 1 = 51` `click` **2.**  Por lo tanto, probablemente quieras pausar el código en el momento en que se ejecuta `click` el agente de escucha.  **Los puntos de interrupción del agente** de escucha de eventos le permiten hacer exactamente lo siguiente:  

1.  En el **panel Depuración de JavaScript,** elija Puntos de interrupción de escucha **de eventos** para expandir la sección.  DevTools muestra una lista de categorías de eventos expandibles, como **animación** y **portapapeles.**  
1.  Junto a la **categoría de eventos del mouse,** elija **Expandir** \( Icono ![ Expandir ][ImageExpandIcon] \).  DevTools muestra una lista de eventos de mouse, **como** hacer clic y pasar **el mouse.**  Cada evento tiene una casilla al lado.  
1.  Seleccione la casilla situada junto a **.**  DevTools ahora está configurado para pausar automáticamente cuando se ejecuta cualquier escucha `click` de eventos.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Elegir la casilla junto a hacer clic" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Seleccione la casilla al lado para **hacer clic**  
    :::image-end:::  
    
1.  De nuevo en la demostración, elija **Agregar número 1 y Número 2** de nuevo.  DevTools pausa la demostración y resalta una línea de código en **el** panel Orígenes.  DevTools debe pausar en la línea 16 in `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Si hace una pausa en una línea de código diferente, presione Reanudar ejecución de **script** \( Reanudar ejecución de script \) hasta que se detenga ![ en la línea ][ImageResumeIcon] correcta.  
    
    > [!NOTE]
    > Si ha pausado en una línea diferente, tiene una extensión de explorador que registra un agente de escucha de eventos en todas las páginas `click` web que visite.  Se ha pausado en el `click` agente de escucha de la extensión.  Si usas el modo InPrivate para navegar en **privado,** lo que deshabilita todas las extensiones, es posible que veas que pausas en la línea de código deseada cada vez.  

<!--todo: add inprivate section when available -->  

**Los puntos de interrupción del agente de** escucha de eventos son solo uno de los muchos tipos de puntos de interrupción disponibles en DevTools.  Memoriza todos los tipos diferentes para ayudarte a depurar diferentes escenarios lo antes posible.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Paso 4: Paso a paso por el código  

Una causa común de errores es cuando un script se ejecuta en un orden incorrecto.  El paso a través del código te permite recorrer el tiempo de ejecución del código.  Puede recorrer una línea cada vez para averiguar exactamente dónde se ejecuta el código en un orden diferente del esperado.  Pruébalo ahora:  

1.  Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).  DevTools ejecuta el siguiente código sin entrar en él.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools omite algunas líneas de código.  Esto se debe a que se evalúa como false, por lo que no se ejecuta el bloque de código de `inputsAreEmpty()` `if` la instrucción.  
    
1.  En **el** panel Orígenes de DevTools, elija Paso a paso en la siguiente llamada de función **\(** Paso a siguiente llamada de función \) para pasar por el tiempo de ejecución de la función, una línea ![ cada ][ImageIntoIcon] `updateLabel()` vez.  
    
Revisar una línea a la vez es la idea básica de pasar por el código.  Si observa el código en , verá que el error probablemente se encuentra en `get-started.js` algún lugar de la `updateLabel()` función.  En lugar de pasar por cada línea de código, puede usar otro tipo de punto de interrupción para pausar el código más cerca de la ubicación probable del error.  

## Paso 5: Establecer un punto de interrupción de línea de código  

Los puntos de interrupción de línea de código son el tipo más común de punto de interrupción.  Cuando llegue a la línea de código específica que desea pausar, use un punto de interrupción de línea de código.  

1.  Mire la última línea de código `updateLabel()` en:  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  A la izquierda, el número de esta línea de código en particular se muestra como **34**.  Elija la **línea 34.**  DevTools coloca un icono rojo a la izquierda de **34**.  El icono rojo indica que hay un punto de interrupción de línea de código en esta línea.  DevTools siempre hace una pausa antes de ejecutar esta línea de código.  
1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  El script continúa ejecutándose hasta que llega a la línea 33.  En las líneas 31, 32 y 33, DevTools imprime los valores de , y a la derecha del punto y coma `addend1` `addend2` en cada `sum` línea.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools se pausa en el punto de interrupción de línea de código en la línea 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools se pausa en el punto de interrupción de línea de código en la línea 34  
    :::image-end:::  
    
## Paso 6: Comprobar los valores de las variables  

Los valores de `addend1` , `addend2` y parecen `sum` sospechosos.  Los valores se encapsulan entre comillas.  Las comillas significan que el valor es una cadena, que es una buena hipótesis para explicar la causa del error.  Recopila más información sobre la situación.  DevTools proporciona muchas herramientas para examinar valores de variables.  

### Método 1: el panel Ámbito  

Si hace una pausa en **** una línea de código, el panel Ámbito muestra las variables locales y globales que están definidas actualmente, junto con el valor de cada variable.  También muestra variables de cierre, según corresponda.  Haga doble clic en un valor de variable para editarlo.  Si no pausa una línea de código, el **panel** Ámbito está vacío.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   Panel **Ámbito**  
:::image-end:::  

### Método 2: Expresiones de reloj  

El **panel Expresiones de supervisión** permite supervisar los valores de las variables a lo largo del tiempo.  Como su nombre indica, **las expresiones de** watch no están limitadas a variables.  Puede almacenar cualquier expresión de JavaScript válida en una **expresión watch**.  Pruébalo ahora.  

1.  Elija el **panel** Ver.  
1.  Elija **Agregar expresión** \( Agregar expresión ![ ][ImageAddIcon] \).  
1.  Escribe `typeof sum`.  
1.  Seleccione `Enter` .  DevTools muestra `typeof sum: "string"` .  El valor a la derecha de los dos puntos es el resultado de la expresión de reloj.  
    
> [!NOTE]
> En el **panel Expresión de** reloj \(abajo a la derecha\) de la siguiente figura, se muestra la expresión de la `typeof sum` vista.  Si la ventana DevTools **** es grande, el panel Expresión de reloj se encuentra a la derecha sobre el panel Puntos de interrupción de escucha **de eventos.**  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Panel De expresiones de reloj" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Panel **De expresiones de** reloj  
:::image-end:::  

Como se sospecha, `sum` se está evaluando como una cadena, cuando debe ser un número.  Ahora ha confirmado que el tipo de valor es la causa del error.  

### Método 3: La consola  

La **consola** le permite ver mensajes y también puede usarlos para evaluar `console.log()` instrucciones arbitrarias de JavaScript.  Para la depuración, puede usar la **consola para** probar posibles correcciones de errores.  Pruébalo ahora.  

1.  Si el **cajón** de la consola está cerrado, `Escape` selecciónelo para abrirlo.  El **cajón** de la consola se abre en el panel inferior de la ventana DevTools.  
1.  En la **consola,** escriba `parseInt(addend1) + parseInt(addend2)` .  La instrucción que la herramienta se pausa en una línea de código donde `addend1` y están en el `addend2` ámbito.  
1.  Seleccione `Enter` .  DevTools evalúa la instrucción e imprime, que es el `6` resultado que esperas que produzca la demostración.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="El cajón de la consola, después de evaluar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       El **cajón de** la consola, después de evaluar `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## Paso 7: Aplicar una corrección  

Si encuentras una corrección para el error, prueba la corrección editando el código y rerunning la demostración.  Puedes editar código JavaScript directamente en la interfaz de usuario de DevTools y aplicar la corrección.  Pruébalo ahora.  

1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  
1.  En el **Editor de**código, reemplace la línea 32, , `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.  
1.  Elija **Desactivar puntos de interrupción** \( Desactivar puntos de ![ ][ImageDeactivateIcon] interrupción \).  Cambia de color azul para indicar que la opción está activa.  Mientras **se establecen los puntos de interrupción** Deactivate, DevTools omite los puntos de interrupción que establezca.  
1.  Pruebe la demostración con diferentes valores.  La demostración ahora calcula correctamente.  
    
> [!CAUTION]
> Este flujo de trabajo solo aplica una corrección al código que se ejecuta en el explorador.  No corrige el código de todos los usuarios que visitan la página web.  Para ello, debe corregir el código que se encuentra en los servidores.  

## Pasos siguientes  

¡Enhorabuena!  Ahora ya sabes cómo obtener el máximo partido de Microsoft Edge DevTools al depurar JavaScript.  Las herramientas y los métodos que aprendió en este artículo pueden ahorrarle incontables horas.  

En este artículo solo se le enseñaron dos formas de establecer puntos de interrupción.  DevTools ofrece muchas otras formas, incluida la siguiente configuración.  

*   Puntos de interrupción condicionales que solo se desencadenan cuando la condición que se proporciona es verdadera.  
*   Puntos de interrupción en excepciones detectadas o no detectadas.  
*   Puntos de interrupción XHR que se desencadenan cuando la dirección URL solicitada coincide con una subcadena que se proporciona.  
    
Para obtener más información sobre cuándo y cómo usar cada tipo, vaya a [Pausar el código con puntos de interrupción.][DevtoolsJavscriptBreakpoints]  

En este artículo no se explica un par de controles paso a paso de código.  Para obtener más información, vaya [a Paso a través de la línea de código.][DevtoolsJavascriptReferenceStepThroughCode]  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Código paso a paso: referencia de depuración de JavaScript | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abra el archivo de demostración | Problemas"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
