---
description: Si te encuentras escribiendo las mismas expresiones de JavaScript en la consola repetidamente, prueba Live Expressions en su lugar.
title: Ver valores de expresión de JavaScript en tiempo real con live expressions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 51b7aa5119775f43861a84c1055ac9149a626d8a
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483159"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a><span data-ttu-id="4e83d-104">Supervisar los cambios en JavaScript mediante expresiones live</span><span class="sxs-lookup"><span data-stu-id="4e83d-104">Monitor changes in JavaScript using Live Expressions</span></span>  

<span data-ttu-id="4e83d-105">**Las expresiones live** son una excelente manera de supervisar expresiones de JavaScript que cambian mucho.</span><span class="sxs-lookup"><span data-stu-id="4e83d-105">**Live Expressions** are an excellent way to monitor JavaScript expressions that change a lot.</span></span>    <span data-ttu-id="4e83d-106">En lugar de tener muchos mensajes de consola para leer y navegar, puede anclar las expresiones de JavaScript específicas a la parte superior de la **consola**.</span><span class="sxs-lookup"><span data-stu-id="4e83d-106">Instead of having many Console messages to read and navigate, you may pin your specific JavaScript expressions to the top of the **Console**.</span></span>  

## <a name="add-a-new-live-expression"></a><span data-ttu-id="4e83d-107">Agregar una nueva expresión en directo</span><span class="sxs-lookup"><span data-stu-id="4e83d-107">Add a new live expression</span></span>  

<span data-ttu-id="4e83d-108">Para empezar, elija el **botón Crear expresión en** directo \(eye\) junto al cuadro de texto **Filter.**</span><span class="sxs-lookup"><span data-stu-id="4e83d-108">To start, choose the **Create live expression** \(eye\) button next to the **Filter** textbox.</span></span>  <span data-ttu-id="4e83d-109">Después de elegirlo, se muestra un cuadro de texto para que escriba la nueva expresión en él.</span><span class="sxs-lookup"><span data-stu-id="4e83d-109">After you choose it, a textbox is displayed for you to enter your new expression in it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Elija el botón Nueva expresión en directo para abrir un cuadro de texto para escribir una expresión" lightbox="../media/console-live-expressions-new.msft.png":::
    <span data-ttu-id="4e83d-111">Elija el `New live expression` botón para abrir un cuadro de texto para escribir una expresión</span><span class="sxs-lookup"><span data-stu-id="4e83d-111">Choose the `New live expression` button to open a textbox to type an expression</span></span>  
:::image-end:::  

