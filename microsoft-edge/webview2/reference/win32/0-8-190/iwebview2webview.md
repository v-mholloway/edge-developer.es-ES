---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5711a1dbf501df55fefc9709763c1fe225865e11
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886433"
---
# <span data-ttu-id="10574-104">0.8.355: IWebView2WebView</span><span class="sxs-lookup"><span data-stu-id="10574-104">0.8.355 - interface IWebView2WebView</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView
  : public IUnknown
```

<span data-ttu-id="10574-105">WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.</span><span class="sxs-lookup"><span data-stu-id="10574-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="10574-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="10574-106">Summary</span></span>

 <span data-ttu-id="10574-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="10574-107">Members</span></span>                        | <span data-ttu-id="10574-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10574-109">get_Settings</span><span class="sxs-lookup"><span data-stu-id="10574-109">get_Settings</span></span>](#get_settings) | <span data-ttu-id="10574-110">El objeto [IWebView2Settings](IWebView2Settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="10574-110">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="10574-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="10574-111">get_Source</span></span>](#get_source) | <span data-ttu-id="10574-112">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="10574-112">The URI of the current top level document.</span></span>
[<span data-ttu-id="10574-113">Busque</span><span class="sxs-lookup"><span data-stu-id="10574-113">Navigate</span></span>](#navigate) | <span data-ttu-id="10574-114">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="10574-114">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="10574-115">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="10574-115">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="10574-116">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-116">Move focus into WebView.</span></span>
[<span data-ttu-id="10574-117">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="10574-117">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="10574-118">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="10574-118">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="10574-119">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-119">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="10574-120">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-120">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="10574-121">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-121">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="10574-122">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-122">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="10574-123">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="10574-123">add_DocumentStateChanged</span></span>](#add_documentstatechanged) | <span data-ttu-id="10574-124">Agregue un controlador de eventos para el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-124">Add an event handler for the DocumentStateChanged event.</span></span>
[<span data-ttu-id="10574-125">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="10574-125">remove_DocumentStateChanged</span></span>](#remove_documentstatechanged) | <span data-ttu-id="10574-126">Quitar un controlador de eventos agregado previamente con add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-126">Remove an event handler previously added with add_DocumentStateChanged.</span></span>
[<span data-ttu-id="10574-127">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="10574-127">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="10574-128">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10574-128">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="10574-129">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="10574-129">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="10574-130">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10574-130">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="10574-131">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-131">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="10574-132">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-132">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="10574-133">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-133">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="10574-134">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-134">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="10574-135">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="10574-135">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="10574-136">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-136">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="10574-137">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="10574-137">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="10574-138">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-138">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="10574-139">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="10574-139">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="10574-140">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-140">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="10574-141">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="10574-141">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="10574-142">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-142">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="10574-143">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="10574-143">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="10574-144">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-144">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="10574-145">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="10574-145">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="10574-146">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-146">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="10574-147">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="10574-147">add_WebResourceRequested_deprecated</span></span>](#add_webresourcerequested_deprecated) | <span data-ttu-id="10574-148">Esta API estará en desuso; usa la nueva API de add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-148">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>
[<span data-ttu-id="10574-149">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="10574-149">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="10574-150">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-150">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="10574-151">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="10574-151">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="10574-152">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="10574-152">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="10574-153">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="10574-153">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="10574-154">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="10574-154">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="10574-155">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="10574-155">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="10574-156">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-156">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="10574-157">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="10574-157">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="10574-158">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-158">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="10574-159">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="10574-159">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="10574-160">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-160">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="10574-161">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="10574-161">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="10574-162">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-162">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="10574-163">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="10574-163">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="10574-164">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="10574-164">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="10574-165">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="10574-165">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="10574-166">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="10574-166">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="10574-167">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="10574-167">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="10574-168">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="10574-168">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="10574-169">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="10574-169">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="10574-170">Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="10574-170">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="10574-171">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="10574-171">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="10574-172">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-172">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="10574-173">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="10574-173">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="10574-174">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="10574-174">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="10574-175">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="10574-175">Reload</span></span>](#reload) | <span data-ttu-id="10574-176">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="10574-176">Reload the current page.</span></span>
[<span data-ttu-id="10574-177">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="10574-177">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="10574-178">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="10574-178">The webview bounds.</span></span>
[<span data-ttu-id="10574-179">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="10574-179">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="10574-180">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="10574-180">Set the Bounds property.</span></span>
[<span data-ttu-id="10574-181">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="10574-181">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="10574-182">El factor de zoom para la página actual en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="10574-182">The zoom factor for the current page in the WebView.</span></span>
[<span data-ttu-id="10574-183">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="10574-183">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="10574-184">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="10574-184">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="10574-185">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="10574-185">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="10574-186">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-186">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="10574-187">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="10574-187">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="10574-188">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="10574-188">Set the IsVisible property.</span></span>
[<span data-ttu-id="10574-189">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="10574-189">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="10574-190">Publique el mensaje webmensaje especificado en el documento de nivel superior de este [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="10574-190">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>
[<span data-ttu-id="10574-191">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="10574-191">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="10574-192">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10574-192">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="10574-193">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="10574-193">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="10574-194">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="10574-194">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="10574-195">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="10574-195">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="10574-196">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="10574-196">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="10574-197">Cerrar</span><span class="sxs-lookup"><span data-stu-id="10574-197">Close</span></span>](#close) | <span data-ttu-id="10574-198">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="10574-198">Closes the webview and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="10574-199">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="10574-199">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="10574-200">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="10574-200">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="10574-201">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="10574-201">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="10574-202">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="10574-202">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="10574-203">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="10574-203">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="10574-204">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="10574-204">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>
[<span data-ttu-id="10574-205">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="10574-205">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="10574-206">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="10574-206">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="10574-207">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="10574-207">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="10574-208">Puede navegar por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-208">Can navigate the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="10574-209">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="10574-209">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="10574-210">Puede navegar por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-210">Can navigate the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="10574-211">GoBack</span><span class="sxs-lookup"><span data-stu-id="10574-211">GoBack</span></span>](#goback) | <span data-ttu-id="10574-212">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-212">Navigates the webview to the previous page in the navigation history.</span></span>
[<span data-ttu-id="10574-213">GoForward</span><span class="sxs-lookup"><span data-stu-id="10574-213">GoForward</span></span>](#goforward) | <span data-ttu-id="10574-214">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-214">Navigates the webview to the next page in the navigation history.</span></span>
[<span data-ttu-id="10574-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="10574-215">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#webview2_capture_preview_image_format) | <span data-ttu-id="10574-216">Formato de imagen usado por el método [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="10574-216">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>
[<span data-ttu-id="10574-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="10574-217">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#webview2_script_dialog_kind) | <span data-ttu-id="10574-218">Cuadro de diálogo tipo de JavaScript usado en la interfaz [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="10574-218">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>
[<span data-ttu-id="10574-219">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="10574-219">WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#webview2_process_failed_kind) | <span data-ttu-id="10574-220">Tipo de error de proceso usado en la interfaz de [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="10574-220">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>
[<span data-ttu-id="10574-221">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="10574-221">WEBVIEW2_PERMISSION_TYPE</span></span>](#webview2_permission_type) | <span data-ttu-id="10574-222">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="10574-222">The type of a permission request.</span></span>
[<span data-ttu-id="10574-223">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="10574-223">WEBVIEW2_PERMISSION_STATE</span></span>](#webview2_permission_state) | <span data-ttu-id="10574-224">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="10574-224">Response to a permission request.</span></span>
[<span data-ttu-id="10574-225">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="10574-225">WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#webview2_move_focus_reason) | <span data-ttu-id="10574-226">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="10574-226">Reason for moving focus.</span></span>
[<span data-ttu-id="10574-227">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="10574-227">WEBVIEW2_WEB_ERROR_STATUS</span></span>](#webview2_web_error_status) | <span data-ttu-id="10574-228">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="10574-228">Error status values for web navigations.</span></span>
[<span data-ttu-id="10574-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="10574-229">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#webview2_web_resource_context) | <span data-ttu-id="10574-230">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="10574-230">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="10574-231">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="10574-231">Navigation events</span></span>

<span data-ttu-id="10574-232">La secuencia normal de eventos de navegación es NavigationStarting, DocumentStateChanged y, después, NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10574-232">The normal sequence of navigation events is NavigationStarting, DocumentStateChanged and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="10574-234">Ten en cuenta que esto es para los eventos de navegación con el mismo evento NavigationId.</span><span class="sxs-lookup"><span data-stu-id="10574-234">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="10574-235">Los eventos de navegación con diferentes argumentos de evento de NavigationId se pueden solapar.</span><span class="sxs-lookup"><span data-stu-id="10574-235">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="10574-236">Por ejemplo, si inicia una espera de navegación para su evento NavigationStarting y, a continuación, inicia otra navegación, verá el NavigationStarting para la primera navegación, seguida de la NavigationStarting del segundo Navigate, seguido de la NavigationCompleted de la primera navegación y, a continuación, todos los demás eventos de navegación correspondientes para la segunda navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-236">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="10574-237">En casos de error puede haber o no un evento DocumentStateChanged dependiendo de si la navegación continúa o no en una página de error.</span><span class="sxs-lookup"><span data-stu-id="10574-237">In error cases there may or may not be a DocumentStateChanged event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="10574-238">En el caso de una redirección HTTP, habrá varios eventos NavigationStarting en una fila, y los siguientes tendrán establecido el marcador IsRedirect.</span><span class="sxs-lookup"><span data-stu-id="10574-238">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="10574-239">Para los submarcos dentro de WebView, el único evento de navegación desencadenado es el evento NavigationStarting, que proporciona a los host la capacidad de bloquear la navegación de los submarcos.</span><span class="sxs-lookup"><span data-stu-id="10574-239">For subframes inside WebView, the only navigation event fired is the NavigationStarting event which gives host the ability to block subframe navigations.</span></span>

## <span data-ttu-id="10574-240">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="10574-240">Process model</span></span>

<span data-ttu-id="10574-241">WebView2 usa el mismo modelo de proceso que el explorador Web de Edge.</span><span class="sxs-lookup"><span data-stu-id="10574-241">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="10574-242">Hay un proceso de explorador Edge por cada directorio de datos de usuario especificado en una sesión de usuario que servirá a cualquier proceso de llamada de WebView2 que especifique el directorio de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="10574-242">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="10574-243">Esto significa que un proceso del navegador Edge puede estar atendiendo varios procesos de llamadas y un proceso de llamada puede estar usando varios procesos de explorador.</span><span class="sxs-lookup"><span data-stu-id="10574-243">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="10574-245">Fuera de un proceso de explorador, habrá varios procesos de representación.</span><span class="sxs-lookup"><span data-stu-id="10574-245">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="10574-246">Estos se crean según sea necesario para dar servicio a varios marcos que se encuentren en diferentes vistas previas.</span><span class="sxs-lookup"><span data-stu-id="10574-246">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="10574-247">La cantidad de procesos de representación varía en función de la característica de explorador de aislamiento del sitio y la cantidad de orígenes distintos desconectados representados en las vistas de web asociadas.</span><span class="sxs-lookup"><span data-stu-id="10574-247">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="10574-249">Puede reaccionar ante los bloqueos y los bloqueos en estos procesos del explorador y el representador mediante el evento ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="10574-249">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="10574-250">Puede apagar de forma segura los procesos del explorador y el representador asociados con el método Close.</span><span class="sxs-lookup"><span data-stu-id="10574-250">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="10574-251">Modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="10574-251">Threading model</span></span>

<span data-ttu-id="10574-252">El WebView2 debe crearse en un subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="10574-252">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="10574-253">Específicamente un hilo con un bombeo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="10574-253">Specifically a thread with a message pump.</span></span> <span data-ttu-id="10574-254">Todas las devoluciones de llamada se producirán en ese subproceso y las llamadas a la vista en WebView deberán realizarse en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="10574-254">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="10574-255">No es seguro usar la vista en WebView desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="10574-255">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="10574-256">Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.</span><span class="sxs-lookup"><span data-stu-id="10574-256">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="10574-257">Es decir, si tiene un controlador de eventos ejecutándose y comienza un bucle de mensaje, no se empezarán a ejecutar de forma reentrante otros controladores de eventos o devoluciones de llamada de finalización.</span><span class="sxs-lookup"><span data-stu-id="10574-257">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="10574-258">Seguridad</span><span class="sxs-lookup"><span data-stu-id="10574-258">Security</span></span>

<span data-ttu-id="10574-259">Comprueba siempre la propiedad de origen de WebView antes de usar ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString o cualquier otro método para enviar información a WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-259">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="10574-260">Es posible que la vista Web haya navegado a otra página a través del usuario final interactuando con la página o script de la página que provoca la navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-260">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="10574-261">Del mismo modo, preste mucha atención a AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="10574-261">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="10574-262">Todas las navegaciones futuras ejecutarán esta secuencia de comandos y si proporciona acceso a información dirigida únicamente a un determinado origen, cualquier documento HTML puede tener acceso.</span><span class="sxs-lookup"><span data-stu-id="10574-262">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="10574-263">Al examinar el resultado de una llamada a un método ExecuteScript, un evento de WebMessageReceived, comprobar siempre el origen del remitente o cualquier otro mecanismo de recepción de la información de un documento HTML en una vista previa valide el URI del documento HTML es el que espera.</span><span class="sxs-lookup"><span data-stu-id="10574-263">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="10574-264">Al construir un mensaje para enviarlo a un WebView, prefiere usar PostWebMessageAsJson y construir el parámetro de cadena JSON con una biblioteca JSON.</span><span class="sxs-lookup"><span data-stu-id="10574-264">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="10574-265">Esto evitará cualquier accidente potencial de codificación de información en una cadena o script de JSON y asegúrese de que ninguna entrada controlada por el atacante pueda modificar el resto del mensaje JSON o ejecutar una secuencia de comandos arbitraria.</span><span class="sxs-lookup"><span data-stu-id="10574-265">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="10574-266">Tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="10574-266">String types</span></span>

<span data-ttu-id="10574-267">Los parámetros de salida de cadenas son LPWSTR null terminada.</span><span class="sxs-lookup"><span data-stu-id="10574-267">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="10574-268">El destinatario de la llamada asigna la cadena con CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="10574-268">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="10574-269">La propiedad se transfiere a la persona que llama y la persona que llama puede liberar la memoria usando CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="10574-269">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="10574-270">La cadena en los parámetros son cadenas terminadas en NULL LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="10574-270">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="10574-271">La persona que llama garantiza que la cadena es válida durante la llamada de función sincrónica.</span><span class="sxs-lookup"><span data-stu-id="10574-271">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="10574-272">Si el destinatario de la llamada tiene que conservar ese valor en algún punto después de que se complete la llamada de función, el destinatario de la llamada debe asignar su propia copia del valor de la cadena.</span><span class="sxs-lookup"><span data-stu-id="10574-272">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="10574-273">URI y análisis de JSON</span><span class="sxs-lookup"><span data-stu-id="10574-273">URI and JSON parsing</span></span>

<span data-ttu-id="10574-274">Varios métodos proporcionan o aceptan identificadores URI y JSON como cadenas.</span><span class="sxs-lookup"><span data-stu-id="10574-274">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="10574-275">Use su propia biblioteca preferida para analizar y generar estas cadenas.</span><span class="sxs-lookup"><span data-stu-id="10574-275">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="10574-276">Si WinRT está disponible para tu aplicación, puedes usar `RuntimeClass_Windows_Data_Json_JsonObject` y `IJsonObjectStatics` analizar o producir cadenas JSON, o bien, `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analizar y producir URI.</span><span class="sxs-lookup"><span data-stu-id="10574-276">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="10574-277">Ambos funcionan en las aplicaciones Win32.</span><span class="sxs-lookup"><span data-stu-id="10574-277">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="10574-278">Si usas IUri y CreateUri para analizar URI, es posible que desees usar los siguientes marcadores de creación de URI para que el comportamiento de CreateUri sea más parecido al de análisis de URI en la vista de vistas en vista previa:</span><span class="sxs-lookup"><span data-stu-id="10574-278">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="10574-279">Depuración</span><span class="sxs-lookup"><span data-stu-id="10574-279">Debugging</span></span>

