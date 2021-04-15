---
description: Obtenga información sobre cómo filtrar mensajes de consola
title: Introducción al filtrado de mensajes en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: b493bb790b48bc1c4dca0e6802d2f638099b7644
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483677"
---
# <a name="filter-console-messages"></a>Filtrar mensajes de consola  

Al navegar por la web, es posible que encuentre que **la consola** está inundada de todo tipo de información.  A menudo, la información no es relevante para usted.  Por ejemplo, información sobre el proyecto en directo que otro desarrollador registró durante la depuración.  O más información sobre infracciones y advertencias sobre el rendimiento del sitio actual que no puede cambiar.  Tiene sentido usar las opciones de filtro de **La consola** para reducir el ruido.  

## <a name="filter-by-log-level"></a>Filtrar por nivel de registro  

Cada método del `console` objeto tiene un nivel de gravedad asociado.  Los niveles de gravedad `Verbose` son , , o `Info` `Warning` `Error` .  Muestra los niveles de gravedad en la [documentación de la API][DevtoolsConsoleApi].  Por ejemplo, `console.log()` es un `Info` mensaje -level, pero `console.error()` es un mensaje de `Error` -level.  

Para filtrar mensajes en la **consola,** use el **menú desplegable Nivel de** registro.  Puede alternar el estado de cada nivel.  Para desactivar cada nivel, quite la marca de verificación junto a cada uno.  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="El menú desplegable filtra los mensajes de consola mediante el nivel de registro" lightbox="../media/console-filter-dropdown.msft.png":::
    El menú desplegable filtra los **mensajes de** consola mediante el nivel de registro  
:::image-end:::  

Dado que no se aplica ningún filtro, la siguiente figura muestra decenas de mensajes.  A continuación, reduzca y administre el número de mensajes.  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Ningún conjunto de filtros significa que puede mostrar muchos mensajes de consola" lightbox="../media/console-filter-displays-all.msft.png":::
    Ningún conjunto de filtros significa que puede mostrar muchos mensajes de consola  
:::image-end:::  

Elija ocultar todos los mensajes de nivel de advertencia para reducir el ruido.  Vaya a la lista **desplegable Niveles de** registro y desactive el `Warnings` nivel.  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Ocultar todos los mensajes de nivel de advertencia en la consola para filtrar gran parte del ruido" lightbox="../media/console-filter-hide-warning.msft.png":::
    Ocultar todos los mensajes de nivel de advertencia en la **consola** para filtrar gran parte del ruido  
:::image-end:::  

## <a name="filter-by-text"></a>Filtrar por texto  

Si desea revisar más detalles, para filtrar mensajes con texto, escriba una cadena en el **cuadro de** texto Filtrar.  Por ejemplo, escriba en el cuadro para mostrar solo los mensajes sobre el `block` explorador que bloquea la carga de recursos.

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Muestra los mensajes que contienen el bloque de palabras" lightbox="../media/console-filter-text.msft.png":::
    Muestra los mensajes que contienen la palabra `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a>Filtrar por expresión regular

[Las expresiones regulares][MdnDocsWebJavascriptGuideRegularExpressions] son una forma eficaz de filtrar mensajes.  Por ejemplo, escriba en el cuadro de texto Filtrar para mostrar solo `/^Tracking/` los mensajes que empiezan por el término **** `Tracking` .  Si no está familiarizado con las expresiones regulares, [RegExr][|::ref1::|Main] es un gran recurso para aprender a usar expresiones regulares.

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Muestra los mensajes que comienzan con el filtro de palabras mediante una expresión regular en el cuadro de texto Filtro" lightbox="../media/console-filter-regex.msft.png":::
    Muestra los mensajes que comienzan con la palabra `filter` mediante una expresión regular en el cuadro de texto **Filtro**  
:::image-end:::  

## <a name="filter-by-message-source"></a>Filtrar por origen de mensaje  

También puede definir qué tipo de mensajes desea mostrar y dónde se originó cada uno con la **barra** lateral de la **consola**.  Para hacerlo, elija el botón **Mostrar barra lateral de la** consola.  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Para abrir la barra lateral, elija el icono Barra lateral" lightbox="../media/console-filter-sidebar-icon.msft.png":::
    Para abrir la **barra lateral,** elija el **botón Mostrar barra lateral de la** consola  
:::image-end:::  

Cuando la **barra lateral** está abierta, puede mostrar el número total de mensajes y dónde se originó cada uno.  Las opciones son `All messages` , , , , y `User Messages` `Errors` `Warnings` `Info` `Verbose` .  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="La barra lateral de consola muestra los diferentes orígenes de mensajes originados" lightbox="../media/console-filter-sidebar-open.msft.png":::
    La **barra lateral de** consola muestra los diferentes orígenes de mensajes originados  
:::image-end:::  

Elija cualquiera de las opciones para mostrar solo los mensajes de ese tipo.  Por ejemplo, para mostrar mensajes de usuario, elija la opción mensajes de usuario para mostrar menos ruido.

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Elegir mostrar solo mensajes de usuario en la consola mediante el filtro de la barra lateral" lightbox="../media/console-filter-select-user-messages.msft.png":::
    Elegir mostrar solo mensajes de usuario en la **consola** mediante el filtro de la barra **lateral**  
:::image-end:::  

Para filtrar más y expandir la opción, elija el icono de triángulo junto a él.  De este modo, se obtienen más opciones para mostrar solo los mensajes que proceden de un origen específico.  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Elegir el icono de flecha expande cada una de las secciones" lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    Elegir el icono de flecha expande cada una de las secciones  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Elegir cualquiera de las nuevas opciones para filtrar mediante el tipo y el origen" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    Elegir cualquiera de las nuevas opciones para filtrar mediante el tipo y el origen  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
