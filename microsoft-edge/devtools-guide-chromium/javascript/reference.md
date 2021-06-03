---
description: Descubra nuevos flujos de trabajo de depuración en esta referencia completa de Microsoft Edge de depuración de DevTools.
title: Usar las características del depurador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6b15d317d4c720ab5ad76b7047532df101f69376
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564129"
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
# <a name="use-the-debugger-features"></a>Usar las características del depurador

En este artículo se describe cómo usar el depurador en Microsoft Edge DevTools, incluido cómo establecer un punto de interrupción de línea de código.  Para establecer otros tipos de puntos de interrupción, vea [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].  

Para conocer los conceptos básicos de la depuración, vaya a Introducción a la depuración de JavaScript en [Microsoft Edge DevTools][DevToolsJavascriptGetStarted], que es un tutorial que usa una página web existente basada en formularios.  El tutorial tiene capturas de pantalla, por lo que puedes desaconscarla.  Puedes probar fácilmente las características del depurador mediante la página web de demostración.

## <a name="view-and-edit-javascript-code"></a>Ver y editar código JavaScript

Al corregir un error, a menudo quieres probar algunos cambios en el código JavaScript.  No es necesario realizar los cambios en un editor externo o IDE, volver a cargar el archivo en el servidor y, a continuación, actualizar la página; en su lugar, para probar los cambios, puede editar el código JavaScript directamente en DevTools y ver el resultado inmediatamente.  

Para ver y editar un archivo JavaScript:  

1.  Vaya a la **herramienta Orígenes.**  
1.  En el **panel** Navegador, seleccione el archivo para abrirlo en el **panel Editor.**
1.  En el **panel Editor,** edite el archivo.  
1.  Seleccione `Ctrl` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar.  A continuación, DevTools carga el archivo JavaScript en el motor JavaScript de Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Panel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Panel **Editor**  
    :::image-end:::  
     
## <a name="reformat-a-minified-javascript-file-with-pretty-print"></a>Volver a formatear un archivo JavaScript minificado con pretty-print

Para que un archivo minificado sea legible, elija el botón **Formato** \( Formato \) situado en la parte inferior ![ del ](../media/format-icon.msft.png) **panel** Editor.

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="El botón Formato" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   El **botón** Formato  
:::image-end:::  

## <a name="set-a-breakpoint-to-pause-code"></a>Establecer un punto de interrupción para pausar el código

Para pausar el código en medio del tiempo de ejecución, establezca un punto de interrupción.  El tipo de punto de interrupción más básico y conocido es un punto de interrupción de línea de código.

Use un punto de interrupción de línea de código cuando sepa la región exacta del código que necesita investigar.  DevTools siempre se pausa en la línea de código especificada, antes de ejecutarlo.

Para establecer un punto de interrupción de línea de código:  

1.  Vaya a la **herramienta Orígenes.**  
1.  Abra el archivo que contiene la línea de código.  
1.  Seleccione el área a la izquierda del número de línea para la línea de código.  O bien, haga clic con el botón secundario en el número de línea y, a continuación, **elija Agregar punto de interrupción**.  A continuación, aparece un círculo rojo junto al número de línea, que indica un punto de interrupción.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Punto de interrupción de línea de código  
    :::image-end:::  

Los puntos de interrupción de línea de código pueden ser ineficientes para establecer, especialmente si no sabe exactamente dónde buscar o si su base de código es grande.  Para ahorrar tiempo al depurar, obtenga información sobre cómo y cuándo usar los otros tipos de puntos de interrupción.  Para obtener más información, vaya [a Pausar el código con puntos de interrupción.][DevToolsJavascriptBreakpoints]

## <a name="step-through-code"></a>Paso a través del código  

Después de pausar el código en un punto de interrupción, pase por el código, una línea a la vez, investigando el flujo de control y los valores de propiedad en el camino.  

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

Al depurar una función larga, puede haber una gran cantidad de código que no esté relacionado con el problema que está depurando.  

Puede optar por pasar por todas las líneas, pero eso es tedioso.  Puede elegir establecer un punto de interrupción de línea de código en la línea en la que está interesado y, a continuación, elegir el botón Reanudar ejecución de **script** \( Reanudar ejecución de script \), pero hay una forma más ![ ](../media/resume-script-run-icon.msft.png) rápida.  

Mantenga el mouse sobre la línea de código en la que le interesa, abra el menú contextual \(hacer clic con el botón secundario\) y **elija Continuar hasta aquí**.  DevTools ejecuta todo el código hasta ese punto y, a continuación, se pausa en esa línea.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Elija Continuar hasta aquí" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Elija **Continuar hasta aquí**  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a>Reiniciar la función superior de la pila de llamadas  

Para pausar en la primera línea de la función superior de la pila de **** llamadas, mientras está pausada en una línea de código, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(haga clic con el botón secundario\) y elija **Reiniciar**fotograma .  La función superior es la última función que se ha ejecutado.  

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

Está en pausa en `A` .  Después de elegir **Reiniciar fotograma,** debe pausarse en , sin establecer nunca un punto de interrupción ni elegir Reanudar ejecución `B` de **script**.  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Elegir fotograma reiniciar" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Elegir **fotograma reiniciar**  
:::image-end:::  

### <a name="resume-script-runtime"></a>Resume script runtime  

Para continuar con el tiempo de ejecución después de una pausa del script, elija el botón Reanudar ejecución de **script** \( ![ Reanudar ejecución de script ](../media/resume-script-run-icon.msft.png) \).  DevTools ejecuta el script hasta el siguiente punto de interrupción, si lo hay.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Elegir Reanudar ejecución de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Elegir **Reanudar ejecución de script**  
:::image-end:::  

