---
description: Visualice y edite archivos, cree fragmentos, depure JavaScript y configure áreas de trabajo en el panel orígenes de Microsoft Edge DevTools.
title: Información general del panel orígenes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b90f927670146c004a335256ace28203219442eb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236048"
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

# Información general del panel orígenes  

Use el panel de **orígenes** de Microsoft Edge DevTools para realizar las siguientes acciones.  

*   [Archivos de visualización](#display-files).  
*   [Edite CSS y JavaScript](#edit-css-and-javascript).  
*   [Cree y guarde **fragmentos** de código de JavaScript](#create-save-and-run-snippets), que puede ejecutar en cualquier página web.  Los **fragmentos de código** son similares a bookmarklets.  
*   [Depure JavaScript](#debug-javascript).  
*   [Configure un área de trabajo](#set-up-a-workspace)para que los cambios que realice en DevTools se guarden en el código de su sistema de archivos.  
    
## Archivos de visualización  

Use el panel de **páginas** para mostrar todos los recursos que la página ha cargado.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="El panel de páginas" lightbox="../media/sources-page-pane.msft.png":::
   El panel de **páginas**  
:::image-end:::  

Organización del panel de **páginas** :  
*   El nivel superior, como `top` en la figura anterior, representa un [marco html][W3CHtml4Frames].  Buscar `top` en cada página que visite.  `top` representa el marco del documento principal.  
*   El segundo nivel, como `docs.microsoft.com` en la figura anterior, representa un [origen][HtmlstandardOrigin].  
*   El tercer nivel, el cuarto nivel, etc., representan los directorios y recursos que se cargaron desde ese origen.  Por ejemplo, en la ilustración anterior, la ruta de acceso completa al recurso `devtools-guide-chromium` es `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Elija un archivo en el panel de **páginas** para mostrar el contenido en el panel del **Editor** .  Puede mostrar cualquier tipo de archivo.  Para las imágenes, se muestra una vista previa de la imagen.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Mostrar el contenido de a4d10f71.index-docs.js en el panel Editor" lightbox="../media/sources-editor-pane.msft.png":::
   Mostrar el contenido de `a4d10f71.index-docs.js` en el panel **Editor**  
:::image-end:::  

## Editar CSS y JavaScript  

Use el panel **Editor** para editar CSS y JavaScript.  DevTools actualiza la página para ejecutar el nuevo código.  Por ejemplo, Si edita un archivo CSS agregando la regla de estilo a continuación:

```css
.metadata.page-metadata {
    color: red;
}
```

Ese cambio debe surtir efecto inmediatamente.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS en el panel del editor para cambiar el color del texto del subtítulo a rojo" lightbox="../media/edit-css.msft.png":::
   Editar CSS en el panel del **Editor** para cambiar el color del texto del subtítulo a rojo  
:::image-end:::  

Los cambios de CSS se aplican inmediatamente, no es necesario guardar.  Para que los cambios de JavaScript surtan efecto, seleccione `Control` + `S` \ (Windows, Linux \) o `Command` + `S` \ (MacOS \).  DevTools no vuelve a ejecutar un script, por lo que los únicos cambios de JavaScript que se aplican son los que realiza dentro de las funciones.  Por ejemplo, en la siguiente ilustración, observe cómo `console.log('A')` no se ejecuta, pero `console.log('B')` sí.  Si DevTools vuelve a ejecutar la secuencia de comandos completa después de realizar el cambio, el texto `A` se habría grabado en la **consola**.  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Edición de JavaScript en el panel Editor" lightbox="../media/edit-js.msft.png":::
   Edición de JavaScript en el panel **Editor**  
:::image-end:::  

DevTools borra los cambios de CSS y JavaScript al volver a cargar la página.  Vaya a [configurar un área de trabajo](#set-up-a-workspace) para obtener información sobre cómo guardar los cambios en el sistema de archivos.  

## Crear, guardar y ejecutar fragmentos de código  

Los fragmentos de código son scripts que se pueden ejecutar en cualquier página.  Suponga que escribe repetidamente el siguiente código en la **consola**, para insertar la biblioteca de jQuery en una página, de modo que pueda ejecutar comandos de jQuery desde la **consola**.  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

En su lugar, puede guardar este código en un **fragmento** de código y ejecutarlo con un par de clics de botón, cada vez que lo necesite.  DevTools guarda el **fragmento de código** en el sistema de archivos.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Un fragmento de código que inserta la biblioteca jQuery en una página" lightbox="../media/snippet.msft.png":::
   Un **fragmento de código** que inserta la biblioteca jQuery en una página  
:::image-end:::  

Para ejecutar un **fragmento de código**:

*   Abra el archivo con el panel **fragmentos de código** y elija **Ejecutar** \ ( ![ el botón ejecutar ][ImageRunIcon] \).  
*   Abra el [menú de comandos][DevtoolsGuideChromiumCommandMenuIndex], elimine el `>` carácter, escriba `!` , escriba el nombre del **fragmento de código**y, a continuación, seleccione `Enter` .  
    
Navegue para [Ejecutar fragmentos de código desde cualquier página][DevtoolsGuideChromiumJavascriptSnippets] para obtener más información.

## Depurar JavaScript  

En lugar de usar `console.log()` para inferir Dónde está el error de JavaScript, considere la posibilidad de usar las herramientas de depuración de Microsoft Edge DevTools en su lugar.  La idea general es establecer un punto de interrupción, que es un lugar de detención intencionado en el código, y, a continuación, pasar por el tiempo de ejecución del código, de línea en línea.  Mientras recorres el código, puedes mostrar y cambiar los valores de todas las propiedades y variables definidas actualmente, ejecutar JavaScript en la **consola**y mucho más.

Vaya a introducción a la [depuración de JavaScript][DevtoolsGuideChromiumJavascriptIndex] para conocer los conceptos básicos de la depuración en DevTools.

:::image type="complex" source="../media/debugging.msft.png" alt-text="Depurar JavaScript" lightbox="../media/debugging.msft.png":::
   Depurar JavaScript  
:::image-end:::  

## Configurar un área de trabajo  

De forma predeterminada, al editar un archivo en la herramienta **orígenes** , esos cambios se pierden al volver a cargar la página.  Las **áreas de trabajo** le permiten guardar los cambios que realice en DevTools en el sistema de archivos.  Esencialmente, DevTools puede usarse como editor de código.

Desplácese hasta [editar archivos con áreas de trabajo][DevtoolsGuideChromiumWorkspacesIndex] para comenzar.

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar archivos con áreas de trabajo | Microsoft docs"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origen | Estándar HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Marcos | RELATIVA"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/sources) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
