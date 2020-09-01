---
title: Referencia de depuración de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 26f7272534e0834e0fb302a40b7f0ebfc817c88e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982228"
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







# Referencia de depuración de JavaScript   



Descubra nuevos flujos de trabajo de depuración con esta referencia completa de las características de depuración de Microsoft Edge DevTools.  

Consulta Introducción a la [depuración de JavaScript en Microsoft Edge DevTools][DevToolsJavascriptGetStarted] para conocer los conceptos básicos de la depuración.  

## Pausar código con puntos de interrupción   

Establezca un punto de interrupción para que pueda pausar el código en el medio del Runtime.  

Vea [pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints] para obtener información sobre cómo establecer puntos de interrupción.  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools"  

## Recorrer el código   

Una vez que el código esté pausado, recorralo, de una línea a la vez, investigando el flujo de control y los valores de propiedad durante el proceso.  

### Paso a paso por la línea de código   

Cuando esté pausado en una línea de código que contenga una función que no sea relevante para el problema que está depurando, haga clic en el icono **\ (** ![ paso a paso por procedimientos ][ImageStepOverIcon] ) para ejecutar la función sin entrar en él.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Seleccione recorrer" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Seleccione **recorrer**  
:::image-end:::  

Por ejemplo, supongamos que está depurando el código siguiente:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

Estás pausado el `A` .  Si pulsas **paso a paso**, DevTools ejecuta todo el código de la función que estás recorriendo, que `B` es `C` y.  DevTools, luego, se detiene en `D` .  

### Ir a la línea de código   

Cuando esté pausado en una línea de código que contenga una llamada de función que esté relacionada con el problema que está depurando, haga clic en el icono **de \ (** ![ paso a paso ][ImageStepIntoIcon] \) para investigar la función más.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Seleccione ir a" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Seleccione **ir a**  
:::image-end:::  

Por ejemplo, supongamos que está depurando el código siguiente:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

Estás pausado el `A` .  Al presionar **paso a paso por instrucciones**, DevTools ejecuta esta línea de código y luego detiene el `B` .  

### Paso fuera de la línea de código   

Cuando esté pausado dentro de una función que no esté relacionada con el problema que está depurando, haga clic en el icono **\ (** ![ paso salir ][ImageStepOutIcon] \) para ejecutar el resto del código de la función.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Seleccione salir" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Seleccione **salir**  
:::image-end:::  

Por ejemplo, supongamos que está depurando el siguiente fragmento de código.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

Estás pausado el `A` .  Si pulsas **paso a paso**, DevTools ejecuta el resto del código de `getName()` , que se encuentra `B` en este ejemplo, y luego realiza una pausa en `C` .  

### Ejecutar todo el código hasta una línea específica   

Cuando se depura una función Long, puede haber una gran cantidad de código que no está relacionado con el problema que se está depurando.  

Puede elegir recorrer todas las líneas, pero eso es tedioso.  Puede optar por establecer un punto de interrupción de línea de código en la línea en la que está interesado y, a continuación, hacer clic en el icono de **ejecución de script de reanudación** \ ( ![ resume script Execution ][ImageResumeScriptExecutionIcon] \), pero hay una forma más rápida.  

Haga clic con el botón derecho en la línea de código en la que está interesado y seleccione **continuar aquí**.  DevTools ejecuta todo el código hasta ese punto y, después, se detiene en esa línea.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Seleccione continuar aquí" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Seleccione **continuar aquí**  
:::image-end:::  

### Reiniciar la función superior de la pila de llamadas   

Mientras esté pausado en una línea de código, haga clic con el botón secundario en cualquier lugar del panel **pila de llamadas** y seleccione **reiniciar marco** para hacer una pausa en la primera línea de la función superior de la pila de llamadas.  La función Top es la última función que se ejecutó.  

Por ejemplo, supongamos que está recorriendo el siguiente fragmento de código.  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Estás pausado el `A` .  Después de hacer clic en **Restarted Frame**, debe estar pausado `B` , sin tener que establecer un punto de interrupción ni Pulsar **resume script Execution**.  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Seleccionar el marco de reinicio" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Seleccionar el **marco de reinicio**  
:::image-end:::  

### Reanudar script Runtime   

Para continuar el tiempo de ejecución después de una pausa de la secuencia de comandos, haga clic en el icono de **ejecución de script de reanudación** \ ( ![ resume script Execution ][ImageResumeScriptExecutionIcon] \).  DevTools ejecuta la secuencia de comandos hasta el siguiente punto de interrupción, si existe.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Seleccione reanudar script Execution" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Seleccione **reanudar script Execution**  
:::image-end:::  

#### Tiempo de ejecución de script forzado   

Para ignorar todos los puntos de interrupción y forzar la reanudación de su script, haga clic y mantenga presionado el icono de **ejecución de script de reanudación** \ ( ![ reanudar ejecución de script ][ImageResumeScriptExecutionIcon] \) y, después, seleccione **forzar ejecución** de script \ ( ![ forzar ejecución de script ][ImageForceScriptExecutionIcon] \).  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Seleccione forzar ejecución de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Seleccione **forzar ejecución de script**  
:::image-end:::  

### Cambiar el contexto del hilo   

Cuando trabaje con trabajadores web o trabajos de servicio, haga clic en el contexto que aparece en el panel de **subprocesos** para cambiar a ese contexto.  El icono de flecha azul representa el contexto que está seleccionado actualmente.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="El panel de subprocesos" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   El panel de **subprocesos**  
:::image-end:::  

