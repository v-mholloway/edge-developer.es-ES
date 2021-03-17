---
description: Descubra nuevos flujos de trabajo de depuración en esta referencia completa de las características de depuración de Microsoft Edge DevTools.
title: Referencia de depuración de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2944e054a08a901d2e1752fa7c4e48ae110f5787
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439461"
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

# <a name="javascript-debugging-reference"></a>Referencia de depuración de JavaScript  

Descubra nuevos flujos de trabajo de depuración con la siguiente referencia completa de las características de depuración de Microsoft Edge DevTools.  

Para obtener información sobre los conceptos básicos de la depuración, vaya a Introducción a [La depuración de JavaScript en Microsoft Edge DevTools][DevToolsJavascriptGetStarted].  

## <a name="pause-code-with-breakpoints"></a>Pausar código con puntos de interrupción  

Establece un punto de interrupción para que puedas pausar el código en medio del tiempo de ejecución.  

Para obtener información sobre cómo establecer puntos de interrupción, vaya [a Pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].  

## <a name="step-through-code"></a>Paso a través del código  

Una vez que el código está en pausa, pase por él, una línea a la vez, investigando el flujo de control y los valores de propiedad en el camino.  

### <a name="step-over-line-of-code"></a>Paso a paso por la línea de código  

Cuando se pausa en una línea de código que contiene una función que no es relevante para el problema que está depurando, elija el botón **Paso** a paso \( Paso sobre \) para ejecutar la función sin entrar en ![ ](../media/step-over-icon.msft.png) ella.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Elija Paso a paso" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Elija **Paso a paso**  
:::image-end:::  

Por ejemplo, supongamos que está depurando el siguiente fragmento de código.  

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

Está en pausa en `A` .  Después de elegir **Paso a paso**, DevTools ejecuta todo el código de la función que va a pasar, que es y `B` `C` .  A continuación, DevTools hace una pausa en `D` .  

### <a name="step-into-line-of-code"></a>Paso a paso en la línea de código  

Cuando se pausa en una línea de código que contiene una llamada de función relacionada con el problema que está depurando, elija el botón Paso a **paso** en \( Paso a \) para investigar esa función más ![ ](../media/step-into-icon.msft.png) adelante.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Elija Paso a paso" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Elija **Paso a paso**  
:::image-end:::  

Por ejemplo, supongamos que está depurando el siguiente fragmento de código.  

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

Está en pausa en `A` .  Después de elegir **Paso en**, DevTools ejecuta esta línea de código y, a continuación, se pausa en `B` .  

### <a name="step-out-of-line-of-code"></a>Salir de la línea de código  

Cuando se pausa dentro de una función que no está relacionada con el problema que está depurando, elija el botón Salir **\(** Salir \) para ejecutar el resto del código de ![ la ](../media/step-out-icon.msft.png) función.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Elija Salir" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Elija **Salir**  
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

Está en pausa en `A` .  Después de elegir **Step out**, DevTools ejecuta el resto del código en , que está en este ejemplo y, a `getName()` continuación, se pausa en `B` `C` .  

### <a name="run-all-code-up-to-a-specific-line"></a>Ejecutar todo el código hasta una línea específica  

Al depurar una función larga, puede haber una gran cantidad de código que no está relacionado con el problema que está depurando.  

Puede optar por pasar por todas las líneas, pero eso es tedioso.  Puede elegir establecer un punto de interrupción de línea de código en la línea en la que está interesado y, a continuación, elegir el botón Reanudar ejecución de **script** \( Reanudar ejecución de script \), pero hay una forma más ![ ](../media/resume-script-run-icon.msft.png) rápida.  

Mantenga el mouse sobre la línea de código en la que le interesa, abra el menú contextual \(hacer clic con el botón secundario\) y **elija Continuar hasta aquí**.  DevTools ejecuta todo el código hasta ese punto y, a continuación, se pausa en esa línea.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Elija Continuar hasta aquí" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Elija **Continuar hasta aquí**  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a>Reiniciar la función superior de la pila de llamadas  

