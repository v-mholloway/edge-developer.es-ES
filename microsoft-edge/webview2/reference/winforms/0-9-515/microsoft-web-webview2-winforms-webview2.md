---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WinForms. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. WinForms. WebView2
ms.openlocfilehash: 7d707c2a6ecb8127074735f06ba6d4f1f28eea0c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879453"
---
# <span data-ttu-id="6c508-104">Clase Microsoft. Web. WebView2. WinForms. WebView2</span><span class="sxs-lookup"><span data-stu-id="6c508-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="6c508-105">Espacio de nombres: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="6c508-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="6c508-106">Ensamblado: Microsoft.Web.WebView2.WinForms.dll</span><span class="sxs-lookup"><span data-stu-id="6c508-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="6c508-107">Control para incrustar WebView2 en WinForms.</span><span class="sxs-lookup"><span data-stu-id="6c508-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="6c508-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6c508-108">Summary</span></span>

 <span data-ttu-id="6c508-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c508-109">Members</span></span>                        | <span data-ttu-id="6c508-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6c508-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c508-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="6c508-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="6c508-112">ContentLoading las distribuciones después de la navegación comienzan a un nuevo URI y el contenido de ese URI comienza a representarse.</span><span class="sxs-lookup"><span data-stu-id="6c508-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="6c508-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="6c508-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="6c508-114">Este evento se desencadena cuando se ha terminado de inicializar el [CoreWebView2](#corewebview2) del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="6c508-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="6c508-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6c508-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="6c508-116">NavigationCompleted se envía después de navegar por el documento de nivel superior para representarlo correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="6c508-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="6c508-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6c508-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="6c508-118">NavigationStarting se envía antes de que se inicie una nueva navegación en el documento de nivel superior de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="6c508-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="6c508-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="6c508-120">SourceChanged se distribuye después de que cambie la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="6c508-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="6c508-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="6c508-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="6c508-122">WebMessageReceived se distribuye después de que el contenido web envíe un mensaje al host de la aplicación a través de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="6c508-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="6c508-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="6c508-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="6c508-124">El CoreWebView2 subyacente.</span><span class="sxs-lookup"><span data-stu-id="6c508-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="6c508-125">Source</span><span class="sxs-lookup"><span data-stu-id="6c508-125">Source</span></span>](#source) | <span data-ttu-id="6c508-126">La propiedad Source es el identificador URI del documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="6c508-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6c508-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="6c508-128">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="6c508-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="6c508-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="6c508-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="6c508-130">Devuelve true si la vista Web puede navegar a una página anterior en el historial de navegación a través del método GoBack.</span><span class="sxs-lookup"><span data-stu-id="6c508-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="6c508-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="6c508-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="6c508-132">Devuelve true si la vista Web puede navegar a una página siguiente del historial de navegación a través del método GoForward.</span><span class="sxs-lookup"><span data-stu-id="6c508-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="6c508-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="6c508-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="6c508-134">Desencadenar de forma explícita la inicialización de la [CoreWebView2](#corewebview2)del control.</span><span class="sxs-lookup"><span data-stu-id="6c508-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="6c508-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="6c508-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="6c508-136">Ejecuta el script proporcionado en el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="6c508-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="6c508-137">GoBack</span></span>](#goback) | <span data-ttu-id="6c508-138">Ir a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="6c508-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="6c508-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="6c508-139">GoForward</span></span>](#goforward) | <span data-ttu-id="6c508-140">Ir a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="6c508-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="6c508-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="6c508-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="6c508-142">Representar el código HTML proporcionado como documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="6c508-143">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="6c508-143">Reload</span></span>](#reload) | <span data-ttu-id="6c508-144">Vuelva a cargar el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="6c508-145">Detener</span><span class="sxs-lookup"><span data-stu-id="6c508-145">Stop</span></span>](#stop) | <span data-ttu-id="6c508-146">Detenga cualquier navegación en curso en el WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="6c508-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="6c508-147">WebView2</span></span>](#webview2) | <span data-ttu-id="6c508-148">Cree un nuevo control WebView2 WinForms.</span><span class="sxs-lookup"><span data-stu-id="6c508-148">Create a new WebView2 WinForms control.</span></span>

## <span data-ttu-id="6c508-149">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c508-149">Members</span></span>

#### <span data-ttu-id="6c508-150">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="6c508-150">ContentLoading</span></span> 

<span data-ttu-id="6c508-151">ContentLoading las distribuciones después de la navegación comienzan a un nuevo URI y el contenido de ese URI comienza a representarse.</span><span class="sxs-lookup"><span data-stu-id="6c508-151">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="6c508-152">evento público EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="6c508-152">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="6c508-153">Esto es equivalente al evento ContentLoading en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-153">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="6c508-154">Para obtener más información, consulta la documentación de CoreWebView2. ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="6c508-154">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="6c508-155">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="6c508-155">CoreWebView2Ready</span></span> 

<span data-ttu-id="6c508-156">Este evento se desencadena cuando se ha terminado de inicializar el [CoreWebView2](#corewebview2) del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="6c508-156">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="6c508-157">evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="6c508-157">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="6c508-158">Debe controlar este evento si necesita realizar operaciones de configuración una vez en el CoreWebView2 el que desea afectar a todos sus usos (por ejemplo, agregar controladores de eventos, configurar valores, instalar scripts de creación de documentos, agregar objetos host).</span><span class="sxs-lookup"><span data-stu-id="6c508-158">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="6c508-159">Este evento no proporciona ningún argumento, y el remitente será el control WebView2, cuya propiedad CoreWebView2 será válida (es decir, no NULL) por primera vez.</span><span class="sxs-lookup"><span data-stu-id="6c508-159">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="6c508-160">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="6c508-160">NavigationCompleted</span></span> 

<span data-ttu-id="6c508-161">NavigationCompleted se envía después de navegar por el documento de nivel superior para representarlo correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="6c508-161">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="6c508-162">evento público EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="6c508-162">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="6c508-163">Esto es equivalente al evento NavigationCompleted en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-163">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="6c508-164">Para obtener más información, consulta la documentación de CoreWebView2. NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6c508-164">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="6c508-165">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="6c508-165">NavigationStarting</span></span> 

<span data-ttu-id="6c508-166">NavigationStarting se envía antes de que se inicie una nueva navegación en el documento de nivel superior de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-166">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="6c508-167">evento público EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="6c508-167">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="6c508-168">Esto es equivalente al evento NavigationStarting en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-168">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="6c508-169">Para obtener más información, consulta la documentación de CoreWebView2. NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6c508-169">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="6c508-170">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="6c508-170">SourceChanged</span></span> 

<span data-ttu-id="6c508-171">SourceChanged se distribuye después de que cambie la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="6c508-171">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="6c508-172">evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="6c508-172">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="6c508-173">Esto puede ocurrir durante una navegación o si, de lo contrario, el script de la página cambia el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="6c508-173">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="6c508-174">Esto es equivalente al evento SourceChanged en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-174">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="6c508-175">Para obtener más información, consulta la documentación de CoreWebView2. SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="6c508-175">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="6c508-176">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="6c508-176">WebMessageReceived</span></span> 

<span data-ttu-id="6c508-177">WebMessageReceived se distribuye después de que el contenido web envíe un mensaje al host de la aplicación a través de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="6c508-177">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="6c508-178">evento público EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="6c508-178">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="6c508-179">Esto es equivalente al evento WebMessageReceived en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-179">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="6c508-180">Para obtener más información, consulta la documentación de CoreWebView2. WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="6c508-180">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="6c508-181">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="6c508-181">CoreWebView2</span></span> 

<span data-ttu-id="6c508-182">El CoreWebView2 subyacente.</span><span class="sxs-lookup"><span data-stu-id="6c508-182">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="6c508-183">CoreWebView2 pública [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="6c508-183">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="6c508-184">Use esta propiedad para realizar más operaciones en el contenido de WebView2 de las que se exponen en el WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-184">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="6c508-185">Este valor es null hasta que se inicializa.</span><span class="sxs-lookup"><span data-stu-id="6c508-185">This value is null until it is initialized.</span></span> <span data-ttu-id="6c508-186">Puedes forzar que el CoreWebView2 subyacente se inicialice mediante el método InitializeAsync.</span><span class="sxs-lookup"><span data-stu-id="6c508-186">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="6c508-187">Source</span><span class="sxs-lookup"><span data-stu-id="6c508-187">Source</span></span> 

<span data-ttu-id="6c508-188">La propiedad Source es el identificador URI del documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-188">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="6c508-189">[origen](#source) de URI público</span><span class="sxs-lookup"><span data-stu-id="6c508-189">public Uri [Source](#source)</span></span>

<span data-ttu-id="6c508-190">Establecer el origen es equivalente a llamar a CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="6c508-190">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="6c508-191">Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es "About: Blank".</span><span class="sxs-lookup"><span data-stu-id="6c508-191">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="6c508-192">Si la propiedad se establece en un URI no absoluto o en null, la propiedad permanece sin modificar.</span><span class="sxs-lookup"><span data-stu-id="6c508-192">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="6c508-193">Para obtener más información, consulta la documentación de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-193">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="6c508-194">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="6c508-194">ZoomFactor</span></span> 

<span data-ttu-id="6c508-195">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="6c508-195">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="6c508-196">[ZoomFactor](#zoomfactor) doble público</span><span class="sxs-lookup"><span data-stu-id="6c508-196">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="6c508-197">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="6c508-197">CanGoBack</span></span> 

<span data-ttu-id="6c508-198">Devuelve true si la vista Web puede navegar a una página anterior en el historial de navegación a través del método GoBack.</span><span class="sxs-lookup"><span data-stu-id="6c508-198">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="6c508-199">Public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="6c508-199">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="6c508-200">Esto es equivalente a la propiedad CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-200">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="6c508-201">Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es falsa.</span><span class="sxs-lookup"><span data-stu-id="6c508-201">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="6c508-202">Para obtener más información, consulta la documentación de CoreWebView2. CanGoBack.</span><span class="sxs-lookup"><span data-stu-id="6c508-202">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="6c508-203">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="6c508-203">CanGoForward</span></span> 

<span data-ttu-id="6c508-204">Devuelve true si la vista Web puede navegar a una página siguiente del historial de navegación a través del método GoForward.</span><span class="sxs-lookup"><span data-stu-id="6c508-204">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="6c508-205">Public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="6c508-205">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="6c508-206">Esto es equivalente a la propiedad CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-206">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="6c508-207">Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es falsa.</span><span class="sxs-lookup"><span data-stu-id="6c508-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="6c508-208">Para obtener más información, consulta la documentación de CoreWebView2. CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="6c508-208">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="6c508-209">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="6c508-209">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="6c508-210">Desencadenar de forma explícita la inicialización de la [CoreWebView2](#corewebview2)del control.</span><span class="sxs-lookup"><span data-stu-id="6c508-210">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="6c508-211">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tareas públicas (entorno de CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="6c508-211">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="6c508-212">Parameters</span><span class="sxs-lookup"><span data-stu-id="6c508-212">Parameters</span></span>
* `environment` <span data-ttu-id="6c508-213">Un CoreWebView2Environment creado previamente que se debe usar para crear el CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-213">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="6c508-214">Crear su propio entorno le proporciona control sobre varias opciones que afectan a la forma en que se inicializa CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-214">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="6c508-215">Si pasa null (el valor predeterminado), se creará un entorno predeterminado y se usará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6c508-215">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="6c508-216">Devuelve</span><span class="sxs-lookup"><span data-stu-id="6c508-216">Returns</span></span>
<span data-ttu-id="6c508-217">Una tarea que representa el proceso de inicialización en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6c508-217">A Task that represents the background initialization process.</span></span> <span data-ttu-id="6c508-218">Cuando la tarea se complete, la propiedad CoreWebView2 estará disponible para su uso (es decir, no NULL).</span><span class="sxs-lookup"><span data-stu-id="6c508-218">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="6c508-219">Observe que el evento [CoreWebView2Ready](#corewebview2ready) del control se invocará antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="6c508-219">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="6c508-220">Llamar a este método los tiempos adicionales no tendrán efecto (se ignora cualquier entorno especificado) y devolverán la misma tarea que la primera llamada.</span><span class="sxs-lookup"><span data-stu-id="6c508-220">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="6c508-221">La llamada a este método después de la inicialización se ha desencadenado de forma implícita mediante la configuración de la propiedad [source](#source) no tendrá ningún efecto (se ignora cualquier entorno especificado) y simplemente devuelva una tarea que represente la inicialización que ya está en curso.</span><span class="sxs-lookup"><span data-stu-id="6c508-221">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="6c508-222">Excepciones</span><span class="sxs-lookup"><span data-stu-id="6c508-222">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="6c508-223">Se produce cuando se invoca desde un subproceso que no es de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6c508-223">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="6c508-224">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="6c508-224">ExecuteScriptAsync</span></span> 

<span data-ttu-id="6c508-225">Ejecuta el script proporcionado en el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-225">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="6c508-226">Tarea asincrónica pública< cadena > [ExecuteScriptAsync](#executescriptasync)(secuencia de comandos de cadena)</span><span class="sxs-lookup"><span data-stu-id="6c508-226">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="6c508-227">Es equivalente al método ExecuteScriptAsync en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-227">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="6c508-228">Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="6c508-228">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="6c508-229">Para obtener más información, consulte CoreWebView2.Exedocumentación de cuteScriptAsync.</span><span class="sxs-lookup"><span data-stu-id="6c508-229">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="6c508-230">GoBack</span><span class="sxs-lookup"><span data-stu-id="6c508-230">GoBack</span></span> 

<span data-ttu-id="6c508-231">Ir a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="6c508-231">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="6c508-232">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="6c508-232">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="6c508-233">Esto es equivalente al método GoBack de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-233">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="6c508-234">Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="6c508-234">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="6c508-235">Para obtener más información, vea la documentación de CoreWebView2. GoBack.</span><span class="sxs-lookup"><span data-stu-id="6c508-235">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="6c508-236">GoForward</span><span class="sxs-lookup"><span data-stu-id="6c508-236">GoForward</span></span> 

<span data-ttu-id="6c508-237">Ir a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="6c508-237">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="6c508-238">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="6c508-238">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="6c508-239">Es equivalente al método GoForward de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-239">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="6c508-240">Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="6c508-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="6c508-241">Para obtener más información, consulte la documentación de CoreWebView2. GoForward.</span><span class="sxs-lookup"><span data-stu-id="6c508-241">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="6c508-242">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="6c508-242">NavigateToString</span></span> 

<span data-ttu-id="6c508-243">Representar el código HTML proporcionado como documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-243">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="6c508-244">public void [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="6c508-244">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="6c508-245">Es equivalente al método NavigateToString en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-245">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="6c508-246">Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="6c508-246">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="6c508-247">Para obtener más información, consulta la documentación de CoreWebView2. NavigateToString.</span><span class="sxs-lookup"><span data-stu-id="6c508-247">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="6c508-248">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="6c508-248">Reload</span></span> 

<span data-ttu-id="6c508-249">Vuelva a cargar el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-249">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="6c508-250">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="6c508-250">public void [Reload](#reload)()</span></span>

<span data-ttu-id="6c508-251">Es equivalente al método Reload de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-251">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="6c508-252">Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="6c508-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="6c508-253">Consulte CoreWebView2. Vuelva a cargar la documentación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6c508-253">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="6c508-254">Detener</span><span class="sxs-lookup"><span data-stu-id="6c508-254">Stop</span></span> 

<span data-ttu-id="6c508-255">Detenga cualquier navegación en curso en el WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-255">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="6c508-256">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="6c508-256">public void [Stop](#stop)()</span></span>

<span data-ttu-id="6c508-257">Es equivalente al método Stop de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="6c508-257">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="6c508-258">Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="6c508-258">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="6c508-259">Consulte CoreWebView2. detenga la documentación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6c508-259">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="6c508-260">WebView2</span><span class="sxs-lookup"><span data-stu-id="6c508-260">WebView2</span></span> 

<span data-ttu-id="6c508-261">Cree un nuevo control WebView2 WinForms.</span><span class="sxs-lookup"><span data-stu-id="6c508-261">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="6c508-262">[WebView2](#webview2)pública ()</span><span class="sxs-lookup"><span data-stu-id="6c508-262">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="6c508-263">Después de la construcción, la propiedad CoreWebView2 es NULL.</span><span class="sxs-lookup"><span data-stu-id="6c508-263">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="6c508-264">Llama a [EnsureCoreWebView2Async](#ensurecorewebview2async) para inicializar el CoreWebView2 subyacente.</span><span class="sxs-lookup"><span data-stu-id="6c508-264">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

