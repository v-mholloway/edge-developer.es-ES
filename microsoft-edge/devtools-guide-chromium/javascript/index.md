---
title: Introducción a la depuración de JavaScript en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 06df1fd4d6457a3f02be85b95959bdc353865495
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581827"
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



Este tutorial le enseña el flujo de trabajo básico para la depuración de cualquier problema de JavaScript en DevTools.  

## Paso 1: reproducir el error   

Encontrar una serie de acciones que reproduce sistemáticamente un error siempre es el primer paso para la depuración.  

1.  Haga clic en **abrir demo**.  Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y abra la demostración en una pestaña nueva.  

    [Abrir demos] [OpenDebugJSDemo]  

1.  Escriba `5` en el cuadro de texto **número 1** .  
1.  Escriba `1` en el cuadro de texto **número 2** .  
1.  Haga clic en **Agregar número 1 y número 2**.  La etiqueta que se encuentra debajo del botón dice `5 + 1 = 51` .  El resultado debería ser `6` .  Este es el error que va a corregir.  
    
    > ##### Figura 1  
    > El resultado de `5 + 1` es `51` , pero debe ser `6`  
    > ![El resultado de 5 + 1 es 51, pero debe ser 6][ImageJSBugs]  

## Paso 2: Familiarícese con la interfaz de usuario del panel de orígenes   

DevTools proporciona una gran variedad de herramientas para diferentes tareas, como, por ejemplo, el cambio de CSS, la generación de perfiles de rendimiento de carga de páginas y la supervisión de solicitudes de red.  El panel **orígenes** es donde se depura JavaScript.  

1.  Abra DevTools presionando `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  Este método abreviado de teclado abre el panel de **consola** .  
    
    > ##### Figura 2  
    > Panel de **consola**  
    > ![Panel de consola][ImageJSConsole]  

1.  Haga clic en la pestaña **orígenes** .  
    
    > ##### Imagen 3  
    > Panel **orígenes**  
    > ![Panel orígenes][ImageJSSources]  

La interfaz de usuario del panel de **orígenes** tiene 3 partes:  

> ##### Imagen 4  
> Las 3 partes de la interfaz de usuario del panel de **fuentes**  
> ![Las 3 partes de la interfaz de usuario del panel de fuentes][ImageJSSourcesAnnotated]  

1.  El panel **Explorador de archivos** \ (sección 1 de la [ilustración 4](#figure-4)\).  Todos los archivos que solicita la página se muestran aquí.  
1.  El panel del **Editor de código** \ (sección 2 de la [ilustración 4](#figure-4)\).  Después de seleccionar un archivo en el panel **Explorador de archivos** , el contenido de ese archivo se muestra aquí.  
1.  El panel de **depuración de JavaScript** \ (sección 3 de la [figura 4](#figure-4)\).  Varias herramientas para inspeccionar el JavaScript de la página.  Si la ventana de DevTools es ancha, este panel se muestra a la derecha del panel del **Editor de código** .  

## Paso 3: pausar el código con un punto de interrupción   

Un método común para depurar un problema como este es insertar muchas instrucciones en `console.log()` el código, para poder inspeccionar valores a medida que se ejecuta el script.  Por ejemplo:  

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

El `console.log()` método puede realizar el trabajo, pero los **puntos de interrupción** pueden hacerlo más rápido.  Un punto de interrupción le permite pausar el código en el medio del tiempo de ejecución y examinar todos los valores en ese momento.  Los puntos de interrupción tienen algunas ventajas en comparación con el `console.log()` método:  

*   Con `console.log()` , debe abrir manualmente el código fuente, buscar el código correspondiente, insertar las `console.log()` instrucciones y, a continuación, volver a cargar la página para ver los mensajes en la consola.  Con los puntos de interrupción, puedes hacer una pausa en el código relevante sin necesidad de saber cómo se estructura el código.  
*   En las `console.log()` instrucciones debe especificar explícitamente cada valor que desee inspeccionar.  Con los puntos de interrupción, DevTools muestra los valores de todas las variables en ese momento.  A veces, hay variables que afectan al código que aún no se tiene en cuenta.  

En Resumen, los puntos de interrupción pueden ayudarle a encontrar y corregir errores más rápidamente que el `console.log()` método.  

Si toma un paso atrás y piensa en cómo funciona la aplicación, puede hacer una conjetura educada de que la suma incorrecta ( `5 + 1 = 51` ) se calcula en el `click` agente de escucha de eventos asociado al botón **Agregar número 1 y número 2** .  Por lo tanto, es probable que desee pausar el código en el momento en que `click` se ejecuta el agente de escucha.  Los **puntos de interrupción de escucha de eventos** te permiten hacer exactamente eso:  

1.  En el panel de **depuración de JavaScript** , haga clic en **puntos de interrupción de escucha de eventos** para expandir la sección.  DevTools revela una lista de categorías de eventos expansibles, como la **animación** y el **portapapeles**.  
1.  Junto a la categoría de evento **del mouse** , haga clic en **expandir** ![ icono expandir ][ImageExpandIcon] .  DevTools revela una lista de los eventos del mouse, como **click** y **MouseDown**.  Cada evento tiene una casilla al lado.  
1.  Active la casilla **click** .  DevTools está configurado para pausarse automáticamente cuando *any* `click` se ejecuta cualquier detector de eventos.  
    
    > ##### Imagen 5  
    > La casilla **click** está habilitada  
    > ![La casilla click está habilitada][ImageJSClickCheckbox]  
    
1.  De nuevo en la demostración, haz clic en **Añadir número 1 y número 2 de** nuevo.  DevTools en pausa la demostración y resalta una línea de código en el panel **orígenes** .  DevTools se debe pausar en la línea 16 `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Si se detiene en una línea de código diferente, presione **reanudar script Execution** ![ resume script Execution ][ImageResumeIcon] hasta que se detenga en la línea correcta.  
    
    > [!NOTE]
    > Si ha pausado en una línea diferente, tiene una extensión de explorador que registra un `click` detector de eventos en cada página que visite.  Se pausó en la `click` escucha de la extensión.  Si usa el modo de InPrivate para **explorar en privado**, lo que deshabilita todas las extensiones, es posible que vea que se detiene en la línea de código deseada cada vez.  

