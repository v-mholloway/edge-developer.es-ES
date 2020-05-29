---
description: Hospedar contenido web en la aplicación de Windows 10 con el control WebView (EdgeHTML)
title: Vista de Microsoft Edge para aplicaciones de Windows 10
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: x-MS-WebView, MSHTMLWebViewElement, WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 08efb1bb87877e0b11cbc3bee1061f9be6c9ab3f
ms.sourcegitcommit: 831fc41ea347e2d1160b1804fb5e5a427dc3070d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629552"
---
# <span data-ttu-id="53d11-104">Vista de WebView (EdgeHTML) para aplicaciones de Windows 10</span><span class="sxs-lookup"><span data-stu-id="53d11-104">WebView (EdgeHTML) for Windows 10 apps</span></span>

<span data-ttu-id="53d11-105">El control WebView (EdgeHTML) te permite hospedar contenido web en tu aplicación de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="53d11-105">The WebView (EdgeHTML) control enables you to host web content in your Windows 10 app.</span></span> 

<span data-ttu-id="53d11-106">Puedes usarlo como un elemento XAML (para aplicaciones de la [plataforma universal de Windows (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) y [aplicaciones de escritorio de Windows Forms y WPF](/windows/communitytoolkit/controls/wpf-winforms/webview)) o un elemento HTML (x-MS-WebView)/Dom Object (MSHTMLWebViewElement) para aplicaciones de Windows 10 basadas en JavaScript, tal y como se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="53d11-106">You can use it as a XAML element (for [Universal Windows Platform (UWP) apps](/uwp/api/Windows.UI.Xaml.Controls.WebView) and [Windows Forms and WPF desktop applications](/windows/communitytoolkit/controls/wpf-winforms/webview)), or an HTML element (x-ms-webview)/DOM object (MSHTMLWebViewElement) for JavaScript-based Windows 10 apps, as described here.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="53d11-107">Eventos</span><span class="sxs-lookup"><span data-stu-id="53d11-107">Events</span></span>**](#events) | <span data-ttu-id="53d11-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted, MSWebViewNavigationStarting](#mswebviewnavigationcompleted) [, MSWebViewNewWindowRequested](#mswebviewnavigationstarting) [, MSWebViewPermissionRequested](#mswebviewnewwindowrequested) [, MSWebViewProcessExited](#mswebviewpermissionrequested) [, MSWebViewWebResourceRequested](#mswebviewprocessexited) [, MSWebViewScriptNotify](#mswebviewwebresourcerequested) [, MSWebViewUnsafeContentWarningDisplaying](#mswebviewscriptnotify) [, MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) [MSWebViewUnviewableContentIdentified](#mswebviewunsupportedurischemeidentified)</span><span class="sxs-lookup"><span data-stu-id="53d11-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span></span>
| [**<span data-ttu-id="53d11-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="53d11-109">Methods</span></span>**](#methods) | <span data-ttu-id="53d11-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [GoBack](#goback), [goForward](#goforward), [Navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri) [, navigateToString,](#navigatetostring) [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Refresh](#refresh), [Stop](#stop)</span><span class="sxs-lookup"><span data-stu-id="53d11-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward](#goforward), [navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [refresh](#refresh), [stop](#stop)</span></span> |
| [**<span data-ttu-id="53d11-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53d11-111">Properties</span></span>**](#properties) | <span data-ttu-id="53d11-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [Process](#process), [Settings](#settings), [src](#src), [width](#width)</span><span class="sxs-lookup"><span data-stu-id="53d11-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [process](#process), [settings](#settings), [src](#src), [width](#width)</span></span> |

## <span data-ttu-id="53d11-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53d11-113">Syntax</span></span>

```js
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```

## <span data-ttu-id="53d11-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53d11-114">Remarks</span></span>

### <span data-ttu-id="53d11-115">Vista de visualización frente a iframe</span><span class="sxs-lookup"><span data-stu-id="53d11-115">WebView versus iframe</span></span>

<span data-ttu-id="53d11-116">Como un elemento HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) estándar, puedes usar la vista Web para cargar páginas remotas a través de http y páginas locales (*MS-appx-Web:///*) del paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53d11-116">Like a standard HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) element,  you can use WebView to load remote pages over HTTP and local pages (*ms-appx-web:///*) from your app package.</span></span> <span data-ttu-id="53d11-117">Sin embargo, la WebView también puede:</span><span class="sxs-lookup"><span data-stu-id="53d11-117">However, the WebView can also:</span></span>

 - <span data-ttu-id="53d11-118">Cargue páginas y recursos de las carpetas de [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, roaming, temporal) (*MS-AppData:///*) y las [secuencias en memoria](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)</span><span class="sxs-lookup"><span data-stu-id="53d11-118">Load pages and resources from your [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, roaming, temp) folders (*ms-appdata:///*) and [in-memory streams](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*ms-local-stream:///*)</span></span>

 - <span data-ttu-id="53d11-119">Proporcionar controles de tipo explorador: para [volver atrás](#goback) y [avanzar](#goforward) en el historial de navegación, y [detener](#stop) o [Actualizar](#refresh) la página actual.</span><span class="sxs-lookup"><span data-stu-id="53d11-119">Provide browser-like controls: for going [back](#goback) and [forward](#goforward) in navigation history, and [stopping](#stop) or [refreshing](#refresh) the current page.</span></span> 

 - <span data-ttu-id="53d11-120">[Captura capturas de pantallas de contenido web](#capturepreviewtoblobasync) para que sea más fácil implementar el contrato para [compartir](/windows/uwp/app-to-app/share-data) aplicaciones de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="53d11-120">[Capture screenshots of web content](#capturepreviewtoblobasync) making it easy to implement the Windows 10 app [Share](/windows/uwp/app-to-app/share-data) contract.</span></span>

 - <span data-ttu-id="53d11-121">Permite que el código de JavaScript que se ejecuta en una vista webproduzca eventos personalizados ([MSWebViewScriptNotify](#mswebviewscriptnotify)) en la aplicación y permite que la aplicación ejecute JavaScript en la vista de contenido ([invokeScriptAsync](#invokescriptasync)).</span><span class="sxs-lookup"><span data-stu-id="53d11-121">Allow JavaScript code running within a webview to raise custom events ([MSWebViewScriptNotify](#mswebviewscriptnotify)) to your app, and allow your app to run JavaScript within the webview ([invokeScriptAsync](#invokescriptasync)).</span></span>

 - <span data-ttu-id="53d11-122">Proporcionarle eventos de contenido de WebView con ajuste fino:</span><span class="sxs-lookup"><span data-stu-id="53d11-122">Provide you with fine-tuned webview content events:</span></span>
    
    <span data-ttu-id="53d11-123">Evento de DOM de WebView</span><span class="sxs-lookup"><span data-stu-id="53d11-123">WebView DOM event</span></span> | <span data-ttu-id="53d11-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="53d11-124">Description</span></span>
    --------- | ------
    [<span data-ttu-id="53d11-125">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="53d11-125">MSWebViewNavigationStarting</span></span>](#mswebviewnavigationstarting) | <span data-ttu-id="53d11-126">Indica que la vista en WebView está empezando a navegar</span><span class="sxs-lookup"><span data-stu-id="53d11-126">Indicates the WebView is starting to navigate</span></span>
    [<span data-ttu-id="53d11-127">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="53d11-127">MSWebViewContentLoading</span></span>](#mswebviewcontentloading) | <span data-ttu-id="53d11-128">El contenido HTML se descarga y se carga en el control</span><span class="sxs-lookup"><span data-stu-id="53d11-128">The HTML content is downloaded and is being loaded into the control</span></span>
    [<span data-ttu-id="53d11-129">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="53d11-129">MSWebViewDOMContentLoaded</span></span>](#mswebviewdomcontentloaded) | <span data-ttu-id="53d11-130">Indica que los elementos principales de DOM han terminado de cargarse</span><span class="sxs-lookup"><span data-stu-id="53d11-130">Indicates that the main DOM elements have finished loading</span></span>
    [<span data-ttu-id="53d11-131">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="53d11-131">MSWebViewNavigationCompleted</span></span>](#mswebviewnavigationcompleted) | <span data-ttu-id="53d11-132">Indica que la navegación se ha completado y todos los elementos multimedia están representados.</span><span class="sxs-lookup"><span data-stu-id="53d11-132">Indicates the navigation is complete, and all media elements are rendered</span></span>
    [<span data-ttu-id="53d11-133">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="53d11-133">MSWebViewUnviewableContentIdentified</span></span>](#mswebviewunviewablecontentidentified) | <span data-ttu-id="53d11-134">El WebView encontró que el contenido no era HTML</span><span class="sxs-lookup"><span data-stu-id="53d11-134">The WebView found the content was not HTML</span></span>
    [<span data-ttu-id="53d11-135">UnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="53d11-135">UnsafeContentWarningDisplaying</span></span>](#mswebviewunsafecontentwarningdisplaying) | <span data-ttu-id="53d11-136">La vista Web muestra una página de advertencia para el contenido notificado como no seguro por el *Filtro SmartScreen*de Windows.</span><span class="sxs-lookup"><span data-stu-id="53d11-136">The WebView shows a warning page for content that was reported as unsafe by Windows *SmartScreen Filter*.</span></span>

    <span data-ttu-id="53d11-137">... incluye [los eventos](#events) correspondientes para el contenido de iframe cargado en una vista previa (como [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="53d11-137">...including corresponding [events](#events) for iframe content loaded within a WebView (such as [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) and so on.)</span></span>

### <span data-ttu-id="53d11-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="53d11-138">Printing</span></span>

<span data-ttu-id="53d11-139">Cuando se imprime una aplicación de Windows con JavaScript, las `<x-ms-webview>` etiquetas se transforman en `<iframe>` etiquetas antes de imprimir.</span><span class="sxs-lookup"><span data-stu-id="53d11-139">When a Windows app using JavaScript is printed, the `<x-ms-webview>` tags are transformed into `<iframe>` tags before printing.</span></span> <span data-ttu-id="53d11-140">Además de la diferencia normal entre Mostrar en pantalla y representarse para impresión, los estilos CSS aplicados a `<iframe>` elementos se aplican a los elementos `<iframe>` transformados `<x-ms-webview>` .</span><span class="sxs-lookup"><span data-stu-id="53d11-140">Besides the normal difference between displaying on screen and rendered for print, CSS styles applied to `<iframe>` elements are then applicable to the `<iframe>` transformed from `<x-ms-webview>`.</span></span>

### <span data-ttu-id="53d11-141">Trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="53d11-141">Service workers</span></span>

<span data-ttu-id="53d11-142">A partir de la [actualización de 2018 de octubre de Windows](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [los trabajos de servicio se admiten en el control WebView](/microsoft-edge/dev-guide#service-workers) (además de en el explorador Microsoft Edge y las aplicaciones de Windows 10 con JavaScript).</span><span class="sxs-lookup"><span data-stu-id="53d11-142">Starting with the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [service workers are supported in the WebView control](/microsoft-edge/dev-guide#service-workers) (in addition to the Microsoft Edge browser and Windows 10 apps with JavaScript).</span></span>

<span data-ttu-id="53d11-143">Las arquitecturas de aplicaciones x64 requieren paquetes neutros (cualquier CPU) o x64, ya que los trabajos de servicio no son compatibles con los procesos de WoW64.</span><span class="sxs-lookup"><span data-stu-id="53d11-143">x64 app architectures require Neutral (Any CPU) or x64 packages, as service workers are not supported in WoW64 processes.</span></span> <span data-ttu-id="53d11-144">(Para ahorrar espacio en el disco, la versión de WoW de los archivos dll necesarios no se incluye de forma nativa en Windows).</span><span class="sxs-lookup"><span data-stu-id="53d11-144">(To conserve disk space, the WoW version of the required DLLs are not natively included in Windows.)</span></span>

### <span data-ttu-id="53d11-145">Confiabilidad y modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="53d11-145">Threading model and reliability</span></span>

<span data-ttu-id="53d11-146">Al crear una vista previa mediante `document.createElement("x-ms-webview")` marcado o mediante marcado, se `<x-ms-webview>` crea una vista previa en un nuevo hilo único en el proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53d11-146">Creating a WebView via `document.createElement("x-ms-webview")` or via `<x-ms-webview>` markup creates a WebView on a new unique thread in the app's process.</span></span> <span data-ttu-id="53d11-147">La ejecución de un nuevo subproceso único significa que el script en ejecución prolongada de un WebView no puede bloquear la aplicación ni otras vistas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53d11-147">Running on a new unique thread means that long running script from one WebView is unable to hang the app or other WebViews.</span></span> <span data-ttu-id="53d11-148">Al crear una vista previa mediante el constructor, se `new MSWebView()` crea una vista previa en un proceso de WebView independiente.</span><span class="sxs-lookup"><span data-stu-id="53d11-148">Creating a WebView via the `new MSWebView()` constructor creates a WebView in a separate WebView process.</span></span> <span data-ttu-id="53d11-149">Ejecutarse en un único proceso significa que además de protegerse del script de larga ejecución, la aplicación también está protegida contra contenido web que bloquea el proceso de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-149">Running in a unique process means that in addition to protection from long running script, the app is also protected from web content that crashes the WebView process.</span></span> <span data-ttu-id="53d11-150">Crear una vista previa mediante el [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) método también crea WebView en un proceso independiente, pero permite que la persona que llama tenga más control sobre la configuración de procesos y la agrupación de Webviews en procesos de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-150">Creating a WebView via the [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) method also creates a WebView in a separate process but allows the caller more control over process settings and grouping WebViews in WebView processes.</span></span> <span data-ttu-id="53d11-151">Vea `MSWebViewProcess` para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="53d11-151">See `MSWebViewProcess` for more information.</span></span> 

### <span data-ttu-id="53d11-152">Acceso API a WinRT</span><span class="sxs-lookup"><span data-stu-id="53d11-152">WinRT API access</span></span>

<span data-ttu-id="53d11-153">Una aplicación para UWP puede permitir que los documentos HTML dentro de las vistas previas tengan acceso a las API de WinRT.</span><span class="sxs-lookup"><span data-stu-id="53d11-153">A UWP app may allow HTML documents inside WebViews to have access to WinRT APIs.</span></span> <span data-ttu-id="53d11-154">Esto se realiza a través del atributo WindowsRuntimeAccess de los elementos secundarios Rule del elemento ApplicationContentUriRules del AppxManifest. XML de la aplicación para UWP.</span><span class="sxs-lookup"><span data-stu-id="53d11-154">This is via the WindowsRuntimeAccess attribute of the Rule child elements of the ApplicationContentUriRules element of the AppxManifest.xml of the UWP app.</span></span> <span data-ttu-id="53d11-155">Establezca WindowsRuntimeAccess en "todos" y los documentos HTML con URI coincidentes podrán usar WinRT.</span><span class="sxs-lookup"><span data-stu-id="53d11-155">Set WindowsRuntimeAccess to 'all' and HTML documents with matching URIs will be allowed to use WinRT.</span></span> <span data-ttu-id="53d11-156">Esto es lo mismo que proporcionar acceso a WinRT a contenido HTML en aplicaciones para UWP de JavaScript, así que consulta [llamar a las API de WinRT de tu PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="53d11-156">This is the same as providing WinRT access to HTML content in JavaScript UWP apps so see [Call WinRT APIs from your PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) for more information.</span></span>

<span data-ttu-id="53d11-157">Es posible que las API de WinRT relacionadas con la interfaz de usuario no funcionen cuando se les llame desde una vista previa ejecutándose en su propio subproceso, pero puede funcionar cuando se le llama desde una vista previa que se ejecuta en un proceso WebView independiente.</span><span class="sxs-lookup"><span data-stu-id="53d11-157">UI related WinRT APIs may not work when called from a WebView running on its own thread but may work when called from a WebView running in a separate WebView process.</span></span> <span data-ttu-id="53d11-158">Al usar una vista previa en su propio subproceso, ese subproceso no es el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53d11-158">When using a WebView on its own unique thread, that thread is not the app's view thread.</span></span> <span data-ttu-id="53d11-159">Algunas API de WinRT relacionadas con la interfaz de usuario deben llamarse desde el subproceso de la vista de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53d11-159">Some UI related WinRT APIs require to be called from the app's view thread.</span></span> <span data-ttu-id="53d11-160">Las vistas en vista previa creadas en un proceso de WebView independiente se ejecutan en un subproceso de vista y, por lo tanto, no deberían enfrentar las mismas restricciones que la vista de WebView en su propio subproceso.</span><span class="sxs-lookup"><span data-stu-id="53d11-160">WebViews created in a separate WebView process do run on a view thread and so should not face the same restrictions as WebView's running on their own unique thread.</span></span> <span data-ttu-id="53d11-161">Si tienes problemas con las API de WinRT relacionadas con la interfaz de usuario en una vista previa, asegúrate de estar usando una vista previa en su propio proceso de WebView, tal y como se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="53d11-161">If you have trouble with UI related WinRT APIs in a WebView ensure that you're using a WebView in its own WebView process as described above.</span></span>

### <span data-ttu-id="53d11-162">Limitaciones de almacenamiento de AppCache</span><span class="sxs-lookup"><span data-stu-id="53d11-162">AppCache storage limitations</span></span>

<span data-ttu-id="53d11-163">Las aplicaciones que usan la compatibilidad de JavaScript de la API de caché de la aplicación (o AppCache), según se define en la [especificación HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), para crear aplicaciones web sin conexión deben observar las limitaciones de almacenamiento disponibles.</span><span class="sxs-lookup"><span data-stu-id="53d11-163">Applications using JavaScript support of the Application Cache API (or AppCache), as defined in the [HTML5 specification](https://go.microsoft.com/fwlink/p/?LinkId=228542), to create offline web applications must observe available storage limitations.</span></span> <span data-ttu-id="53d11-164">Esto es especialmente cierto en dispositivos con espacio de memoria limitado.</span><span class="sxs-lookup"><span data-stu-id="53d11-164">This is especially true in devices with limited memory space.</span></span> <span data-ttu-id="53d11-165">Los límites prácticos del tamaño de las AppCache siempre son una función del espacio de almacenamiento disponible en disco.</span><span class="sxs-lookup"><span data-stu-id="53d11-165">The practical limits on the size of the AppCache are always a function of available disk storage space.</span></span> <span data-ttu-id="53d11-166">A continuación se muestran las directrices generales.</span><span class="sxs-lookup"><span data-stu-id="53d11-166">The general guidelines are shown below.</span></span>

| <span data-ttu-id="53d11-167">Tamaño del volumen</span><span class="sxs-lookup"><span data-stu-id="53d11-167">Volume size</span></span>         |<span data-ttu-id="53d11-168">AppCache por dominio</span><span class="sxs-lookup"><span data-stu-id="53d11-168">AppCache per domain</span></span> | <span data-ttu-id="53d11-169">AppCache por usuario</span><span class="sxs-lookup"><span data-stu-id="53d11-169">AppCache per user</span></span>   | 
|---------------|---------------|-------------------------|
<span data-ttu-id="53d11-170">Hasta 4 GB</span><span class="sxs-lookup"><span data-stu-id="53d11-170">Up to 4GB</span></span> | <span data-ttu-id="53d11-171">10MB</span><span class="sxs-lookup"><span data-stu-id="53d11-171">10MB</span></span> | <span data-ttu-id="53d11-172">50MB</span><span class="sxs-lookup"><span data-stu-id="53d11-172">50MB</span></span> |
<span data-ttu-id="53d11-173">4GB a 16 GB</span><span class="sxs-lookup"><span data-stu-id="53d11-173">4GB to 16GB</span></span> | <span data-ttu-id="53d11-174">50MB</span><span class="sxs-lookup"><span data-stu-id="53d11-174">50MB</span></span> | <span data-ttu-id="53d11-175">CERCA</span><span class="sxs-lookup"><span data-stu-id="53d11-175">500MB</span></span> | 
<span data-ttu-id="53d11-176">de 16 GB a 32 GB</span><span class="sxs-lookup"><span data-stu-id="53d11-176">16GB to 32 GB</span></span> | <span data-ttu-id="53d11-177">50MB</span><span class="sxs-lookup"><span data-stu-id="53d11-177">50MB</span></span> | <span data-ttu-id="53d11-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="53d11-178">1GB</span></span> |

<span data-ttu-id="53d11-179">Todas las aplicaciones de Windows10 se han diseñado para usar el mismo modelo de cuota de AppCache, por lo que se aplica la limitación de almacenamiento en disco disponible a las aplicaciones de escritorio y de teléfono.</span><span class="sxs-lookup"><span data-stu-id="53d11-179">All Windows10 apps are intended to use the same AppCache quota model, so the available disk storage limitation applies to both desktop and phone apps.</span></span> <span data-ttu-id="53d11-180">El es también un límite rígido después de que las páginas cargadas en la **vista** Web juntos hayan consumido 1 GB de espacio en *AppCache* ; se denegarán las solicitudes de almacenamiento adicional de *AppCache* por encima de este límite.</span><span class="sxs-lookup"><span data-stu-id="53d11-180">The is also a hard limit after pages loaded inside **WebView** together have consumed 1 GB of *AppCache* space; requests for additional *AppCache* storage above this limit will be denied.</span></span> 

<span data-ttu-id="53d11-181">Para obtener más información, consulta el [ejemplo de control WebView HTML](https://go.microsoft.com/fwlink/p/?linkid=309825) y el JSBrowser de la documentación de [control WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .</span><span class="sxs-lookup"><span data-stu-id="53d11-181">For more information, see the [HTML WebView control sample](https://go.microsoft.com/fwlink/p/?linkid=309825) and the JSBrowser's [Harnessing the WebView control](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) documentation.</span></span>

## <span data-ttu-id="53d11-182">Eventos</span><span class="sxs-lookup"><span data-stu-id="53d11-182">Events</span></span>

### <span data-ttu-id="53d11-183">departingFocus</span><span class="sxs-lookup"><span data-stu-id="53d11-183">departingFocus</span></span>

<span data-ttu-id="53d11-184">Indica que el foco va de la **vista** web a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53d11-184">Indicates focus departing from the **webview** into the app.</span></span> <span data-ttu-id="53d11-185">Se desencadena cuando la ventana de llamadas de nivel superior de la vista de vistas de WebView. departFocus.</span><span class="sxs-lookup"><span data-stu-id="53d11-185">Fires when the webview's top level document calls window.departFocus.</span></span> <span data-ttu-id="53d11-186">Los argumentos FocusNavigationEvent en el evento departingFocus coinciden con los parámetros proporcionados a departFocus excepto que los parámetros de origen se traducen desde el espacio de coordenadas de document's de WebView al espacio de coordenadas del documento host de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-186">The FocusNavigationEvent args in the departingFocus event match the parameters provided to departFocus except the origin parameters are translated from the webview's document's coordinate space to the coordinate space of the webview host document.</span></span> <span data-ttu-id="53d11-187">Consulta el método WebView. navigateFocus y el evento de navigatingFocus de la ventana correspondiente para transferir el foco del host a la vista de ventana.</span><span class="sxs-lookup"><span data-stu-id="53d11-187">See the webview.navigateFocus method and corresponding window navigatingFocus event for transferring focus from host to webview.</span></span> <span data-ttu-id="53d11-188">Consulte la [biblioteca de navegación dirección de TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obtener un ejemplo de una implementación de la navegación de foco mediante un teclado o un controlador para juegos que controla este evento.</span><span class="sxs-lookup"><span data-stu-id="53d11-188">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that handles this event.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```

#### <span data-ttu-id="53d11-189">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-189">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-190">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-190">Interface</span></span>** | [<span data-ttu-id="53d11-191">FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-191">FocusNavigationEvent</span></span>](./webview/FocusNavigationEvent.md) |
|**<span data-ttu-id="53d11-192">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-192">Synchronous</span></span>** |<span data-ttu-id="53d11-193">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-193">Yes</span></span> |    
|**<span data-ttu-id="53d11-194">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-194">Bubbles</span></span>**     |<span data-ttu-id="53d11-195">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-195">Yes</span></span> |   
|**<span data-ttu-id="53d11-196">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-196">Cancelable</span></span>**  |<span data-ttu-id="53d11-197">No</span><span class="sxs-lookup"><span data-stu-id="53d11-197">No</span></span> |            

### <span data-ttu-id="53d11-198">MSWebViewContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="53d11-198">MSWebViewContainsFullScreenElementChanged</span></span>

<span data-ttu-id="53d11-199">Se produce cuando el estado cambia para si la **vista previa** contiene o no un elemento de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="53d11-199">Occurs when the status changes of whether or not the **webview** currently contains a full screen element.</span></span> <span data-ttu-id="53d11-200">Use la propiedad containsFullScreenElement para el valor actual.</span><span class="sxs-lookup"><span data-stu-id="53d11-200">Use the containsFullScreenElement property to the current value.</span></span> <span data-ttu-id="53d11-201">Elemento de pantalla completa aquí se hace referencia a la noción de [API Dom](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) en pantalla completa de un elemento de pantalla completa a través de las funciones Element. requestFullScreen y Document. exitFullScreen Dom.</span><span class="sxs-lookup"><span data-stu-id="53d11-201">Full screen element here refers to the [Fullscreen DOM APIs](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) notion of a full screen element via the element.requestFullScreen and document.exitFullScreen DOM functions.</span></span>

```js
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```

#### <span data-ttu-id="53d11-202">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-202">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-203">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-203">Interface</span></span>** | **<span data-ttu-id="53d11-204">Evento</span><span class="sxs-lookup"><span data-stu-id="53d11-204">Event</span></span>** |
|**<span data-ttu-id="53d11-205">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-205">Synchronous</span></span>** |<span data-ttu-id="53d11-206">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-206">Yes</span></span> |    
|**<span data-ttu-id="53d11-207">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-207">Bubbles</span></span>**     |<span data-ttu-id="53d11-208">No</span><span class="sxs-lookup"><span data-stu-id="53d11-208">No</span></span> |   
|**<span data-ttu-id="53d11-209">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-209">Cancelable</span></span>**  |<span data-ttu-id="53d11-210">No</span><span class="sxs-lookup"><span data-stu-id="53d11-210">No</span></span> |  

### <span data-ttu-id="53d11-211">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="53d11-211">MSWebViewContentLoading</span></span>

<span data-ttu-id="53d11-212">Indica que el contenido HTML se descarga y se carga en el control.</span><span class="sxs-lookup"><span data-stu-id="53d11-212">Indicates that the HTML content is downloaded and is being loaded into the control.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```

#### <span data-ttu-id="53d11-213">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-213">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-214">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-214">Interface</span></span>** | [<span data-ttu-id="53d11-215">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-215">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="53d11-216">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-216">Synchronous</span></span>** |<span data-ttu-id="53d11-217">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-217">Yes</span></span>  |    
|**<span data-ttu-id="53d11-218">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-218">Bubbles</span></span>**     |<span data-ttu-id="53d11-219">No</span><span class="sxs-lookup"><span data-stu-id="53d11-219">No</span></span> |   
|**<span data-ttu-id="53d11-220">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-220">Cancelable</span></span>**  |<span data-ttu-id="53d11-221">No</span><span class="sxs-lookup"><span data-stu-id="53d11-221">No</span></span> |    

### <span data-ttu-id="53d11-222">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="53d11-222">MSWebViewDOMContentLoaded</span></span>

<span data-ttu-id="53d11-223">Indica que los elementos DOM principales han finalizado de cargarse.</span><span class="sxs-lookup"><span data-stu-id="53d11-223">Indicates that the main DOM elements have finished loading.</span></span>


```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```

#### <span data-ttu-id="53d11-224">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-224">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-225">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-225">Interface</span></span>** | [<span data-ttu-id="53d11-226">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-226">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="53d11-227">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-227">Synchronous</span></span>** |<span data-ttu-id="53d11-228">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-228">Yes</span></span>  |    
|**<span data-ttu-id="53d11-229">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-229">Bubbles</span></span>**     |<span data-ttu-id="53d11-230">No</span><span class="sxs-lookup"><span data-stu-id="53d11-230">No</span></span> |   
|**<span data-ttu-id="53d11-231">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-231">Cancelable</span></span>**  |<span data-ttu-id="53d11-232">No</span><span class="sxs-lookup"><span data-stu-id="53d11-232">No</span></span> |                 

### <span data-ttu-id="53d11-233">MSWebViewFrameContentLoading</span><span class="sxs-lookup"><span data-stu-id="53d11-233">MSWebViewFrameContentLoading</span></span>

<span data-ttu-id="53d11-234">Indica que el contenido HTML descargado y se carga en el `<iframe>` control.</span><span class="sxs-lookup"><span data-stu-id="53d11-234">Indicates that the HTML content downloaded and is being loaded into the `<iframe>` control.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```

#### <span data-ttu-id="53d11-235">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-235">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-236">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-236">Interface</span></span>** | [<span data-ttu-id="53d11-237">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-237">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="53d11-238">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-238">Synchronous</span></span>** |<span data-ttu-id="53d11-239">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-239">Yes</span></span>  |    
|**<span data-ttu-id="53d11-240">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-240">Bubbles</span></span>**     |<span data-ttu-id="53d11-241">No</span><span class="sxs-lookup"><span data-stu-id="53d11-241">No</span></span> |   
|**<span data-ttu-id="53d11-242">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-242">Cancelable</span></span>**  |<span data-ttu-id="53d11-243">No</span><span class="sxs-lookup"><span data-stu-id="53d11-243">No</span></span> |                 

### <span data-ttu-id="53d11-244">MSWebViewFrameDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="53d11-244">MSWebViewFrameDOMContentLoaded</span></span>

<span data-ttu-id="53d11-245">Indica que los elementos DOM principales han finalizado de cargarse en `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="53d11-245">Indicates that the main DOM elements have finished loading in the `<iframe>`.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```

#### <span data-ttu-id="53d11-246">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-246">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-247">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-247">Interface</span></span>** | [<span data-ttu-id="53d11-248">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-248">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="53d11-249">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-249">Synchronous</span></span>** |<span data-ttu-id="53d11-250">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-250">Yes</span></span>  |    
|**<span data-ttu-id="53d11-251">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-251">Bubbles</span></span>**     |<span data-ttu-id="53d11-252">No</span><span class="sxs-lookup"><span data-stu-id="53d11-252">No</span></span> |   
|**<span data-ttu-id="53d11-253">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-253">Cancelable</span></span>**  |<span data-ttu-id="53d11-254">No</span><span class="sxs-lookup"><span data-stu-id="53d11-254">No</span></span> |    


### <span data-ttu-id="53d11-255">MSWebViewFrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="53d11-255">MSWebViewFrameNavigationCompleted</span></span>

<span data-ttu-id="53d11-256">Indica que la navegación se ha completado y todos los elementos multimedia se representan en el `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="53d11-256">Indicates the navigation is complete, and all media elements are rendered in the `<iframe>`.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```

#### <span data-ttu-id="53d11-257">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-257">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-258">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-258">Interface</span></span>** | [<span data-ttu-id="53d11-259">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-259">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |
|**<span data-ttu-id="53d11-260">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-260">Synchronous</span></span>** |<span data-ttu-id="53d11-261">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-261">Yes</span></span> |    
|**<span data-ttu-id="53d11-262">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-262">Bubbles</span></span>**     |<span data-ttu-id="53d11-263">No</span><span class="sxs-lookup"><span data-stu-id="53d11-263">No</span></span> |   
|**<span data-ttu-id="53d11-264">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-264">Cancelable</span></span>**  |<span data-ttu-id="53d11-265">No</span><span class="sxs-lookup"><span data-stu-id="53d11-265">No</span></span> |       

### <span data-ttu-id="53d11-266">MSWebViewFrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="53d11-266">MSWebViewFrameNavigationStarting</span></span>

<span data-ttu-id="53d11-267">Indica `<iframe>` que una en un **WebView** está empezando a navegar.</span><span class="sxs-lookup"><span data-stu-id="53d11-267">Indicates a `<iframe>` within a **webview** is starting to navigate.</span></span> <span data-ttu-id="53d11-268">Esto se activa antes de obtener los recursos de la red para la navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-268">This is fired before obtaining any resources from the network for the navigation.</span></span> <span data-ttu-id="53d11-269">La navegación no se inicia hasta que se completan todos los controladores de eventos de MSWebViewFrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="53d11-269">The navigation is not started until all MSWebViewFrameNavigationStarting event handlers complete.</span></span> <span data-ttu-id="53d11-270">Este evento se encuentra cancelable por medio de llamadas `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="53d11-270">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span> <span data-ttu-id="53d11-271">Si se cancela, WebView no realizará la navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-271">If cancelled, the WebView will not perform the navigation.</span></span>


```js
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```

#### <span data-ttu-id="53d11-272">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-272">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-273">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-273">Interface</span></span>** | [<span data-ttu-id="53d11-274">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-274">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="53d11-275">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-275">Synchronous</span></span>** |<span data-ttu-id="53d11-276">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-276">Yes</span></span>  |    
|**<span data-ttu-id="53d11-277">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-277">Bubbles</span></span>**     |<span data-ttu-id="53d11-278">No</span><span class="sxs-lookup"><span data-stu-id="53d11-278">No</span></span> |   
|**<span data-ttu-id="53d11-279">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-279">Cancelable</span></span>**  |<span data-ttu-id="53d11-280">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-280">Yes</span></span> |                 
          
### <span data-ttu-id="53d11-281">MSWebViewLongRunningScriptDetected</span><span class="sxs-lookup"><span data-stu-id="53d11-281">MSWebViewLongRunningScriptDetected</span></span>

<span data-ttu-id="53d11-282">Se produce de forma periódica durante la ejecución de scripts sin interrupciones en la **vista de WebView**y permite detener el script.</span><span class="sxs-lookup"><span data-stu-id="53d11-282">Occurs periodically during uninterrupted script execution in the **webview**, letting you halt the script.</span></span>

```js
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```

#### <span data-ttu-id="53d11-283">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-283">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-284">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-284">Interface</span></span>** | [<span data-ttu-id="53d11-285">LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-285">LongRunningScriptDetectedEvent</span></span>](./webview/LongRunningScriptDetectedEvent.md) |
|**<span data-ttu-id="53d11-286">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-286">Synchronous</span></span>** |<span data-ttu-id="53d11-287">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-287">Yes</span></span> |    
|**<span data-ttu-id="53d11-288">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-288">Bubbles</span></span>**     |<span data-ttu-id="53d11-289">No</span><span class="sxs-lookup"><span data-stu-id="53d11-289">No</span></span> |   
|**<span data-ttu-id="53d11-290">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-290">Cancelable</span></span>**  |<span data-ttu-id="53d11-291">No</span><span class="sxs-lookup"><span data-stu-id="53d11-291">No</span></span> |            

### <span data-ttu-id="53d11-292">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="53d11-292">MSWebViewNavigationCompleted</span></span>

<span data-ttu-id="53d11-293">Indica que la navegación se ha completado y todos los elementos multimedia se han procesado o se ha producido un error de navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-293">Indicates the navigation is complete, and all media elements are rendered or there was a navigation error.</span></span> <span data-ttu-id="53d11-294">Compruebe la propiedad argumentos de evento isSuccess para saber si la navegación se realizó correctamente y la propiedad webErrorStatus para obtener información sobre el error de navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-294">Check the event args isSuccess property to tell if the navigation was successful and the webErrorStatus property for details on the navigation error.</span></span> <span data-ttu-id="53d11-295">Es posible que se produzcan errores de navegación antes de obtener contenido de la red por ejemplo, si el nombre de host de un URI no se resuelve en ese caso, el evento MSWebViewNavigationStarted se desencadenará seguido del evento MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="53d11-295">Navigation errors can occur before obtaining any content from the network for instance if the hostname of a URI does not resolve in which case the MSWebViewNavigationStarted event will fire followed by the MSWebViewNavigationCompleted event.</span></span> <span data-ttu-id="53d11-296">Los errores de navegación también pueden producirse después de recibir una página de error de un servidor Web, por ejemplo, una página de 404 de un servidor HTTP en cuyo caso todos los eventos de navegación se desencadenarán, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded y MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="53d11-296">Navigation errors may also occur after receiving an error page from a web server, for instance a 404 page from an HTTP server in which case all navigation events will fire, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, and then MSWebViewNavigationCompleted.</span></span> <span data-ttu-id="53d11-297">Para proporcionar una página de error de navegación de la aplicación para los casos en los que el servidor Web no ha proporcionado una página de error, debe comprobar si MSWebViewContentLoading se ha activado para una navegación fallida que indica que no se ha proporcionado ninguna página de error del servidor.</span><span class="sxs-lookup"><span data-stu-id="53d11-297">To provide an app navigation error page for cases where the web server hasn't provided an error page, you'll need to check if MSWebViewContentLoading hasn't fired for a failed navigation which indicates there is no server provided error page.</span></span>

```js
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```

#### <span data-ttu-id="53d11-298">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-298">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-299">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-299">Interface</span></span>** | [<span data-ttu-id="53d11-300">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-300">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |
|**<span data-ttu-id="53d11-301">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-301">Synchronous</span></span>** |<span data-ttu-id="53d11-302">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-302">Yes</span></span>  |    
|**<span data-ttu-id="53d11-303">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-303">Bubbles</span></span>**     |<span data-ttu-id="53d11-304">No</span><span class="sxs-lookup"><span data-stu-id="53d11-304">No</span></span> |   
|**<span data-ttu-id="53d11-305">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-305">Cancelable</span></span>**  |<span data-ttu-id="53d11-306">No</span><span class="sxs-lookup"><span data-stu-id="53d11-306">No</span></span> |                 
         

### <span data-ttu-id="53d11-307">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="53d11-307">MSWebViewNavigationStarting</span></span>

<span data-ttu-id="53d11-308">Indica que la **vista en WebView** está empezando a navegar.</span><span class="sxs-lookup"><span data-stu-id="53d11-308">Indicates the **webview** is starting to navigate.</span></span> <span data-ttu-id="53d11-309">Esto se activa antes de obtener los recursos de la red para la navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-309">This is fired before obtaining any resources from the network for the navigation.</span></span> <span data-ttu-id="53d11-310">La navegación no se inicia hasta que se completan todos los controladores de eventos de MSWebViewNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="53d11-310">The navigation is not started until all MSWebViewNavigationStarting event handlers complete.</span></span> <span data-ttu-id="53d11-311">Este evento se encuentra cancelable por medio de llamadas `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="53d11-311">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span> <span data-ttu-id="53d11-312">Si se cancela, WebView no realizará la navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-312">If cancelled, the WebView will not perform the navigation.</span></span>


```js
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```

#### <span data-ttu-id="53d11-313">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-313">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-314">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-314">Interface</span></span>** | [<span data-ttu-id="53d11-315">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-315">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="53d11-316">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-316">Synchronous</span></span>** |<span data-ttu-id="53d11-317">No</span><span class="sxs-lookup"><span data-stu-id="53d11-317">No</span></span>  |    
|**<span data-ttu-id="53d11-318">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-318">Bubbles</span></span>**     |<span data-ttu-id="53d11-319">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-319">Yes</span></span> |   
|**<span data-ttu-id="53d11-320">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-320">Cancelable</span></span>**  |<span data-ttu-id="53d11-321">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-321">Yes</span></span> |      

### <span data-ttu-id="53d11-322">MSWebViewNewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="53d11-322">MSWebViewNewWindowRequested</span></span>

<span data-ttu-id="53d11-323">Se genera cuando el contenido de **WebView** está intentando abrir una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="53d11-323">Raised when content in **webview** is trying to open a new window.</span></span> <span data-ttu-id="53d11-324">Si el evento no se cancela, WebView iniciará el URI de la nueva solicitud de ventana en el explorador predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="53d11-324">If the event isn't cancelled the webview will launch the URI of the new window request in the user's default browser.</span></span>

```js
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```

#### <span data-ttu-id="53d11-325">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-325">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-326">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-326">Interface</span></span>** | [<span data-ttu-id="53d11-327">NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="53d11-327">NavigationEventWithReferrer</span></span>](./webview/NavigationEventWithReferrer.md) |
|**<span data-ttu-id="53d11-328">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-328">Synchronous</span></span>** |<span data-ttu-id="53d11-329">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-329">Yes</span></span>  |    
|**<span data-ttu-id="53d11-330">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-330">Bubbles</span></span>**     |<span data-ttu-id="53d11-331">No</span><span class="sxs-lookup"><span data-stu-id="53d11-331">No</span></span> |   
|**<span data-ttu-id="53d11-332">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-332">Cancelable</span></span>**  |<span data-ttu-id="53d11-333">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-333">Yes</span></span> |                 
           

### <span data-ttu-id="53d11-334">MSWebViewPermissionRequested</span><span class="sxs-lookup"><span data-stu-id="53d11-334">MSWebViewPermissionRequested</span></span>

<span data-ttu-id="53d11-335">Indica que el contenido de la **vista en WebView** está intentando acceder a funcionalidades (como el acceso de bloqueo de puntero) que normalmente requiere permisos de usuario final.</span><span class="sxs-lookup"><span data-stu-id="53d11-335">Indicates that content in the **webview**  is trying to access functionality (such as geolocation, or pointer lock access) that normally requires end-user permissions.</span></span> <span data-ttu-id="53d11-336">Si no hay ningún controlador de eventos registrado o si el controlador de eventos no llama a eventArgs. permissionRequest. allow (), defer () o Deny (), se denegará la solicitud de permiso de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="53d11-336">If no event handler is registered or if the event handler doesn't call eventArgs.permissionRequest.allow(), defer(), or deny(), then by default the permission request will be denied.</span></span> <span data-ttu-id="53d11-337">Si necesita decidir si el permiso está permitido o denegado de forma asincrónica por ejemplo, si necesita solicitar la intervención del usuario, use eventArgs. permissionRequest. defer ().</span><span class="sxs-lookup"><span data-stu-id="53d11-337">If you need to decide if permission is allowed or denied asynchronously for instance if you need to prompt the user, use eventArgs.permissionRequest.defer().</span></span> <span data-ttu-id="53d11-338">La solicitud de permiso se aplazará hasta que uses WebView. getDeferredPermissionRequestById o WebView. getDeferredPermissionRequests y llame a allow () o Deny () en la DeferredPermissionRequest con el valor de ID correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53d11-338">The permission request will be deferred until you use webview.getDeferredPermissionRequestById or webview.getDeferredPermissionRequests and call allow() or deny() on the DeferredPermissionRequest with the corresponding id value.</span></span>

```js
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```

#### <span data-ttu-id="53d11-339">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-339">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-340">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-340">Interface</span></span>** | [<span data-ttu-id="53d11-341">PermissionRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-341">PermissionRequestedEvent</span></span>](./webview/PermissionRequestedEvent.md) |
|**<span data-ttu-id="53d11-342">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-342">Synchronous</span></span>** |<span data-ttu-id="53d11-343">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-343">Yes</span></span>  |    
|**<span data-ttu-id="53d11-344">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-344">Bubbles</span></span>**     |<span data-ttu-id="53d11-345">No</span><span class="sxs-lookup"><span data-stu-id="53d11-345">No</span></span> |   
|**<span data-ttu-id="53d11-346">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-346">Cancelable</span></span>**  |<span data-ttu-id="53d11-347">No</span><span class="sxs-lookup"><span data-stu-id="53d11-347">No</span></span> |    


### <span data-ttu-id="53d11-348">MSWebViewProcessExited</span><span class="sxs-lookup"><span data-stu-id="53d11-348">MSWebViewProcessExited</span></span>

<span data-ttu-id="53d11-349">Indica que el proceso del componente **WebView** se bloqueó.</span><span class="sxs-lookup"><span data-stu-id="53d11-349">Indicates that the **webview** component process crashsed.</span></span> <span data-ttu-id="53d11-350">Esto solo es relevante para una vista previa fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="53d11-350">This is only relevant for an out-of-process WebView.</span></span> <span data-ttu-id="53d11-351">Vea la sección de comentarios sobre cómo crear una WebView fuera de proceso en lugar de una vista previa en proceso.</span><span class="sxs-lookup"><span data-stu-id="53d11-351">See the Remarks section for how to create an out-of-process WebView as opposed to an in-process WebView.</span></span> <span data-ttu-id="53d11-352">Después de que este evento se desencadene, la vista previa correspondiente se pone en un estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="53d11-352">After this event fires, the corresponding WebView is put into a crashed state.</span></span> <span data-ttu-id="53d11-353">Si llamas a la mayoría de los métodos específicos de WebView o accedes a la mayoría de las propiedades específicas de WebView en una WebView bloqueada, se iniciará una excepción.</span><span class="sxs-lookup"><span data-stu-id="53d11-353">Calling most WebView specific methods or accessing most WebView specific properties on a crashed WebView will throw an exception.</span></span> <span data-ttu-id="53d11-354">Para recuperar a partir de este evento, quite la vista previa bloqueada del DOM y sustitúyala por una nueva vista previa.</span><span class="sxs-lookup"><span data-stu-id="53d11-354">To recover from this event, remove the crashed WebView from the DOM and replace it with a new WebView.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```

#### <span data-ttu-id="53d11-355">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-355">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-356">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-356">Interface</span></span>** | **<span data-ttu-id="53d11-357">Evento</span><span class="sxs-lookup"><span data-stu-id="53d11-357">Event</span></span>** |
|**<span data-ttu-id="53d11-358">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-358">Synchronous</span></span>** |<span data-ttu-id="53d11-359">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-359">Yes</span></span> |    
|**<span data-ttu-id="53d11-360">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-360">Bubbles</span></span>**     |<span data-ttu-id="53d11-361">No</span><span class="sxs-lookup"><span data-stu-id="53d11-361">No</span></span> |   
|**<span data-ttu-id="53d11-362">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-362">Cancelable</span></span>**  |<span data-ttu-id="53d11-363">No</span><span class="sxs-lookup"><span data-stu-id="53d11-363">No</span></span> |      


### <span data-ttu-id="53d11-364">MSWebViewWebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="53d11-364">MSWebViewWebResourceRequested</span></span>

<span data-ttu-id="53d11-365">Se genera cuando una página del elemento **WebView** solicita un recurso.</span><span class="sxs-lookup"><span data-stu-id="53d11-365">Raised when a page inside the **webview** element requests a resource.</span></span>

```js
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```

#### <span data-ttu-id="53d11-366">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-366">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-367">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-367">Interface</span></span>** | [<span data-ttu-id="53d11-368">WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-368">WebResourceRequestedEvent</span></span>](./webview/WebResourceRequestedEvent.md) |
|**<span data-ttu-id="53d11-369">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-369">Synchronous</span></span>** |<span data-ttu-id="53d11-370">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-370">Yes</span></span> |    
|**<span data-ttu-id="53d11-371">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-371">Bubbles</span></span>**     |<span data-ttu-id="53d11-372">No</span><span class="sxs-lookup"><span data-stu-id="53d11-372">No</span></span> |   
|**<span data-ttu-id="53d11-373">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-373">Cancelable</span></span>**  |<span data-ttu-id="53d11-374">No</span><span class="sxs-lookup"><span data-stu-id="53d11-374">No</span></span> |      


### <span data-ttu-id="53d11-375">MSWebViewScriptNotify</span><span class="sxs-lookup"><span data-stu-id="53d11-375">MSWebViewScriptNotify</span></span>

<span data-ttu-id="53d11-376">Se genera cuando una página dentro del elemento **WebView** llama al método **window. external. Notify** .</span><span class="sxs-lookup"><span data-stu-id="53d11-376">Raised when a page inside the **webview** element calls the **window.external.notify** method.</span></span> <span data-ttu-id="53d11-377">El método window. external. Notify solo está disponible para los documentos con URI que coinciden con las reglas del manifest's ApplicationContentUriRules de la aplicación o que se ha permitido mediante programación mediante la configuración de WebView. Settings. isScriptNotifyAllowed en true.</span><span class="sxs-lookup"><span data-stu-id="53d11-377">The window.external.notify method is only available to documents with URIs that match rules in the app's manifest's ApplicationContentUriRules or that has been programatically allowed via setting webview.settings.isScriptNotifyAllowed to true.</span></span> <span data-ttu-id="53d11-378">Además, Window. external. Notify solo está disponible para el documento de nivel superior de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-378">Additionally window.external.notify is only available to the webview's top level document.</span></span>

```js
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```

#### <span data-ttu-id="53d11-379">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-379">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-380">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-380">Interface</span></span>** | [<span data-ttu-id="53d11-381">ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-381">ScriptNotifyEvent</span></span>](./webview/ScriptNotifyEvent.md) |
|**<span data-ttu-id="53d11-382">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-382">Synchronous</span></span>** |<span data-ttu-id="53d11-383">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-383">Yes</span></span>  |    
|**<span data-ttu-id="53d11-384">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-384">Bubbles</span></span>**     |<span data-ttu-id="53d11-385">No</span><span class="sxs-lookup"><span data-stu-id="53d11-385">No</span></span> |   
|**<span data-ttu-id="53d11-386">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-386">Cancelable</span></span>**  |<span data-ttu-id="53d11-387">No</span><span class="sxs-lookup"><span data-stu-id="53d11-387">No</span></span> |      

### <span data-ttu-id="53d11-388">MSWebViewUnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="53d11-388">MSWebViewUnsafeContentWarningDisplaying</span></span>

<span data-ttu-id="53d11-389">Se produce cuando la **vista** Web muestra una página de advertencia para el contenido notificado como no seguro por Filtro SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="53d11-389">Occurs when the **webview** shows a warning page for content that was reported as unsafe by SmartScreen Filter.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```

#### <span data-ttu-id="53d11-390">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-390">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-391">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-391">Interface</span></span>** | **<span data-ttu-id="53d11-392">Evento</span><span class="sxs-lookup"><span data-stu-id="53d11-392">Event</span></span>** |
|**<span data-ttu-id="53d11-393">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-393">Synchronous</span></span>** |<span data-ttu-id="53d11-394">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-394">Yes</span></span> |    
|**<span data-ttu-id="53d11-395">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-395">Bubbles</span></span>**     |<span data-ttu-id="53d11-396">No</span><span class="sxs-lookup"><span data-stu-id="53d11-396">No</span></span> |   
|**<span data-ttu-id="53d11-397">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-397">Cancelable</span></span>**  |<span data-ttu-id="53d11-398">No</span><span class="sxs-lookup"><span data-stu-id="53d11-398">No</span></span> |    

### <span data-ttu-id="53d11-399">MSWebViewUnsupportedUriSchemeIdentified</span><span class="sxs-lookup"><span data-stu-id="53d11-399">MSWebViewUnsupportedUriSchemeIdentified</span></span>

<span data-ttu-id="53d11-400">Se genera cuando hay navegación en un identificador de recursos uniforme (URI) que no es compatible con **WebView** .</span><span class="sxs-lookup"><span data-stu-id="53d11-400">Raised when there is navigation to an Uniform Resource Identifier (URI) that the **webview** does not support.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```

#### <span data-ttu-id="53d11-401">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-401">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-402">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-402">Interface</span></span>** | [<span data-ttu-id="53d11-403">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-403">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="53d11-404">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-404">Synchronous</span></span>** |<span data-ttu-id="53d11-405">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-405">Yes</span></span>  |    
|**<span data-ttu-id="53d11-406">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-406">Bubbles</span></span>**     |<span data-ttu-id="53d11-407">No</span><span class="sxs-lookup"><span data-stu-id="53d11-407">No</span></span> |   
|**<span data-ttu-id="53d11-408">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-408">Cancelable</span></span>**  |<span data-ttu-id="53d11-409">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-409">Yes</span></span> |     

### <span data-ttu-id="53d11-410">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="53d11-410">MSWebViewUnviewableContentIdentified</span></span>

<span data-ttu-id="53d11-411">Se genera cuando la **vista** Web intenta navegar al contenido web con un tipo de contenido no admitido.</span><span class="sxs-lookup"><span data-stu-id="53d11-411">Raised when the **webview** attempts to navigate to web content with an unsupported content type.</span></span> <span data-ttu-id="53d11-412">Por ejemplo, los documentos PDF no son compatibles actualmente con WebView y los desplazamientos a documentos PDF no se desplazarán y provocarán este evento.</span><span class="sxs-lookup"><span data-stu-id="53d11-412">For example, PDFs are currently not supported by webview and navigations to PDF documents will not navigate and instead raise this event.</span></span>

```js
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```

#### <span data-ttu-id="53d11-413">Información del evento</span><span class="sxs-lookup"><span data-stu-id="53d11-413">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-414">Interfaz</span><span class="sxs-lookup"><span data-stu-id="53d11-414">Interface</span></span>** | [<span data-ttu-id="53d11-415">UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="53d11-415">UnviewableContentIdentifiedEvent</span></span>](./webview/UnviewableContentIdentifiedEvent.md) |
|**<span data-ttu-id="53d11-416">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="53d11-416">Synchronous</span></span>** |<span data-ttu-id="53d11-417">Sí</span><span class="sxs-lookup"><span data-stu-id="53d11-417">Yes</span></span>  |    
|**<span data-ttu-id="53d11-418">Pase</span><span class="sxs-lookup"><span data-stu-id="53d11-418">Bubbles</span></span>**     |<span data-ttu-id="53d11-419">No</span><span class="sxs-lookup"><span data-stu-id="53d11-419">No</span></span> |   
|**<span data-ttu-id="53d11-420">Cancelable</span><span class="sxs-lookup"><span data-stu-id="53d11-420">Cancelable</span></span>**  |<span data-ttu-id="53d11-421">No</span><span class="sxs-lookup"><span data-stu-id="53d11-421">No</span></span> |                 
         

## <span data-ttu-id="53d11-422">Métodos</span><span class="sxs-lookup"><span data-stu-id="53d11-422">Methods</span></span>

### <span data-ttu-id="53d11-423">addWebAllowedObject</span><span class="sxs-lookup"><span data-stu-id="53d11-423">addWebAllowedObject</span></span>

<span data-ttu-id="53d11-424">Agrega un objeto de Windows Runtime nativo como un parámetro global al documento de nivel superior dentro de un **WebView**.</span><span class="sxs-lookup"><span data-stu-id="53d11-424">Adds a native Windows Runtime object as a global parameter to the top-level document inside of a **webview**.</span></span>

<span data-ttu-id="53d11-425">El objeto no se inserta en el documento actual, sino en el siguiente documento de nivel superior al que navega la vista en la vista.</span><span class="sxs-lookup"><span data-stu-id="53d11-425">The object is not injected into the current document, but rather the next top-level document to which the webview navigates.</span></span> <span data-ttu-id="53d11-426">El objeto se inserta antes de que se ejecute cualquier script del documento HTML para que pueda basarse en el objeto en el script global del documento.</span><span class="sxs-lookup"><span data-stu-id="53d11-426">The object is injected before any script from the HTML document runs so you can rely on the object in your document's global script.</span></span>

<span data-ttu-id="53d11-427">Debes usar addWebAllowedObject durante un evento MSWebViewNavigationStarting o antes de llamar explícitamente a un método Navigate.</span><span class="sxs-lookup"><span data-stu-id="53d11-427">You should use addWebAllowedObject either during an MSWebViewNavigationStarting event or before explicitly calling a navigate method.</span></span> <span data-ttu-id="53d11-428">En estos casos, el objeto se inserta en el documento de la navegación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="53d11-428">In these cases the object is injected into the document of the corresponding navigation.</span></span> <span data-ttu-id="53d11-429">Si lo llama en algún otro contexto, no tiene una forma de estar seguro de qué documento inyectará.</span><span class="sxs-lookup"><span data-stu-id="53d11-429">Calling it in some other context, you don't have a way to be certain into what document you'll inject your object.</span></span>

<span data-ttu-id="53d11-430">Al llamar a addWebAllowedObject varias veces seguidas, se insertarán varios objetos en el documento.</span><span class="sxs-lookup"><span data-stu-id="53d11-430">Calling addWebAllowedObject multiple times in a row will inject multiple objects into the document.</span></span> <span data-ttu-id="53d11-431">Si llamas antes de una llamada de navegación explícita y luego de nuevo durante el evento MSWebViewNavigationStarting correspondiente, ambas llamadas se realizarán correctamente y tendrás varios objetos inyectados.</span><span class="sxs-lookup"><span data-stu-id="53d11-431">If you call it both before an explicit navigate call and then again during the corresponding MSWebViewNavigationStarting event, both calls will succeed and you'll have multiple objects injected.</span></span> <span data-ttu-id="53d11-432">Si llamas varias veces con el mismo parámetro de nombre, se ignorará la última llamada ganada y las llamadas anteriores con ese nombre.</span><span class="sxs-lookup"><span data-stu-id="53d11-432">If you call multiple times with the same name parameter, the last call wins and the previous calls with that name are ignored.</span></span>

<span data-ttu-id="53d11-433">Si se produce un error en la navegación o se redirige, las llamadas de addWebAllowedObject para esa navegación se omiten.</span><span class="sxs-lookup"><span data-stu-id="53d11-433">If a navigate fails or is redirected, the addWebAllowedObject calls for that navigation are ignored.</span></span> <span data-ttu-id="53d11-434">Si deseas controlar las redirecciones, puedes suscribirte al reloj de eventos de MSWebViewNavigationStarting de redireccionamientos y llamar de addWebAllowedObject de nuevo según los criterios que sean adecuados para tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="53d11-434">If you want to handle redirects you can subscribe to the MSWebViewNavigationStarting event watch for redirects and call addWebAllowedObject again according to whatever criteria is appropriate for your application.</span></span> <span data-ttu-id="53d11-435">De forma similar, una vez que un documento se desplaza fuera de los objetos insertados a través de addWebAllowedObject para ese documento, no pasará al siguiente documento y deberá llamar explícitamente a addWebAllowedObject si desea que los pasen.</span><span class="sxs-lookup"><span data-stu-id="53d11-435">Similarly, once a document navigates away any objects injected via addWebAllowedObject for that document will not carry over to the next document and you'll need to explicitly call addWebAllowedObject if you want them to carry over.</span></span>

<span data-ttu-id="53d11-436">Si llamas a addWebAllowedObject para un documento que no tiene acceso a WinRT de otro modo, o si tiene [AllowForWebOnly acceso a través de ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , el objeto solo se insertará si el objeto tiene el atributo Windows. Foundation. Metadata. AllowForWeb metadatos.</span><span class="sxs-lookup"><span data-stu-id="53d11-436">If you call addWebAllowedObject for a document that has no WinRT access otherwise, or if it has [AllowForWebOnly access via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) then the object will only be injected if the object has the Windows.Foundation.Metadata.AllowForWeb metadata attribute.</span></span> <span data-ttu-id="53d11-437">De lo contrario, no se producirá una inyección y se notificará un error a la consola del desarrollador de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="53d11-437">Otherwise injection will fail and an error will be reported to the JavaScript developer console.</span></span> <span data-ttu-id="53d11-438">Si se llama en un documento que tiene acceso completo a WinRT, el objeto se insertará independientemente del atributo AllowForWeb.</span><span class="sxs-lookup"><span data-stu-id="53d11-438">If called on a document that has full WinRT access, then the object will be injected regardless of the AllowForWeb attribute.</span></span> 

<span data-ttu-id="53d11-439">Además, el objeto debe implementar la interfaz IAgileObject.</span><span class="sxs-lookup"><span data-stu-id="53d11-439">Additionally, the object must implement the IAgileObject interface.</span></span> <span data-ttu-id="53d11-440">Esto se debe a que los elementos XAML y WebView se ejecutan en el ASTA de la aplicación y el subproceso de JavaScript de WebView es un hilo de ASTA diferente y queremos alentar a los programadores de aplicaciones para que puedan ejecutarse en el subproceso de JavaScript sin bloquear el subproceso de la vista de la aplicación, si es posible.</span><span class="sxs-lookup"><span data-stu-id="53d11-440">This is because the XAML and HTML webview elements run on their app's ASTA view threads and the WebView's JavaScript thread is a different ASTA thread and we want to encourage app developers to ensure their object can run on the JavaScript thread without blocking the app view thread if possible.</span></span>

<span data-ttu-id="53d11-441">El parámetro de nombre debe ser un nombre de propiedad de JavaScript válido; de lo contrario, la llamada fallará de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="53d11-441">The name parameter must be a valid JavaScript property name otherwise the call will fail silently.</span></span> <span data-ttu-id="53d11-442">Si el nombre es de una propiedad que ya existe en el objeto global, esa propiedad se sobrescribe si se puede configurar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="53d11-442">If the name is of a property that already exists on the global object then that property is overwritten if the property is configurable.</span></span> <span data-ttu-id="53d11-443">No se sobrescriben las propiedades no configurables del objeto global y se produce un error en la llamada de addWebAllowedObject silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="53d11-443">Non-configurable properties on the global object are not overwritten and the addWebAllowedObject call fails silently.</span></span> <span data-ttu-id="53d11-444">Las propiedades de JavaScript creadas a través de addWebAllowedObject son modificables, configurables y enumerables.</span><span class="sxs-lookup"><span data-stu-id="53d11-444">JavaScript properties created via addWebAllowedObject are writable, configurable, and enumerable.</span></span>

```js
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```

#### <span data-ttu-id="53d11-445">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-445">Parameters</span></span>
*<span data-ttu-id="53d11-446">name</span><span class="sxs-lookup"><span data-stu-id="53d11-446">name</span></span>*
* <span data-ttu-id="53d11-447">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-447">Type: **String**</span></span>
* <span data-ttu-id="53d11-448">El nombre del objeto que se va a exponer en el documento en la **vista de vista de vistas**.</span><span class="sxs-lookup"><span data-stu-id="53d11-448">The name of the object to expose to the document in the **webview**.</span></span>

*<span data-ttu-id="53d11-449">applicationObject</span><span class="sxs-lookup"><span data-stu-id="53d11-449">applicationObject</span></span>*
* <span data-ttu-id="53d11-450">Tipo: **objeto**</span><span class="sxs-lookup"><span data-stu-id="53d11-450">Type: **Object**</span></span>
* <span data-ttu-id="53d11-451">Objeto que se va a exponer en el documento en la **vista de vista de vista**.</span><span class="sxs-lookup"><span data-stu-id="53d11-451">The object to expose to the document in the **webview**.</span></span>

#### <span data-ttu-id="53d11-452">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-452">Return value</span></span>
<span data-ttu-id="53d11-453">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-453">This method does not return a value.</span></span>

#### <span data-ttu-id="53d11-454">Características y requisitos adicionales</span><span class="sxs-lookup"><span data-stu-id="53d11-454">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-455">Cliente mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-455">Minimum supported client</span></span>** |<span data-ttu-id="53d11-456">Windows10 [solo aplicaciones de la tienda Windows]</span><span class="sxs-lookup"><span data-stu-id="53d11-456">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="53d11-457">Servidor mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-457">Minimum supported server</span></span>** |<span data-ttu-id="53d11-458">Ninguna compatibilidad</span><span class="sxs-lookup"><span data-stu-id="53d11-458">None supported</span></span> |   
|**<span data-ttu-id="53d11-459">Teléfono mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-459">Minimum supported phone</span></span>**  |<span data-ttu-id="53d11-460">Ninguna compatibilidad</span><span class="sxs-lookup"><span data-stu-id="53d11-460">None supported</span></span> |  

### <span data-ttu-id="53d11-461">buildLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="53d11-461">buildLocalStreamUri</span></span>

<span data-ttu-id="53d11-462">Crea un URI que puedes pasar a [navigateToLocalStreamUri](#methods).</span><span class="sxs-lookup"><span data-stu-id="53d11-462">Creates a URI that you can pass to [navigateToLocalStreamUri](#methods).</span></span>

```js
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```

#### <span data-ttu-id="53d11-463">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-463">Parameters</span></span>
*<span data-ttu-id="53d11-464">contentIdentifier</span><span class="sxs-lookup"><span data-stu-id="53d11-464">contentIdentifier</span></span>*
* <span data-ttu-id="53d11-465">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-465">Type: **String**</span></span>
* <span data-ttu-id="53d11-466">Un identificador único para el contenido al que hace referencia el URI.</span><span class="sxs-lookup"><span data-stu-id="53d11-466">A unique identifier for the content the URI is referencing.</span></span> <span data-ttu-id="53d11-467">Define la raíz del URI.</span><span class="sxs-lookup"><span data-stu-id="53d11-467">This defines the root of the URI.</span></span>

*<span data-ttu-id="53d11-468">relativePath</span><span class="sxs-lookup"><span data-stu-id="53d11-468">relativePath</span></span>*
* <span data-ttu-id="53d11-469">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-469">Type: **String**</span></span>
* <span data-ttu-id="53d11-470">La ruta de acceso al recurso, relativa a la raíz.</span><span class="sxs-lookup"><span data-stu-id="53d11-470">The path to the resource, relative to the root.</span></span>

#### <span data-ttu-id="53d11-471">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-471">Return value</span></span>
<span data-ttu-id="53d11-472">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-472">Type: **String**</span></span>

<span data-ttu-id="53d11-473">Identificador URI creado mediante la combinación y la normalización de *contentIdentifier* y *relativePath*.</span><span class="sxs-lookup"><span data-stu-id="53d11-473">The URI created by combining and normalizing the *contentIdentifier* and *relativePath*.</span></span>

#### <span data-ttu-id="53d11-474">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53d11-474">Example</span></span>

<span data-ttu-id="53d11-475">En el ejemplo siguiente se muestra un caso de uso típico.</span><span class="sxs-lookup"><span data-stu-id="53d11-475">The following example illustrates a typical use case.</span></span> 

```js
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### <span data-ttu-id="53d11-476">capturePreviewToBlobAsync</span><span class="sxs-lookup"><span data-stu-id="53d11-476">capturePreviewToBlobAsync</span></span>

<span data-ttu-id="53d11-477">Crea una imagen del [elemento WebView](./webview.md) actual y la escribe en el elemento de imagen especificado.</span><span class="sxs-lookup"><span data-stu-id="53d11-477">Creates an image of the current [webview element](./webview.md) and write it to the specified image element.</span></span>

```js
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```

#### <span data-ttu-id="53d11-478">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-478">Parameters</span></span>
<span data-ttu-id="53d11-479">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53d11-479">This method has no parameters.</span></span>

#### <span data-ttu-id="53d11-480">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-480">Return value</span></span>
<span data-ttu-id="53d11-481">Escriba: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="53d11-481">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="53d11-482">Un objeto **MSWebViewAsyncOperation** que, cuando se completa, proporciona un objeto **BLOB** que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="53d11-482">An **MSWebViewAsyncOperation** object that, when it completes, provides a **Blob** object that contains the image.</span></span> <span data-ttu-id="53d11-483">Al usar **capturePreviewToBlobAsync**, es necesario definir controladores de éxito y error después de definir la operación.</span><span class="sxs-lookup"><span data-stu-id="53d11-483">When using **capturePreviewToBlobAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="53d11-484">Después de aplicar los controladores de eventos, llama al método Start del objeto [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) para ejecutar la operación.</span><span class="sxs-lookup"><span data-stu-id="53d11-484">After applying the event handlers, call the start method on the [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) object to execute the operation.</span></span>

### <span data-ttu-id="53d11-485">captureSelectedContentToDataPackageAsync</span><span class="sxs-lookup"><span data-stu-id="53d11-485">captureSelectedContentToDataPackageAsync</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="53d11-486">Este método ha quedado obsoleto y tiene un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="53d11-486">This method has been deprecated and has a known issue.</span></span> <span data-ttu-id="53d11-487">Evite usar este método en su código de producción.</span><span class="sxs-lookup"><span data-stu-id="53d11-487">Avoid using this method in your production code.</span></span> 

<span data-ttu-id="53d11-488">Obtiene de forma asincrónica un [paquete de paquetes](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) de contenido que contiene el contenido seleccionado en la **vista**de contenido.</span><span class="sxs-lookup"><span data-stu-id="53d11-488">Asynchronously gets a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) that contains the selected content within the **webview**.</span></span>

```js
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```

#### <span data-ttu-id="53d11-489">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-489">Parameters</span></span>
<span data-ttu-id="53d11-490">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53d11-490">This method has no parameters.</span></span>

#### <span data-ttu-id="53d11-491">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-491">Return value</span></span>
<span data-ttu-id="53d11-492">Escriba: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="53d11-492">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="53d11-493">Un objeto **MSWebViewAsyncOperation** que, cuando se completa, proporciona un objeto de [paquete](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) de datos que contiene la imagen.</span><span class="sxs-lookup"><span data-stu-id="53d11-493">An **MSWebViewAsyncOperation** object that, when it completes, provides a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) object that contains the image.</span></span> <span data-ttu-id="53d11-494">Al usar **captureSelectedContentToDataPackageAsync**, es necesario definir controladores de éxito y error después de definir la operación.</span><span class="sxs-lookup"><span data-stu-id="53d11-494">When using **captureSelectedContentToDataPackageAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="53d11-495">Después de aplicar los controladores de eventos, llama al método Start del objeto MSWebViewAsyncOperation para ejecutar la operación.</span><span class="sxs-lookup"><span data-stu-id="53d11-495">After applying the event handlers, call the start method on the MSWebViewAsyncOperation object to execute the operation.</span></span>

```js
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();  

```

### <span data-ttu-id="53d11-496">invokeScriptAsync</span><span class="sxs-lookup"><span data-stu-id="53d11-496">invokeScriptAsync</span></span>

<span data-ttu-id="53d11-497">Como una acción asincrónica, ejecuta la función de secuencia de comandos especificada desde el código HTML cargado actualmente, con argumentos específicos.</span><span class="sxs-lookup"><span data-stu-id="53d11-497">As an asynchronous action, executes the specified script function from the currently loaded HTML, with specific arguments.</span></span>

```js
webview.invokeScriptAsync(functionName, ...args)
```

#### <span data-ttu-id="53d11-498">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-498">Parameters</span></span>

**<span data-ttu-id="53d11-499">functionName</span><span class="sxs-lookup"><span data-stu-id="53d11-499">functionName</span></span>**
* <span data-ttu-id="53d11-500">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-500">Type: **String**</span></span>
* <span data-ttu-id="53d11-501">Nombre de la función que se va a invocar.</span><span class="sxs-lookup"><span data-stu-id="53d11-501">The name of the function to invoke.</span></span> <span data-ttu-id="53d11-502">Este es un nombre de propiedad en el objeto de ventana global del documento de nivel superior de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-502">This is a property name on the global window object of the WebView's top level document.</span></span> <span data-ttu-id="53d11-503">Puede ser una función global integrada como eval o abrir, o puede ser una función definida por script en el objeto de ventana global.</span><span class="sxs-lookup"><span data-stu-id="53d11-503">This can be a built-in global function like eval or open, or it can be a script defined function on the global window object.</span></span> <span data-ttu-id="53d11-504">Solo se pueden invocar funciones en el documento de nivel superior de la vista de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-504">Only functions in the top level document of the WebView may be invoked.</span></span>

**<span data-ttu-id="53d11-505">EventArgs</span><span class="sxs-lookup"><span data-stu-id="53d11-505">args</span></span>**
* <span data-ttu-id="53d11-506">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-506">Type: **String**</span></span>
* <span data-ttu-id="53d11-507">Parámetros de cadena opcionales que se pasan a la función invocada.</span><span class="sxs-lookup"><span data-stu-id="53d11-507">Optional string parameters to pass to the invoked function.</span></span> <span data-ttu-id="53d11-508">Después de functionName, los parámetros adicionales para invokeScriptAsync son cadenas que se pasan a la función invocada.</span><span class="sxs-lookup"><span data-stu-id="53d11-508">After functionName, any additional parameters to invokeScriptAsync are strings passed to the invoked function.</span></span>

#### <span data-ttu-id="53d11-509">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-509">Return value</span></span>
<span data-ttu-id="53d11-510">Escriba: **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="53d11-510">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="53d11-511">Al usar **invokeScriptAsync**, es necesario definir controladores de éxito y error después de definir la operación.</span><span class="sxs-lookup"><span data-stu-id="53d11-511">When using **invokeScriptAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="53d11-512">Después de aplicar los controladores de eventos, llama a **MSWebViewAsyncOperation. Start** para ejecutar la operación.</span><span class="sxs-lookup"><span data-stu-id="53d11-512">After applying the event handlers, call **MSWebViewAsyncOperation.start** to execute the operation.</span></span> <span data-ttu-id="53d11-513">Si el evento completo de MSWebViewAsyncOperation se desencadena, la propiedad result de MSWebViewAsyncOperation es el valor devuelto por la cadena para invocar la función.</span><span class="sxs-lookup"><span data-stu-id="53d11-513">If the MSWebViewAsyncOperation's complete event fires then the MSWebViewAsyncOperation's result property is the string return value from invoking the function.</span></span> <span data-ttu-id="53d11-514">El uso del valor devuelto por la función invocada permite que el contenido de la vista en la vista previa vuelva a comunicarse de forma sincrónica con el host de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-514">Using the invoked function's return value allows for the WebView content to communication synchronously back to the WebView host.</span></span> <span data-ttu-id="53d11-515">Para que el contenido de WebView se comunique de forma asincrónica al host WebView, consulta el evento MSWebViewScriptNotify.</span><span class="sxs-lookup"><span data-stu-id="53d11-515">To instead have the WebView content communicate asynchronously back to the WebView host see the MSWebViewScriptNotify event.</span></span> <span data-ttu-id="53d11-516">Si la función invocada produce una excepción no controlada, se desencadenará el evento de error del MSWebViewAsyncOperation.</span><span class="sxs-lookup"><span data-stu-id="53d11-516">If the function invoked throws an unhandled exception then the MSWebViewAsyncOperation's error event will fire.</span></span> 

```js
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```

### <span data-ttu-id="53d11-517">getDeferredPermissionRequests</span><span class="sxs-lookup"><span data-stu-id="53d11-517">getDeferredPermissionRequests</span></span>

<span data-ttu-id="53d11-518">Devuelve una lista de las solicitudes de permisos diferidos emitidas por el contenido en el control **WebView** .</span><span class="sxs-lookup"><span data-stu-id="53d11-518">Returns a list of deferred permission requests issued by content in the **webview** control.</span></span>

```js
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```

#### <span data-ttu-id="53d11-519">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-519">Parameters</span></span>
<span data-ttu-id="53d11-520">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53d11-520">This method has no parameters.</span></span>

#### <span data-ttu-id="53d11-521">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-521">Return value</span></span>
<span data-ttu-id="53d11-522">Escriba: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="53d11-522">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>

<span data-ttu-id="53d11-523">La solicitud de permisos diferidos especificada.</span><span class="sxs-lookup"><span data-stu-id="53d11-523">The specified deferred permission request.</span></span>

#### <span data-ttu-id="53d11-524">Características y requisitos adicionales</span><span class="sxs-lookup"><span data-stu-id="53d11-524">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-525">Cliente mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-525">Minimum supported client</span></span>** |<span data-ttu-id="53d11-526">Windows10 [solo aplicaciones de la tienda Windows]</span><span class="sxs-lookup"><span data-stu-id="53d11-526">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="53d11-527">Servidor mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-527">Minimum supported server</span></span>** |<span data-ttu-id="53d11-528">Ninguna compatibilidad</span><span class="sxs-lookup"><span data-stu-id="53d11-528">None supported</span></span>|   
|**<span data-ttu-id="53d11-529">Teléfono mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-529">Minimum supported phone</span></span>**  |<span data-ttu-id="53d11-530">Ninguna compatibilidad</span><span class="sxs-lookup"><span data-stu-id="53d11-530">None supported</span></span> |    


### <span data-ttu-id="53d11-531">getDeferredPermissionRequestById</span><span class="sxs-lookup"><span data-stu-id="53d11-531">getDeferredPermissionRequestById</span></span>

<span data-ttu-id="53d11-532">Devuelve la solicitud de permiso diferido especificada.</span><span class="sxs-lookup"><span data-stu-id="53d11-532">Returns the specified deferred permission request.</span></span> 

```js
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```

#### <span data-ttu-id="53d11-533">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-533">Parameters</span></span>
*<span data-ttu-id="53d11-534">id</span><span class="sxs-lookup"><span data-stu-id="53d11-534">id</span></span>*
* <span data-ttu-id="53d11-535">Tipo: **largo sin signo**</span><span class="sxs-lookup"><span data-stu-id="53d11-535">Type: **unsigned long**</span></span>
* <span data-ttu-id="53d11-536">IDENTIFICADOR de la solicitud de permiso diferido que desea obtener.</span><span class="sxs-lookup"><span data-stu-id="53d11-536">The ID of the deferred permission request you wish to get.</span></span>

#### <span data-ttu-id="53d11-537">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-537">Return value</span></span>
<span data-ttu-id="53d11-538">Escriba: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="53d11-538">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>

<span data-ttu-id="53d11-539">La solicitud de permisos diferidos especificada.</span><span class="sxs-lookup"><span data-stu-id="53d11-539">The specified deferred permission request.</span></span>

#### <span data-ttu-id="53d11-540">Características y requisitos adicionales</span><span class="sxs-lookup"><span data-stu-id="53d11-540">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="53d11-541">Cliente mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-541">Minimum supported client</span></span>** |<span data-ttu-id="53d11-542">Windows10 [solo aplicaciones de la tienda Windows]</span><span class="sxs-lookup"><span data-stu-id="53d11-542">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="53d11-543">Servidor mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-543">Minimum supported server</span></span>** |<span data-ttu-id="53d11-544">Ninguna compatibilidad</span><span class="sxs-lookup"><span data-stu-id="53d11-544">None supported</span></span>|   
|**<span data-ttu-id="53d11-545">Teléfono mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="53d11-545">Minimum supported phone</span></span>**  |<span data-ttu-id="53d11-546">Ninguna compatibilidad</span><span class="sxs-lookup"><span data-stu-id="53d11-546">None supported</span></span> | 

### <span data-ttu-id="53d11-547">goBack</span><span class="sxs-lookup"><span data-stu-id="53d11-547">goBack</span></span>

<span data-ttu-id="53d11-548">Navega por la **vista** web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-548">Navigates the **webview** to the previous page in the navigation history.</span></span> 

```js
webview.goBack();
```

#### <span data-ttu-id="53d11-549">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-549">Parameters</span></span>
<span data-ttu-id="53d11-550">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53d11-550">This method has no parameters.</span></span>

#### <span data-ttu-id="53d11-551">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-551">Return value</span></span>
<span data-ttu-id="53d11-552">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-552">This method does not return a value.</span></span>

### <span data-ttu-id="53d11-553">goForward</span><span class="sxs-lookup"><span data-stu-id="53d11-553">goForward</span></span>

<span data-ttu-id="53d11-554">Navega por la **vista** web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-554">Navigates the **webview** to the next page in the navigation history.</span></span> 

```js
webview.goForward();
```

#### <span data-ttu-id="53d11-555">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-555">Parameters</span></span>
<span data-ttu-id="53d11-556">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53d11-556">This method has no parameters.</span></span>

#### <span data-ttu-id="53d11-557">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-557">Return value</span></span>
<span data-ttu-id="53d11-558">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-558">This method does not return a value.</span></span>

### <span data-ttu-id="53d11-559">navegar</span><span class="sxs-lookup"><span data-stu-id="53d11-559">navigate</span></span>

<span data-ttu-id="53d11-560">Carga el contenido HTML en el identificador uniforme de recursos (URI) especificado.</span><span class="sxs-lookup"><span data-stu-id="53d11-560">Loads the HTML content at the specified Uniform Resource Identifier (URI).</span></span> 

```js
webview.navigate(uri);
```

#### <span data-ttu-id="53d11-561">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-561">Parameters</span></span>

**<span data-ttu-id="53d11-562">uri</span><span class="sxs-lookup"><span data-stu-id="53d11-562">uri</span></span>**
* <span data-ttu-id="53d11-563">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-563">Type: **String**</span></span>
* <span data-ttu-id="53d11-564">URI que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="53d11-564">The URI to load.</span></span>

#### <span data-ttu-id="53d11-565">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-565">Return value</span></span>
<span data-ttu-id="53d11-566">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-566">This  method does not return a value.</span></span>

### <span data-ttu-id="53d11-567">navigateFocus</span><span class="sxs-lookup"><span data-stu-id="53d11-567">navigateFocus</span></span>

<span data-ttu-id="53d11-568">Desplaza el foco a la **vista de vistas en WebView**.</span><span class="sxs-lookup"><span data-stu-id="53d11-568">Navigates focus onto the **webview**.</span></span> <span data-ttu-id="53d11-569">Desencadena el evento window's navigatingfocus del documento de nivel superior de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-569">Fires the webview's top level document's window's navigatingfocus event.</span></span> <span data-ttu-id="53d11-570">El FocusNavigationEvent args usado en el evento navigatingfocus coincide con los parámetros proporcionados a navigateFocus excepto que los parámetros de origen se traducen desde el espacio de coordenadas del documento host al espacio de coordenadas del documento de nivel superior de WebView.</span><span class="sxs-lookup"><span data-stu-id="53d11-570">The FocusNavigationEvent args used in the navigatingfocus event match the parameters provided to navigateFocus except the origin parameters are translated from the host document's coordinate space to the coordinate space of the webview's top level document.</span></span> <span data-ttu-id="53d11-571">Consulta el evento WebView departingFocus y el método window. departFocus correspondiente para transferir el foco de la vista en webal host.</span><span class="sxs-lookup"><span data-stu-id="53d11-571">See the webview departingFocus event and corresponding window.departFocus method for transferring focus from the webview to the host.</span></span> <span data-ttu-id="53d11-572">Vea la [biblioteca de navegación de direcciones de TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obtener un ejemplo de una implementación de la navegación de foco mediante un teclado o un controlador para juegos que usa este método.</span><span class="sxs-lookup"><span data-stu-id="53d11-572">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that uses this method.</span></span>

```js
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```

#### <span data-ttu-id="53d11-573">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-573">Parameters</span></span>
*<span data-ttu-id="53d11-574">navigationReason</span><span class="sxs-lookup"><span data-stu-id="53d11-574">navigationReason</span></span>*
* <span data-ttu-id="53d11-575">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-575">Type: **String**</span></span>
* <span data-ttu-id="53d11-576">El motivo de la navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-576">The reason for the navigation.</span></span> <span data-ttu-id="53d11-577">El valor debe ser "left", "up", "Right" o "Down".</span><span class="sxs-lookup"><span data-stu-id="53d11-577">The value should be either "left", "up", "right", or "down".</span></span> <span data-ttu-id="53d11-578">Es la dirección en la que el foco se aleja del elemento que se encuentra enfocado.</span><span class="sxs-lookup"><span data-stu-id="53d11-578">It is the direction in which focus is moving away from the currently focused element.</span></span>

*<span data-ttu-id="53d11-579">origen</span><span class="sxs-lookup"><span data-stu-id="53d11-579">origin</span></span>*
* <span data-ttu-id="53d11-580">Tipo: **objeto**</span><span class="sxs-lookup"><span data-stu-id="53d11-580">Type: **Object**</span></span>
* <span data-ttu-id="53d11-581">El origen de la navegación.</span><span class="sxs-lookup"><span data-stu-id="53d11-581">The origin of the navigation.</span></span> <span data-ttu-id="53d11-582">Este es un objeto de JavaScript con las propiedades "originLeft", "originTop", "originWidth" y "originHeight".</span><span class="sxs-lookup"><span data-stu-id="53d11-582">This is a JavaScript object with properties "originLeft", "originTop", "originWidth", and "originHeight".</span></span> <span data-ttu-id="53d11-583">Estos valores deben describir la posición y el tamaño del elemento que se encuentra actualmente enfocado y en el que se mueve el foco.</span><span class="sxs-lookup"><span data-stu-id="53d11-583">These values should describe the position and size of the currently focused element away from which focus is moving.</span></span>

#### <span data-ttu-id="53d11-584">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-584">Return value</span></span>
<span data-ttu-id="53d11-585">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-585">This method does not return a value.</span></span>

### <span data-ttu-id="53d11-586">navigateToLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="53d11-586">navigateToLocalStreamUri</span></span>

<span data-ttu-id="53d11-587">Carga el contenido Web local en el URI especificado usando un [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span><span class="sxs-lookup"><span data-stu-id="53d11-587">Loads local web content at the specified URI using a [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span></span>

```js
webview.navigateToLocalStreamUri(source, streamResolver); 
```

#### <span data-ttu-id="53d11-588">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-588">Parameters</span></span>

*<span data-ttu-id="53d11-589">origen</span><span class="sxs-lookup"><span data-stu-id="53d11-589">source</span></span>*
* <span data-ttu-id="53d11-590">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-590">Type: **String**</span></span>
* <span data-ttu-id="53d11-591">Un identificador URI MS-local-Stream que identifica el contenido HTML local que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="53d11-591">An ms-local-stream URI identifying the local HTML content to load.</span></span> <span data-ttu-id="53d11-592">Cree esta cadena con [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span><span class="sxs-lookup"><span data-stu-id="53d11-592">Create this string using [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span></span>

*<span data-ttu-id="53d11-593">streamResolver</span><span class="sxs-lookup"><span data-stu-id="53d11-593">streamResolver</span></span>*
* <span data-ttu-id="53d11-594">Escriba lo siguiente: cualquiera</span><span class="sxs-lookup"><span data-stu-id="53d11-594">Type: any</span></span>
* <span data-ttu-id="53d11-595">Una resolución que convierte el identificador URI en una secuencia que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="53d11-595">A resolver that converts the URI into a stream to load.</span></span>

#### <span data-ttu-id="53d11-596">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-596">Return value</span></span>
<span data-ttu-id="53d11-597">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-597">This method does not return a value.</span></span>

### <span data-ttu-id="53d11-598">navigateToString</span><span class="sxs-lookup"><span data-stu-id="53d11-598">navigateToString</span></span>

<span data-ttu-id="53d11-599">Carga el contenido HTML especificado como un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="53d11-599">Loads the specified HTML content as a new document.</span></span> 

```js
webview.navigateToString(contents);
```

#### <span data-ttu-id="53d11-600">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-600">Parameters</span></span>

*<span data-ttu-id="53d11-601">contenidos</span><span class="sxs-lookup"><span data-stu-id="53d11-601">contents</span></span>*
* <span data-ttu-id="53d11-602">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-602">Type: **String**</span></span>
* <span data-ttu-id="53d11-603">Contenido HTML que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="53d11-603">The HTML content to display.</span></span>

#### <span data-ttu-id="53d11-604">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-604">Return value</span></span>
<span data-ttu-id="53d11-605">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-605">This method does not return a value.</span></span>

### <span data-ttu-id="53d11-606">navigateWithHttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="53d11-606">navigateWithHttpRequestMessage</span></span>

<span data-ttu-id="53d11-607">Navega por la vista en WebView a un identificador uniforme de recursos (URI) con una solicitud POST y encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="53d11-607">Navigates the webview to a Uniform Resource Identifier (URI) with a POST request and HTTP headers.</span></span> 

```js
webview.navigateWithHttpRequestMessage(requestMessage);
```

#### <span data-ttu-id="53d11-608">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-608">Parameters</span></span>

*<span data-ttu-id="53d11-609">requestMessage</span><span class="sxs-lookup"><span data-stu-id="53d11-609">requestMessage</span></span>*
* <span data-ttu-id="53d11-610">Tipo: **HttpRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="53d11-610">Type: **HttpRequestMessage**</span></span>
* <span data-ttu-id="53d11-611">Detalles de la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="53d11-611">The details of the HTTP request.</span></span> 

#### <span data-ttu-id="53d11-612">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-612">Return value</span></span>
<span data-ttu-id="53d11-613">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-613">This method does not return a value.</span></span>

#### <span data-ttu-id="53d11-614">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53d11-614">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="53d11-615">Si agrega encabezados adicionales a esta solicitud, como las credenciales de autenticación, recuerde que esos encabezados también se incluirán en las solicitudes secundarias subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="53d11-615">If you add additional headers to this request, such as authentication credentials, remember that those headers will also be included with any subsequent child requests.</span></span> <span data-ttu-id="53d11-616">Use precaución para evitar la revelación accidental de información confidencial o personal.</span><span class="sxs-lookup"><span data-stu-id="53d11-616">Use caution to prevent accidental disclosure of confidential or personal information.</span></span> 


### <span data-ttu-id="53d11-617">fresca</span><span class="sxs-lookup"><span data-stu-id="53d11-617">refresh</span></span> 

<span data-ttu-id="53d11-618">Vuelve a cargar el contenido actual en la **vista**de contenido.</span><span class="sxs-lookup"><span data-stu-id="53d11-618">Reloads the current content in the **webview**.</span></span> 

```js
webview.refresh();
```

#### <span data-ttu-id="53d11-619">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-619">Parameters</span></span>
<span data-ttu-id="53d11-620">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53d11-620">This method has no parameters.</span></span>

#### <span data-ttu-id="53d11-621">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-621">Return value</span></span>
<span data-ttu-id="53d11-622">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-622">This method does not return a value.</span></span>


### <span data-ttu-id="53d11-623">stop</span><span class="sxs-lookup"><span data-stu-id="53d11-623">stop</span></span>

<span data-ttu-id="53d11-624">Detiene la navegación o descarga de la **vista en WebView** actual.</span><span class="sxs-lookup"><span data-stu-id="53d11-624">Halts the current **webview** navigation or download.</span></span> 

```js
webview.stop();
```

#### <span data-ttu-id="53d11-625">Parameters</span><span class="sxs-lookup"><span data-stu-id="53d11-625">Parameters</span></span>
<span data-ttu-id="53d11-626">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="53d11-626">This method has no parameters.</span></span>

#### <span data-ttu-id="53d11-627">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53d11-627">Return value</span></span>
<span data-ttu-id="53d11-628">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="53d11-628">This method does not return a value.</span></span>


## <span data-ttu-id="53d11-629">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53d11-629">Properties</span></span>

### <span data-ttu-id="53d11-630">canGoBack</span><span class="sxs-lookup"><span data-stu-id="53d11-630">canGoBack</span></span>

<span data-ttu-id="53d11-631">Obtiene un valor que indica si la **vista de vista previa** puede desplazarse hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="53d11-631">Gets a value that indicates whether the **webview** can navigate backward.</span></span>

<span data-ttu-id="53d11-632">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53d11-632">This property is read-only.</span></span>

```js
var canGoBack = webview.canGoBack;
```

#### <span data-ttu-id="53d11-633">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-633">Property value</span></span>
<span data-ttu-id="53d11-634">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="53d11-634">Type: **Boolean**</span></span>

<span data-ttu-id="53d11-635">**True** si la **vista en WebView** puede desplazarse hacia atrás; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="53d11-635">**True** if the **webview** can navigate backward; otherwise, **false**.</span></span>

### <span data-ttu-id="53d11-636">canGoForward</span><span class="sxs-lookup"><span data-stu-id="53d11-636">canGoForward</span></span>

<span data-ttu-id="53d11-637">Obtiene un valor que indica si la **vista previa** puede navegar hacia delante.</span><span class="sxs-lookup"><span data-stu-id="53d11-637">Gets a value that indicates whether the **webview** can navigate forward.</span></span>

<span data-ttu-id="53d11-638">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53d11-638">This property is read-only.</span></span>

```js
var canGoForward = webview.canGoForward;
```

#### <span data-ttu-id="53d11-639">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-639">Property value</span></span>
<span data-ttu-id="53d11-640">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="53d11-640">Type: **Boolean**</span></span>

<span data-ttu-id="53d11-641">**True** si la **vista en WebView** puede navegar hacia delante; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="53d11-641">**True** if the **webview** can navigate forward; otherwise, **false**.</span></span>

### <span data-ttu-id="53d11-642">containsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="53d11-642">containsFullScreenElement</span></span>

<span data-ttu-id="53d11-643">Obtiene un valor que indica si la **vista** de página contiene un elemento que admite la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="53d11-643">Gets a value that indicates whether the **webview** contains an element that supports full screen.</span></span> <span data-ttu-id="53d11-644">Para obtener más información, consulta el evento MSWebViewContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="53d11-644">See the MSWebViewContainsFullScreenElementChanged event for more info.</span></span>

<span data-ttu-id="53d11-645">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53d11-645">This property is read-only.</span></span>

```js
var containsFullScreenElement = webview.containsFullScreenElement;
```

#### <span data-ttu-id="53d11-646">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-646">Property value</span></span>
<span data-ttu-id="53d11-647">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="53d11-647">Type: **Boolean**</span></span>

<span data-ttu-id="53d11-648">**True** **si la ventana** contiene un elemento que admite la pantalla completa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="53d11-648">**True** if the **webview** contains an element that supports full screen; otherwise, **false**.</span></span>


### <span data-ttu-id="53d11-649">documentTitle</span><span class="sxs-lookup"><span data-stu-id="53d11-649">documentTitle</span></span>

<span data-ttu-id="53d11-650">Obtiene el título de la página que se muestra actualmente en la **vista**Web.</span><span class="sxs-lookup"><span data-stu-id="53d11-650">Gets the title of the page currently displayed in the **webview**.</span></span> 

<span data-ttu-id="53d11-651">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53d11-651">This property is read-only.</span></span>

```js
var documentTitle = webview.documentTitle;
```

#### <span data-ttu-id="53d11-652">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-652">Property value</span></span>
<span data-ttu-id="53d11-653">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-653">Type: **String**</span></span>

<span data-ttu-id="53d11-654">El título de la página.</span><span class="sxs-lookup"><span data-stu-id="53d11-654">The page title.</span></span>

### <span data-ttu-id="53d11-655">height</span><span class="sxs-lookup"><span data-stu-id="53d11-655">height</span></span>

<span data-ttu-id="53d11-656">Obtiene o establece el alto de la **vista en WebView**.</span><span class="sxs-lookup"><span data-stu-id="53d11-656">Gets or sets the height of the **webview**.</span></span> 

```js
var height = webview.height;
webview.height = height;

```

#### <span data-ttu-id="53d11-657">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-657">Property value</span></span>
<span data-ttu-id="53d11-658">Tipo: **número**</span><span class="sxs-lookup"><span data-stu-id="53d11-658">Type: **Number**</span></span>

<span data-ttu-id="53d11-659">El alto de la **vista en WebView**.</span><span class="sxs-lookup"><span data-stu-id="53d11-659">The height of the **webview**.</span></span> 


### <span data-ttu-id="53d11-660">proceso</span><span class="sxs-lookup"><span data-stu-id="53d11-660">process</span></span>

<span data-ttu-id="53d11-661">Obtiene el proceso de **WebView** .</span><span class="sxs-lookup"><span data-stu-id="53d11-661">Gets the **webview** process.</span></span>

<span data-ttu-id="53d11-662">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53d11-662">This property is read-only.</span></span>

```js
var process = webview.process;
webview.process = process;
```

#### <span data-ttu-id="53d11-663">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-663">Property value</span></span>
<span data-ttu-id="53d11-664">Escriba: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span><span class="sxs-lookup"><span data-stu-id="53d11-664">Type: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span></span>


### <span data-ttu-id="53d11-665">settings</span><span class="sxs-lookup"><span data-stu-id="53d11-665">settings</span></span>

<span data-ttu-id="53d11-666">Obtiene un objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contiene propiedades para habilitar o deshabilitar las características de **WebView** .</span><span class="sxs-lookup"><span data-stu-id="53d11-666">Gets a [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>

<span data-ttu-id="53d11-667">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53d11-667">This property is read-only.</span></span>

```js
var settings = webview.settings;
webview.settings = settings;
```

#### <span data-ttu-id="53d11-668">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-668">Property value</span></span>
<span data-ttu-id="53d11-669">Escriba: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span><span class="sxs-lookup"><span data-stu-id="53d11-669">Type: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span></span>

<span data-ttu-id="53d11-670">Un objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contiene propiedades para habilitar o deshabilitar características de **WebView** .</span><span class="sxs-lookup"><span data-stu-id="53d11-670">A [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>

### <span data-ttu-id="53d11-671">src</span><span class="sxs-lookup"><span data-stu-id="53d11-671">src</span></span>

<span data-ttu-id="53d11-672">Obtiene o establece el origen del identificador uniforme de recursos (URI) del contenido HTML que se va a mostrar en el control **WebView** .</span><span class="sxs-lookup"><span data-stu-id="53d11-672">Gets or sets the Uniform Resource Identifier (URI) source of the HTML content to display in the **webview** control.</span></span> 

```js
var src = webview.src;
webview.src = src;
```

#### <span data-ttu-id="53d11-673">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-673">Property value</span></span>
<span data-ttu-id="53d11-674">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53d11-674">Type: **String**</span></span>

<span data-ttu-id="53d11-675">El origen de URI del contenido HTML que se muestra en el control **WebView** .</span><span class="sxs-lookup"><span data-stu-id="53d11-675">The URI source of the HTML content to display in the **webview** control.</span></span> 


### <span data-ttu-id="53d11-676">width</span><span class="sxs-lookup"><span data-stu-id="53d11-676">width</span></span>

<span data-ttu-id="53d11-677">Obtiene o establece el ancho de la **vista en WebView**.</span><span class="sxs-lookup"><span data-stu-id="53d11-677">Gets or sets the width of the **webview**.</span></span>

```js
var width = webview.width;
webview.width = width;
```

#### <span data-ttu-id="53d11-678">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53d11-678">Property value</span></span>
<span data-ttu-id="53d11-679">Tipo: **número**</span><span class="sxs-lookup"><span data-stu-id="53d11-679">Type: **Number**</span></span>

<span data-ttu-id="53d11-680">El ancho de la **vista en WebView**.</span><span class="sxs-lookup"><span data-stu-id="53d11-680">The width of the **webview**.</span></span>
