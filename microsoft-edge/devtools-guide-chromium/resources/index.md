---
title: Ver recursos de página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4265841501bdd74d2976ecab1c2a07f1fb215535
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984475"
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





# Ver recursos de página con Microsoft Edge DevTools   

  

Esta guía le enseña cómo usar Microsoft Edge DevTools para ver los recursos de una página web.  Los recursos son los archivos que necesita una página para que se muestren correctamente.  Algunos ejemplos de recursos son los archivos CSS, JavaScript y HTML, así como las imágenes.  

En esta guía se presupone que está familiarizado con los conceptos básicos de [desarrollo web][MDNLearnWebDevelopment] y [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Abrir recursos   

Cuando conoce el nombre del recurso que quiere inspeccionar, el **menú de comandos** proporciona una forma rápida de abrir el recurso.  

1.  Pulse `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \).  Se abrirá el cuadro de diálogo **Abrir archivo** .  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       Cuadro de diálogo **Abrir archivo**  
    :::image-end:::  
    
1.  Seleccione el archivo de la lista desplegable o empiece a escribir el nombre de archivo y presione `Enter` una vez que el archivo correcto esté resaltado en el cuadro Autocompletar.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Escribir un nombre de archivo en el cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Escribir un nombre de archivo en el cuadro de diálogo **Abrir archivo**  
    :::image-end:::  
    
### Abrir recursos en el panel red   

Consulte [inspeccionar los detalles de un recurso][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspeccionar un recurso en el panel red" lightbox="../media/resources-network-response.msft.png":::
   Inspeccionar un recurso en el panel **red**  
:::image-end:::  

### Mostrar recursos en el panel de red de otros paneles   

En la sección [examinar recursos](#browse-resources) que se muestra a continuación se muestra cómo ver los recursos de varias partes de la interfaz de usuario de DevTools.  Si alguna vez desea inspeccionar un recurso en el panel **red** , haga clic con el botón derecho en el recurso y seleccione **Mostrar en el panel de red**.  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Mostrar en el panel red" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Mostrar en el panel red**  
:::image-end:::  

## Examinar recursos   

### Examinar recursos en el panel red   

Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página en el registro de red" lightbox="../media/resources-network-resources.msft.png":::
   Recursos de página en el registro de **red**  
:::image-end:::  

### Examinar por directorio   

Para ver los recursos de una página organizada por directorio:  

1.  Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .  
1.  Haga clic en la pestaña de la **Página** para mostrar los recursos de la página.  Se abre el panel de **páginas** .  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="El panel de páginas" lightbox="../media/resources-sources-page-empty.msft.png":::
       El panel de **páginas**  
    :::image-end:::  
    
    Este es un desglose de los elementos no obvios de la ilustración anterior.  
    
    | Elemento de página | Descripción |  
    |:--- |:--- |  
    | `top` | [Contexto de examen][MDNInlineFrame]de documento principal. |  
    | `airhorner.com` | El dominio.  Todos los recursos anidados en él provienen de ese dominio.  Por ejemplo, la dirección URL completa del `comlink.global.j` archivo es probablemente `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Un directorio. |  
    | `(index)` | Documento HTML principal. |  
    | `sw.js` | Contexto en tiempo de ejecución de un trabajo de servicio. |  
    
1.  Haga clic en un recurso para verlo en el **Editor**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Ver un archivo en el editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       Ver un archivo en el **Editor**  
    :::image-end:::  
    
### Examinar por nombre de archivo   

De forma predeterminada, el panel de **páginas** agrupa los recursos por directorio.  Para deshabilitar esta agrupación y ver los recursos de cada dominio como una lista plana:  

1.  Abra el panel de **páginas** .  Consulte [examinar por directorio](#browse-by-directory).  
1.  Haga clic en **más opciones** `...` y deshabilite **Agrupar por carpeta**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="La opción agrupar por carpeta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       La opción **Agrupar por carpeta**  
    :::image-end:::  
    
    Los recursos están organizados por tipo de archivo.  Dentro de cada tipo de archivo, los recursos están organizados alfabéticamente.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="El panel de páginas después de deshabilitar agrupar por carpeta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       El panel de **páginas** después de deshabilitar **Agrupar por carpeta**  
    :::image-end:::  
    
### Examinar por tipo de archivo   

Para agrupar recursos en función de su tipo de archivo:  

1.  Haga clic en la pestaña **aplicación** .  Se abre el panel de la **aplicación** .  De forma predeterminada, el panel **manifiesto** generalmente se abre en primer lugar.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="El panel de aplicaciones" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       El panel de **aplicaciones**  
    :::image-end:::  
    
1.  Desplácese hacia abajo hasta el panel **Marcos** .  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="El panel marcos" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       El panel **Marcos**  
    :::image-end:::  
    
1.  Expanda las secciones en las que esté interesado.  
1.  Haga clic en un recurso para verlo.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Ver un recurso en el panel de aplicaciones" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Ver un recurso en el panel de **aplicaciones**  
    :::image-end:::  
    
#### Examinar archivos por tipo en el panel red   

Consulte [filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrar por CSS en el registro de red" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtrar por CSS en el registro de **red**  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso-comprobar actividad de red en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Revise los detalles de la actividad de red inspeccionar recursos en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Registrar actividad de red: inspeccionar actividad de red en Microsoft Edge DevTools | Microsoft docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> iframe: el elemento marco alineado | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprenda el desarrollo web | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/resources/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
