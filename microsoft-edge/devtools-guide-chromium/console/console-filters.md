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
# <a name="filter-console-messages"></a><span data-ttu-id="ce4d9-104">Filtrar mensajes de consola</span><span class="sxs-lookup"><span data-stu-id="ce4d9-104">Filter Console messages</span></span>  

<span data-ttu-id="ce4d9-105">Al navegar por la web, es posible que encuentre que **la consola** está inundada de todo tipo de información.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-105">When you surf the web, you may find the **Console** is flooded with all kinds of information.</span></span>  <span data-ttu-id="ce4d9-106">A menudo, la información no es relevante para usted.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-106">Often the information isn't relevant to you.</span></span>  <span data-ttu-id="ce4d9-107">Por ejemplo, información sobre el proyecto en directo que otro desarrollador registró durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-107">Such as information about the live project that another developer logged while you debug.</span></span>  <span data-ttu-id="ce4d9-108">O más información sobre infracciones y advertencias sobre el rendimiento del sitio actual que no puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-108">Or more information about violations and warnings about the performance of the current site that you aren't able to change.</span></span>  <span data-ttu-id="ce4d9-109">Tiene sentido usar las opciones de filtro de **La consola** para reducir el ruido.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-109">It makes sense to use the filter options of **Console** to reduce the noise.</span></span>  

## <a name="filter-by-log-level"></a><span data-ttu-id="ce4d9-110">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="ce4d9-110">Filter by log level</span></span>  

<span data-ttu-id="ce4d9-111">Cada método del `console` objeto tiene un nivel de gravedad asociado.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-111">Each method of the `console` object has a severity level attached to it.</span></span>  <span data-ttu-id="ce4d9-112">Los niveles de gravedad `Verbose` son , , o `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="ce4d9-112">The severity levels are `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="ce4d9-113">Muestra los niveles de gravedad en la [documentación de la API][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="ce4d9-113">Display the severity levels in the [API documentation][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="ce4d9-114">Por ejemplo, `console.log()` es un `Info` mensaje -level, pero `console.error()` es un mensaje de `Error` -level.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-114">For example, `console.log()` is an `Info`-level message, but `console.error()` is an `Error`-level message.</span></span>  

<span data-ttu-id="ce4d9-115">Para filtrar mensajes en la **consola,** use el **menú desplegable Nivel de** registro.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-115">To filter messages in the **Console**, use the **Log Level** dropdown menu.</span></span>  <span data-ttu-id="ce4d9-116">Puede alternar el estado de cada nivel.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-116">You may toggle the state of each level.</span></span>  <span data-ttu-id="ce4d9-117">Para desactivar cada nivel, quite la marca de verificación junto a cada uno.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-117">To turn off each level, remove the checkmark next to each.</span></span>  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="El menú desplegable filtra los mensajes de consola mediante el nivel de registro" lightbox="../media/console-filter-dropdown.msft.png":::
    <span data-ttu-id="ce4d9-119">El menú desplegable filtra los **mensajes de** consola mediante el nivel de registro</span><span class="sxs-lookup"><span data-stu-id="ce4d9-119">The dropdown menu filters **Console** messages using the log level</span></span>  
:::image-end:::  

<span data-ttu-id="ce4d9-120">Dado que no se aplica ningún filtro, la siguiente figura muestra decenas de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-120">Since no filter is applied, the following figure displays dozens of messages.</span></span>  <span data-ttu-id="ce4d9-121">A continuación, reduzca y administre el número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-121">Next, reduce and manage the number of messages.</span></span>  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Ningún conjunto de filtros significa que puede mostrar muchos mensajes de consola" lightbox="../media/console-filter-displays-all.msft.png":::
    <span data-ttu-id="ce4d9-123">Ningún conjunto de filtros significa que puede mostrar muchos mensajes de consola</span><span class="sxs-lookup"><span data-stu-id="ce4d9-123">No filter set means you may display many console messages</span></span>  
:::image-end:::  

