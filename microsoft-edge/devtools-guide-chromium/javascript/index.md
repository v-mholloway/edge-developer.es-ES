---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para buscar y corregir errores de JavaScript.
title: Introducción a la depuración de JavaScript en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e146c6708f097b1ea8dc82f08be58f5aa5e52d1f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398444"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a>Introducción a la depuración de JavaScript en Microsoft Edge DevTools  

Este artículo le enseña el flujo de trabajo básico para depurar cualquier problema de JavaScript en DevTools.  

## <a name="step-1-reproduce-the-bug"></a>Paso 1: Reproducir el error  

Encontrar una serie de acciones que reproducen un error de forma coherente siempre es el primer paso para la depuración.  

1.  Elija **Abrir demostración**.  Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y abra la demostración en una nueva pestaña del explorador.  
    
    [Demostración abierta][OpenDebugJSDemo]  
    
1.  Escriba `5` en el cuadro de texto Número **1.**  
1.  Escriba `1` en el cuadro de texto Número **2.**  
1.  Elija **Agregar número 1 y número 2**.  La etiqueta debajo del botón indica `5 + 1 = 51` .  El resultado debe ser `6` .  A continuación, corrija el error de adición que es el error.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 da como resultado 51, pero debe ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` da como `51` resultado , pero debe ser `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a>Paso 2: Familiarizarse con la interfaz de usuario de la herramienta Orígenes  

DevTools proporciona muchas herramientas diferentes para distintas tareas.  Entre las tareas diferentes se incluyen cambiar CSS, generar perfiles de rendimiento de carga de página y supervisar solicitudes de red.  La **herramienta Orígenes** es donde se depura JavaScript.  

1.  Para abrir la **herramienta Consola** en DevTools, seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="La herramienta Consola" lightbox="../media/javascript-console-empty.msft.png":::
       La **herramienta Consola**  
    :::image-end:::  
    
1.  Elija la **herramienta Orígenes.**  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="La herramienta Orígenes" lightbox="../media/javascript-sources-sections.msft.png":::
       La **herramienta Orígenes**  
    :::image-end:::  
    
La **interfaz de usuario de** la herramienta Orígenes tiene tres partes.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Las 3 partes de la interfaz de usuario de la herramienta Orígenes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   Las 3 partes de la interfaz **de usuario de la herramienta Orígenes**  
:::image-end:::  

1.  El **panel Explorador de** archivos \(Sección 1 de la figura anterior\).  Aquí se enumeran todos los archivos que solicita la página web.  
1.  El **panel Editor de** código \(Sección 2 de la figura anterior\).  Después de seleccionar un archivo en el panel **Explorador de** archivos, el contenido de ese archivo se muestra aquí.  
1.  El **panel Depuración de JavaScript** \(Sección 3 de la figura anterior\).  Varias herramientas para inspeccionar JavaScript para la página web.  Si la ventana DevTools es amplia, este panel se muestra a la derecha del **panel Editor de** código.  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a>Paso 3: Pausar el código con un punto de interrupción  

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

El `console.log()` método puede realizar el trabajo, pero los puntos de **interrupción** lo hacen más rápido.  Un punto de interrupción permite pausar el código en medio del tiempo de ejecución y examinar todos los valores en ese momento.  Los puntos de interrupción tienen las siguientes ventajas sobre el `console.log()` método.  

*   Con , debe abrir manualmente el código fuente, buscar el código relevante, insertar las instrucciones y, a continuación, actualizar la página web para mostrar los mensajes en `console.log()` `console.log()` la **consola**.  Con los puntos de interrupción, puede pausar el código relevante sin saber siquiera cómo se estructura el código.  
*   En las `console.log()` instrucciones, debe especificar explícitamente cada valor que desea inspeccionar.  Con puntos de interrupción, DevTools muestra los valores de todas las variables en ese momento.  A veces, las variables que afectan al código están ocultas y ocultas.  
    
En resumen, los puntos de interrupción pueden ayudarle a encontrar y corregir errores más rápido que el `console.log()` método.  

Si retroces y piensas en cómo funciona la aplicación, puedes hacer una conjetura educada de que la suma incorrecta \( \) se calcula en el agente de escucha de eventos asociado con los botones Agregar número 1 y Número `5 + 1 = 51` `click` **2.**  Por lo tanto, probablemente quiera pausar el código durante el tiempo en que se ejecute `click` el agente de escucha.  **Los puntos de interrupción de escucha de** eventos le permiten hacer exactamente lo siguiente:  