<span data-ttu-id="10574-280">Abra DevTools con los métodos abreviados normales: `F12` o `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="10574-280">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="10574-281">Puede usar el `--auto-open-devtools-for-tabs` modificador de argumento de comando para que la ventana de DevTools se abra inmediatamente al crear una vista en vista previa.</span><span class="sxs-lookup"><span data-stu-id="10574-281">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="10574-282">Consulte la documentación de CreateWebView para obtener información sobre cómo proporcionar argumentos de la línea de comandos adicionales para el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="10574-282">See CreateWebView documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="10574-283">Consulte la clave del registro LoaderOverride para probar las diferentes compilaciones de WebView2 sin modificar la aplicación en la documentación de CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="10574-283">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateWebView documentation.</span></span>

## <span data-ttu-id="10574-284">Control de versiones</span><span class="sxs-lookup"><span data-stu-id="10574-284">Versioning</span></span>

<span data-ttu-id="10574-285">Después de haber usado una versión determinada del SDK para compilar la aplicación, es posible que la aplicación termine de funcionar con una versión anterior o posterior de los archivos binarios instalados en el explorador.</span><span class="sxs-lookup"><span data-stu-id="10574-285">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="10574-286">Hasta la versión 1.0.0.0 de WebView2, es posible que se produzcan cambios importantes durante las actualizaciones que impidan que el SDK funcione con diferentes versiones de los archivos binarios del explorador instalados.</span><span class="sxs-lookup"><span data-stu-id="10574-286">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="10574-287">Después de la versión 1.0.0.0, las diferentes versiones del SDK pueden funcionar con las distintas versiones del explorador instalado siguiendo estos procedimientos recomendados:</span><span class="sxs-lookup"><span data-stu-id="10574-287">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="10574-288">Para tener en cuenta los cambios importantes en la API, asegúrate de comprobar si se produjo un error al llamar a la CreateWebView2Environment de exportación de DLL y al llamar a QueryInterface en cualquier objeto WebView2.</span><span class="sxs-lookup"><span data-stu-id="10574-288">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateWebView2Environment and when calling QueryInterface on any WebView2 object.</span></span> <span data-ttu-id="10574-289">Un valor devuelto de E_NOINTERFACE puede indicar que el SDK no es compatible con los archivos binarios del explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="10574-289">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="10574-290">Comprobar si hay un error en QueryInterface también tendrá en cuenta los casos en los que el SDK es más reciente que la versión del explorador Edge y la aplicación intenta usar una interfaz de la que no está consciente el explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="10574-290">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="10574-291">Cuando una interfaz no está disponible, puede considerar deshabilitar la característica asociada si es posible o informar al usuario final de que necesita actualizar su explorador.</span><span class="sxs-lookup"><span data-stu-id="10574-291">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="10574-292">Miembros</span><span class="sxs-lookup"><span data-stu-id="10574-292">Members</span></span>

#### <span data-ttu-id="10574-293">get_Settings</span><span class="sxs-lookup"><span data-stu-id="10574-293">get_Settings</span></span> 

<span data-ttu-id="10574-294">El objeto [IWebView2Settings](IWebView2Settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="10574-294">The [IWebView2Settings](IWebView2Settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="10574-295">[get_Settings](#get_settings)pública HRESULT (configuración de[IWebView2Settings](IWebView2Settings.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="10574-295">public HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="10574-296">get_Source</span><span class="sxs-lookup"><span data-stu-id="10574-296">get_Source</span></span> 

<span data-ttu-id="10574-297">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="10574-297">The URI of the current top level document.</span></span>

> <span data-ttu-id="10574-298">[get_Source](#get_source)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="10574-298">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="10574-299">Este valor puede cambiar potencialmente como parte del desencadenador de eventos DocumentStateChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="10574-299">This value potentially changes as a part of the DocumentStateChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="10574-300">Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="10574-300">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="10574-301">Busque</span><span class="sxs-lookup"><span data-stu-id="10574-301">Navigate</span></span> 

<span data-ttu-id="10574-302">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="10574-302">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="10574-303">[desplazarse](#navigate)con HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="10574-303">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="10574-304">Para obtener más información, consulta los eventos de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-304">See the navigation events for more information.</span></span> <span data-ttu-id="10574-305">Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-305">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### <span data-ttu-id="10574-306">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="10574-306">MoveFocus</span></span> 

<span data-ttu-id="10574-307">Mover el foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-307">Move focus into WebView.</span></span>

> <span data-ttu-id="10574-308">[MOVEFOCUS](#movefocus)HRESULT público (razón[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) )</span><span class="sxs-lookup"><span data-stu-id="10574-308">public HRESULT [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="10574-309">La vista web obtendrá el foco y el foco se establecerá en el elemento de corresponsal de la página hospedada en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="10574-309">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="10574-310">Por motivos de programación, el foco se establece en elemento con enfoque anterior o en el elemento predeterminado si no hay ningún elemento con el foco anterior.</span><span class="sxs-lookup"><span data-stu-id="10574-310">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="10574-311">Por el siguiente motivo, el foco se establece en el primer elemento.</span><span class="sxs-lookup"><span data-stu-id="10574-311">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="10574-312">Por el motivo anterior, el foco se establece en el último elemento.</span><span class="sxs-lookup"><span data-stu-id="10574-312">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="10574-313">WebView también puede obtener el foco a través de la interacción del usuario, como hacer clic en la vista previa o en la pestaña en la misma.</span><span class="sxs-lookup"><span data-stu-id="10574-313">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="10574-314">Para la tabulación, la aplicación puede llamar a MoveFocus con la función siguiente o anterior para alinear con la tabulación y Mayús + Tab, respectivamente al decidir la vista previa del elemento tabulador.</span><span class="sxs-lookup"><span data-stu-id="10574-314">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="10574-315">O bien, la aplicación puede llamar a IsDialogMessage como parte de su bucle de mensajes para permitir que la plataforma maneje automáticamente la tabulación.</span><span class="sxs-lookup"><span data-stu-id="10574-315">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="10574-316">La plataforma girará en todas las ventanas con WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="10574-316">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="10574-317">Cuando la vista de la vista de la vista de IsDialogMessage, coloca internamente el foco en el primer o el último elemento de Tab y Mayús + Tab, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="10574-317">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (int i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="10574-318">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="10574-318">NavigateToString</span></span> 

<span data-ttu-id="10574-319">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="10574-319">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="10574-320">HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="10574-320">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="10574-321">El parámetro htmlContent no puede tener más de 2 MB de caracteres.</span><span class="sxs-lookup"><span data-stu-id="10574-321">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="10574-322">El origen de la nueva página será acerca de: Blank.</span><span class="sxs-lookup"><span data-stu-id="10574-322">The origin of the new page will be about:blank.</span></span>

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="10574-323">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-323">add_NavigationStarting</span></span> 

<span data-ttu-id="10574-324">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-324">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="10574-325">[add_NavigationStarting](#add_navigationstarting)de HRESULT público ([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-325">public HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-326">NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="10574-326">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="10574-327">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="10574-327">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### <span data-ttu-id="10574-328">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-328">remove_NavigationStarting</span></span> 

<span data-ttu-id="10574-329">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-329">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="10574-330">[remove_NavigationStarting](#remove_navigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-330">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-331">add_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="10574-331">add_DocumentStateChanged</span></span> 

<span data-ttu-id="10574-332">Agregue un controlador de eventos para el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-332">Add an event handler for the DocumentStateChanged event.</span></span>

> <span data-ttu-id="10574-333">[add_DocumentStateChanged](#add_documentstatechanged)de HRESULT público ([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-333">public HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-334">DocumentStateChanged se desencadena cuando se comienza a cargar contenido nuevo en el marco principal de WebView o si se produce una navegación de la misma página (por ejemplo, a través de la navegación de fragmentos o del historial. navegación de pushState).</span><span class="sxs-lookup"><span data-stu-id="10574-334">DocumentStateChanged fires when new content has started loading on the webview's main frame or if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="10574-335">Esto sigue el evento NavigationStarting y precede al evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10574-335">This follows the NavigationStarting event and precedes the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### <span data-ttu-id="10574-336">remove_DocumentStateChanged</span><span class="sxs-lookup"><span data-stu-id="10574-336">remove_DocumentStateChanged</span></span> 

<span data-ttu-id="10574-337">Quitar un controlador de eventos agregado previamente con add_DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-337">Remove an event handler previously added with add_DocumentStateChanged.</span></span>

> <span data-ttu-id="10574-338">[remove_DocumentStateChanged](#remove_documentstatechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-338">public HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-339">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="10574-339">add_NavigationCompleted</span></span> 

<span data-ttu-id="10574-340">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10574-340">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="10574-341">[add_NavigationCompleted](#add_navigationcompleted)de HRESULT público ([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-341">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-342">El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.</span><span class="sxs-lookup"><span data-stu-id="10574-342">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="10574-343">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="10574-343">remove_NavigationCompleted</span></span> 

<span data-ttu-id="10574-344">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10574-344">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="10574-345">[remove_NavigationCompleted](#remove_navigationcompleted)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-345">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-346">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-346">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="10574-347">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-347">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="10574-348">[add_FrameNavigationStarting](#add_framenavigationstarting)de HRESULT público ([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-348">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-349">FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="10574-349">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="10574-350">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="10574-350">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### <span data-ttu-id="10574-351">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="10574-351">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="10574-352">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10574-352">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="10574-353">[remove_FrameNavigationStarting](#remove_framenavigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-353">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-354">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="10574-354">add_MoveFocusRequested</span></span> 

<span data-ttu-id="10574-355">Agregue un controlador de eventos para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-355">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="10574-356">[add_MoveFocusRequested](#add_movefocusrequested)de HRESULT público ([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-356">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-357">MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista.</span><span class="sxs-lookup"><span data-stu-id="10574-357">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="10574-358">El foco de la vista de WebView no ha cambiado cuando se desencadena este evento.</span><span class="sxs-lookup"><span data-stu-id="10574-358">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="10574-359">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="10574-359">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="10574-360">Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-360">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="10574-361">[remove_MoveFocusRequested](#remove_movefocusrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-361">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-362">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="10574-362">add_GotFocus</span></span> 

<span data-ttu-id="10574-363">Agregue un controlador de eventos para el evento GotFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-363">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="10574-364">[add_GotFocus](#add_gotfocus)de HRESULT público ([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-364">public HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-365">GotFocus se desencadena cuando WebView tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="10574-365">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="10574-366">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="10574-366">remove_GotFocus</span></span> 

<span data-ttu-id="10574-367">Quitar un controlador de eventos agregado previamente con add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-367">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="10574-368">[remove_GotFocus](#remove_gotfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-368">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-369">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="10574-369">add_LostFocus</span></span> 

<span data-ttu-id="10574-370">Agregue un controlador de eventos para el evento LostFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-370">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="10574-371">[add_LostFocus](#add_lostfocus)de HRESULT público ([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-371">public HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-372">LostFocus se desencadena cuando WebView pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="10574-372">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="10574-373">En caso de que se inicie el evento MoveFocusRequested, el foco seguirá en la vista previa cuando se desencadene el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-373">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="10574-374">Perder el foco solo se activa cuando el código de la aplicación o la acción predeterminada del evento MoveFocusRequested está lejos de WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-374">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="10574-375">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="10574-375">remove_LostFocus</span></span> 

<span data-ttu-id="10574-376">Quitar un controlador de eventos agregado previamente con add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="10574-376">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="10574-377">[remove_LostFocus](#remove_lostfocus)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-377">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-378">add_WebResourceRequested_deprecated</span><span class="sxs-lookup"><span data-stu-id="10574-378">add_WebResourceRequested_deprecated</span></span> 

<span data-ttu-id="10574-379">Esta API estará en desuso; usa la nueva API de add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-379">This API will be deprecated, please use the new add_WebResourceRequested API.</span></span>

> <span data-ttu-id="10574-380">[add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)pública HRESULT (LPCWSTR \* const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \* const resourceContextFilter, SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-380">public HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR \*const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) \*const resourceContextFilter,SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-381">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-381">Add an event handler for the WebResourceRequested event.</span></span> <span data-ttu-id="10574-382">Se desencadena cuando WebView realiza cualquier solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="10574-382">Fires when the WebView has performs any HTTP request.</span></span> <span data-ttu-id="10574-383">Usa urlFilter para pasar una lista con filterLength de tamaño de las direcciones URL que deseas escuchar.</span><span class="sxs-lookup"><span data-stu-id="10574-383">Use urlFilter to pass in a list with size filterLength of urls to listen for.</span></span> <span data-ttu-id="10574-384">Cada entrada de dirección URL también admite caracteres comodín: ' \* ' coincide con cero o más caracteres, y '? ' coincide exactamente con un carácter.</span><span class="sxs-lookup"><span data-stu-id="10574-384">Each url entry also supports wildcards: '\*' matches zero or more characters, and '?' matches exactly one character.</span></span> <span data-ttu-id="10574-385">Para cada entrada de urlFilter, proporciona una resourceContextFilter de coincidencia que representa los tipos de recursos para los que se debe activar WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-385">For each urlFilter entry, provide a matching resourceContextFilter representing the types of resources for which WebResourceRequested should fire.</span></span> <span data-ttu-id="10574-386">Si filterLength es 0, el evento se desencadenará para todas las solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="10574-386">If filterLength is 0, the event will fire for all network requests.</span></span> <span data-ttu-id="10574-387">Los contextos de recursos admitidos son: documento, hoja de estilos, imagen, multimedia, fuente, script, XHR, Fetch.</span><span class="sxs-lookup"><span data-stu-id="10574-387">The supported resource contexts are: Document, Stylesheet, Image, Media, Font, Script, XHR, Fetch.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="10574-388">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="10574-388">remove_WebResourceRequested</span></span> 

<span data-ttu-id="10574-389">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-389">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="10574-390">[remove_WebResourceRequested](#remove_webresourcerequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-390">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-391">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="10574-391">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="10574-392">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="10574-392">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="10574-393">[add_ScriptDialogOpening](#add_scriptdialogopening)de HRESULT público ([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-393">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-394">El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-394">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="10574-395">Este evento solo se desencadena si la propiedad IWebView2Settings:: AreDefaultScriptDialogsEnabled se establece en false.</span><span class="sxs-lookup"><span data-stu-id="10574-395">This event only fires if the IWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### <span data-ttu-id="10574-396">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="10574-396">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="10574-397">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="10574-397">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="10574-398">[remove_ScriptDialogOpening](#remove_scriptdialogopening)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-398">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-399">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="10574-399">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="10574-400">Agregue un controlador de eventos para el evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-400">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="10574-401">[add_ZoomFactorChanged](#add_zoomfactorchanged)de HRESULT público ([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-401">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-402">El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="10574-402">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="10574-403">El evento se podría activar porque el autor de la llamada modificó la propiedad ZoomFactor o debido a que el usuario modificaba manualmente el zoom.</span><span class="sxs-lookup"><span data-stu-id="10574-403">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="10574-404">Cuando el autor de la llamada lo modifica a través de la propiedad ZoomFactor, el factor de zoom interno se actualiza inmediatamente y no se producirá ningún evento ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-404">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="10574-405">La vista Web asocia el último factor de zoom usado para cada sitio.</span><span class="sxs-lookup"><span data-stu-id="10574-405">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="10574-406">Por lo tanto, es posible que el factor de zoom cambie al navegar a una página diferente.</span><span class="sxs-lookup"><span data-stu-id="10574-406">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="10574-407">Cuando el factor de zoom cambia debido a esto, el evento ZoomFactorChanged se activa justo después del evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-407">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the DocumentStateChanged event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="10574-408">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="10574-408">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="10574-409">Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-409">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="10574-410">[remove_ZoomFactorChanged](#remove_zoomfactorchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-410">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-411">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="10574-411">add_PermissionRequested</span></span> 

<span data-ttu-id="10574-412">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-412">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="10574-413">[add_PermissionRequested](#add_permissionrequested)de HRESULT público ([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-413">public HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-414">Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="10574-414">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="10574-415">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="10574-415">remove_PermissionRequested</span></span> 

<span data-ttu-id="10574-416">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="10574-416">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="10574-417">[remove_PermissionRequested](#remove_permissionrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-417">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-418">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="10574-418">add_ProcessFailed</span></span> 

<span data-ttu-id="10574-419">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="10574-419">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="10574-420">[add_ProcessFailed](#add_processfailed)de HRESULT público ([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-420">public HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-421">Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.</span><span class="sxs-lookup"><span data-stu-id="10574-421">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="10574-422">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="10574-422">remove_ProcessFailed</span></span> 

<span data-ttu-id="10574-423">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="10574-423">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="10574-424">[remove_ProcessFailed](#remove_processfailed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-424">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-425">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="10574-425">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="10574-426">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="10574-426">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="10574-427">[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)de HRESULT público (LPCWSTR JavaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="10574-427">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="10574-428">El script insertado se aplicará a todas las navegaciones del marco secundario y el documento de primer nivel superior hasta que se elimine con RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="10574-428">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="10574-429">Esto se aplica de forma asincrónica y debes esperar a que se ejecute el controlador de finalización para poder asegurarte de que el script está listo para ejecutarse en navegaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="10574-429">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="10574-430">Tenga en cuenta que si un documento HTML contiene algún tipo de espacio aislado a través de propiedades de [espacio aislado](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) o el [encabezado HTTP de seguridad de contenido](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , esto afectará a la secuencia de comandos que se ejecuta aquí.</span><span class="sxs-lookup"><span data-stu-id="10574-430">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="10574-431">Así, por ejemplo, si la palabra clave "Allow-modal" no se establece, se omitirán las llamadas a la `alert` función.</span><span class="sxs-lookup"><span data-stu-id="10574-431">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="10574-432">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="10574-432">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="10574-433">Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="10574-433">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="10574-434">HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR ID)</span><span class="sxs-lookup"><span data-stu-id="10574-434">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="10574-435">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="10574-435">ExecuteScript</span></span> 

<span data-ttu-id="10574-436">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-436">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="10574-437">[ExecuteScript](#executescript)de HRESULT público (LPCWSTR JavaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="10574-437">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="10574-438">Esto se ejecutará de forma asincrónica y cuando se complete, si se proporciona un controlador en el parámetro ExecuteScriptCompletedHandler, se llamará a su método Invoke con el resultado de evaluar el JavaScript proporcionado.</span><span class="sxs-lookup"><span data-stu-id="10574-438">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="10574-439">El valor del resultado es una cadena codificada por JSON.</span><span class="sxs-lookup"><span data-stu-id="10574-439">The result value is a JSON encoded string.</span></span> <span data-ttu-id="10574-440">Si el resultado es no definido, contiene un ciclo de referencia o, de lo contrario, no se puede codificar en JSON, el valor de JSON NULL se devolverá como la cadena "null".</span><span class="sxs-lookup"><span data-stu-id="10574-440">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="10574-441">Observe que una función que no tiene ningún valor explícito devuelto devuelve undefined.</span><span class="sxs-lookup"><span data-stu-id="10574-441">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="10574-442">Si el script ejecutado inicia una excepción no controlada, el resultado es también ' null '.</span><span class="sxs-lookup"><span data-stu-id="10574-442">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="10574-443">Este método se aplica de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="10574-443">This method is applied asynchronously.</span></span> <span data-ttu-id="10574-444">Si la llamada se realiza mientras la vista en la vista previa está en un documento y se realiza una navegación después de que se realiza la llamada, pero antes de que se ejecute JavaScript, no se ejecutará el script y se llamará al controlador con E_FAIL para su parámetro errorCode.</span><span class="sxs-lookup"><span data-stu-id="10574-444">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="10574-445">ExecuteScript funcionará incluso si IsScriptEnabled se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="10574-445">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<IWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### <span data-ttu-id="10574-446">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="10574-446">CapturePreview</span></span> 

<span data-ttu-id="10574-447">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="10574-447">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="10574-448">[CAPTUREPREVIEW](#capturepreview)HRESULT público ([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream \* imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="10574-448">public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="10574-449">Especifique el formato de la imagen con el parámetro imageFormat.</span><span class="sxs-lookup"><span data-stu-id="10574-449">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="10574-450">Los datos binarios de la imagen resultantes se escriben en el parámetro imageStream proporcionado.</span><span class="sxs-lookup"><span data-stu-id="10574-450">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="10574-451">Cuando CapturePreview termina de escribir en la secuencia, se llama al método Invoke del parámetro handler proporcionado.</span><span class="sxs-lookup"><span data-stu-id="10574-451">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="10574-452">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="10574-452">Reload</span></span> 

<span data-ttu-id="10574-453">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="10574-453">Reload the current page.</span></span>

> <span data-ttu-id="10574-454">[recarga](#reload)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="10574-454">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="10574-455">Esto es similar a desplazarse hasta el URI del documento de nivel superior actual, incluidos todos los eventos de navegación que desencadenan y respetan cualquier entrada de la caché HTTP.</span><span class="sxs-lookup"><span data-stu-id="10574-455">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="10574-456">Sin embargo, el historial de atrás y reenvío no se modificará.</span><span class="sxs-lookup"><span data-stu-id="10574-456">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="10574-457">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="10574-457">get_Bounds</span></span> 

<span data-ttu-id="10574-458">Los límites de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="10574-458">The webview bounds.</span></span>

> <span data-ttu-id="10574-459">[get_Boundss](#get_bounds)HRESULT públicos (límites Rect \*)</span><span class="sxs-lookup"><span data-stu-id="10574-459">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="10574-460">Los límites son relativos al identificador HWND primario.</span><span class="sxs-lookup"><span data-stu-id="10574-460">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="10574-461">La aplicación tiene dos formas en las que puede ubicar una vista en WebView:</span><span class="sxs-lookup"><span data-stu-id="10574-461">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="10574-462">Cree un HWND secundario que sea el objeto HWND de la vista < View.</span><span class="sxs-lookup"><span data-stu-id="10574-462">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="10574-463">Coloque esta ventana donde debería estar la vista en la vista.</span><span class="sxs-lookup"><span data-stu-id="10574-463">Position this window where the WebView should be.</span></span> <span data-ttu-id="10574-464">En este caso, use (0,0) para la Bound's esquina superior izquierda de la vista de vista previa (el desplazamiento).</span><span class="sxs-lookup"><span data-stu-id="10574-464">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="10574-465">Use la última ventana de la aplicación como el HWND primario de WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-465">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="10574-466">Establezca la Bound's esquina superior izquierda de la vista previa para que la vista de la vista en la aplicación se coloque correctamente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10574-466">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="10574-467">Los valores de la entrada enlazada están en el espacio de coordenadas del host.</span><span class="sxs-lookup"><span data-stu-id="10574-467">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="10574-468">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="10574-468">put_Bounds</span></span> 

<span data-ttu-id="10574-469">Establezca la propiedad Bounds.</span><span class="sxs-lookup"><span data-stu-id="10574-469">Set the Bounds property.</span></span>

> <span data-ttu-id="10574-470">[put_Bounds](#put_bounds)de HRESULT público (límites Rect)</span><span class="sxs-lookup"><span data-stu-id="10574-470">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### <span data-ttu-id="10574-471">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="10574-471">get_ZoomFactor</span></span> 

<span data-ttu-id="10574-472">El factor de zoom para la página actual en la vista Web.</span><span class="sxs-lookup"><span data-stu-id="10574-472">The zoom factor for the current page in the WebView.</span></span>

> <span data-ttu-id="10574-473">[get_ZoomFactor](#get_zoomfactor)de HRESULT público (Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="10574-473">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="10574-474">El factor de zoom se conserva por sitio.</span><span class="sxs-lookup"><span data-stu-id="10574-474">The zoom factor is persisted per site.</span></span> <span data-ttu-id="10574-475">Ten en cuenta que cambiar el factor de zoom podría provocar un `window.innerWidth/innerHeight` cambio en el diseño de página.</span><span class="sxs-lookup"><span data-stu-id="10574-475">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="10574-476">Cuando se desplaza por la vista Web a una página de un sitio diferente, no se aplicará el factor de zoom establecido para la página anterior.</span><span class="sxs-lookup"><span data-stu-id="10574-476">When WebView navigates to a page from a different site, the zoom factor set for the previous page will not be applied.</span></span> <span data-ttu-id="10574-477">Si la aplicación quiere establecer el factor de zoom para una página determinada, el primer lugar para hacerlo es el controlador de eventos DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-477">If the app wants to set the zoom factor for a certain page, the earliest place to do it is in the DocumentStateChanged event handler.</span></span> <span data-ttu-id="10574-478">Ten en cuenta que si lo hace, es posible que reciba un evento ZoomFactorChanged para el factor de zoom persistente antes de recibir el evento ZoomFactorChanged para el factor de zoom especificado.</span><span class="sxs-lookup"><span data-stu-id="10574-478">Note that if it does that, it might receive a ZoomFactorChanged event for the persisted zoom factor before receiving the ZoomFactorChanged event for the specified zoom factor.</span></span> <span data-ttu-id="10574-479">No se permite especificar un zoomFactor menor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="10574-479">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="10574-480">WebView también tiene un intervalo de factor de zoom compatible interno.</span><span class="sxs-lookup"><span data-stu-id="10574-480">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="10574-481">Cuando un factor de zoom especificado está fuera de ese rango, se normalizará para que esté dentro del rango y se desencadenará un evento ZoomFactorChanged para el factor de zoom aplicado real.</span><span class="sxs-lookup"><span data-stu-id="10574-481">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="10574-482">Cuando se produzca esta normalización de rango, la propiedad ZoomFactor informará sobre el factor de zoom especificado durante la modificación anterior de la propiedad ZoomFactor hasta que se reciba el evento ZoomFactorChanged después de que la vista previa aplique el factor de zoom normalizado.</span><span class="sxs-lookup"><span data-stu-id="10574-482">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="10574-483">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="10574-483">put_ZoomFactor</span></span> 

<span data-ttu-id="10574-484">Establezca la propiedad ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="10574-484">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="10574-485">[put_ZoomFactor](#put_zoomfactor)de HRESULT público (Double ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="10574-485">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="10574-486">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="10574-486">get_IsVisible</span></span> 

<span data-ttu-id="10574-487">La propiedad IsVisible determina si se muestra u oculta la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-487">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="10574-488">HRESULT público [get_IsVisible](#get_isvisible)(bool \* IsVisible)</span><span class="sxs-lookup"><span data-stu-id="10574-488">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="10574-489">Si IsVisible se establece en false, WebView será transparente y no se representará.</span><span class="sxs-lookup"><span data-stu-id="10574-489">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="10574-490">Sin embargo, esto no afectará a la ventana que contenga la vista de contenido (el parámetro HWND pasado a CreateWebView).</span><span class="sxs-lookup"><span data-stu-id="10574-490">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateWebView).</span></span> <span data-ttu-id="10574-491">Si desea que esta ventana desaparezca también, llame a ShowWindow directamente, además de modificar la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="10574-491">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="10574-492">Si la ventana superior está minimizada o restaurada, WebView no recibirá mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="10574-492">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="10574-493">Por motivos de rendimiento, desarrollador debe establecer el valor de la propiedad IsVisible de la WebView en falso cuando la ventana de la aplicación está minimizada y volver a ser true cuando se restaura la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10574-493">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="10574-494">La ventana de la aplicación puede hacerlo controlando SC_MINIMIZE y SC_RESTORE comando al recibir WM_SYSCOMMAND mensaje.</span><span class="sxs-lookup"><span data-stu-id="10574-494">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="10574-495">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="10574-495">put_IsVisible</span></span> 

<span data-ttu-id="10574-496">Establezca la propiedad IsVisible.</span><span class="sxs-lookup"><span data-stu-id="10574-496">Set the IsVisible property.</span></span>

> <span data-ttu-id="10574-497">[put_IsVisible](#put_isvisible)de HRESULT público (bool IsVisible)</span><span class="sxs-lookup"><span data-stu-id="10574-497">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="10574-498">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="10574-498">PostWebMessageAsJson</span></span> 

<span data-ttu-id="10574-499">Publique el mensaje webmensaje especificado en el documento de nivel superior de este [IWebView2WebView]().</span><span class="sxs-lookup"><span data-stu-id="10574-499">Post the specified webMessage to the top level document in this [IWebView2WebView]().</span></span>

> <span data-ttu-id="10574-500">HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="10574-500">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="10574-501">Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="10574-501">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="10574-502">JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="10574-502">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="10574-503">El argumentos del evento es una instancia de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="10574-503">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="10574-504">La opción IWebView2Settings:: IsWebMessageEnabled debe ser true o este método dará un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="10574-504">The IWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="10574-505">La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10574-505">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="10574-506">La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto.</span><span class="sxs-lookup"><span data-stu-id="10574-506">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="10574-507">Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host.</span><span class="sxs-lookup"><span data-stu-id="10574-507">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="10574-508">Este mensaje se envía de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="10574-508">This message is sent asynchronously.</span></span> <span data-ttu-id="10574-509">Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.</span><span class="sxs-lookup"><span data-stu-id="10574-509">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="10574-510">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="10574-510">PostWebMessageAsString</span></span> 

<span data-ttu-id="10574-511">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10574-511">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="10574-512">HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="10574-512">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="10574-513">Esto se comporta exactamente de la misma manera que PostWebMessageAsJson, pero la `window.chrome.webview` propiedad data del argumento de evento de mensaje será una cadena con el mismo valor que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="10574-513">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="10574-514">Use este en lugar de PostWebMessageAsJson si desea comunicarse a través de cadenas simples en lugar de objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="10574-514">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="10574-515">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="10574-515">add_WebMessageReceived</span></span> 

<span data-ttu-id="10574-516">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="10574-516">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="10574-517">[add_WebMessageReceived](#add_webmessagereceived)pública HRESULT (controlador[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-517">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-518">La función postmensaje es `void postMessage(object)` donde objeto es cualquier objeto compatible con la conversión de JSON.</span><span class="sxs-lookup"><span data-stu-id="10574-518">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```cpp
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```

 <span data-ttu-id="10574-519">Cuando se llama a PostMessage, se invocará el [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) establecido a través de este método SetWebMessageReceivedEventHandler con el parámetro de objeto PostMessage convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="10574-519">When postMessage is called, the [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### <span data-ttu-id="10574-520">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="10574-520">remove_WebMessageReceived</span></span> 

<span data-ttu-id="10574-521">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="10574-521">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="10574-522">[remove_WebMessageReceived](#remove_webmessagereceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="10574-522">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-523">Cerrar</span><span class="sxs-lookup"><span data-stu-id="10574-523">Close</span></span> 

<span data-ttu-id="10574-524">Cierra WebView y limpia la instancia de explorador subyacente.</span><span class="sxs-lookup"><span data-stu-id="10574-524">Closes the webview and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="10574-525">HRESULT público [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="10574-525">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="10574-526">Si limpias el explorador instace, se liberarán los recursos que encienden la vista Web.</span><span class="sxs-lookup"><span data-stu-id="10574-526">Cleaning up the browser instace will release the resources powering the webview.</span></span> <span data-ttu-id="10574-527">La instancia del explorador se cerrará si no hay ninguna otra vista previa con ella.</span><span class="sxs-lookup"><span data-stu-id="10574-527">The browser instance will be shut down if there are no other webviews using it.</span></span>

<span data-ttu-id="10574-528">Después de llamar a Close, todas las llamadas a métodos producirán errores y los controladores de eventos dejarán de activarse.</span><span class="sxs-lookup"><span data-stu-id="10574-528">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="10574-529">Específicamente, la WebView liberará sus referencias a los controladores de eventos cuando se llama a Close.</span><span class="sxs-lookup"><span data-stu-id="10574-529">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="10574-530">Se llama implícitamente a Close cuando WebView pierde su referencia final y se destruye.</span><span class="sxs-lookup"><span data-stu-id="10574-530">Close is implicitly called when the WebView loses its final reference and is destructed.</span></span> <span data-ttu-id="10574-531">Sin embargo, se recomienda llamar de forma explícita a Close para evitar cualquier ciclo de referencias entre la vista de WebView y el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10574-531">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="10574-532">En concreto, si capturas una referencia a la vista de la vista en un controlador de eventos, crearás un ciclo de referencia entre la vista en WebView y el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="10574-532">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="10574-533">Close interrumpirá este ciclo liberando todos los controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="10574-533">Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="10574-534">Pero para evitar esta situación, se recomienda llamar explícitamente a Close en WebView y no capturar una referencia a WebView para asegurarte de que la WebView pueda limpiarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="10574-534">But to avoid this situation it is best practice to both explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### <span data-ttu-id="10574-535">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="10574-535">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="10574-536">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="10574-536">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="10574-537">HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR NOMBREDEMÉTODO, LPCWSTR ParametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="10574-537">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="10574-538">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles.</span><span class="sxs-lookup"><span data-stu-id="10574-538">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="10574-539">El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="10574-539">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="10574-540">El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente.</span><span class="sxs-lookup"><span data-stu-id="10574-540">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="10574-541">Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="10574-541">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="10574-542">Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="10574-542">Invoke will be called with the method's return object as a JSON string.</span></span>

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="10574-543">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="10574-543">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="10574-544">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="10574-544">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="10574-545">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)de HRESULT público (LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="10574-545">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="10574-546">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los eventos disponibles.</span><span class="sxs-lookup"><span data-stu-id="10574-546">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available events.</span></span> <span data-ttu-id="10574-547">El parámetro eventName es el nombre completo del evento en el formato `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="10574-547">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="10574-548">Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente.</span><span class="sxs-lookup"><span data-stu-id="10574-548">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="10574-549">Se llamará a Invoke con el objeto de los argumentos de un evento que contiene el objeto de parámetro CDP como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="10574-549">Invoke will be called with the an event args object containing the CDP event's parameter object as a JSON string.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="10574-550">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="10574-550">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="10574-551">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="10574-551">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="10574-552">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)de HRESULT público (LPCWSTR, EventRegistrationToken token)</span><span class="sxs-lookup"><span data-stu-id="10574-552">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName,EventRegistrationToken token)</span></span>

