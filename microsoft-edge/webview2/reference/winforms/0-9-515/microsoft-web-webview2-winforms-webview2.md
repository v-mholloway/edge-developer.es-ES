---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 25ea8367aa9d64d0a1066cf8c1564f4d9c9f05ed
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655076"
---
# <span data-ttu-id="05db8-104">Clase Microsoft. Web. WebView2. WinForms. WebView2</span><span class="sxs-lookup"><span data-stu-id="05db8-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="05db8-105">Espacio de nombres: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="05db8-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="05db8-106">Ensamblado: Microsoft. Web. WebView2. WinForms. dll</span><span class="sxs-lookup"><span data-stu-id="05db8-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="05db8-107">Control para incrustar WebView2 en WinForms.</span><span class="sxs-lookup"><span data-stu-id="05db8-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="05db8-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="05db8-108">Summary</span></span>

 <span data-ttu-id="05db8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="05db8-109">Members</span></span>                        | <span data-ttu-id="05db8-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="05db8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="05db8-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="05db8-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="05db8-112">ContentLoading las distribuciones después de la navegación comienzan a un nuevo URI y el contenido de ese URI comienza a representarse.</span><span class="sxs-lookup"><span data-stu-id="05db8-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="05db8-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="05db8-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="05db8-114">Este evento se desencadena cuando se ha terminado de inicializar el [CoreWebView2](#corewebview2) del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="05db8-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="05db8-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="05db8-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="05db8-116">NavigationCompleted se envía después de navegar por el documento de nivel superior para representarlo correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="05db8-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="05db8-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="05db8-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="05db8-118">NavigationStarting se envía antes de que se inicie una nueva navegación en el documento de nivel superior de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="05db8-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="05db8-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="05db8-120">SourceChanged se distribuye después de que cambie la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="05db8-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="05db8-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="05db8-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="05db8-122">WebMessageReceived se distribuye después de que el contenido web envíe un mensaje al host de la aplicación a través de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="05db8-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="05db8-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="05db8-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="05db8-124">El CoreWebView2 subyacente.</span><span class="sxs-lookup"><span data-stu-id="05db8-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="05db8-125">Source</span><span class="sxs-lookup"><span data-stu-id="05db8-125">Source</span></span>](#source) | <span data-ttu-id="05db8-126">La propiedad Source es el identificador URI del documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="05db8-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="05db8-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="05db8-128">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="05db8-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="05db8-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="05db8-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="05db8-130">Devuelve true si la vista Web puede navegar a una página anterior en el historial de navegación a través del método GoBack.</span><span class="sxs-lookup"><span data-stu-id="05db8-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="05db8-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="05db8-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="05db8-132">Devuelve true si la vista Web puede navegar a una página siguiente del historial de navegación a través del método GoForward.</span><span class="sxs-lookup"><span data-stu-id="05db8-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="05db8-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="05db8-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="05db8-134">Desencadenar de forma explícita la inicialización de la [CoreWebView2](#corewebview2)del control.</span><span class="sxs-lookup"><span data-stu-id="05db8-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="05db8-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="05db8-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="05db8-136">Ejecuta el script proporcionado en el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="05db8-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="05db8-137">GoBack</span></span>](#goback) | <span data-ttu-id="05db8-138">Ir a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="05db8-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="05db8-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="05db8-139">GoForward</span></span>](#goforward) | <span data-ttu-id="05db8-140">Ir a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="05db8-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="05db8-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="05db8-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="05db8-142">Representar el código HTML proporcionado como documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="05db8-143">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="05db8-143">Reload</span></span>](#reload) | <span data-ttu-id="05db8-144">Vuelva a cargar el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="05db8-145">Detener</span><span class="sxs-lookup"><span data-stu-id="05db8-145">Stop</span></span>](#stop) | <span data-ttu-id="05db8-146">Detenga cualquier navegación en curso en el WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="05db8-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="05db8-147">WebView2</span></span>](#webview2) | <span data-ttu-id="05db8-148">Cree un nuevo control WebView2 WinForms.</span><span class="sxs-lookup"><span data-stu-id="05db8-148">Create a new WebView2 WinForms control.</span></span>
[<span data-ttu-id="05db8-149">Entrar</span><span class="sxs-lookup"><span data-stu-id="05db8-149">OnEnter</span></span>](#onenter) | <span data-ttu-id="05db8-150">Controlador de foco protegido.</span><span class="sxs-lookup"><span data-stu-id="05db8-150">Protected focus handler.</span></span>
[<span data-ttu-id="05db8-151">OnSizeChanged</span><span class="sxs-lookup"><span data-stu-id="05db8-151">OnSizeChanged</span></span>](#onsizechanged) | <span data-ttu-id="05db8-152">Controlador SizeChanged protegido.</span><span class="sxs-lookup"><span data-stu-id="05db8-152">Protected SizeChanged handler.</span></span>
[<span data-ttu-id="05db8-153">OnVisibleChanged</span><span class="sxs-lookup"><span data-stu-id="05db8-153">OnVisibleChanged</span></span>](#onvisiblechanged) | <span data-ttu-id="05db8-154">Controlador de VisibilityChanged protegido.</span><span class="sxs-lookup"><span data-stu-id="05db8-154">Protected VisibilityChanged handler.</span></span>

## <span data-ttu-id="05db8-155">Miembros</span><span class="sxs-lookup"><span data-stu-id="05db8-155">Members</span></span>

#### <span data-ttu-id="05db8-156">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="05db8-156">ContentLoading</span></span> 

<span data-ttu-id="05db8-157">ContentLoading las distribuciones después de la navegación comienzan a un nuevo URI y el contenido de ese URI comienza a representarse.</span><span class="sxs-lookup"><span data-stu-id="05db8-157">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="05db8-158">evento público EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="05db8-158">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="05db8-159">Esto es equivalente al evento ContentLoading en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-159">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="05db8-160">Para obtener más información, consulta la documentación de CoreWebView2. ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="05db8-160">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="05db8-161">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="05db8-161">CoreWebView2Ready</span></span> 

<span data-ttu-id="05db8-162">Este evento se desencadena cuando se ha terminado de inicializar el [CoreWebView2](#corewebview2) del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="05db8-162">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="05db8-163">evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="05db8-163">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="05db8-164">Debe controlar este evento si necesita realizar operaciones de configuración una vez en el CoreWebView2 el que desea afectar a todos sus usos (por ejemplo, agregar controladores de eventos, configurar valores, instalar scripts de creación de documentos, agregar objetos host).</span><span class="sxs-lookup"><span data-stu-id="05db8-164">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="05db8-165">Este evento no proporciona ningún argumento, y el remitente será el control WebView2, cuya propiedad CoreWebView2 será válida (es decir, no NULL) por primera vez.</span><span class="sxs-lookup"><span data-stu-id="05db8-165">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="05db8-166">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="05db8-166">NavigationCompleted</span></span> 

<span data-ttu-id="05db8-167">NavigationCompleted se envía después de navegar por el documento de nivel superior para representarlo correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="05db8-167">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="05db8-168">evento público EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="05db8-168">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="05db8-169">Esto es equivalente al evento NavigationCompleted en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-169">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="05db8-170">Para obtener más información, consulta la documentación de CoreWebView2. NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="05db8-170">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="05db8-171">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="05db8-171">NavigationStarting</span></span> 

<span data-ttu-id="05db8-172">NavigationStarting se envía antes de que se inicie una nueva navegación en el documento de nivel superior de la WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-172">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="05db8-173">evento público EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="05db8-173">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="05db8-174">Esto es equivalente al evento NavigationStarting en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-174">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="05db8-175">Para obtener más información, consulta la documentación de CoreWebView2. NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="05db8-175">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="05db8-176">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="05db8-176">SourceChanged</span></span> 

<span data-ttu-id="05db8-177">SourceChanged se distribuye después de que cambie la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="05db8-177">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="05db8-178">evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="05db8-178">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="05db8-179">Esto puede ocurrir durante una navegación o si, de lo contrario, el script de la página cambia el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="05db8-179">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="05db8-180">Esto es equivalente al evento SourceChanged en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-180">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="05db8-181">Para obtener más información, consulta la documentación de CoreWebView2. SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="05db8-181">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="05db8-182">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="05db8-182">WebMessageReceived</span></span> 

<span data-ttu-id="05db8-183">WebMessageReceived se distribuye después de que el contenido web envíe un mensaje al host de la aplicación a través de `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="05db8-183">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="05db8-184">evento público EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="05db8-184">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="05db8-185">Esto es equivalente al evento WebMessageReceived en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-185">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="05db8-186">Para obtener más información, consulta la documentación de CoreWebView2. WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="05db8-186">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="05db8-187">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="05db8-187">CoreWebView2</span></span> 

<span data-ttu-id="05db8-188">El CoreWebView2 subyacente.</span><span class="sxs-lookup"><span data-stu-id="05db8-188">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="05db8-189">CoreWebView2 pública [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="05db8-189">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="05db8-190">Use esta propiedad para realizar más operaciones en el contenido de WebView2 de las que se exponen en el WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-190">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="05db8-191">Este valor es null hasta que se inicializa.</span><span class="sxs-lookup"><span data-stu-id="05db8-191">This value is null until it is initialized.</span></span> <span data-ttu-id="05db8-192">Puedes forzar que el CoreWebView2 subyacente se inicialice mediante el método InitializeAsync.</span><span class="sxs-lookup"><span data-stu-id="05db8-192">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="05db8-193">Source</span><span class="sxs-lookup"><span data-stu-id="05db8-193">Source</span></span> 

<span data-ttu-id="05db8-194">La propiedad Source es el identificador URI del documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-194">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="05db8-195">[origen](#source) de URI público</span><span class="sxs-lookup"><span data-stu-id="05db8-195">public Uri [Source](#source)</span></span>

<span data-ttu-id="05db8-196">Establecer el origen es equivalente a llamar a CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="05db8-196">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="05db8-197">Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es "About: Blank".</span><span class="sxs-lookup"><span data-stu-id="05db8-197">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="05db8-198">Si la propiedad se establece en un URI no absoluto o en null, la propiedad permanece sin modificar.</span><span class="sxs-lookup"><span data-stu-id="05db8-198">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="05db8-199">Para obtener más información, consulta la documentación de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-199">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="05db8-200">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="05db8-200">ZoomFactor</span></span> 

<span data-ttu-id="05db8-201">El factor de zoom para la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="05db8-201">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="05db8-202">[ZoomFactor](#zoomfactor) doble público</span><span class="sxs-lookup"><span data-stu-id="05db8-202">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="05db8-203">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="05db8-203">CanGoBack</span></span> 

<span data-ttu-id="05db8-204">Devuelve true si la vista Web puede navegar a una página anterior en el historial de navegación a través del método GoBack.</span><span class="sxs-lookup"><span data-stu-id="05db8-204">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="05db8-205">Public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="05db8-205">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="05db8-206">Esto es equivalente a la propiedad CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-206">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="05db8-207">Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es falsa.</span><span class="sxs-lookup"><span data-stu-id="05db8-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="05db8-208">Para obtener más información, consulta la documentación de CoreWebView2. CanGoBack.</span><span class="sxs-lookup"><span data-stu-id="05db8-208">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="05db8-209">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="05db8-209">CanGoForward</span></span> 

<span data-ttu-id="05db8-210">Devuelve true si la vista Web puede navegar a una página siguiente del historial de navegación a través del método GoForward.</span><span class="sxs-lookup"><span data-stu-id="05db8-210">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="05db8-211">Public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="05db8-211">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="05db8-212">Esto es equivalente a la propiedad CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-212">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="05db8-213">Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es falsa.</span><span class="sxs-lookup"><span data-stu-id="05db8-213">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="05db8-214">Para obtener más información, consulta la documentación de CoreWebView2. CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="05db8-214">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="05db8-215">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="05db8-215">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="05db8-216">Desencadenar de forma explícita la inicialización de la [CoreWebView2](#corewebview2)del control.</span><span class="sxs-lookup"><span data-stu-id="05db8-216">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="05db8-217">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tareas públicas (entorno de CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="05db8-217">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="05db8-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="05db8-218">Parameters</span></span>
* `environment` <span data-ttu-id="05db8-219">Un CoreWebView2Environment creado previamente que se debe usar para crear el CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-219">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="05db8-220">Crear su propio entorno le proporciona control sobre varias opciones que afectan a la forma en que se inicializa CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-220">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="05db8-221">Si pasa null (el valor predeterminado), se creará un entorno predeterminado y se usará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="05db8-221">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="05db8-222">Devuelve</span><span class="sxs-lookup"><span data-stu-id="05db8-222">Returns</span></span>
<span data-ttu-id="05db8-223">Una tarea que representa el proceso de inicialización en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="05db8-223">A Task that represents the background initialization process.</span></span> <span data-ttu-id="05db8-224">Cuando la tarea se complete, la propiedad CoreWebView2 estará disponible para su uso (es decir, no NULL).</span><span class="sxs-lookup"><span data-stu-id="05db8-224">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="05db8-225">Observe que el evento [CoreWebView2Ready](#corewebview2ready) del control se invocará antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="05db8-225">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="05db8-226">Llamar a este método los tiempos adicionales no tendrán efecto (se ignora cualquier entorno especificado) y devolverán la misma tarea que la primera llamada.</span><span class="sxs-lookup"><span data-stu-id="05db8-226">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="05db8-227">La llamada a este método después de la inicialización se ha desencadenado de forma implícita mediante la configuración de la propiedad [source](#source) no tendrá ningún efecto (se ignora cualquier entorno especificado) y simplemente devuelva una tarea que represente la inicialización que ya está en curso.</span><span class="sxs-lookup"><span data-stu-id="05db8-227">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="05db8-228">Excepciones</span><span class="sxs-lookup"><span data-stu-id="05db8-228">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="05db8-229">Se produce cuando se invoca desde un subproceso que no es de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="05db8-229">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="05db8-230">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="05db8-230">ExecuteScriptAsync</span></span> 

<span data-ttu-id="05db8-231">Ejecuta el script proporcionado en el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-231">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="05db8-232">Tarea asincrónica pública< cadena > [ExecuteScriptAsync](#executescriptasync)(secuencia de comandos de cadena)</span><span class="sxs-lookup"><span data-stu-id="05db8-232">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="05db8-233">Es equivalente al método ExecuteScriptAsync en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-233">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="05db8-234">Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="05db8-234">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="05db8-235">Para obtener más información, consulta la documentación de CoreWebView2. ExecuteScriptAsync.</span><span class="sxs-lookup"><span data-stu-id="05db8-235">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="05db8-236">GoBack</span><span class="sxs-lookup"><span data-stu-id="05db8-236">GoBack</span></span> 

<span data-ttu-id="05db8-237">Ir a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="05db8-237">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="05db8-238">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="05db8-238">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="05db8-239">Esto es equivalente al método GoBack de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-239">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="05db8-240">Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="05db8-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="05db8-241">Para obtener más información, vea la documentación de CoreWebView2. GoBack.</span><span class="sxs-lookup"><span data-stu-id="05db8-241">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="05db8-242">GoForward</span><span class="sxs-lookup"><span data-stu-id="05db8-242">GoForward</span></span> 

<span data-ttu-id="05db8-243">Ir a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="05db8-243">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="05db8-244">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="05db8-244">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="05db8-245">Es equivalente al método GoForward de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-245">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="05db8-246">Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="05db8-246">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="05db8-247">Para obtener más información, consulte la documentación de CoreWebView2. GoForward.</span><span class="sxs-lookup"><span data-stu-id="05db8-247">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="05db8-248">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="05db8-248">NavigateToString</span></span> 

<span data-ttu-id="05db8-249">Representar el código HTML proporcionado como documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-249">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="05db8-250">public void [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="05db8-250">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="05db8-251">Es equivalente al método NavigateToString en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-251">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="05db8-252">Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="05db8-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="05db8-253">Para obtener más información, consulta la documentación de CoreWebView2. NavigateToString.</span><span class="sxs-lookup"><span data-stu-id="05db8-253">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="05db8-254">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="05db8-254">Reload</span></span> 

<span data-ttu-id="05db8-255">Vuelva a cargar el documento de nivel superior del WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-255">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="05db8-256">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="05db8-256">public void [Reload](#reload)()</span></span>

<span data-ttu-id="05db8-257">Es equivalente al método Reload de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-257">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="05db8-258">Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="05db8-258">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="05db8-259">Consulte CoreWebView2. Vuelva a cargar la documentación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="05db8-259">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="05db8-260">Detener</span><span class="sxs-lookup"><span data-stu-id="05db8-260">Stop</span></span> 

<span data-ttu-id="05db8-261">Detenga cualquier navegación en curso en el WebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-261">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="05db8-262">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="05db8-262">public void [Stop](#stop)()</span></span>

<span data-ttu-id="05db8-263">Es equivalente al método Stop de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="05db8-263">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="05db8-264">Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="05db8-264">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="05db8-265">Consulte CoreWebView2. detenga la documentación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="05db8-265">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="05db8-266">WebView2</span><span class="sxs-lookup"><span data-stu-id="05db8-266">WebView2</span></span> 

<span data-ttu-id="05db8-267">Cree un nuevo control WebView2 WinForms.</span><span class="sxs-lookup"><span data-stu-id="05db8-267">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="05db8-268">[WebView2](#webview2)pública ()</span><span class="sxs-lookup"><span data-stu-id="05db8-268">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="05db8-269">Después de la construcción, la propiedad CoreWebView2 es NULL.</span><span class="sxs-lookup"><span data-stu-id="05db8-269">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="05db8-270">Llama a [EnsureCoreWebView2Async](#ensurecorewebview2async) para inicializar el CoreWebView2 subyacente.</span><span class="sxs-lookup"><span data-stu-id="05db8-270">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

#### <span data-ttu-id="05db8-271">Entrar</span><span class="sxs-lookup"><span data-stu-id="05db8-271">OnEnter</span></span> 

<span data-ttu-id="05db8-272">Controlador de foco protegido.</span><span class="sxs-lookup"><span data-stu-id="05db8-272">Protected focus handler.</span></span>

> <span data-ttu-id="05db8-273">Protected override void [entrar](#onenter)(EventArgs e)</span><span class="sxs-lookup"><span data-stu-id="05db8-273">protected override void [OnEnter](#onenter)(EventArgs e)</span></span>

#### <span data-ttu-id="05db8-274">OnSizeChanged</span><span class="sxs-lookup"><span data-stu-id="05db8-274">OnSizeChanged</span></span> 

<span data-ttu-id="05db8-275">Controlador SizeChanged protegido.</span><span class="sxs-lookup"><span data-stu-id="05db8-275">Protected SizeChanged handler.</span></span>

> <span data-ttu-id="05db8-276">Protected override void [OnSizeChanged](#onsizechanged)(EventArgs e)</span><span class="sxs-lookup"><span data-stu-id="05db8-276">protected override void [OnSizeChanged](#onsizechanged)(EventArgs e)</span></span>

#### <span data-ttu-id="05db8-277">OnVisibleChanged</span><span class="sxs-lookup"><span data-stu-id="05db8-277">OnVisibleChanged</span></span> 

<span data-ttu-id="05db8-278">Controlador de VisibilityChanged protegido.</span><span class="sxs-lookup"><span data-stu-id="05db8-278">Protected VisibilityChanged handler.</span></span>

> <span data-ttu-id="05db8-279">Protected override void [OnVisibleChanged](#onvisiblechanged)(EventArgs e)</span><span class="sxs-lookup"><span data-stu-id="05db8-279">protected override void [OnVisibleChanged](#onvisiblechanged)(EventArgs e)</span></span>