<!--todo: add inprivate section when available -->  

Los puntos de interrupción de **escucha de eventos** son solo uno de los muchos tipos de puntos de interrupción disponibles en DevTools.  Merece la pena memorizar todos los tipos diferentes, ya que cada tipo en último término le ayuda a depurar diferentes escenarios lo antes posible.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Paso 4: recorrer el código   

Una causa común de los errores es cuando un script se ejecuta en el orden equivocado.  Al recorrer el código, podrás recorrer el motor en tiempo de ejecución de tu código, de línea en línea, y averiguar exactamente dónde se está ejecutando en un orden diferente del esperado.  Pruébelo ahora:  

1.  Haga clic en **paso a paso por la siguiente llamada de función** ![ ][ImageOverIcon] .  DevTools ejecuta el siguiente código sin entrar en él.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  

    > [!NOTE]
    > DevTools omite unas líneas de código.  Esto se debe `inputsAreEmpty()` a que evalúa como falso, por lo que el bloque de código para la instrucción no se `if` ejecuta.  

1.  En el panel **orígenes** de DevTools, haga clic en **paso a** paso por la siguiente función llamar ![ a la siguiente llamada de función para desplazarse ][ImageIntoIcon] por el motor en tiempo de ejecución de la `updateLabel()` función, una línea cada vez.  

Es la idea básica de recorrer el código.  Si miras el código de `get-started.js` , verás que el error probablemente esté en algún lugar de la `updateLabel()` función.  En lugar de ir pasando por todas las líneas de código, puede usar otro tipo de punto de interrupción para pausar el código más cerca de la ubicación probable del error.  

