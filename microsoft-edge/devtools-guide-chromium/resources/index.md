---
description: Organice los recursos por marco, dominio, tipo u otros criterios.
title: Ver recursos de página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 415ed45bf650aa6800ab674cce74179f783a82c7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565074"
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
# <a name="view-page-resources-with-microsoft-edge-devtools"></a>Ver recursos de página con Microsoft Edge DevTools  

Esta guía le enseña a usar Microsoft Edge DevTools para ver los recursos de una página web.  Los recursos son los archivos que necesita una página para mostrarse correctamente.  Algunos ejemplos de recursos incluyen archivos CSS, JavaScript y HTML, así como imágenes.  

En esta guía se supone que está familiarizado con los conceptos básicos del desarrollo [web][MDNLearnWebDevelopment] y [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## <a name="open-resources"></a>Recursos abiertos  

Cuando conoce el nombre del recurso que desea inspeccionar, el menú **comando** proporciona una forma rápida de abrir el recurso.  

1.  Seleccione `Control` + `P` \(Windows, Linux\) o `Command` + `P` \(macOS\).  Se **abre el cuadro de diálogo** Abrir archivo.  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       Cuadro **de diálogo Abrir** archivo  
    :::image-end:::  
    
1.  Elija el archivo en el desplegable o empiece a escribir el nombre de archivo y seleccione una vez que el archivo correcto esté `Enter` resaltado en el cuadro autocompletar.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Escriba un nombre de archivo en el cuadro de diálogo Abrir archivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Escriba un nombre de archivo en el **cuadro de diálogo Abrir** archivo  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a>Abrir recursos en la herramienta Red  

Vaya a [Inspeccionar los detalles de un recurso][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspeccionar un recurso en la herramienta Red" lightbox="../media/resources-network-response.msft.png":::
   Inspeccionar un recurso en la **herramienta Red**  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a>Mostrar recursos de la herramienta Red desde otros paneles  

La [sección Examinar recursos](#browse-resources) siguiente muestra cómo ver recursos de varias partes de la interfaz de usuario de DevTools.  Si alguna vez desea inspeccionar **** un recurso en la herramienta Red, mantenga el mouse en el recurso, abra el menú contextual \(clic con el botón secundario\) y elija Mostrar en el **panel Red**.  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Mostrar en el panel Red" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Mostrar en el panel Red**  
:::image-end:::  

## <a name="browse-resources"></a>Examinar recursos  

### <a name="browse-resources-in-the-network-panel"></a>Examinar recursos en el panel Red  

Vaya a [Registrar actividad de red][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página en el registro de red" lightbox="../media/resources-network-resources.msft.png":::
   Recursos de página en el **registro de** red  
:::image-end:::  

### <a name="browse-by-directory"></a>Examinar por directorio  

Para ver los recursos de una página web organizada por directorio:  

1.  Abra DevTools.
1.  Elija la **herramienta Orígenes** y, a continuación, en el **panel** Navegador de la parte superior izquierda, elija la **pestaña** Página.
1.  Elija el **botón Más opciones** (...) a la derecha de la pestaña **Página** y, a continuación, elija Agrupar **por carpeta**.
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="La pestaña Página del panel Navegador de la herramienta Orígenes" lightbox="../media/resources-sources-page-empty.msft.png":::
       La **pestaña Página** del panel **Navegador** de la herramienta **Orígenes**  
    :::image-end:::  
    
    Este es un desglose de los elementos no obvios de la figura anterior.  
    
    | Elemento de página | Descripción |  
    |:--- |:--- |  
    | `top` | El contexto de [exploración del documento principal][MDNInlineFrame]. |  
    | `airhorner.com` | El dominio.  Todos los recursos anidados en él proceden de ese dominio.  Por ejemplo, la dirección URL completa del `comlink.global.j` archivo es probablemente `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Un directorio. |  
    | `(index)` | El documento HTML principal. |  
    | `sw.js` | Contexto de tiempo de ejecución de un trabajador de servicio. |  
    
1.  Elija un recurso para verlo en el **Editor**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Ver un archivo en el Editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       Ver un archivo en el **Editor**  
    :::image-end:::  
    
### <a name="browse-by-filename"></a>Examinar por nombre de archivo  

De forma predeterminada, la pestaña **Página** agrupa los recursos por directorio.  Para mostrar los recursos de cada dominio como una lista plana, en lugar de agruparlos por directorio:

1.  Vaya a la **herramienta Orígenes.**  
1.  En el **panel** Navegador (a la izquierda), elija la **pestaña** Página.  
1.  Elija **Más opciones y,** `...` a continuación, desactive la marca de verificación junto **a Grupo por carpeta**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="La opción Agrupar por carpeta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       La **opción Agrupar por** carpeta  
    :::image-end:::  
    
    Los recursos se organizan por tipo de archivo.  Dentro de cada tipo de archivo, los recursos se organizan alfabéticamente.  

    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="La pestaña Página después de borrar la marca de verificación Grupo por carpeta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       La **pestaña Página** después de borrar la marca de verificación Grupo **por** carpeta  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a>Examinar por tipo de archivo  

Para agrupar recursos en función de su tipo de archivo:  

1.  Elija la **pestaña** Aplicación.  Se **abre la herramienta** Aplicación.  De forma predeterminada, **el panel** Manifiesto normalmente se abre primero.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="La herramienta Aplicación" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       La **herramienta Aplicación**  
    :::image-end:::  
    
1.  Desplácese hacia abajo hasta el **panel Marcos.**  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Panel Marcos" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       Panel **Marcos**  
    :::image-end:::  
    
1.  Expanda las secciones en las que está interesado.  
1.  Elija un recurso para verlo.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Ver un recurso en el panel Aplicación" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Ver un recurso en **el** panel Aplicación  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a>Examinar archivos por tipo en el panel Red  

Vaya a [Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrar para CSS en el registro de red" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtrar para CSS en el registro **de** red  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Herramientas para desarrolladores | Microsoft Docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspeccionar los detalles del recurso: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Actividad de red de registro: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: el elemento Frame en línea | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Información sobre desarrollo web | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/resources/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
