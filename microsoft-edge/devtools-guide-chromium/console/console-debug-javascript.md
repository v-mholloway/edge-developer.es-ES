---
description: Las herramientas de desarrollo notifican errores de JavaScript y depuran cada uno en la consola
title: Seguimiento de errores con la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: ebd12f8932332b3e63162ab6952577bdb43bbccd
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483658"
---
# <a name="debug-errors-reported-in-console"></a><span data-ttu-id="7da58-104">Errores de depuración notificados en la consola</span><span class="sxs-lookup"><span data-stu-id="7da58-104">Debug errors reported in Console</span></span>  

<span data-ttu-id="7da58-105">La primera experiencia que tiene con **la consola es** probablemente un error en un script.</span><span class="sxs-lookup"><span data-stu-id="7da58-105">The first experience you have with the **Console** is probably an error in a script.</span></span>  <span data-ttu-id="7da58-106">Para probarlo, vaya a [Error de JavaScript notificado en la herramienta consola][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].</span><span class="sxs-lookup"><span data-stu-id="7da58-106">To try it, navigate to [JavaScript error reported in the Console tool][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].</span></span>  

<span data-ttu-id="7da58-107">Si abre DevTools en el explorador, un botón de la parte superior derecha muestra un error para la página web.</span><span class="sxs-lookup"><span data-stu-id="7da58-107">If you open DevTools in the browser, a button on the top right displays an error for the webpage.</span></span>  
<span data-ttu-id="7da58-108">Elija el botón para llevarle a la **consola** y darle más información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="7da58-108">Choose the button to take you to the **Console** and give you more information about the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools proporciona información detallada sobre el error en la consola" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="7da58-110">DevTools proporciona información detallada sobre el error en la **consola**</span><span class="sxs-lookup"><span data-stu-id="7da58-110">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="7da58-111">A partir de la información, puede recopilar que el error está en la línea 16 del `error.html` archivo.</span><span class="sxs-lookup"><span data-stu-id="7da58-111">From the information, you may gather that the error is on line 16 of the `error.html` file.</span></span>  <span data-ttu-id="7da58-112">Si elige el vínculo a la derecha de la consola, le llevará a la herramienta Orígenes y resaltará la `error.html:16` línea de código con el error. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7da58-112">If you choose the `error.html:16` link on the right of the **Console**, it takes you to the **Sources** tool and highlights the line of code with the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="La herramienta Orígenes resalta la línea de código que provoca el error" lightbox="../media/console-debug-displays-in-sources.msft.png":::
   <span data-ttu-id="7da58-114">La **herramienta Orígenes** resalta la línea de código que provoca el error</span><span class="sxs-lookup"><span data-stu-id="7da58-114">The **Sources** tool highlights the line of code that causes the error</span></span>  
:::image-end:::  

<span data-ttu-id="7da58-115">El script intenta obtener el primer `h2` elemento del documento y pintar un borde rojo alrededor de él.</span><span class="sxs-lookup"><span data-stu-id="7da58-115">The script tries to get the first `h2` element in the document and paint a red border around it.</span></span>  <span data-ttu-id="7da58-116">Pero no `h2` existe ningún elemento, por lo que se produce un error en el script.</span><span class="sxs-lookup"><span data-stu-id="7da58-116">But no `h2` element exists, so the script fails.</span></span>  

## <a name="find-and-debug-network-issues"></a><span data-ttu-id="7da58-117">Buscar y depurar problemas de red</span><span class="sxs-lookup"><span data-stu-id="7da58-117">Find and debug network issues</span></span>  