1.  En el **panel Depuración de JavaScript,** elija Puntos de interrupción de **escucha de eventos** para expandir la sección.  DevTools muestra una lista de categorías de eventos expandibles, como **Animación y** **Portapapeles.**  
1.  Junto a la categoría de eventos **Mouse,** elija **Expandir** \( ![ Expandir icono ][ImageExpandIcon] \).  DevTools muestra una lista de eventos de mouse, como clic **y** **mousedown**.  Cada evento tiene una casilla junto a él.  
1.  Seleccione la casilla situada junto **a**.  DevTools ahora está configurado para pausar automáticamente cuando se ejecuta cualquier `click` escucha de eventos.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Seleccione la casilla situada junto a hacer clic" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Seleccione la casilla situada junto a **hacer clic**  
    :::image-end:::  
    
1.  En la demostración, vuelve **a elegir Agregar número 1 y Número 2.**  DevTools pausa la demostración y resalta una línea de código en la **herramienta** Orígenes.  DevTools debe pausar la línea 16 en `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Si pausa en una línea de código diferente, elija Reanudar ejecución de **script** \( Reanudar ejecución de script \) hasta que se detenga ![ en la línea ][ImageResumeIcon] correcta.  
    
    > [!NOTE]
    > Si hizo una pausa en una línea diferente, tiene una extensión de explorador que registra un agente de escucha de eventos en todas las páginas `click` web que visita.  Está en pausa en el agente `click` de escucha de la extensión.  Si usa el modo InPrivate para examinar en privado **,** lo que deshabilita todas las extensiones, es posible que vea que se pausa en la línea de código deseada cada vez.  

<!--todo: add inprivate section when available -->  

**Los puntos de interrupción de escucha de** eventos son solo uno de los muchos tipos de puntos de interrupción disponibles en DevTools.  Memoriza todos los tipos diferentes para ayudarte a depurar escenarios diferentes lo antes posible.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a>Paso 4: Paso a paso por el código  

Una causa común de errores es cuando un script se ejecuta en el orden incorrecto.  El paso a través del código le permite recorrer el tiempo de ejecución del código.  Puede recorrer una línea a la vez para ayudarle a averiguar exactamente dónde se ejecuta el código en un orden diferente del esperado.  Pruébalo ahora:  

1.  Elija **Paso sobre la siguiente llamada de función** \( Paso sobre la siguiente llamada de función ![ ][ImageOverIcon] \).  DevTools ejecuta el siguiente código sin entrar en él.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools omite algunas líneas de código.  Esto se debe a que se evalúa como false, por lo que no se ejecuta el bloque `inputsAreEmpty()` de código de la `if` instrucción.  
    
1.  En la **herramienta Orígenes** de DevTools, elija Paso a siguiente llamada de función **\(** Paso a siguiente llamada de función \) para pasar por el tiempo de ejecución de la función, una línea ![ a ][ImageIntoIcon] `updateLabel()` la vez.  
    
Revisar una línea a la vez es la idea básica de pasar por el código.  Si revisa el código en , el error probablemente esté en `get-started.js` algún lugar de la `updateLabel()` función.  En lugar de pasar por todas las líneas de código, puede usar otro tipo de punto de interrupción para pausar el código más cerca de la ubicación probable del error.  

## <a name="step-5-set-a-line-of-code-breakpoint"></a>Paso 5: Establecer un punto de interrupción de línea de código  

Los puntos de interrupción de línea de código son el tipo más común de punto de interrupción.  Cuando llegue a la línea de código específica que desea pausar, use un punto de interrupción de línea de código.  

1.  Vea la última línea de código en `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  A la izquierda, el número de esta línea de código en particular se muestra como **34**.  Elija la **línea 34**.  DevTools muestra un icono rojo a la izquierda de **34**.  El icono rojo indica que un punto de interrupción de línea de código está en esta línea.  DevTools siempre se pausa antes de que se ejecute esta línea de código.  
1.  Elija **Reanudar ejecución de script** \( Reanudar ejecución de script ![ ][ImageResumeIcon] \).  El script continúa en ejecución hasta que llega a la línea 33.  En las líneas 31, 32 y 33, DevTools imprime los valores de , y a la derecha de los dos puntos y coma `addend1` `addend2` en cada `sum` línea.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools se pausa en el punto de interrupción de línea de código en la línea 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools se pausa en el punto de interrupción de línea de código en la línea 34  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a>Paso 6: Comprobar valores de variables  

Los valores de `addend1` , `addend2` y parecen `sum` sospechosos.  Los valores están entre comillas.  Las comillas significan que el valor es una cadena, que es una buena hipótesis para explicar la causa del error.  Recopila más información sobre la situación.  DevTools proporciona muchas herramientas para examinar valores de variables.  

### <a name="method-1-the-scope-panel"></a>Método 1: panel Ámbito  

