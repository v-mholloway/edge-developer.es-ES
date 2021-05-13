---
description: Use la herramienta Problemas para buscar y solucionar problemas con su sitio web.
title: Buscar y solucionar problemas con la Microsoft Edge de problemas de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 64954d632416f7d1353269d04c1550ca7a0652b7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564185"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a>Buscar y solucionar problemas con la Microsoft Edge de problemas de DevTools  

La **herramienta Problemas** en Microsoft Edge DevTools reduce la fatiga de notificación y el desorden de la **consola**.  Úselo para buscar soluciones a problemas detectados por el explorador, como problemas de cookies y contenido mixto.  

> [!NOTE]
> En Microsoft Edge 84, la **herramienta Problemas** admite tres tipos de problema:  
> *   [Problemas de cookies][MDNSameSiteCookies]  
> *   [Contenido mixto][MDNMixedContent]  
> *   [Problemas del COEP][W3CCOEPSpec]
> 
> El Microsoft Edge de DevTools planea admitir más tipos de problemas en versiones futuras de Microsoft Edge.  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a>Abra la herramienta Problemas en el cajón DevTools  

1.  Navegue a una página web, como [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], que contiene problemas que corregir.  
1.  [Abra DevTools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Elija el **botón Ir a problemas** en la barra de advertencia amarilla.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Vaya al botón Problemas en la barra de advertencia amarilla cuando se detecten problemas" lightbox="../media/issues-open-issues-tab.msft.png":::
             El **botón Ir a Problemas** de la barra de advertencia amarilla cuando se detectan problemas.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Como alternativa, elija **Problemas** en el **menú Más** herramientas.  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Herramienta Problemas en el menú Más herramientas" lightbox="../media//issues-more-tools-menu.msft.png":::
             **Herramienta Problemas** en **el menú Más** herramientas  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Elija el **botón Volver a cargar** página, si es necesario.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Herramienta Problemas en el botón de página DevTools Drawer with Reload" lightbox="../media/issues-tab-before-refresh.msft.png":::
       **Herramienta Problemas** en el botón de página DevTools Drawer with **Reload**  
    :::image-end:::  

    Los problemas notificados en **la consola** son bastante difíciles de comprender, como las advertencias de cookies de la siguiente imagen.  En función de los problemas notificados, puede que no esté claro lo que debe hacer.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Herramienta Problemas en el cajón de DevTools con tres problemas de cookies" lightbox="../media/issues-tab-after-refresh.msft.png":::
       **Herramienta** Problemas en el cajón de DevTools con tres problemas de cookies  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a>Ver elementos en la herramienta Problemas  

La **herramienta Problemas** del cajón DevTools presenta advertencias de una forma estructurada, agregada y que puede actuar.  

1.  Elija un elemento en la **herramienta Problemas** para obtener instrucciones sobre cómo solucionar el problema y encontrar los recursos afectados.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marcar las cookies entre sitios como problema seguro abierto en la herramienta Problemas" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Marcar las cookies entre sitios como problema seguro** abierto en la herramienta **Problemas**  
    :::image-end:::  
    
    Cada elemento tiene cuatro componentes:  
    
    *   Un titular que describe el problema.  
    *   Una descripción que proporciona el contexto y la solución.  
    *   Sección **RECURSOS AFECTADOS que** vincula a recursos dentro del contexto de DevTools adecuado, como el panel Red.  
    *   Vínculos a más instrucciones.  
    
1.  Elija elementos en **RECURSOS AFECTADOS** para ver detalles.  En el siguiente ejemplo, el problema **Marcar las cookies entre** sitios como seguridad afecta a una cookie y dos solicitudes.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Recursos afectados abiertos en la herramienta Problemas" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Recursos afectados abiertos en la **herramienta Problemas** en el cajón DevTools  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a>Ver problemas en contexto  

1.  Elija un vínculo de recurso para ver el elemento en el contexto adecuado dentro de DevTools.  En el ejemplo siguiente, elija `samesite-sandbox.glitch.me` en **Solicitudes** para mostrar las cookies adjuntas a esa solicitud.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Ver la cookie afectada en la herramienta DevTools Network" lightbox="../media/issues-tab-view-request.msft.png":::
       Ver la cookie afectada en la herramienta DevTools **Network**  
    :::image-end:::  

1.  Desplácese para ver el elemento con un problema: para el siguiente ejemplo, la `ck02` cookie.  Mantenga el mouse en **la columna SameSite** para revisar `None` el valor detectado por el problema.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Valor ninguno en la columna SameSite para la cookie de ck02 en la herramienta DevTools Network" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` valor de la **columna SameSite** de `ck02` la cookie en la herramienta DevTools **Network**  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Pruebas de cookies de SameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies de SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Contenido mixto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Directiva de incrustación entre orígenes | Grupo de Community web de la Community web"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/issues/index) y es creado por [Sam Dutton][SamDutton] \(Developer Advocate\).  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton  
