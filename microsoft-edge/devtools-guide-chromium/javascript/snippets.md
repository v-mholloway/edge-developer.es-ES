---
description: Los fragmentos de código son pequeños scripts que puede crear y ejecutar en la herramienta Orígenes de Microsoft Edge DevTools.  Puede acceder y ejecutar recursos desde cualquier página web.  Cuando se ejecuta un fragmento de código, se ejecuta desde el contexto de la página web abierta actualmente.
title: Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 00c612a1573c7446711a2dc9d22985c83140eecd
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519432"
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

# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a>Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools  

Si ejecuta el mismo código en la [consola][DevtoolsConsoleIndex] repetidamente, considere la posibilidad de guardar el código como fragmento de código en su lugar.  Los fragmentos de código son scripts que se pueden crear en la [herramienta][DevToolsSourcesTool] Orígenes.  Los fragmentos de código tienen acceso al contexto de JavaScript de la página web y puede ejecutar fragmentos de código en cualquier página web.  La configuración de seguridad de la mayoría de las páginas web bloquea la carga de otros scripts en fragmentos de código.  Por este motivo, debe incluir todo el código en un archivo.  

Los fragmentos de código son una alternativa a [los bookmarklets][WikiBookmarklet] con la diferencia de que los fragmentos de código solo se ejecutan en DevTools y no se limitan a la longitud permitida de una dirección URL.  

El uso de fragmentos de código es una excelente manera de cambiar algunas cosas en una página web de terceros.  Los cambios de código en fragmentos de código se agregan a la página web actual y se ejecutan en el mismo contexto.  Para obtener más información sobre cómo cambiar el código existente de una página web, vaya a [Invalidaciones][DevtoolsJavascriptOverrides].  

:::row:::
   :::column span="":::
      Por ejemplo, en la siguiente figura se muestra la página principal de DevTools a la izquierda y algún código fuente de fragmento de código a la derecha.  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Antes de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         La página web antes de ejecutar el fragmento de código  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      El código fuente de fragmento de código de la página web antes de ejecutar el fragmento de código.  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

En la siguiente figura, la página web aparece después de ejecutar el fragmento de código.  El **cajón de** consola aparece para mostrar el mensaje de que el fragmento de `Hello, Snippets!` código registra y el contenido de la página web cambia por completo.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="La página web después de ejecutar el fragmento de código" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   La página web después de ejecutar el fragmento de código  
:::image-end:::  

## <a name="open-the-snippets-tab"></a>Abrir la pestaña Fragmentos de código  

En **la pestaña Fragmentos** de código, en el **panel Navegador** de la izquierda, se enumeran los fragmentos de código.  Cuando quiera editar un fragmento de código, debe abrirlo desde la pestaña **Fragmentos de** código.  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Ficha Fragmentos de código" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Ficha **Fragmentos de** código  
:::image-end:::  

### <a name="open-the-snippets-tab-with-a-mouse"></a>Abra la pestaña Fragmentos de código con un mouse  

1.  Elija la **pestaña Orígenes.**  Aparece **la herramienta** Orígenes.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="La herramienta Orígenes con la pestaña Página abierta a la izquierda" lightbox="../media/javascript-sources-page-pane.msft.png":::
       La **herramienta Orígenes** con la pestaña **Página** abierta a la izquierda  
    :::image-end:::  
    
1.  En el **panel** Navegador (a la izquierda), elija la pestaña **Fragmentos de** código.  Para obtener acceso **a la opción Fragmentos** de código, es posible que deba elegir **Más pestañas** \( ![ Más pestañas ](../media/more-tabs-icon.msft.png) \).  
    
### <a name="open-the-snippets-tab-with-the-command-menu"></a>Abra la pestaña Fragmentos de código con el menú comando  

1.  Seleccione cualquier cosa en DevTools, para que DevTools tenga el foco.  
1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el menú comando.  
1.  Escriba `Snippets` , elija Mostrar **fragmentos de código**y, a continuación, seleccione para ejecutar el `Enter` comando.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="El comando Mostrar fragmentos de código" lightbox="../media/javascript-search-show-snippets.msft.png":::
       El **comando Mostrar fragmentos de código**  
    :::image-end:::  
    