<span data-ttu-id="7da58-118">Otros errores que los informes **de consola** son errores de red.</span><span class="sxs-lookup"><span data-stu-id="7da58-118">Other errors that the **Console** reports are network errors.</span></span>  <span data-ttu-id="7da58-119">Para mostrarlo en acción, vaya al [error de red notificado en consola][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].</span><span class="sxs-lookup"><span data-stu-id="7da58-119">To display it in action, navigate to the [Network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="La consola muestra una red y un error de JavaScript" lightbox="../media/console-debug-network-error.msft.png":::
   <span data-ttu-id="7da58-121">**La** consola muestra una red y un error de JavaScript</span><span class="sxs-lookup"><span data-stu-id="7da58-121">**Console** displays a Network and a JavaScript error</span></span>  
:::image-end:::  

<span data-ttu-id="7da58-122">La tabla muestra , pero nada cambia en la página `loading` web porque los datos nunca se recuperan.</span><span class="sxs-lookup"><span data-stu-id="7da58-122">The table displays `loading`, but nothing changes on the webpage because the data is never retrieved.</span></span>  <span data-ttu-id="7da58-123">En la **consola,** se produjeron los dos errores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7da58-123">In the **Console**, the following two errors occurred.</span></span>  

*   <span data-ttu-id="7da58-124">Error de red que comienza con el `GET` método HTTP seguido de un URI.</span><span class="sxs-lookup"><span data-stu-id="7da58-124">A network error that starts with `GET` HTTP method followed by a URI.</span></span>  
*   <span data-ttu-id="7da58-125">`Uncaught (in promise) TypeError: data.forEach is not a function`Error.</span><span class="sxs-lookup"><span data-stu-id="7da58-125">An `Uncaught (in promise) TypeError: data.forEach is not a function` error.</span></span>  
    
<span data-ttu-id="7da58-126">Si elige el vínculo `network-error.html:40` en la **consola**, DevTools le llevará a la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="7da58-126">If you choose the `network-error.html:40` link in the **Console**, DevTools takes you to the **Sources** tool.</span></span>  <span data-ttu-id="7da58-127">La línea de código problemática está resaltada y seguida de un `error` botón \( `x` \).</span><span class="sxs-lookup"><span data-stu-id="7da58-127">The problematic line of code is highlighted and followed by an `error` \(`x`\) button.</span></span>  <span data-ttu-id="7da58-128">Para mostrar el `Failed to load resource: the server responded with a status of 404 ()` mensaje de error, elija el **botón error** \( `x` \).</span><span class="sxs-lookup"><span data-stu-id="7da58-128">To display the `Failed to load resource: the server responded with a status of 404 ()` error message, choose the **error** \(`x`\) button.</span></span>  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Elegir el vínculo a la página web y el código donde se produce el error se abre la herramienta Orígenes" lightbox="../media/console-debug-network-error-code-line.msft.png":::
         <span data-ttu-id="7da58-130">Elegir el vínculo a la página web y el código donde se produce el error se abre la **herramienta** Orígenes</span><span class="sxs-lookup"><span data-stu-id="7da58-130">Choose the link to the webpage and code where the error occurs line opens the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Para encontrar el error en JavaScript, use la herramienta Orígenes" lightbox="../media/console-debug-network-error-sources.msft.png":::
         <span data-ttu-id="7da58-132">Para encontrar el error en JavaScript, use la **herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="7da58-132">To find the error in JavaScript, use the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="7da58-133">En el ejemplo, el error le informa de que no se encuentra la dirección URL solicitada.</span><span class="sxs-lookup"><span data-stu-id="7da58-133">In the example, the error informs you that the requested URL isn't found.</span></span>  <span data-ttu-id="7da58-134">Después, complete las siguientes acciones para abrir la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="7da58-134">Next, complete the following actions to open the **Network** tool.</span></span>  

1.  <span data-ttu-id="7da58-135">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="7da58-135">Open the **Console**.</span></span>  
1.  <span data-ttu-id="7da58-136">Elija el URI asociado al error.</span><span class="sxs-lookup"><span data-stu-id="7da58-136">Choose the URI associated with the error.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="La consola muestra un código de estado HTTP del error después de no cargar un recurso" lightbox="../media/console-debug-network-error-url.msft.png":::
   <span data-ttu-id="7da58-138">**La** consola muestra un código de estado HTTP del error después de no cargar un recurso</span><span class="sxs-lookup"><span data-stu-id="7da58-138">**Console** displays an HTTP status code of the error after a resource isn't loaded</span></span>  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="La herramienta Red muestra más información sobre la solicitud con errores" lightbox="../media/console-debug-network-error-network.msft.png":::
           <span data-ttu-id="7da58-140">La **herramienta Red** muestra más información sobre la solicitud con errores</span><span class="sxs-lookup"><span data-stu-id="7da58-140">The **Network** tool displays more information about the failed request</span></span>  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="Inspeccionar los encabezados de la herramienta Red puede dar más información" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           <span data-ttu-id="7da58-142">Inspeccionar los encabezados de la **herramienta Red** puede dar más información</span><span class="sxs-lookup"><span data-stu-id="7da58-142">Inspect the headers in the **Network** tool may give more insight</span></span>  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="7da58-143">¿Cuál fue el problema?</span><span class="sxs-lookup"><span data-stu-id="7da58-143">What was the problem?</span></span>  <span data-ttu-id="7da58-144">Dos caracteres de barra diagonal `//` \( \) se producen en el URI solicitado después de la palabra `repos` .</span><span class="sxs-lookup"><span data-stu-id="7da58-144">Two slash characters \(`//`\) occur in the requested URI after the word `repos`.</span></span>  <span data-ttu-id="7da58-145">Abra la **herramienta Orígenes** e inspeccione la línea 26.</span><span class="sxs-lookup"><span data-stu-id="7da58-145">Open the **Sources** tool and inspect line 26.</span></span>  <span data-ttu-id="7da58-146">Un carácter de barra diagonal final \( `/` \) se produce al final del URI base.</span><span class="sxs-lookup"><span data-stu-id="7da58-146">A trailing slash character \(`/`\) occurs at the end of the base URI.</span></span>  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="La herramienta Orígenes muestra la línea de código con el error" lightbox="../media/console-debug-network-error-code-error.msft.png":::
   <span data-ttu-id="7da58-148">La **herramienta Orígenes** muestra la línea de código con el error</span><span class="sxs-lookup"><span data-stu-id="7da58-148">The **Sources** tool displays the line of code with the error</span></span>  
:::image-end:::  

<span data-ttu-id="7da58-149">Para revisar ningún error en la **consola,** vaya a [Error de red fijo notificado en consola][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span><span class="sxs-lookup"><span data-stu-id="7da58-149">To review no errors in the **Console**, navigate to [Fixed network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="El ejemplo sin errores carga información de GitHub y la muestra" lightbox="../media/console-debug-network-error-fixed.msft.png":::
   <span data-ttu-id="7da58-151">El ejemplo sin errores carga información de GitHub y la muestra</span><span class="sxs-lookup"><span data-stu-id="7da58-151">The example without any errors loads information from GitHub and displays it</span></span>  
:::image-end:::  

<span data-ttu-id="7da58-152">Asegúrese de proporcionar técnicas de codificación defensivas para evitar las experiencias anteriores del usuario.</span><span class="sxs-lookup"><span data-stu-id="7da58-152">Ensure you provide defensive coding techniques to avoid the previous user experiences.</span></span>  <span data-ttu-id="7da58-153">Además, asegúrate de que el código detecta errores y muestra cada uno en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="7da58-153">Also, ensure your code catches errors and display each in the **Console**.</span></span>  <span data-ttu-id="7da58-154">Vaya a [Informes de errores de red en consola e interfaz de][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] usuario y revise los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="7da58-154">Navigate to [Network error reporting in Console and UI][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] and review the following items.</span></span>  

*   <span data-ttu-id="7da58-155">Proporcionar interfaz de usuario al usuario que algo salió mal.</span><span class="sxs-lookup"><span data-stu-id="7da58-155">Provide UI to the user that something went wrong.</span></span>  
*   <span data-ttu-id="7da58-156">En la **consola,** proporcione información útil sobre el error de red del código.</span><span class="sxs-lookup"><span data-stu-id="7da58-156">In the **Console**, provide helpful information about the Network error from your code.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Un ejemplo que detecta e informa de errores" lightbox="../media/console-debug-network-error-report.msft.png":::
   <span data-ttu-id="7da58-158">Un ejemplo que detecta e informa de errores</span><span class="sxs-lookup"><span data-stu-id="7da58-158">An example that catches and reports errors</span></span>  
:::image-end:::  

<span data-ttu-id="7da58-159">El siguiente fragmento de código detecta e informa de errores mediante el `handleErrors` método, específicamente la `throw Error` línea.</span><span class="sxs-lookup"><span data-stu-id="7da58-159">The following code snippet catches and reports errors using the `handleErrors` method, specifically the `throw Error` line.</span></span>  

```javascript
const handleErrors = (response) => {
    if (!response.ok) {
        let message = 'Could not load the information'
        document.querySelector('tbody').innerHTML = `
        <tr><td colspan=3>Error ${message}</td></tr>
        `;
        throw Error(response.status + ' ' + response.statusText);
    }
    return response;
};
```  

## <a name="create-errors-and-traces-in-the-console"></a><span data-ttu-id="7da58-160">Crear errores y seguimientos en la consola</span><span class="sxs-lookup"><span data-stu-id="7da58-160">Create errors and traces in the Console</span></span>

<span data-ttu-id="7da58-161">Además del ejemplo de la sección anterior, también puede crear diferentes errores y problemas de `throw Error` seguimiento en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="7da58-161">Besides the `throw Error` example in the previous section, you may also create different errors and trace problems in the **Console**.</span></span>  
<span data-ttu-id="7da58-162">Para mostrar dos mensajes de error creados en la **consola,** vaya a Crear informes [de error y aserciones en consola][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].</span><span class="sxs-lookup"><span data-stu-id="7da58-162">To display two created error messages in the **Console**, navigate to [Creating error reports and assertions in Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].</span></span>  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Mensajes de error creados desde la consola" lightbox="../media/console-debug-error-assert.msft.png":::
   <span data-ttu-id="7da58-164">Mensajes de error creados desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="7da58-164">Error messages created from **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="7da58-165">El siguiente fragmento de código se usó en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="7da58-165">The following code snippet was used in the previous example.</span></span>  

```javascript
function first(name) { second(name); }
function second(name) { third(name); }
function third(name) {
    if (!name) {
        console.error(`Name isn't defined :(`)
    } else {
        console.assert(
            name.length <= 8, 
            `"${name} is not less than eight letters"`
        );
    }
}
first();
first('Console');
first('Microsoft Edge Canary');
```  

<span data-ttu-id="7da58-166">Tiene tres funciones que se solicitan mutuamente sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7da58-166">You have three functions that request each other in succession.</span></span>  

*   `first()`  
*   `second()`  
*   `third()`  
    
<span data-ttu-id="7da58-167">Cada uno envía un `name` argumento al otro.</span><span class="sxs-lookup"><span data-stu-id="7da58-167">Each sends a `name` argument to the other.</span></span>  <span data-ttu-id="7da58-168">En la función, se comprueba si el argumento existe y, si no lo hace, se registra un error que no `third()` `name` se define ese nombre.</span><span class="sxs-lookup"><span data-stu-id="7da58-168">In the `third()` function, you check if the `name` argument exists and if it doesn't, you log an error that name isn't defined.</span></span>  <span data-ttu-id="7da58-169">Si `name` está definido, se usa el método para comprobar si el argumento tiene menos de ocho letras de `assert()` `name` longitud.</span><span class="sxs-lookup"><span data-stu-id="7da58-169">If `name` is defined, you use the `assert()` method to check if the `name` argument is fewer than eight letters long.</span></span>  <span data-ttu-id="7da58-170">La función se `first()` solicita tres veces, con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7da58-170">You request the `first()` function three times, with the following parameters.</span></span>  

*   <span data-ttu-id="7da58-171">Ningún argumento que desencadena `console.error()` el método en la `third()` función.</span><span class="sxs-lookup"><span data-stu-id="7da58-171">No argument that triggers the `console.error()` method in the `third()` function.</span></span>  
*   <span data-ttu-id="7da58-172">El término como parámetro de la función no provoca un error porque el argumento existe y `Console` es inferior a ocho `first()` `name` letras.</span><span class="sxs-lookup"><span data-stu-id="7da58-172">The term `Console` as a parameter to the `first()` function doesn't cause an error because `name` argument exists and is shorter than eight letters.</span></span>  
*   <span data-ttu-id="7da58-173">La frase como parámetro para funcionar hace que el método informe de un error, ya que `Microsoft Edge Canary` el parámetro tiene más de ocho `first()` `console.assert()` letras.</span><span class="sxs-lookup"><span data-stu-id="7da58-173">The phrase `Microsoft Edge Canary` as a parameter to `first()` function causes the `console.assert()` method to report an error, because the parameter is longer than eight letters.</span></span>  
    
<span data-ttu-id="7da58-174">Use el `console.assert()` método para crear informes de errores condicionales.</span><span class="sxs-lookup"><span data-stu-id="7da58-174">Use the `console.assert()` method to create conditional error reports.</span></span>  <span data-ttu-id="7da58-175">Los dos ejemplos siguientes tienen el mismo resultado, pero se necesita una instrucción `if{}` adicional.</span><span class="sxs-lookup"><span data-stu-id="7da58-175">The following two examples have the same result, but one needs an extra `if{}` statement.</span></span>  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> <span data-ttu-id="7da58-176">La segunda y tercera líneas del código realizan la misma prueba.</span><span class="sxs-lookup"><span data-stu-id="7da58-176">The second and third lines of the code perform the same test.</span></span>  <span data-ttu-id="7da58-177">Dado que la aserción debe registrar un resultado negativo, debe probar en `x < 40` el caso y para la `if` `x >= 40` aserción.</span><span class="sxs-lookup"><span data-stu-id="7da58-177">Because the assertion needs to record a negative result, you test for `x < 40` in the `if` case and `x >= 40` for the assertion.</span></span>  

<span data-ttu-id="7da58-178">Si no está seguro de qué función solicita otra función, use el método para realizar un seguimiento de las funciones que se solicitan para llegar a `console.trace()` la función actual.</span><span class="sxs-lookup"><span data-stu-id="7da58-178">If you aren't sure which function requests another function, use the `console.trace()` method to track which functions are requested to get to the current one.</span></span>  <span data-ttu-id="7da58-179">Para mostrar el seguimiento en la **consola,** vaya [a Crear seguimientos en consola][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].</span><span class="sxs-lookup"><span data-stu-id="7da58-179">To display the trace in the **Console**, navigate to [Creating traces in Console][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].</span></span>  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

<span data-ttu-id="7da58-180">El resultado es un seguimiento para mostrar que se denomina y, a continuación, y en el `here()` segundo ejemplo que se denomina `there()` `everywhere()` `everywhere()` .</span><span class="sxs-lookup"><span data-stu-id="7da58-180">The result is a trace to display that `here()` is named `there()` and then `everywhere()` and in the second example that it's named `everywhere()`.</span></span>  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Seguimiento creado desde la consola" lightbox="../media/console-debug-trace.msft.png":::
   <span data-ttu-id="7da58-182">Seguimiento creado desde la **consola**</span><span class="sxs-lookup"><span data-stu-id="7da58-182">A trace created from **Console**</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7da58-183">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7da58-183">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Error de JavaScript notificado en la herramienta consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Creación de informes de error y aserciones en consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Error de red notificado en la consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "Se ha corregido un error de red notificado en la consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Informes de errores de red en consola e interfaz de usuario | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Creación de seguimientos en la consola | GitHub"  