#### <span data-ttu-id="10574-553">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="10574-553">get_BrowserProcessId</span></span> 

<span data-ttu-id="10574-554">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="10574-554">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="10574-555">[get_BrowserProcessId](#get_browserprocessid)de HRESULT público (UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="10574-555">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="10574-556">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="10574-556">get_CanGoBack</span></span> 

<span data-ttu-id="10574-557">Puede navegar por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-557">Can navigate the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="10574-558">[get_CanGoBack](#get_cangoback)de HRESULT público (bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="10574-558">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="10574-559">get_CanGoBack cambiar el valor con el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-559">get_CanGoBack change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="10574-560">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="10574-560">get_CanGoForward</span></span> 

<span data-ttu-id="10574-561">Puede navegar por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-561">Can navigate the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="10574-562">[get_CanGoForward](#get_cangoforward)de HRESULT público (bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="10574-562">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="10574-563">get_CanGoForward cambiar el valor con el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="10574-563">get_CanGoForward change value with the DocumentStateChanged event.</span></span>

#### <span data-ttu-id="10574-564">GoBack</span><span class="sxs-lookup"><span data-stu-id="10574-564">GoBack</span></span> 

<span data-ttu-id="10574-565">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-565">Navigates the webview to the previous page in the navigation history.</span></span>

> <span data-ttu-id="10574-566">HRESULT público [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="10574-566">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="10574-567">GoForward</span><span class="sxs-lookup"><span data-stu-id="10574-567">GoForward</span></span> 

<span data-ttu-id="10574-568">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="10574-568">Navigates the webview to the next page in the navigation history.</span></span>

> <span data-ttu-id="10574-569">[HRESULT público](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="10574-569">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="10574-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="10574-570">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="10574-571">Formato de imagen usado por el método [IWebView2WebView:: CapturePreview](#capturepreview) .</span><span class="sxs-lookup"><span data-stu-id="10574-571">Image format used by the [IWebView2WebView::CapturePreview](#capturepreview) method.</span></span>

> <span data-ttu-id="10574-572">[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) enum</span><span class="sxs-lookup"><span data-stu-id="10574-572">enum [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="10574-573">Los</span><span class="sxs-lookup"><span data-stu-id="10574-573">Values</span></span>                         | <span data-ttu-id="10574-574">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-574">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="10574-575">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="10574-576">Formato de imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="10574-576">PNG image format.</span></span>
<span data-ttu-id="10574-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="10574-577">WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="10574-578">Formato de imagen JPEG.</span><span class="sxs-lookup"><span data-stu-id="10574-578">JPEG image format.</span></span>

#### <span data-ttu-id="10574-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="10574-579">WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="10574-580">Cuadro de diálogo tipo de JavaScript usado en la interfaz [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="10574-580">Kind of JavaScript dialog used in the [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) interface.</span></span>

> <span data-ttu-id="10574-581">[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) enum</span><span class="sxs-lookup"><span data-stu-id="10574-581">enum [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="10574-582">Los</span><span class="sxs-lookup"><span data-stu-id="10574-582">Values</span></span>                         | <span data-ttu-id="10574-583">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-583">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="10574-584">WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="10574-585">Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.</span><span class="sxs-lookup"><span data-stu-id="10574-585">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="10574-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="10574-586">WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="10574-587">Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10574-587">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="10574-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="10574-588">WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="10574-589">Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10574-589">A dialog invoked via the window.prompt JavaScript function.</span></span>

#### <span data-ttu-id="10574-590">WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="10574-590">WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="10574-591">Tipo de error de proceso usado en la interfaz de [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .</span><span class="sxs-lookup"><span data-stu-id="10574-591">Kind of process failure used in the [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) interface.</span></span>

> <span data-ttu-id="10574-592">[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) enum</span><span class="sxs-lookup"><span data-stu-id="10574-592">enum [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)</span></span>

 <span data-ttu-id="10574-593">Los</span><span class="sxs-lookup"><span data-stu-id="10574-593">Values</span></span>                         | <span data-ttu-id="10574-594">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-594">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="10574-595">WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="10574-596">Indica que el proceso del explorador ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="10574-596">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="10574-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="10574-597">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="10574-598">Indica que el proceso de representación ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="10574-598">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="10574-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="10574-599">WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="10574-600">Indica que el proceso de representación deja de responder.</span><span class="sxs-lookup"><span data-stu-id="10574-600">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="10574-601">WEBVIEW2_PERMISSION_TYPE</span><span class="sxs-lookup"><span data-stu-id="10574-601">WEBVIEW2_PERMISSION_TYPE</span></span> 

<span data-ttu-id="10574-602">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="10574-602">The type of a permission request.</span></span>

> <span data-ttu-id="10574-603">[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) enum</span><span class="sxs-lookup"><span data-stu-id="10574-603">enum [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)</span></span>

 <span data-ttu-id="10574-604">Los</span><span class="sxs-lookup"><span data-stu-id="10574-604">Values</span></span>                         | <span data-ttu-id="10574-605">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-605">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="10574-606">WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="10574-607">Permiso desconocido.</span><span class="sxs-lookup"><span data-stu-id="10574-607">Unknown permission.</span></span>
<span data-ttu-id="10574-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="10574-608">WEBVIEW2_PERMISSION_TYPE_MICROPHONE</span></span>            | <span data-ttu-id="10574-609">Permiso para capturar audio.</span><span class="sxs-lookup"><span data-stu-id="10574-609">Permission to capture audio.</span></span>
<span data-ttu-id="10574-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span><span class="sxs-lookup"><span data-stu-id="10574-610">WEBVIEW2_PERMISSION_TYPE_CAMERA</span></span>            | <span data-ttu-id="10574-611">Permiso para capturar video.</span><span class="sxs-lookup"><span data-stu-id="10574-611">Permission to capture video.</span></span>
<span data-ttu-id="10574-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="10574-612">WEBVIEW2_PERMISSION_TYPE_GEOLOCATION</span></span>            | <span data-ttu-id="10574-613">Permiso para acceder a la ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="10574-613">Permission to access geolocation.</span></span>
<span data-ttu-id="10574-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="10574-614">WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS</span></span>            | <span data-ttu-id="10574-615">Permiso para enviar notificaciones Web.</span><span class="sxs-lookup"><span data-stu-id="10574-615">Permission to send web notifications.</span></span>
<span data-ttu-id="10574-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="10574-616">WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS</span></span>            | <span data-ttu-id="10574-617">Permiso para acceder al sensor genérico.</span><span class="sxs-lookup"><span data-stu-id="10574-617">Permission to access generic sensor.</span></span>
<span data-ttu-id="10574-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="10574-618">WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ</span></span>            | <span data-ttu-id="10574-619">Permiso para leer el Portapapeles del sistema sin un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="10574-619">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="10574-620">WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="10574-620">WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="10574-621">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="10574-621">Response to a permission request.</span></span>

> <span data-ttu-id="10574-622">[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) enum</span><span class="sxs-lookup"><span data-stu-id="10574-622">enum [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)</span></span>

 <span data-ttu-id="10574-623">Los</span><span class="sxs-lookup"><span data-stu-id="10574-623">Values</span></span>                         | <span data-ttu-id="10574-624">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-624">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="10574-625">WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="10574-626">Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.</span><span class="sxs-lookup"><span data-stu-id="10574-626">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="10574-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="10574-627">WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="10574-628">Otorgue la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="10574-628">Grant the permission request.</span></span>
<span data-ttu-id="10574-629">WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="10574-629">WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="10574-630">Denegar la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="10574-630">Deny the permission request.</span></span>

#### <span data-ttu-id="10574-631">WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="10574-631">WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="10574-632">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="10574-632">Reason for moving focus.</span></span>

> <span data-ttu-id="10574-633">[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) enum</span><span class="sxs-lookup"><span data-stu-id="10574-633">enum [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)</span></span>

 <span data-ttu-id="10574-634">Los</span><span class="sxs-lookup"><span data-stu-id="10574-634">Values</span></span>                         | <span data-ttu-id="10574-635">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-635">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="10574-636">WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="10574-637">El ajuste del foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="10574-637">Code setting focus into WebView.</span></span>
<span data-ttu-id="10574-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="10574-638">WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="10574-639">Moviendo el foco debido a una resaltado de pestañas hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="10574-639">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="10574-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="10574-640">WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="10574-641">Moviendo el foco debido a un recorrido de tabulación hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="10574-641">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="10574-642">WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="10574-642">WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="10574-643">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="10574-643">Error status values for web navigations.</span></span>

> <span data-ttu-id="10574-644">[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) enum</span><span class="sxs-lookup"><span data-stu-id="10574-644">enum [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)</span></span>

 <span data-ttu-id="10574-645">Los</span><span class="sxs-lookup"><span data-stu-id="10574-645">Values</span></span>                         | <span data-ttu-id="10574-646">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-646">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="10574-647">WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="10574-648">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="10574-648">An unknown error occurred.</span></span>
<span data-ttu-id="10574-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="10574-649">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="10574-650">El nombre común del certificado SSL no coincide con la dirección Web.</span><span class="sxs-lookup"><span data-stu-id="10574-650">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="10574-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="10574-651">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="10574-652">El certificado SSL ha expirado.</span><span class="sxs-lookup"><span data-stu-id="10574-652">The SSL certificate has expired.</span></span>
<span data-ttu-id="10574-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="10574-653">WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="10574-654">El certificado de cliente SSL contiene errores.</span><span class="sxs-lookup"><span data-stu-id="10574-654">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="10574-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="10574-655">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="10574-656">El certificado SSL ha sido revocado.</span><span class="sxs-lookup"><span data-stu-id="10574-656">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="10574-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="10574-657">WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="10574-658">El certificado SSL no es válido.</span><span class="sxs-lookup"><span data-stu-id="10574-658">The SSL certificate is invalid.</span></span>
<span data-ttu-id="10574-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="10574-659">WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="10574-660">No se puede comunicar con el host.</span><span class="sxs-lookup"><span data-stu-id="10574-660">The host is unreachable.</span></span>
<span data-ttu-id="10574-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="10574-661">WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="10574-662">Se agotó el tiempo de espera de la conexión.</span><span class="sxs-lookup"><span data-stu-id="10574-662">The connection has timed out.</span></span>
<span data-ttu-id="10574-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="10574-663">WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="10574-664">El servidor ha devuelto una respuesta no válida o no reconocida.</span><span class="sxs-lookup"><span data-stu-id="10574-664">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="10574-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="10574-665">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="10574-666">La conexión ha sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="10574-666">The connection was aborted.</span></span>
<span data-ttu-id="10574-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="10574-667">WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="10574-668">Se restableció la conexión.</span><span class="sxs-lookup"><span data-stu-id="10574-668">The connection was reset.</span></span>
<span data-ttu-id="10574-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="10574-669">WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="10574-670">Se perdió la conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="10574-670">The Internet connection has been lost.</span></span>
<span data-ttu-id="10574-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="10574-671">WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="10574-672">No se puede conectar al destino.</span><span class="sxs-lookup"><span data-stu-id="10574-672">Cannot connect to destination.</span></span>
<span data-ttu-id="10574-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="10574-673">WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="10574-674">No se pudo resolver el nombre de host proporcionado.</span><span class="sxs-lookup"><span data-stu-id="10574-674">Could not resolve provided host name.</span></span>
<span data-ttu-id="10574-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="10574-675">WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="10574-676">Se canceló la operación.</span><span class="sxs-lookup"><span data-stu-id="10574-676">The operation was canceled.</span></span>
<span data-ttu-id="10574-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="10574-677">WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="10574-678">Error en la redirección de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10574-678">The request redirect failed.</span></span>
<span data-ttu-id="10574-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="10574-679">WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="10574-680">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="10574-680">An unexpected error occurred.</span></span>

#### <span data-ttu-id="10574-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="10574-681">WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="10574-682">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="10574-682">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="10574-683">[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) enum</span><span class="sxs-lookup"><span data-stu-id="10574-683">enum [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)</span></span>

 <span data-ttu-id="10574-684">Los</span><span class="sxs-lookup"><span data-stu-id="10574-684">Values</span></span>                         | <span data-ttu-id="10574-685">Descripciones</span><span class="sxs-lookup"><span data-stu-id="10574-685">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="10574-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="10574-686">WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="10574-687">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="10574-687">All resources.</span></span>
<span data-ttu-id="10574-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="10574-688">WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="10574-689">Recursos de documentos.</span><span class="sxs-lookup"><span data-stu-id="10574-689">Document resources.</span></span>
<span data-ttu-id="10574-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="10574-690">WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="10574-691">Recursos de CSS.</span><span class="sxs-lookup"><span data-stu-id="10574-691">CSS resources.</span></span>
<span data-ttu-id="10574-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="10574-692">WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="10574-693">Recursos de imagen.</span><span class="sxs-lookup"><span data-stu-id="10574-693">Image resources.</span></span>
<span data-ttu-id="10574-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="10574-694">WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="10574-695">Otros recursos multimedia, como los vídeos.</span><span class="sxs-lookup"><span data-stu-id="10574-695">Other media resources such as videos.</span></span>
<span data-ttu-id="10574-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="10574-696">WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="10574-697">Recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="10574-697">Font resources.</span></span>
<span data-ttu-id="10574-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="10574-698">WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="10574-699">Recursos de script.</span><span class="sxs-lookup"><span data-stu-id="10574-699">Script resources.</span></span>
<span data-ttu-id="10574-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="10574-700">WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="10574-701">Solicitudes XML HTTP.</span><span class="sxs-lookup"><span data-stu-id="10574-701">XML HTTP requests.</span></span>
<span data-ttu-id="10574-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="10574-702">WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="10574-703">Capture la comunicación de la API.</span><span class="sxs-lookup"><span data-stu-id="10574-703">Fetch API communication.</span></span>
<span data-ttu-id="10574-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="10574-704">WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="10574-705">Recursos de TextTrack.</span><span class="sxs-lookup"><span data-stu-id="10574-705">TextTrack resources.</span></span>
<span data-ttu-id="10574-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="10574-706">WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | 
<span data-ttu-id="10574-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="10574-707">WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | 
<span data-ttu-id="10574-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="10574-708">WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | 
<span data-ttu-id="10574-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="10574-709">WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | 
<span data-ttu-id="10574-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="10574-710">WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | 
<span data-ttu-id="10574-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="10574-711">WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | 
<span data-ttu-id="10574-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="10574-712">WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="10574-713">Otros recursos.</span><span class="sxs-lookup"><span data-stu-id="10574-713">Other resources.</span></span>