Por ejemplo, supongamos que está pausado en un punto de interrupción tanto en el script principal como en el script de trabajo de servicio.  Desea ver las propiedades locales y globales del contexto de trabajo de servicio, pero el panel **orígenes** muestra el contexto de script principal.  Al hacer clic en la entrada de trabajador de servicio en el panel de **subprocesos** , debería poder cambiar a ese contexto.  

## Ver y editar propiedades locales, de cierre y globales   

Mientras esté pausado en una línea de código, use el panel **ámbito** para ver y editar los valores de las propiedades y variables de los ámbitos local, de cierre y global.  

*   Haga doble clic en un valor de propiedad para cambiarlo.  
*   Las propiedades no enumerables están atenuadas.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="El panel ámbito" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   El panel **ámbito**  
:::image-end:::  

## Ver la pila de llamadas actual   

Mientras esté pausado en una línea de código, use el panel **pila de llamadas** para ver la pila de llamadas que le han llegado a este punto.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Haga clic en una entrada para ir a la línea de código donde se llamó a esa función.  El icono de flecha azul representa qué función DevTools está resaltando actualmente.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Panel pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Panel **pila de llamadas**  
:::image-end:::  

> [!NOTE]
> Cuando no está pausado en una línea de código, el panel **pila de llamadas** está vacío.  

### Copiar seguimiento de pila   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Haga clic con el botón secundario en cualquier lugar del panel de la **pila de llamadas** y seleccione **copiar seguimiento de pila** para copiar la pila de llamadas actual en el portapapeles.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Seleccione copiar seguimiento de pila" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Seleccione **copiar seguimiento de pila**  
:::image-end:::  

A continuación se muestra un ejemplo del resultado:  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Ignorar un script o una trama de scripts  

Marque un script como código de biblioteca cuando desee omitir ese script durante la depuración.  Cuando se marca como código de biblioteca, un script se oculta en el panel **pila de llamadas** y nunca se le detallan las funciones de la secuencia de comandos cuando pasa por el código.  

Por ejemplo, supongamos que está recorriendo el siguiente fragmento de código.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` es una biblioteca de terceros en la que confía.  Si está seguro de que el problema que está depurando no está relacionado con la biblioteca de terceros, tiene sentido marcar el script como **código de biblioteca**.  

### Marcar un script como código de biblioteca desde el panel Editor  

Para marcar un script como **código de biblioteca** desde el panel **Editor** :  

1.  Abra el archivo.  
1.  Haga clic con el botón derecho en cualquier parte.  
1.  Seleccione **marcar como código de biblioteca**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde el panel **Editor**  
    :::image-end:::  
    
### Marcar un script como código de biblioteca desde el panel de pila de llamadas  

Para marcar un script como **código de biblioteca** desde el panel **pila de llamadas** :  

1.  Haga clic con el botón derecho en una función de la secuencia de comandos.  
1.  Seleccione **marcar como código de biblioteca**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde el panel **pila de llamadas**  
    :::image-end:::  
    
### Marcar un script como código de biblioteca desde la configuración  

Para marcar un único script o patrón de scripts de la configuración:  

1.  Abra [configuración][DevToolsCustomize].  
1.  Vaya a la pestaña **código de biblioteca** .  
1.  Haga clic en **Agregar patrón**.  
1.  Escriba el nombre del script o un patrón de Regex de nombres de script para marcarlo como **código de biblioteca**.  
1.  Haz clic en **Agregar**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde la configuración" lightbox="../media/javascript-framework-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde la **configuración**  
    :::image-end:::  
    
## Ejecutar fragmentos de código de depuración desde cualquier página   

Si se encuentra ejecutando el mismo código de depuración en la consola una y otra vez, considere la posibilidad de recortes.  Los fragmentos de código son scripts de tiempo de ejecución que usted crea, almacena y ejecuta dentro de DevTools.  

Vea [Ejecutar fragmentos de código desde cualquier página][DevToolsJavascriptSnippets] para obtener más información.  

## Ver los valores de las expresiones de JavaScript personalizadas   

Use el panel **inspección** para ver los valores de expresiones personalizadas.  Puede ver cualquier expresión válida de JavaScript.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Panel de inspección" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   Panel de **inspección**  
:::image-end:::  

*   Haga clic en el icono **Agregar expresión** \ ( ![ Agregar expresión ][ImageAddExpressionIcon] \) para crear una nueva expresión de inspección.  
*   Haga clic en el icono **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \) para actualizar los valores de todas las expresiones existentes.  Los valores se actualizan automáticamente al recorrer el código.  
*   Mueva el puntero sobre una expresión y haga clic en el icono **eliminar expresión** \ ( ![ eliminar expresión ][ImageDeleteExpressionIcon] \) para eliminarla.  
    
## Hacer que un archivo minified sea legible   

Haga clic en el icono **formato** \ ( ![ formato ][ImageFormatIcon] \) para hacer que un archivo minified sea legible para el usuario.  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="El botón formato" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   El botón **formato**  
:::image-end:::  

## Editar un script   

Al corregir un error, a menudo desearás probar algunos cambios en el código de JavaScript.  No es necesario realizar los cambios en un editor externo o IDE y, a continuación, volver a cargar la página.  Puede editar su script en DevTools.  

Para editar un script:  

1.  Abra el archivo en el panel **Editor** del panel **fuentes** .  
1.  Realice los cambios en el panel **Editor** .  
1.  Pulse `Ctrl` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar.  DevTools revisa todo el archivo JS en el motor de JavaScript de Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="El panel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       El panel **Editor**  
    :::image-end:::  
     
## Deshabilitar JavaScript   

Consulte [deshabilitar JavaScript con Microsoft Edge DevTools][DevToolsJavascriptDisable].  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptDisable]: ./disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