## Paso 5: establecer un punto de interrupción de línea de código   

Los puntos de interrupción de línea de código son el tipo más común de punto de interrupción.  Cuando obtenga la línea de código específica en la que desea hacer una pausa, use un punto de interrupción de línea de código:  

1.  Mire la última línea de código de `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  A la izquierda del código verás el número de línea de esta línea de código en particular, que es **33**.  Haga clic en **33**.  DevTools coloca un icono rojo a la izquierda de **33**.  Esto significa que hay un punto de interrupción de línea de código en esta línea.  DevTools ahora siempre pausa antes de que se ejecute esta línea de código.  
1.  Haga clic en **reanudar ejecución de script** ![ reanudar ejecución de script ][ImageResumeIcon] .  El script continúa ejecutándose hasta que llega a la línea 33.  En las líneas 30, 31 y 32, DevTools imprime los valores de `addend1` , `addend2` y `sum` a la derecha del punto y coma de cada línea.  
    
    > ##### Imagen 6  
    > DevTools pausa en el punto de interrupción de línea de código en la línea 32  
    > ![DevTools pausa en el punto de interrupción de línea de código en la línea 32][ImageJSLineOfCodeBreakpoint]  

## Paso 6: comprobar los valores de las variables   

Los valores de `addend1` , `addend2` y `sum` parecen sospechosos.  Se escriben entre comillas, lo que significa que son cadenas.  Esta es una buena hipótesis para explicar la causa del error.  Ahora es el momento de recopilar más información.  DevTools proporciona una gran cantidad de herramientas para examinar valores de variables.  

### Método 1: el panel ámbito   

Al pausar una línea de código, el panel **ámbito** muestra qué variables locales y globales están definidas actualmente, junto con el valor de cada variable.  También muestra las variables de cierre, cuando corresponda.  Haga doble clic en un valor de variable para modificarlo.  Cuando no se ha pausado en una línea de código, el panel de **ámbito** está vacío.  

> ##### Imagen 7  
> El panel **ámbito**  
> ![El panel ámbito][ImageJSScope]  

### Método 2: ver expresiones   

La pestaña **inspección de expresiones** le permite supervisar los valores de variables a lo largo del tiempo.  Como su nombre implica, las expresiones de inspección no se limitan solo a variables.  Puedes almacenar cualquier expresión de JavaScript válida en una expresión de inspección.  Pruébelo ahora:  

1.  Haga clic en la pestaña **inspección** .  
1.  Haga clic en Agregar expresión de adición de **expresión** ![ ][ImageAddIcon] .  
1.  Escribe `typeof sum`.  
1.  Presione `Enter` .  DevTools `typeof sum: "string"` .  El valor a la derecha de los dos puntos es el resultado de la expresión de inspección.  

> [!NOTE]
> En el panel de expresiones de inspección \ (parte inferior derecha \) en la [ilustración 8](#figure-8), `typeof sum` se muestra la expresión de inspección.  Si la ventana de DevTools es grande, el panel de expresiones de inspección se encuentra a la derecha sobre el panel de **puntos de interrupción de escucha de eventos** .  

> ##### Imagen 8  
> Panel de expresiones de inspección  
> ![Panel de expresiones de inspección][ImageJSWatchExpression]  

Como se sospecha, `sum` se evalúa como una cadena, cuando debería ser un número.  Ya ha confirmado que esta es la causa del error.  

### Método 3: la consola   

Además de ver `console.log()` los mensajes, también puede usar la consola para evaluar instrucciones de JavaScript arbitrarias.  En términos de depuración, puede usar la consola para probar posibles soluciones para errores.  Pruébelo ahora:  

1.  Si no tiene abierto el cajón de la consola, pulse `Escape` para abrirlo.  Se abre en la parte inferior de la ventana de DevTools.  
1.  En la consola, escriba `parseInt(addend1) + parseInt(addend2)` .  Esta instrucción funciona porque se ha pausado en una línea de código en la que `addend1` `addend2` se encuentran en el ámbito.  
1.  Presione `Enter` .  DevTools evalúa la instrucción e imprime `6` , que es el resultado que espera que la demostración produzca.  

> ##### Imagen 9  
> El cajón de consola, después de la evaluación `parseInt(addend1) + parseInt(addend2)`  
> ![El cajón de consola, después de evaluar parseInt (addend1) + parseInt (addend2)][ImageJSConsoleEvaluated]  

## Paso 7: aplicar una corrección   

Si encuentra una corrección para el error, pruebe su corrección editando el código y volviendo a ejecutar la demostración.  No es necesario dejar DevTools para aplicar la corrección.  Puedes editar código JavaScript directamente dentro de la interfaz de usuario de DevTools.  Pruébelo ahora:  

1.  Haga clic en **reanudar ejecución de script** ![ reanudar ejecución de script ][ImageResumeIcon] .  
1.  En el **Editor de código**, cambie la línea 32, `var sum = addend1 + addend2` con `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.  
1.  Haga clic en **desactivar puntos** de ![ interrupción ][ImageDeactivateIcon] .  Cambia de color azul para indicar que está activo.  Aunque está establecido, DevTools omite los puntos de interrupción que haya establecido.  
1.  Pruebe la demostración con diferentes valores.  La demostración ahora se calcula correctamente.  

