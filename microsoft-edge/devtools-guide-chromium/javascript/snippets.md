---
title: Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3a5ae986e3080a0b6a8b1bf34b0e0efc44c90303
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982046"
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





# Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools   



Si tienes que ejecutar el mismo código de forma repetida en la [consola][DevtoolsConsoleIndex] , considera la posibilidad de guardar el código como un fragmento de código.  Los fragmentos de código son scripts que se crean en el panel [fuentes][DevToolsSourcesPanel] .  Tienen acceso al contexto de JavaScript de la página y puede ejecutarlos en cualquier página.  Los fragmentos de código son una alternativa a [bookmarklets][WikiBookmarklet].  
Firefox DevTools tiene una característica similar a la de los fragmentos de código denominado [Bloc][MDNScratchpad]dedo.  

Por ejemplo, en la siguiente ilustración se muestra la Página principal de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aspecto de la página antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   Aspecto de la página antes de ejecutar el fragmento de código  
:::image-end:::  

El código fuente del fragmento de la ilustración anterior.  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

En la siguiente ilustración, la página aparece después de ejecutar el fragmento de código.  El **cajón de consola** emerge para mostrar el `Hello, Snippets!` mensaje que indica que el recorte y el contenido de la página cambian por completo.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aspecto de la página después de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Aspecto de la página después de ejecutar el fragmento de código  
:::image-end:::  

## Abrir el panel de fragmentos   

El panel de **fragmentos de código** muestra los fragmentos de código.  Cuando desee editar un fragmento de código, tendrá que abrirlo desde el panel **fragmentos de código** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="El panel de fragmentos" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   El panel de **fragmentos**  
:::image-end:::  

### Abrir el panel de fragmentos de código con un mouse   

1.  Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .  El panel de **páginas** suele abrirse de forma predeterminada.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Panel orígenes con el panel de páginas abierto a la izquierda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Panel **orígenes** con el panel de **páginas** abierto a la izquierda  
    :::image-end:::  
    
1.  Haga clic en la pestaña **fragmentos** para abrir el panel **fragmentos de código** .  Es posible que tenga que hacer clic en **más pestañas** \ ( ![ más pestañas ][ImageMoreTabsIcon] \) para acceder a la opción **fragmentos** .  
    
### Abrir el panel de fragmentos de código con el menú de comandos   

1.  Centre el cursor en algún lugar dentro de DevTools.  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Comience `Snippets` a escribir, seleccione **Mostrar fragmentos**y, a continuación, presione `Enter` para ejecutar el comando.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="El comando Mostrar fragmentos" lightbox="../media/javascript-search-show-snippets.msft.png":::
       El comando **Mostrar fragmentos**  
    :::image-end:::  
    
## Crear fragmentos   

### Crear un fragmento de código a través del panel orígenes   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic en **nuevo fragmento de código**.  
1.  Escriba un nombre para el fragmento de código y, a continuación, presione `Enter` para guardar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nombrar un fragmento de código" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Nombrar un fragmento de código  
    :::image-end:::  
    
### Crear un fragmento de código mediante el menú de comandos   

1.  Centre el cursor en algún lugar dentro de DevTools.  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Comience `Snippet` a escribir, seleccione **crear nuevo fragmento**y, a continuación, presione `Enter` para ejecutar el comando.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Comando para crear un nuevo fragmento de código" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Comando para crear un nuevo fragmento de código  
    :::image-end:::  
    
Consulte cambiar [el nombre](#rename-snippets) de los fragmentos de código si desea asignar un nombre personalizado al nuevo fragmento de código.  

## Editar fragmentos de código   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  En el panel **fragmentos** de código, haga clic en el nombre del fragmento de código que desea editar para abrirlo en el **Editor de código**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="El editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       El **Editor de código**  
    :::image-end:::  
    
1.  Use el **Editor de código** para agregar JavaScript al fragmento de código.  
1.  Cuando aparece un asterisco junto al nombre del fragmento de código, significa que tiene código no guardado. Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un asterisco junto al nombre del fragmento de código, que indica código no guardado" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Un asterisco junto al nombre del fragmento de código, que indica código no guardado  
    :::image-end:::  
    
## Ejecutar fragmentos de código   

### Ejecutar un recorte desde el panel fuentes   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic en el nombre del fragmento de código que desea ejecutar.  El fragmento de código se abre en el **Editor de código**.  
1.  Haga clic en **Ejecutar fragmento** \ ( ![ Ejecutar fragmento ][ImageRunSnippetIcon] \) o `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \).  
    
### Ejecutar un fragmento de código con el menú de comandos   

1.  Centre el cursor en algún lugar dentro de DevTools.  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Elimine el `>` carácter y escriba el `!` carácter seguido del nombre del fragmento de código que desea ejecutar.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ejecución de un fragmento de código desde el menú de comandos" lightbox="../media/javascript-search-run-command.msft.png":::
       Ejecución de un fragmento de código desde el **menú de comandos**  
    :::image-end:::  
    
1.  Pulse `Enter` para ejecutar el fragmento de código.  

## Cambiar el nombre de los fragmentos de código   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic con el botón derecho en el nombre del fragmento y seleccione cambiar **nombre**.  
    
## Eliminar fragmentos de código   

1.  [Abra el panel **fragmentos de código** ](#open-the-snippets-pane).  
1.  Haga clic con el botón derecho en el nombre del fragmento y seleccione **quitar**.  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft docs"  
[DevToolsSourcesPanel]: ../sources.md "Información general del panel orígenes | Microsoft docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc de la | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet, Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