<span data-ttu-id="ce4d9-124">Elija ocultar todos los mensajes de nivel de advertencia para reducir el ruido.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-124">Choose to hide all the Warning-level messages to cut down on the noise.</span></span>  <span data-ttu-id="ce4d9-125">Vaya a la lista **desplegable Niveles de** registro y desactive el `Warnings` nivel.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-125">Navigate to the **Log Levels** dropdown and uncheck the `Warnings` level.</span></span>  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Ocultar todos los mensajes de nivel de advertencia en la consola para filtrar gran parte del ruido" lightbox="../media/console-filter-hide-warning.msft.png":::
    <span data-ttu-id="ce4d9-127">Ocultar todos los mensajes de nivel de advertencia en la **consola** para filtrar gran parte del ruido</span><span class="sxs-lookup"><span data-stu-id="ce4d9-127">Hide all the warning level messages in the **Console** to filter much of the noise</span></span>  
:::image-end:::  

## <a name="filter-by-text"></a><span data-ttu-id="ce4d9-128">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="ce4d9-128">Filter by text</span></span>  

<span data-ttu-id="ce4d9-129">Si desea revisar más detalles, para filtrar mensajes con texto, escriba una cadena en el **cuadro de** texto Filtrar.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-129">If you want to review more detail, to filter messages using text, type a string into the **Filter** textbox.</span></span>  <span data-ttu-id="ce4d9-130">Por ejemplo, escriba en el cuadro para mostrar solo los mensajes sobre el `block` explorador que bloquea la carga de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-130">For example, type `block` into the box to only display your messages about the browser blocking resources from loading.</span></span>

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Muestra los mensajes que contienen el bloque de palabras" lightbox="../media/console-filter-text.msft.png":::
    <span data-ttu-id="ce4d9-132">Muestra los mensajes que contienen la palabra</span><span class="sxs-lookup"><span data-stu-id="ce4d9-132">Displays the messages that contain the word</span></span> `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a><span data-ttu-id="ce4d9-133">Filtrar por expresión regular</span><span class="sxs-lookup"><span data-stu-id="ce4d9-133">Filter by regular expression</span></span>

<span data-ttu-id="ce4d9-134">[Las expresiones regulares][MdnDocsWebJavascriptGuideRegularExpressions] son una forma eficaz de filtrar mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-134">[Regular expressions][MdnDocsWebJavascriptGuideRegularExpressions] are a powerful way to filter messages.</span></span>  <span data-ttu-id="ce4d9-135">Por ejemplo, escriba en el cuadro de texto Filtrar para mostrar solo `/^Tracking/` los mensajes que empiezan por el término \*\*\*\* `Tracking` .</span><span class="sxs-lookup"><span data-stu-id="ce4d9-135">For example, type `/^Tracking/` into the **Filter** textbox to only displays messages that start with the term `Tracking`.</span></span>  <span data-ttu-id="ce4d9-136">Si no está familiarizado con las expresiones regulares, [RegExr][|::ref1::|Main] es un gran recurso para aprender a usar expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-136">If you're unfamiliar with regular expressions, [RegExr][|::ref1::|Main] is a great resource to learn about using regular expressions.</span></span>

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Muestra los mensajes que comienzan con el filtro de palabras mediante una expresión regular en el cuadro de texto Filtro" lightbox="../media/console-filter-regex.msft.png":::
    <span data-ttu-id="ce4d9-138">Muestra los mensajes que comienzan con la palabra `filter` mediante una expresión regular en el cuadro de texto **Filtro**</span><span class="sxs-lookup"><span data-stu-id="ce4d9-138">Displays the messages that start with the word `filter` using a regular expression in the **Filter** textbox</span></span>  
:::image-end:::  

## <a name="filter-by-message-source"></a><span data-ttu-id="ce4d9-139">Filtrar por origen de mensaje</span><span class="sxs-lookup"><span data-stu-id="ce4d9-139">Filter by message source</span></span>  

<span data-ttu-id="ce4d9-140">También puede definir qué tipo de mensajes desea mostrar y dónde se originó cada uno con la **barra** lateral de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-140">You may also define what kind of messages you want to display and where each originated using the **Sidebar** of the **Console**.</span></span>  <span data-ttu-id="ce4d9-141">Para hacerlo, elija el botón **Mostrar barra lateral de la** consola.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-141">To do it, choose the **Show console sidebar** button.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Para abrir la barra lateral, elija el icono Barra lateral" lightbox="../media/console-filter-sidebar-icon.msft.png":::
    <span data-ttu-id="ce4d9-143">Para abrir la **barra lateral,** elija el **botón Mostrar barra lateral de la** consola</span><span class="sxs-lookup"><span data-stu-id="ce4d9-143">To open the **Sidebar**, choose the **Show console sidebar** button</span></span>  
:::image-end:::  

<span data-ttu-id="ce4d9-144">Cuando la **barra lateral** está abierta, puede mostrar el número total de mensajes y dónde se originó cada uno.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-144">When the **Sidebar** is open, you may display the overall number of messages and where each originated.</span></span>  <span data-ttu-id="ce4d9-145">Las opciones son `All messages` , , , , y `User Messages` `Errors` `Warnings` `Info` `Verbose` .</span><span class="sxs-lookup"><span data-stu-id="ce4d9-145">The options are `All messages`, `User Messages`, `Errors`, `Warnings`, `Info`, and `Verbose`.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="La barra lateral de consola muestra los diferentes orígenes de mensajes originados" lightbox="../media/console-filter-sidebar-open.msft.png":::
    <span data-ttu-id="ce4d9-147">La **barra lateral de** consola muestra los diferentes orígenes de mensajes originados</span><span class="sxs-lookup"><span data-stu-id="ce4d9-147">The **Console Sidebar** displays the different sources messages originated from</span></span>  
:::image-end:::  

<span data-ttu-id="ce4d9-148">Elija cualquiera de las opciones para mostrar solo los mensajes de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-148">Choose any of the options to display only the messages of that type.</span></span>  <span data-ttu-id="ce4d9-149">Por ejemplo, para mostrar mensajes de usuario, elija la opción mensajes de usuario para mostrar menos ruido.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-149">For example, to display user messages, choose the user messages option to display less noise.</span></span>

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Elegir mostrar solo mensajes de usuario en la consola mediante el filtro de la barra lateral" lightbox="../media/console-filter-select-user-messages.msft.png":::
    <span data-ttu-id="ce4d9-151">Elegir mostrar solo mensajes de usuario en la **consola** mediante el filtro de la barra **lateral**</span><span class="sxs-lookup"><span data-stu-id="ce4d9-151">Choose to display only user messages in the **Console** using the filter in the **Sidebar**</span></span>  
:::image-end:::  

<span data-ttu-id="ce4d9-152">Para filtrar más y expandir la opción, elija el icono de triángulo junto a él.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-152">To filter more and expand the choice, choose the triangle icon next to it.</span></span>  <span data-ttu-id="ce4d9-153">De este modo, se obtienen más opciones para mostrar solo los mensajes que proceden de un origen específico.</span><span class="sxs-lookup"><span data-stu-id="ce4d9-153">That way you get more choices to display only messages that originate from a specific source.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Elegir el icono de flecha expande cada una de las secciones" lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    <span data-ttu-id="ce4d9-155">Elegir el icono de flecha expande cada una de las secciones</span><span class="sxs-lookup"><span data-stu-id="ce4d9-155">Choose the arrow icon expands each of the sections</span></span>  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Elegir cualquiera de las nuevas opciones para filtrar mediante el tipo y el origen" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    <span data-ttu-id="ce4d9-157">Elegir cualquiera de las nuevas opciones para filtrar mediante el tipo y el origen</span><span class="sxs-lookup"><span data-stu-id="ce4d9-157">Choose any of the new options to filter using type and source</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ce4d9-158">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ce4d9-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