Si se pausa en una línea de código, el **panel** Ámbito muestra las variables locales y globales que están definidas actualmente, junto con el valor de cada variable.  También muestra variables de cierre, según corresponda.  Haga doble clic en un valor de variable para editarlo.  Si no se pausa en una línea de código, **el** panel Ámbito está vacío.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   Panel **Ámbito**  
:::image-end:::  

### <a name="method-2-watch-expressions"></a>Método 2: Ver expresiones  

El **panel Ver expresiones** le permite supervisar los valores de las variables a lo largo del tiempo.  Como su nombre indica, **las expresiones de** reloj no se limitan a variables.  Puede almacenar cualquier expresión de JavaScript válida en una **expresión Watch**.  Pruébalo ahora.  

1.  Elija **el** panel Ver.  
1.  Elija **Agregar expresión** \( Agregar expresión ![ ][ImageAddIcon] \).  
1.  Escribe `typeof sum`.  
1.  Seleccione `Enter` .  DevTools muestra `typeof sum: "string"` .  El valor a la derecha de los dos puntos es el resultado de la expresión Watch.  
    
> [!NOTE]
> En el **panel Ver expresión** \(bottom-right\) de la siguiente figura, se muestra la expresión `typeof sum` watch.  Si la ventana DevTools es grande, el panel **Ver** expresión se encuentra a la derecha encima del panel Puntos de interrupción **de escucha de eventos.**  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Panel Expresión de reloj" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Panel **Expresión de** reloj  
:::image-end:::  

Como se sospecha, `sum` se está evaluando como una cadena, cuando debe ser un número.  Ahora ha confirmado que el tipo de valor es la causa del error.  

### <a name="method-3-the-console"></a>Método 3: La consola  

La **consola** le permite ver mensajes y también puede usarlos para evaluar `console.log()` instrucciones de JavaScript arbitrarias.  Para la depuración, puede usar la **consola** para probar posibles correcciones de errores.  Pruébalo ahora.  

1.  Si la **herramienta** Consola está cerrada, seleccione `Escape` para abrirla.  La **herramienta** Consola se abre en el panel inferior de la ventana DevTools.  
1.  En la **consola**, escriba `parseInt(addend1) + parseInt(addend2)` .  La instrucción que la herramienta se pausa en una línea de código donde `addend1` y están en el `addend2` ámbito.  
1.  Seleccione `Enter` .  DevTools evalúa la instrucción e imprime , que es el `6` resultado que espera que la demostración produzca.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="La herramienta Consola, después de evaluar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       La **herramienta Consola,** después de evaluar `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a>Paso 7: Aplicar una corrección  

Si encuentras una solución para el error, prueba la corrección editando el código y rerunning la demostración.  Puede editar código JavaScript directamente en la interfaz de usuario de DevTools y aplicar la corrección.  Pruébalo ahora.  

1.  Elija **Reanudar ejecución de script** \( Reanudar ejecución de script ![ ][ImageResumeIcon] \).  
1.  En el **Editor de código,** reemplace la línea 32, `var sum = addend1 + addend2` , por `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.  
1.  Elija **Desactivar puntos de interrupción** \( Desactivar puntos de ![ interrupción ][ImageDeactivateIcon] \).  Cambia de color azul para indicar que la opción está activa.  Mientras **se establecen los puntos** de interrupción Deactivate, DevTools omite los puntos de interrupción establecidos.  
1.  Pruebe la demostración con valores diferentes.  La demostración ahora calcula correctamente.  
    
> [!CAUTION]
> Este flujo de trabajo solo aplica una corrección al código que se ejecuta en el explorador.  No corrige el código de todos los usuarios que visitan la página web.  Para ello, debe corregir el código que está en los servidores.  

## <a name="next-steps"></a>Pasos siguientes  

¡Enhorabuena!  Ahora sabe cómo obtener el máximo partido de Microsoft Edge DevTools al depurar JavaScript.  Las herramientas y los métodos que aprendió en este artículo pueden ahorrarle incontables horas.  

Este artículo solo le enseñó dos formas de establecer puntos de interrupción.  DevTools ofrece muchas otras formas, incluida la siguiente configuración.  

*   Puntos de interrupción condicionales que solo se desencadenan cuando la condición que se proporciona es true.  
*   Puntos de interrupción en excepciones capturadas o no capturadas.  
*   Puntos de interrupción XHR que se desencadenan cuando la dirección URL solicitada coincide con una subcadena que se proporciona.  
    
Para obtener más información sobre cuándo y cómo usar cada tipo, vaya [a Pausar el código con puntos de interrupción][DevtoolsJavscriptBreakpoints].  

En este artículo no se explica un par de controles de paso a paso de código.  Para obtener más información, vaya [a Paso sobre la línea de código][DevtoolsJavascriptReferenceStepThroughCode].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

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
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Paso a paso por el código: referencia de depuración de JavaScript | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abra la demostración | Glitch"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
