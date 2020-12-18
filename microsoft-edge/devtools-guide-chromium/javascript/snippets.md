---
description: Los fragmentos de código son pequeños scripts que puede crear y ejecutar en la herramienta de orígenes de Microsoft Edge DevTools.  Puede obtener acceso a los recursos de cualquier página web y ejecutarlos.  Al ejecutar un fragmento de código, se ejecuta desde el contexto de la página web abierta actualmente.
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 89b028177016a9194a67bbbe44d08572e5755f95
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230960"
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

# Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools  

Si ejecutas el mismo código de la [consola][DevtoolsConsoleIndex] varias veces, te recomendamos que guardes el código como un fragmento de código.  Los fragmentos de código son scripts que se crean en la herramienta [orígenes][DevToolsSourcesTool] .  Los fragmentos de código tienen acceso al contexto de JavaScript de la página web y puede ejecutar fragmentos de código en cualquier página web.  La configuración de seguridad de la mayoría de las páginas web impide que se carguen otros scripts en los fragmentos.  Por ese motivo, debes incluir todo tu código en un archivo.  

Los fragmentos de código son una alternativa a [bookmarklets][WikiBookmarklet] con la diferencia de que los fragmentos de código solo se ejecutan en DevTools y no se limitan a la longitud permitida de una dirección URL.  

El uso de recortes es una excelente manera de cambiar algunas cosas en una página web de terceros.  Los cambios de código en los fragmentos se agregan a la página web actual y se ejecutan en el mismo contexto.  Para obtener más información sobre cómo cambiar el código existente de una página web, vaya a [invalidaciones][DevtoolsJavascriptOverrides].  

:::row:::
   :::column span="":::
      Por ejemplo, en la siguiente ilustración se muestra la Página principal de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         La Página Web antes de ejecutar el fragmento de código  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      El código fuente del fragmento de código de la Página Web antes de ejecutar el fragmento.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

En la siguiente ilustración, la página web aparece después de ejecutar el fragmento de código.  El **cajón de consola** emerge para mostrar el `Hello, Snippets!` mensaje que indica que el fragmento de código registra y el contenido de la página web cambia por completo.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="La página web después de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   La página web después de ejecutar el fragmento de código  
:::image-end:::  

## Abrir el panel de fragmentos  

El panel de **fragmentos de código** muestra los fragmentos de código.  Cuando desee editar un fragmento de código, tendrá que abrirlo desde el panel **fragmentos de código** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="El panel de fragmentos" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   El panel de **fragmentos**  
:::image-end:::  

### Abrir el panel de fragmentos de código con un mouse  

1.  Elija la pestaña **orígenes** para abrir la herramienta **orígenes** .  El panel de **páginas** suele abrirse de forma predeterminada.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="La herramienta orígenes con el panel de páginas abierto a la izquierda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       La herramienta **orígenes** con el panel de **páginas** abierto a la izquierda  
    :::image-end:::  
    
1.  Elija la pestaña **fragmentos** para abrir el panel **fragmentos de código** .  Es posible que tenga que elegir **más pestañas** \ ( ![ más pestañas ][ImageMoreTabsIcon] \) para acceder a la opción **fragmentos de código** .  
    
### Abrir el panel de fragmentos de código con el menú de comandos  

1.  Centre el cursor en algún lugar de DevTools.  
1.  Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Escriba `Snippets` , elija **Mostrar fragmentos**y, a continuación, seleccione `Enter` para ejecutar el comando.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="El comando Mostrar fragmentos" lightbox="../media/javascript-search-show-snippets.msft.png":::
       El comando **Mostrar fragmentos**  
    :::image-end:::  
    
## Crear fragmentos  

### Crear un fragmento de código a través del panel orígenes  

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Elija **nuevo fragmento de código**.  
1.  Escriba un nombre para el fragmento de código y, después, seleccione `Enter` Guardar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nombrar un fragmento de código" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nombrar un fragmento de código  
    :::image-end:::  
    
### Crear un fragmento de código mediante el menú de comandos  

1.  Centre el cursor en algún lugar de DevTools.  
1.  Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Escriba `Snippet` , elija **crear nuevo fragmento de código**y, a continuación, seleccione `Enter` para ejecutar el comando.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Comando para crear un nuevo fragmento de código" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Comando para crear un nuevo fragmento de código  
    :::image-end:::  
    
Para cambiar el nombre de un nuevo fragmento con un nombre personalizado, navegue hasta [cambiar el nombre](#rename-snippets)de los fragmentos.  

## Editar fragmentos de código  

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  En el panel **fragmentos** , elija el nombre del fragmento de código que desea editar.  Se abre en el **Editor de código**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="El editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       El **Editor de código**  
    :::image-end:::  
    
1.  Use el **Editor de código** para agregar JavaScript al fragmento de código.  
1.  Cuando aparece un asterisco junto al nombre del fragmento, significa que tiene código no guardado.  Seleccione `Control` + `S` \ (Windows, Linux \) o `Command` + `S` \ (MacOS \) para guardar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un asterisco junto al nombre del fragmento de código indica que el código no se ha guardado" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Un asterisco junto al nombre del fragmento de código indica que el código no se ha guardado  
    :::image-end:::  
    
## Ejecutar fragmentos de código  

### Ejecutar un recorte desde el panel fuentes  

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Elija el nombre del fragmento de código que desea ejecutar.  El fragmento de código se abre en el **Editor de código**.  
1.  Elija **Ejecutar fragmento** \ ( ![ Ejecutar miniprograma ][ImageRunSnippetIcon] \) o seleccione `Control` + `Enter` \ (Windows, Linux \) o `Command` + `Enter` \ (MacOS \).  
    
### Ejecutar un fragmento de código con el menú de comandos  

1.  Centre el cursor en algún lugar de DevTools.  
1.  Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Elimine el `>` carácter y escriba el `!` carácter seguido del nombre del fragmento de código que desea ejecutar.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ejecución de un fragmento de código desde el menú de comandos" lightbox="../media/javascript-search-run-command.msft.png":::
       Ejecución de un fragmento de código desde el **menú de comandos**  
    :::image-end:::  
    
1.  Seleccione `Enter` para ejecutar el fragmento de código.  

## Cambiar el nombre de los fragmentos de código  

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Desplace el puntero sobre el nombre del fragmento de código, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **cambiar nombre**.  
    
## Eliminar fragmentos de código  

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Desplace el puntero sobre el nombre del fragmento de código, abra el menú contextual \ (haga clic con el botón derecho \) y elija **quitar**.  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft docs"  
[DevToolsSourcesTool]: ../sources/index.md "Información general de la herramienta orígenes | Microsoft docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Invalidaciones | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc de la | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