Para pausar en la primera línea de la función superior de la pila de **** llamadas, mientras se pausa en una línea de código, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(haga clic con el botón secundario\) y elija **Reiniciar**marco .  La función superior es la última función que se ha ejecutado.  

El siguiente fragmento de código es un ejemplo de paso a paso.  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Está en pausa en `A` .  Después de elegir **Reiniciar fotograma**, debe pausarse en , sin establecer nunca un punto de interrupción ni elegir Reanudar ejecución `B` de **script**.  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Elegir fotograma de reinicio" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Elegir **fotograma de reinicio**  
:::image-end:::  

### <a name="resume-script-runtime"></a>Resume script runtime  

Para continuar con el tiempo de ejecución después de una pausa del script, elija el botón Reanudar ejecución de **script** \( ![ Reanudar ejecución de script ](../media/resume-script-run-icon.msft.png) \).  DevTools ejecuta el script hasta el siguiente punto de interrupción, si lo hay.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Elegir Reanudar ejecución de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Elegir **Reanudar ejecución de script**  
:::image-end:::  

#### <a name="force-script-runtime"></a>Forzar tiempo de ejecución de script  

Para omitir todos los puntos de interrupción y forzar la reanudación de la ejecución del script, elija y mantenga presionado el botón Reanudar ejecución de script **\(** Reanudar ejecución de script \) y, a continuación, elija el botón Forzar ejecución de script \( Forzar la ejecución del ![ ](../media/resume-script-run-icon.msft.png) script **** ![ ](../media/force-script-run-icon.msft.png) \).  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Elegir Forzar ejecución de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Elegir **Forzar ejecución de script**  
:::image-end:::  

### <a name="change-thread-context"></a>Cambiar contexto de subproceso  

Al trabajar con trabajadores web o trabajadores **** de servicio, elija en un contexto que aparece en el panel Subprocesos para cambiar a ese contexto.  El icono de flecha azul representa qué contexto está seleccionado actualmente.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Panel Subprocesos" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Panel **Subprocesos**  
:::image-end:::  

Por ejemplo, suponga que está pausado en un punto de interrupción tanto en el script principal como en el script de trabajo de servicio.  Desea ver las propiedades locales y globales del contexto de trabajo de servicio, pero el **panel** Orígenes muestra el contexto de script principal.  Al elegir en la entrada de trabajo de servicio en **el** panel Subprocesos, debería poder cambiar a ese contexto.  

## <a name="view-and-edit-local-closure-and-global-properties"></a>Ver y editar propiedades locales, de cierre y globales  

Mientras está pausado en una **** línea de código, use el panel Ámbito para ver y editar los valores de propiedades y variables en los ámbitos local, de cierre y global.  

*   Haga doble clic en un valor de propiedad para cambiarlo.  
*   Las propiedades no enumerables están grises.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   Panel **Ámbito**  
:::image-end:::  

## <a name="view-the-current-call-stack"></a>Ver la pila de llamadas actual  

Mientras está pausado en una línea de código, use el panel **Pila** de llamadas para ver la pila de llamadas que le ha hecho llegar hasta este punto.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Elija una entrada para saltar a la línea de código donde se llamó a esa función.  El icono de flecha azul representa la función DevTools que está resaltando actualmente.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Panel Pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Panel **Pila de** llamadas  
:::image-end:::  

> [!NOTE]
> Cuando no se pausa en una línea de código, el panel **Pila** de llamadas está vacío.  

### <a name="copy-stack-trace"></a>Copiar seguimiento de pila  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

para copiar la pila de llamadas actual **** en el Portapapeles, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(clic con el botón secundario\) y elija Copiar seguimiento **de pila**.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Elija Copiar seguimiento de pila" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Elija **Copiar seguimiento de pila**  
:::image-end:::  

El siguiente fragmento de código es un ejemplo de la salida.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a>Omitir un script o patrón de scripts  

Marca un script como código de biblioteca cuando quieras omitir ese script durante la depuración.  Cuando se marca como código de biblioteca, un script se oculta en el panel Pila de llamadas y nunca se pasa a las funciones del script cuando se pasa por el código. ****  

