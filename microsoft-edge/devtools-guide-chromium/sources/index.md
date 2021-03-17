---
description: Mostrar y editar archivos, crear fragmentos de código, depurar JavaScript y configurar áreas de trabajo en el panel Orígenes de Microsoft Edge DevTools.
title: Información general del panel orígenes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7ce7ae32b4bf91419512ec9e387cdf75549552a5
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439608"
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

# <a name="sources-panel-overview"></a>Información general del panel orígenes  

Use el panel Orígenes de DevTools **de** Microsoft Edge para realizar las siguientes acciones.  

*   [Mostrar archivos](#display-files).  
*   [Editar CSS y JavaScript](#edit-css-and-javascript).  
*   [Cree y guarde **fragmentos** de código de JavaScript,](#create-save-and-run-snippets)que puede ejecutar en cualquier página web.  **Los fragmentos de** código son similares a los bookmarklets.  
*   [Depurar JavaScript](#debug-javascript).  
*   [Configure un área de](#set-up-a-workspace)trabajo para que los cambios que realice en DevTools se guarden en el código del sistema de archivos.  
    
## <a name="display-files"></a>Mostrar archivos  

Use **el** panel Página; para mostrar todos los recursos que la página ha cargado.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="Panel Página" lightbox="../media/sources-page-pane.msft.png":::
   Panel **Página**  
:::image-end:::  

Cómo se **organiza el** panel Página:  
*   El nivel superior, como en `top` la figura anterior, representa un [marco HTML][W3CHtml4Frames].  Busque `top` en todas las páginas que visite.  `top` representa el marco del documento principal.  
*   El segundo nivel, como en `docs.microsoft.com` la figura anterior, representa un [origen][HtmlstandardOrigin].  
*   El tercer nivel, cuarto nivel, y así sucesivamente, representan directorios y recursos que se cargaron desde ese origen.  Por ejemplo, en la figura anterior, la ruta de acceso completa al recurso `devtools-guide-chromium` es `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Elija un archivo en el panel **Página** para mostrar el contenido en el **panel Editor.**  Puede mostrar cualquier tipo de archivo.  Para las imágenes, se muestra una vista previa de la imagen.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Mostrar el contenido de a4d10f71.index-docs.js en el panel Editor" lightbox="../media/sources-editor-pane.msft.png":::
   Mostrar el contenido del `a4d10f71.index-docs.js` panel **Editor**  
:::image-end:::  

## <a name="edit-css-and-javascript"></a>Editar CSS y JavaScript  

Use el **panel Editor** para editar CSS y JavaScript.  DevTools actualiza la página para ejecutar el nuevo código.  Por ejemplo, si edita un archivo CSS agregando la regla de estilo siguiente:

```css
.metadata.page-metadata {
    color: red;
}
```

Ese cambio debe tener efecto inmediatamente.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS en el panel Editor para cambiar el color del texto del subtítulo a rojo" lightbox="../media/edit-css.msft.png":::
   Editar CSS en el **panel Editor** para cambiar el color del texto del subtítulo a rojo  
:::image-end:::  

Los cambios CSS tienen efecto inmediatamente, sin necesidad de guardar.  Para que los cambios de JavaScript entren en vigor, seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\).  DevTools no vuelve a ejecutar un script, por lo que los únicos cambios de JavaScript que tienen efecto son los que se hacen dentro de las funciones.  Por ejemplo, en la siguiente figura, observe cómo no `console.log('A')` se ejecuta, mientras que `console.log('B')` sí.  Si DevTools vuelve a ejecutar el script completo después de realizar el cambio, el texto se `A` registra en la **consola**.  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Edición de JavaScript en el panel Editor" lightbox="../media/edit-js.msft.png":::
   Edición de JavaScript en el **panel Editor**  
:::image-end:::  

DevTools borra los cambios de CSS y JavaScript al actualizar la página.  Vaya a [Configurar un área de trabajo](#set-up-a-workspace) para obtener información sobre cómo guardar los cambios en el sistema de archivos.  

## <a name="create-save-and-run-snippets"></a>Crear, guardar y ejecutar fragmentos de código  

Los fragmentos de código son scripts que puede ejecutar en cualquier página.  Imagine que escribe repetidamente el siguiente código en la consola **,** para insertar la biblioteca jQuery en una página, de modo que pueda ejecutar comandos de jQuery desde la **consola**.  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

En su lugar, puede guardar este código en un fragmento de **código** y ejecutarlo con un par de clics de botón, en cualquier momento que lo necesite.  DevTools guarda el fragmento **de código** en el sistema de archivos.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Fragmento de código que inserta la biblioteca jQuery en una página" lightbox="../media/snippet.msft.png":::
   Fragmento **de** código que inserta la biblioteca jQuery en una página  
:::image-end:::  

Para ejecutar un **fragmento de código:**

*   Abra el archivo mediante el panel **Fragmentos** de código y elija **Ejecutar** \( ![ El botón Ejecutar ](../media/run-snippet-icon.msft.png) \).  
*   Abra el [menú comando][DevtoolsGuideChromiumCommandMenuIndex], elimine el carácter, escriba , escriba el nombre del fragmento de código y, a `>` continuación, seleccione `!` **** `Enter` .  
    
Vaya a [Ejecutar fragmentos de código desde cualquier página para][DevtoolsGuideChromiumJavascriptSnippets] obtener más información.

## <a name="debug-javascript"></a>Depurar JavaScript  

En lugar de usar para deducir dónde está fallando JavaScript, considere la posibilidad de usar las herramientas `console.log()` de depuración de Microsoft Edge DevTools, en su lugar.  La idea general es establecer un punto de interrupción, que es un lugar de detención intencionado en el código, y, a continuación, pasar por el tiempo de ejecución del código, una línea a la vez.  Al pasar por el código, puede mostrar y cambiar los valores de todas las propiedades y variables definidas actualmente, ejecutar JavaScript en la consola **y**mucho más.

Vaya a [Introducción a La depuración de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para obtener información sobre los conceptos básicos de la depuración en DevTools.

:::image type="complex" source="../media/debugging.msft.png" alt-text="Depurar JavaScript" lightbox="../media/debugging.msft.png":::
   Depurar JavaScript  
:::image-end:::  

## <a name="set-up-a-workspace"></a>Configurar un área de trabajo  

De forma predeterminada, al editar un archivo en la **herramienta Orígenes,** esos cambios se pierden al actualizar la página.  **Las áreas** de trabajo permiten guardar los cambios realizados en DevTools en el sistema de archivos.  Básicamente, DevTools puede usarse como editor de código.

Vaya a [Editar archivos con áreas de trabajo][DevtoolsGuideChromiumWorkspacesIndex] para empezar.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar archivos con áreas de trabajo | Microsoft Docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origen | Estándar HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Fotogramas | W3C"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/sources) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