<span data-ttu-id="4e83d-112">**Las expresiones live** pueden ser cualquier expresión válida de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e83d-112">**Live Expressions** may be any valid JavaScript expression.</span></span>  <span data-ttu-id="4e83d-113">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4e83d-113">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="4e83d-114">Abra el **cuadro de texto Expresión** en directo.</span><span class="sxs-lookup"><span data-stu-id="4e83d-114">Open the **Live Expression** textbox.</span></span>  
1.  <span data-ttu-id="4e83d-115">Escriba `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="4e83d-115">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="4e83d-116">Para guardar la expresión, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4e83d-116">To save the expression, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="4e83d-117">Seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="4e83d-117">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    *   <span data-ttu-id="4e83d-118">Elija fuera del **cuadro de texto Expresión** en directo.</span><span class="sxs-lookup"><span data-stu-id="4e83d-118">Choose outside the **Live Expression** textbox.</span></span>  
        
<span data-ttu-id="4e83d-119">La expresión ahora está en directo y se `body` muestra como resultado.</span><span class="sxs-lookup"><span data-stu-id="4e83d-119">The expression is now live and displays `body` as the result.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="La expresión activa de document.activeElement muestra el cuerpo como resultado" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    <span data-ttu-id="4e83d-121">Expresión en directo para `document.activeElement` muestra el cuerpo como resultado</span><span class="sxs-lookup"><span data-stu-id="4e83d-121">Live expression for `document.activeElement` displays body as the result</span></span>  
:::image-end:::  

<span data-ttu-id="4e83d-122">Si navega por la página web, el valor cambia.</span><span class="sxs-lookup"><span data-stu-id="4e83d-122">If you navigate around the webpage, the value changes.</span></span>  <span data-ttu-id="4e83d-123">Por ejemplo, en la siguiente figura se abre el menú de búsqueda en la página web y la expresión se muestra `button.nav-bar-button.focus-visible` ahora como el valor.</span><span class="sxs-lookup"><span data-stu-id="4e83d-123">For example, in the following figure you open the search menu in the webpage and the expression now displays `button.nav-bar-button.focus-visible` as the value.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Para cambiar el valor de live expression, interactúe con diferentes elementos de la página web" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    <span data-ttu-id="4e83d-125">Para cambiar el valor de **live expression**, interactúe con diferentes elementos de la página web</span><span class="sxs-lookup"><span data-stu-id="4e83d-125">To change the value of the **Live Expression**, interact with different elements on the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="4e83d-126">Para volver a cambiar el valor, abra y elija el cuadro de texto Buscar en la página web.</span><span class="sxs-lookup"><span data-stu-id="4e83d-126">To change the value again, open and choose the Search textbox on the webpage.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Navegue a otro elemento de la página web para actualizar live expression" lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    <span data-ttu-id="4e83d-128">Navegue a otro elemento de la página web para actualizar **live expression**</span><span class="sxs-lookup"><span data-stu-id="4e83d-128">Navigate to a different element in the webpage to update the **Live Expression**</span></span>  
:::image-end:::  

## <a name="remove-live-expressions"></a><span data-ttu-id="4e83d-129">Quitar expresiones en directo</span><span class="sxs-lookup"><span data-stu-id="4e83d-129">Remove Live Expressions</span></span>  

<span data-ttu-id="4e83d-130">Una **expresión activa** está disponible siempre que la mantenga activa.</span><span class="sxs-lookup"><span data-stu-id="4e83d-130">A **Live Expression** is available as long as you keep it active.</span></span>  <span data-ttu-id="4e83d-131">Para deshacerse de **una expresión live,** elija la `x` siguiente.</span><span class="sxs-lookup"><span data-stu-id="4e83d-131">To get rid of a **Live Expression**, choose the `x` next to it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Para quitar live expressions, elija la x junto a ella" lightbox="../media/console-live-expressions-remove.msft.png":::
    <span data-ttu-id="4e83d-133">Para quitar **expresiones en directo,** elija la `x` siguiente.</span><span class="sxs-lookup"><span data-stu-id="4e83d-133">To remove **Live Expressions**, choose the `x` next to it</span></span>  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a><span data-ttu-id="4e83d-134">Reemplazar el registro de consola por expresiones en directo</span><span class="sxs-lookup"><span data-stu-id="4e83d-134">Replace Console logging with Live Expressions</span></span>  

<span data-ttu-id="4e83d-135">Puedes crear tantas expresiones como quieras y conservar cada una de las sesiones y ventanas del explorador.</span><span class="sxs-lookup"><span data-stu-id="4e83d-135">You may create as many expressions as you want and persist each across browser sessions and windows.</span></span>  <span data-ttu-id="4e83d-136">**Las expresiones live** son una forma de reducir el ruido en el flujo de trabajo de depuración.</span><span class="sxs-lookup"><span data-stu-id="4e83d-136">**Live Expressions** are a way to cut down on noise in your debugging workflow.</span></span>  

<span data-ttu-id="4e83d-137">Por ejemplo, desea supervisar el movimiento del mouse en la página web actual.</span><span class="sxs-lookup"><span data-stu-id="4e83d-137">For example, you want to monitor the mouse movement in the current webpage.</span></span>  <span data-ttu-id="4e83d-138">Navegue a [la demostración movimiento][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]del mouse de registro, abra **la consola**y mueva el mouse alrededor para mostrar los registros con mucha información.</span><span class="sxs-lookup"><span data-stu-id="4e83d-138">Navigate to [Logging Mouse Movement demo][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml], open the **Console**, and move your mouse around to display the logs with a lot of information.</span></span>  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="La consola muestra mucha información sobre la posición del mouse" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    <span data-ttu-id="4e83d-140">**La** consola muestra mucha información sobre la posición del mouse</span><span class="sxs-lookup"><span data-stu-id="4e83d-140">**Console** displays much information on mouse position</span></span>  
:::image-end:::  

<span data-ttu-id="4e83d-141">La gran cantidad de información no solo ralentiza el proceso de depuración, sino que también facilita la pérdida de los cambios que desea revisar.</span><span class="sxs-lookup"><span data-stu-id="4e83d-141">The large amount of information not only slows your debug process, but also makes it easy to miss the changes you want to review.</span></span>  <span data-ttu-id="4e83d-142">A medida **que la consola** muestra más mensajes y mueve el mouse, los valores que desea revisar se desplazan fuera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4e83d-142">As the **Console** displays more messages and you move your mouse, the values you want to review scroll off the screen.</span></span>  

<span data-ttu-id="4e83d-143">Para probar **Live Expressions** como alternativa, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4e83d-143">To try **Live Expressions** as an alternative, complete the following actions.</span></span>  

1.  <span data-ttu-id="4e83d-144">Vaya al movimiento [mouse sin la demostración de registro][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].</span><span class="sxs-lookup"><span data-stu-id="4e83d-144">Navigate to the [Mouse movement without logging demo][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].</span></span>  
1.  <span data-ttu-id="4e83d-145">Crear **expresiones en directo** para y `x` `y` .</span><span class="sxs-lookup"><span data-stu-id="4e83d-145">Create **Live Expressions** for `x` and `y`.</span></span>  
    
<span data-ttu-id="4e83d-146">Cuando se usan **expresiones**en directo, siempre se obtiene la \*\*\*\* información en la misma parte de la pantalla y se mantienen los registros de consola para valores que no cambian tanto.</span><span class="sxs-lookup"><span data-stu-id="4e83d-146">When you use **Live Expressions**, you always get the information on the same part of your screen and keep **Console** logs for values that don't change as much.</span></span>

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Mostrar la posición x e y del mouse como expresiones vivas" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    <span data-ttu-id="4e83d-148">Mostrar la `x` posición y el mouse como `y` **expresiones vivas**</span><span class="sxs-lookup"><span data-stu-id="4e83d-148">Display the `x` and `y` position of the mouse as **Live Expressions**</span></span>  
:::image-end:::  

<span data-ttu-id="4e83d-149">**Las expresiones live** se ejecutan exclusivamente en el equipo y no es necesario cambiar nada en el código para mostrar.</span><span class="sxs-lookup"><span data-stu-id="4e83d-149">**Live Expressions** run exclusively on your computer and you don't need to change anything in your code to display.</span></span>  <span data-ttu-id="4e83d-150">**Las expresiones en** directo son una excelente manera de asegurarse de que solo se muestra la información que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="4e83d-150">**Live Expressions** are a great way to ensure that you only display the information you want to debug.</span></span>  <span data-ttu-id="4e83d-151">Además, **live expressions** te ayudan a limitar el ruido en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="4e83d-151">Also, **Live Expressions** help you limit the noise on your users' computers.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4e83d-152">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4e83d-152">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Ejemplos de mensajes de consola: Uso de tablas | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Movimiento del mouse sin registro | GitHub"  