## <a name="create-snippets"></a>Crear fragmentos de código  

### <a name="create-a-snippet-through-the-sources-tool"></a>Crear un fragmento de código a través de la herramienta Orígenes  

1.  [Abra la pestaña Fragmentos de código](#open-the-snippets-tab).  
1.  Elija **Nuevo fragmento de código**.  
1.  Escriba un nombre para el fragmento de código y, a continuación, seleccione `Enter` .  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Asigne un nombre a un fragmento de código" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Asigne un nombre a un fragmento de código  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a>Crear un fragmento de código a través del menú de comandos  

1.  Centra el cursor en alguna parte de DevTools.  
1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el menú comando.  
1.  Escriba `Snippet` , elija Crear nuevo fragmento **de**código y, a continuación, `Enter` seleccione para ejecutar el comando.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="El comando para crear un nuevo fragmento de código" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       El comando para crear un nuevo fragmento de código  
    :::image-end:::  
    
Para cambiar el nombre del nuevo fragmento de código con un nombre personalizado, vaya a [Cambiar el nombre de fragmentos de código](#rename-snippets).  

## <a name="edit-snippets"></a>Editar fragmentos de código  

1.  [Abra la pestaña Fragmentos de código](#open-the-snippets-tab).  
1.  En la **pestaña Fragmentos** de código, elija el nombre del fragmento de código que desea editar.  Se abre en el **Editor de código**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Editor de código" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       Editor **de código**  
    :::image-end:::  
    
1.  Use el **Editor de código** para agregar JavaScript al fragmento de código.  
1.  Cuando aparece un asterisco junto al nombre del fragmento de código, significa que tiene código no guardado.  Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un asterisco junto al nombre del fragmento de código indica código no guardado" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Un asterisco junto al nombre del fragmento de código indica código no guardado  
    :::image-end:::  
    
## <a name="run-snippets"></a>Ejecutar fragmentos de código  

### <a name="run-a-snippet-from-the-sources-tool"></a>Ejecutar un fragmento de código desde la herramienta Orígenes  

1.  [Abra la pestaña Fragmentos de código](#open-the-snippets-tab).  
1.  Elija el nombre del fragmento de código que desea ejecutar.  El fragmento de código se abre en **el Editor de código**.  
1.  Elija **Ejecutar fragmento de código** \( Ejecutar fragmento de código ![ ](../media/run-snippet-icon.msft.png) \).
    
### <a name="run-a-snippet-with-the-command-menu"></a>Ejecutar un fragmento de código con el menú de comandos  

1.  Centra el cursor en alguna parte de DevTools.  
1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el menú comando.  
1.  Elimine el `>` carácter y escriba el carácter seguido del nombre del fragmento de código que desea `!` ejecutar.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Ejecución de un fragmento de código desde el menú de comandos" lightbox="../media/javascript-search-run-command.msft.png":::
       Ejecución de un fragmento de código desde el **menú de comandos**  
    :::image-end:::  
    
1.  Seleccione `Enter` para ejecutar el fragmento de código.  

## <a name="rename-snippets"></a>Cambiar el nombre de fragmentos de código  

1.  [Abra la pestaña Fragmentos de código](#open-the-snippets-tab).  
1.  Mantenga el mouse en el nombre del fragmento de código, abra el menú contextual \(haga clic con el botón secundario\) y elija **Cambiar nombre**.  
    
## <a name="delete-snippets"></a>Eliminar fragmentos de código  

1.  [Abra la pestaña Fragmentos de código](#open-the-snippets-tab).  
1.  Mantenga el mouse sobre el nombre del fragmento de código, abra el menú contextual \(haga clic con el botón secundario en\) y elija **Quitar**.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Información general de la consola | Microsoft Docs"  
[DevToolsSourcesTool]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Invalida | Microsoft Docs"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
