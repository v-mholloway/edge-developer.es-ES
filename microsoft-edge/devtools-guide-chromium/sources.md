---
title: Información general del panel orígenes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601911"
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
   limitations under the License. -->






# Información general del panel orígenes 



Use el panel de **orígenes** de Microsoft Edge DevTools para:

*   [Ver archivos](#view-files).  
*   [Edite CSS y JavaScript](#edit-css-and-javascript).  
*   [Cree y guarde **fragmentos** de código de JavaScript](#create-save-and-run-snippets), que puede ejecutar en cualquier página.  Los **fragmentos de código** son similares a bookmarklets.  
*   [Depure JavaScript](#debug-javascript).  
*   [Configure un área de trabajo](#set-up-a-workspace)para que los cambios que realice en DevTools se guarden en el código de su sistema de archivos.  

## Ver archivos 

Use el panel de **páginas** para ver todos los recursos que la página ha cargado.

> ##### Figura 1  
> El panel de **páginas**  
> ![Ilustración 1: el panel de páginas][ImageSourcesPagePane]  

Organización del panel de **páginas** :  
*   El nivel superior, como en la `top` [**figura 1**](#figure-1), representa un [marco HTML][W3CHtml4Frames].  Buscar `top` en cada página que visite. `top` representa el marco del documento principal.  
*   El segundo nivel, como en la `docs.microsoft.com` [**figura 1**](#figure-1), representa un [origen][HtmlstandardOrigin].  
*   El tercer nivel, el cuarto nivel, etc., representan los directorios y recursos que se cargaron desde ese origen.  Por ejemplo, en la [**figura 1**](#figure-1) , la ruta de acceso completa al recurso `devtools-guide-chromium` es `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

Haga clic en un archivo en el panel de **páginas** para ver el contenido en el panel del **Editor** .  Puede ver cualquier tipo de archivo. Para las imágenes, verá una vista previa de la imagen.  

> ##### Figura 2  
> Ver el contenido de `a4d10f71.index-docs.js` en el panel **Editor**  
> ![Figura 2. Ver el contenido de a4d10f71. index-docs. js en el panel Editor][ImageSourcesEditorPane]  

## Editar CSS y JavaScript 

Use el panel **Editor** para editar CSS y JavaScript.  DevTools actualiza la página para ejecutar el nuevo código. Por ejemplo, Si edita un archivo CSS agregando la regla de estilo a continuación:

```css
.metadata.page-metadata {
    color: red;
}
```

Verá que el cambio se aplicará inmediatamente.

> ##### Imagen 3  
> Editar CSS en el panel **Editor** para cambiar el color del texto del subtítulo a rojo  
> ![Figura 3. Editar CSS en el panel Editor para cambiar el color del texto del subtítulo a rojo][ImageEditCSS]  

Los cambios de CSS se aplican inmediatamente, no es necesario guardar. Para que los cambios de JavaScript surtan efecto, pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \). DevTools no vuelve a ejecutar un script, por lo que los únicos cambios de JavaScript que se aplican son los que realiza dentro de las funciones.  Por ejemplo, en la [**figura 4**](#figure-4) , observe cómo `console.log('A')` no se ejecuta, pero `console.log('B')` sí. Si DevTools vuelto a ejecutar la secuencia de comandos completa después de realizar el cambio, el texto `A` se habría registrado en la **consola**.  

> ##### Imagen 4  
> Edición de JavaScript en el panel **Editor**  
> ![Figura 4. Edición de JavaScript en el panel Editor][ImageEditJS]  

DevTools borra los cambios de CSS y JavaScript al volver a cargar la página. Vea [configurar un área de trabajo](#set-up-a-workspace) para obtener información sobre cómo guardar los cambios en el sistema de archivos.  

## Crear, guardar y ejecutar fragmentos de código 

Los fragmentos de código son scripts que se pueden ejecutar en cualquier página. Suponga que escribe repetidamente el siguiente código en la **consola**, para insertar la biblioteca de jQuery en una página, de modo que pueda ejecutar comandos de jQuery desde la **consola**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

En su lugar, puede guardar este código en un **fragmento** de código y ejecutarlo con un par de clics de botón, cada vez que lo necesite.  DevTools guarda el **fragmento de código** en el sistema de archivos.  

> ##### Imagen 5  
> Un **fragmento de código** que inserta la biblioteca jQuery en una página  
> ![Figura 5. Un fragmento de código que inserta la biblioteca jQuery en una página][ImageSnippet]  

Para ejecutar un **fragmento de código**:

*   Abra el archivo a través del panel **fragmentos de código** y haga clic en **Ejecutar** ![ el botón ejecutar ][ImageRunIcon] .  
*   Abra el **[menú de comandos][DevtoolsGuideChromiumCommandMenuIndex]**, elimine el `>` carácter, escriba `!` , escriba el nombre del **fragmento**y, a continuación, pulse `Enter` .  

Vea [Ejecutar fragmentos de código desde cualquier página][DevtoolsGuideChromiumJavascriptSnippets] para obtener más información.


## Depurar JavaScript 

En lugar de usar `console.log()` para inferir Dónde está el error de JavaScript, considere la posibilidad de usar las herramientas de depuración de Microsoft Edge DevTools en su lugar. La idea general es establecer un punto de interrupción, que es un lugar de detención intencionado en el código, y, a continuación, pasar por el tiempo de ejecución del código, de línea en línea. Mientras recorres el código, puedes ver y cambiar los valores de todas las propiedades y variables definidas actualmente, ejecutar JavaScript en la **consola**y mucho más.

Consulte Introducción a la [depuración de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para conocer los conceptos básicos de la depuración en DevTools.

> ##### Imagen 6  
> Depurar JavaScript  
> ![Figura 6. Depurar JavaScript][ImageDebugging]  

## Configurar un área de trabajo 

De forma predeterminada, al editar un archivo en el panel **orígenes** , esos cambios se pierden al volver a cargar la página.  Las **áreas de trabajo** le permiten guardar los cambios que realice en DevTools en el sistema de archivos.  Esencialmente, esto te permite usar DevTools como tu editor de código.

Consulte [editar archivos con áreas de trabajo][DevtoolsGuideChromiumWorkspacesIndex] para comenzar.

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Ilustración 1: el panel de páginas"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Ilustración 2: visualización del contenido de a4d10f71. index-docs. js en el panel Editor"  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Ilustración 3: edición de CSS en el panel Editor para cambiar el color del texto del subtítulo a rojo"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Ilustración 4: edición de JavaScript en el panel Editor"  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Ilustración 5: un miniprograma que inserta la biblioteca jQuery en una página"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Ilustración 6: depurar JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Introducción a la depuración de JavaScript en Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Editar archivos con áreas de trabajo"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origen-estándar HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Marcos | RELATIVA"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/sources) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