#### <a name="force-script-runtime"></a>Forzar tiempo de ejecución de script  

Para omitir todos los puntos de interrupción y forzar la ejecución del script, elija y mantenga presionado el botón Reanudar ejecución de **scripts** \( Reanudar ejecución de script \) y, a continuación, elija el botón Forzar ejecución de script \( Forzar ejecución de ![ ](../media/resume-script-run-icon.msft.png) script **** ![ ](../media/force-script-run-icon.msft.png) \).  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Elegir Forzar ejecución de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Elegir **Forzar ejecución de script**  
:::image-end:::  

### <a name="change-thread-context"></a>Cambiar contexto de subproceso  

Al trabajar con trabajadores web o trabajadores **** de servicio, elija en un contexto que aparece en el panel Subprocesos para cambiar a ese contexto.  El icono de flecha azul representa qué contexto está seleccionado actualmente.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Panel Subprocesos" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Panel **Subprocesos**  
:::image-end:::  

Por ejemplo, suponga que está pausado en un punto de interrupción tanto en el script principal como en el script de trabajo de servicio.  Desea ver las propiedades locales y globales del contexto de trabajo de servicio, pero la herramienta **Orígenes** muestra el contexto de script principal.  Para cambiar al contexto de trabajo de servicio, en el **panel Subprocesos,** elija la entrada de trabajador de servicio.  

## <a name="view-and-edit-properties-and-variables"></a>Ver y editar propiedades y variables

Mientras está pausado en una **** línea de código, use el panel Ámbito para ver y editar los valores de propiedades y variables en los ámbitos local, de cierre y global.  

*   Haga doble clic en un valor de propiedad para cambiarlo.  
*   Las propiedades no enumerables están grises.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   Panel **Ámbito**  
:::image-end:::  

## <a name="watch-the-values-of-javascript-expressions"></a>Ver los valores de las expresiones de JavaScript  

Use el **panel** Ver para ver los valores de las expresiones personalizadas.  Puede ver cualquier expresión de JavaScript válida.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="El panel Ver" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   El **panel Ver**  
:::image-end:::  

*   Para crear una nueva expresión de reloj, seleccione el botón Agregar expresión **de** reloj \( ![ Agregar expresión de reloj ](../media/add-expression-icon.msft.png) \).  
*   Para actualizar los valores de todas las expresiones existentes, seleccione el botón **Actualizar** ![ \( Actualizar ](../media/refresh-icon.msft.png) \).  Los valores se actualizan automáticamente al pasar por el código.  
*   Para eliminar una expresión de reloj, haga clic con el botón secundario en la expresión y, a continuación, seleccione **Eliminar** expresión de reloj \( ![ Eliminar expresión de reloj ](../media/delete-expression-icon.msft.png) \).  

## <a name="view-the-call-stack"></a>Ver la pila de llamadas  

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

Para copiar la pila de llamadas actual **** en el Portapapeles, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(clic con el botón secundario\) y elija Copiar seguimiento **de pila**.  

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

Por ejemplo, en el siguiente fragmento de código, line `A` usa , que es una biblioteca de `lib` terceros.  Si está seguro de que el problema que está depurando no está relacionado con esa biblioteca de terceros, tiene sentido marcar el script como **código de biblioteca**.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a>Marcar un script como código de biblioteca desde el panel Editor  

Para marcar un script como **código de biblioteca** desde el panel **Editor:**  

1.  Abra el archivo.  
1.  Mantenga el mouse en cualquier lugar y abra el menú contextual \(hacer clic con el botón secundario\).  
1.  Elija **Agregar script para omitir la lista** (anteriormente se muestra como Marcar como código de **biblioteca).**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde el panel **Editor**  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a>Marcar un script como código de biblioteca desde el panel Pila de llamadas  

Para marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas:  

1.  Mantenga el mouse sobre una función del script y abra el menú contextual \(hacer clic con el botón secundario\).  
1.  Elija **Agregar script para omitir la lista** (anteriormente se muestra como Marcar como código de **biblioteca).**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a>Marcar un script como código de biblioteca desde Configuración  

Para marcar un único script o patrón de scripts desde **Configuración**:  

1.  Abra [Configuración][DevToolsCustomize].  
1.  Vaya a la **configuración de código de biblioteca.**  
1.  Elija **Agregar patrón**.  
1.  Escriba el nombre del script o un patrón regex de nombres de script para marcar como **código de biblioteca.**  
1.  Elija **Agregar**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde Configuración" lightbox="../media/javascript-framework-library-code.msft.png":::
       Marcar un script como **código de biblioteca** desde **Configuración**  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a>Ejecutar fragmentos de código de depuración desde cualquier página  

Si se encuentra ejecutando el mismo código de depuración en la consola una y otra vez, considere Fragmentos de código.  Los fragmentos de código son scripts en tiempo de ejecución que se pueden crear, almacenar y ejecutar en DevTools.  

Consulte [Ejecutar fragmentos de código de JavaScript en cualquier página web][DevToolsJavascriptSnippets].  

## <a name="see-also"></a>Consulta también  

*   [Introducción Con depuración de JavaScript en Microsoft Edge DevTools:][DevToolsJavascriptGetStarted] un tutorial sencillo y breve con código existente, con capturas de pantalla.
*   [Introducción a la herramienta][DevToolsSourcesIndex] Orígenes: la **herramienta Orígenes** incluye el depurador y el editor de JavaScript.
*   [Deshabilitar JavaScript con Microsoft Edge DevTools][DevToolsJavascriptDisable].

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ejecute fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsSourcesIndex]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