El siguiente fragmento de código es un ejemplo de paso a paso.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` es una biblioteca de terceros en la que confía.  Si está seguro de que el problema que está depurando no está relacionado con la biblioteca de terceros, tiene sentido marcar el script como **código de biblioteca**.  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a>Marcar un script como código de biblioteca desde el panel Editor  

Complete las siguientes acciones para marcar un script como **código de biblioteca** desde el panel **Editor.**  

1.  Abra el archivo.  
1.  Mantenga el mouse en cualquier lugar y abra el menú contextual \(hacer clic con el botón secundario\).  
1.  Elija **Marcar como código de biblioteca**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde el panel **Editor**  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a>Marcar un script como código de biblioteca desde el panel Pila de llamadas  

Complete las siguientes acciones para marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas.  

1.  Mantenga el mouse sobre una función del script y abra el menú contextual \(hacer clic con el botón secundario\).  
1.  Elija **Marcar como código de biblioteca**.  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a>Marcar un script como código de biblioteca desde Configuración  

Complete las siguientes acciones para marcar un único script o patrón de scripts desde **Configuración**.  

1.  Abra [Configuración][DevToolsCustomize].  
1.  Vaya a la **configuración de código de biblioteca.**  
1.  Elija **Agregar patrón**.  
1.  Escriba el nombre del script o un patrón regex de nombres de script para marcar como **código de biblioteca.**  
1.  Elija **Agregar**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde Configuración" lightbox="../media/javascript-framework-library-code.msft.png":::
       Marcar un script como código **de biblioteca desde** **Configuración**  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a>Ejecutar fragmentos de código de depuración desde cualquier página  

Si se encuentra ejecutando el mismo código de depuración en la consola una y otra vez, considere Fragmentos de código.  Los fragmentos de código son scripts en tiempo de ejecución que se pueden crear, almacenar y ejecutar en DevTools.  

Para obtener más información, vaya [a Ejecutar fragmentos de código desde cualquier página][DevToolsJavascriptSnippets].  

## <a name="watch-the-values-of-custom-javascript-expressions"></a>Ver los valores de las expresiones de JavaScript personalizadas  

Use el **panel** Ver para ver los valores de las expresiones personalizadas.  Puede ver cualquier expresión de JavaScript válida.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="El panel Ver" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   El **panel Ver**  
:::image-end:::  

*   Elija el botón Agregar **expresión** \( ![ Agregar expresión ](../media/add-expression-icon.msft.png) \) para crear una nueva expresión de reloj.  
*   Elija el **botón Actualizar** \( ![ Actualizar ](../media/refresh-icon.msft.png) \) para actualizar los valores de todas las expresiones existentes.  Los valores se actualizan automáticamente al pasar por el código.  
*   Mantenga el mouse sobre una expresión y elija el **botón Eliminar expresión** \( Eliminar expresión ![ ](../media/delete-expression-icon.msft.png) \) para eliminarla.  

## <a name="make-a-minified-file-readable"></a>Hacer que un archivo minified sea legible  

Elija el **botón Formato** \( ![ Formato ](../media/format-icon.msft.png) \) para que un archivo minificado sea legible.  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="El botón Formato" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   El **botón** Formato  
:::image-end:::  

## <a name="edit-a-script"></a>Editar un script  

Al corregir un error, a menudo quieres probar algunos cambios en el código JavaScript.  No es necesario realizar los cambios en un editor externo o IDE y, a continuación, actualizar la página.  Puede editar el script en DevTools.  

Complete las siguientes acciones para editar un script.  

1.  Abra el archivo en el **panel Editor** del panel **Orígenes.**  
1.  Realice los cambios en el **panel Editor.**  
1.  Seleccione `Ctrl` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar.  DevTools parchea todo el archivo JS en el motor JavaScript de Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Panel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Panel **Editor**  
    :::image-end:::  
     
## <a name="disable-javascript"></a>Deshabilitar JavaScript  

Vaya a [Deshabilitar JavaScript con Microsoft Edge DevTools][DevToolsJavascriptDisable].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