> [!CAUTION]
> Este flujo de trabajo solo aplica una corrección para el código que se ejecuta en el explorador.  No se corrige el código de todos los usuarios que visitan la página.  Para ello, debe corregir el código que está en los servidores.  

## Pasos siguientes   

¡Enhorabuena!  Ahora sabes cómo sacar el máximo provecho de Microsoft Edge DevTools al depurar JavaScript.  Las herramientas y métodos que aprendió en este tutorial pueden ahorrar innumerables horas.  

En este tutorial, solo se mostraron dos formas de establecer puntos de interrupción.  DevTools ofrece muchas otras formas, entre las que se incluyen:  

*   Puntos de interrupción condicionales que solo se desencadenan cuando la condición que proporciona es verdadera.  
*   Puntos de interrupción en excepciones detectadas o no capturadas.  
*   XHRlos puntos de interrupción que se desencadenan cuando la dirección URL solicitada coincide con una subcadena que proporciona.  

<!-- See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

<!--There are a couple of code stepping controls that were not explained in this tutorial.  See [Step over line of code][JSReferenceStepping] to learn more.  -->  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: /microsoft-edge/devtools-guide-chromium/media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageResumeIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  

[ImageJSBugs]: /microsoft-edge/devtools-guide-chromium/media/javascript-js-demo-bad.msft.png "Ilustración 1: el resultado de 5 + 1 es 51, pero debe ser 6"  
[ImageJSConsole]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-empty.msft.png "Ilustración 2: panel de consola"  
[ImageJSSources]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections.msft.png "Ilustración 3: el panel orígenes"  
[ImageJSSourcesAnnotated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-sections-annotated.msft.png "Ilustración 4: las 3 partes de la interfaz de usuario del panel de fuentes"  
[ImageJSClickCheckbox]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png "Ilustración 5: la casilla click está habilitada"  
[ImageJSLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused.msft.png "Ilustración 6: la DevTools se detiene en el punto de interrupción de línea de código en la línea 32"  
[ImageJSScope]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-scope.msft.png "Ilustración 7: el panel ámbito"  
[ImageJSWatchExpression]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-watch.msft.png "Ilustración 8: panel de expresiones de inspección"  
[ImageJSConsoleEvaluated]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-breakpoint-paused-console.msft.png "El cajón de consola, después de evaluar parseInt (addend1) + parseInt (addend2)"  

<!-- links -->  

<!--[JSBreakpoints]: breakpoints.md "JavaScript Breakpoints"  -->  
<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->
[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "abrir demostración"  
<!--[JSReferenceStepping]: reference.md#stepping "Reference Stepping"  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
