---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: d80570a82559fccb6ae3896f7543ed75959436fa
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884431"
---
# <span data-ttu-id="57560-104">0.9.430: ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="57560-104">0.9.430 - interface ICoreWebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="57560-105">WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.</span><span class="sxs-lookup"><span data-stu-id="57560-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="57560-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="57560-106">Summary</span></span>

 <span data-ttu-id="57560-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="57560-107">Members</span></span>                        | <span data-ttu-id="57560-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="57560-109">get_Settings</span><span class="sxs-lookup"><span data-stu-id="57560-109">get_Settings</span></span>](#get_settings) | <span data-ttu-id="57560-110">El objeto ICoreWebView2Settings contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="57560-110">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="57560-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="57560-111">get_Source</span></span>](#get_source) | <span data-ttu-id="57560-112">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="57560-112">The URI of the current top level document.</span></span>
[<span data-ttu-id="57560-113">Busque</span><span class="sxs-lookup"><span data-stu-id="57560-113">Navigate</span></span>](#navigate) | <span data-ttu-id="57560-114">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="57560-114">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="57560-115">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="57560-115">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="57560-116">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="57560-116">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="57560-117">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-117">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="57560-118">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-118">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="57560-119">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-119">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="57560-120">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-120">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="57560-121">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="57560-121">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="57560-122">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="57560-122">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="57560-123">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="57560-123">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="57560-124">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="57560-124">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="57560-125">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="57560-125">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="57560-126">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="57560-126">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="57560-127">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="57560-127">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="57560-128">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-128">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="57560-129">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="57560-129">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="57560-130">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="57560-130">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="57560-131">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="57560-131">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="57560-132">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-132">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="57560-133">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="57560-133">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="57560-134">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="57560-134">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="57560-135">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="57560-135">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="57560-136">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="57560-136">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="57560-137">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-137">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="57560-138">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-138">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="57560-139">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-139">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="57560-140">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-140">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="57560-141">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="57560-141">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="57560-142">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="57560-142">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="57560-143">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="57560-143">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="57560-144">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="57560-144">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="57560-145">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="57560-145">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="57560-146">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-146">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="57560-147">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="57560-147">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="57560-148">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-148">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="57560-149">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="57560-149">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="57560-150">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="57560-150">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="57560-151">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="57560-151">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="57560-152">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="57560-152">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="57560-153">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="57560-153">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="57560-154">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="57560-154">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="57560-155">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="57560-155">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="57560-156">Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="57560-156">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="57560-157">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="57560-157">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="57560-158">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-158">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="57560-159">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="57560-159">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="57560-160">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="57560-160">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="57560-161">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="57560-161">Reload</span></span>](#reload) | <span data-ttu-id="57560-162">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="57560-162">Reload the current page.</span></span>
[<span data-ttu-id="57560-163">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="57560-163">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="57560-164">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-164">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="57560-165">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="57560-165">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="57560-166">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-166">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="57560-167">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="57560-167">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="57560-168">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="57560-168">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="57560-169">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="57560-169">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="57560-170">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="57560-170">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="57560-171">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="57560-171">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="57560-172">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="57560-172">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="57560-173">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="57560-173">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="57560-174">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="57560-174">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="57560-175">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="57560-175">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="57560-176">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-176">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="57560-177">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="57560-177">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="57560-178">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-178">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="57560-179">GoBack</span><span class="sxs-lookup"><span data-stu-id="57560-179">GoBack</span></span>](#goback) | <span data-ttu-id="57560-180">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-180">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="57560-181">GoForward</span><span class="sxs-lookup"><span data-stu-id="57560-181">GoForward</span></span>](#goforward) | <span data-ttu-id="57560-182">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-182">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="57560-183">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="57560-183">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="57560-184">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="57560-184">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="57560-185">Detener</span><span class="sxs-lookup"><span data-stu-id="57560-185">Stop</span></span>](#stop) | <span data-ttu-id="57560-186">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="57560-186">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="57560-187">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="57560-187">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="57560-188">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-188">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="57560-189">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="57560-189">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="57560-190">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-190">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="57560-191">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="57560-191">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="57560-192">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-192">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="57560-193">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="57560-193">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="57560-194">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-194">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="57560-195">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="57560-195">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="57560-196">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="57560-196">The title for the current top level document.</span></span>
[<span data-ttu-id="57560-197">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="57560-197">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="57560-198">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="57560-198">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="57560-199">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="57560-199">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="57560-200">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="57560-200">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="57560-201">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="57560-201">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="57560-202">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-202">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="57560-203">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="57560-203">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="57560-204">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="57560-204">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="57560-205">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="57560-205">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="57560-206">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="57560-206">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="57560-207">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="57560-207">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="57560-208">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="57560-208">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="57560-209">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="57560-209">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="57560-210">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-210">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="57560-211">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="57560-211">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="57560-212">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-212">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="57560-213">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="57560-213">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="57560-214">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-214">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="57560-215">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="57560-215">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="57560-216">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-216">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="57560-217">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="57560-217">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="57560-218">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-218">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="57560-219">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="57560-219">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="57560-220">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-220">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="57560-221">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="57560-221">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#core_webview2_capture_preview_image_format) | <span data-ttu-id="57560-222">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="57560-222">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="57560-223">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="57560-223">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#core_webview2_script_dialog_kind) | <span data-ttu-id="57560-224">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="57560-224">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="57560-225">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="57560-225">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#core_webview2_process_failed_kind) | <span data-ttu-id="57560-226">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="57560-226">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="57560-227">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="57560-227">CORE_WEBVIEW2_PERMISSION_KIND</span></span>](#core_webview2_permission_kind) | <span data-ttu-id="57560-228">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="57560-228">The type of a permission request.</span></span>
[<span data-ttu-id="57560-229">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="57560-229">CORE_WEBVIEW2_PERMISSION_STATE</span></span>](#core_webview2_permission_state) | <span data-ttu-id="57560-230">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="57560-230">Response to a permission request.</span></span>
[<span data-ttu-id="57560-231">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="57560-231">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span>](#core_webview2_web_error_status) | <span data-ttu-id="57560-232">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="57560-232">Error status values for web navigations.</span></span>
[<span data-ttu-id="57560-233">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="57560-233">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#core_webview2_web_resource_context) | <span data-ttu-id="57560-234">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="57560-234">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="57560-235">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="57560-235">Navigation events</span></span>

<span data-ttu-id="57560-236">La secuencia normal de eventos de navegación es NavigationStarting, SourceChanged, ContentLoading y, después, NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="57560-236">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="57560-238">Ten en cuenta que esto es para los eventos de navegación con el mismo evento NavigationId.</span><span class="sxs-lookup"><span data-stu-id="57560-238">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="57560-239">Los eventos de navegación con diferentes argumentos de evento de NavigationId se pueden solapar.</span><span class="sxs-lookup"><span data-stu-id="57560-239">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="57560-240">Por ejemplo, si inicia una espera de navegación para su evento NavigationStarting y, a continuación, inicia otra navegación, verá el NavigationStarting para la primera navegación, seguida de la NavigationStarting del segundo Navigate, seguido de la NavigationCompleted de la primera navegación y, a continuación, todos los demás eventos de navegación correspondientes para la segunda navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-240">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="57560-241">En casos de error puede haber o no un evento ContentLoading dependiendo de si la navegación continúa o no en una página de error.</span><span class="sxs-lookup"><span data-stu-id="57560-241">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="57560-242">En el caso de una redirección HTTP, habrá varios eventos NavigationStarting en una fila, y los siguientes tendrán establecido el marcador IsRedirect.</span><span class="sxs-lookup"><span data-stu-id="57560-242">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="57560-243">Para supervisar o cancelar la navegación dentro de los submarcos de la vista en WebView, use FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-243">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="57560-244">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="57560-244">Process model</span></span>

<span data-ttu-id="57560-245">WebView2 usa el mismo modelo de proceso que el explorador Web de Edge.</span><span class="sxs-lookup"><span data-stu-id="57560-245">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="57560-246">Hay un proceso de explorador Edge por cada directorio de datos de usuario especificado en una sesión de usuario que servirá a cualquier proceso de llamada de WebView2 que especifique el directorio de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="57560-246">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="57560-247">Esto significa que un proceso del navegador Edge puede estar atendiendo varios procesos de llamadas y un proceso de llamada puede estar usando varios procesos de explorador.</span><span class="sxs-lookup"><span data-stu-id="57560-247">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="57560-249">Fuera de un proceso de explorador, habrá varios procesos de representación.</span><span class="sxs-lookup"><span data-stu-id="57560-249">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="57560-250">Estos se crean según sea necesario para dar servicio a varios marcos que se encuentren en diferentes vistas previas.</span><span class="sxs-lookup"><span data-stu-id="57560-250">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="57560-251">La cantidad de procesos de representación varía en función de la característica de explorador de aislamiento del sitio y la cantidad de orígenes distintos desconectados representados en las vistas de web asociadas.</span><span class="sxs-lookup"><span data-stu-id="57560-251">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="57560-253">Puede reaccionar ante los bloqueos y los bloqueos en estos procesos del explorador y el representador mediante el evento ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="57560-253">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="57560-254">Puede apagar de forma segura los procesos del explorador y el representador asociados con el método Close.</span><span class="sxs-lookup"><span data-stu-id="57560-254">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="57560-255">Modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="57560-255">Threading model</span></span>

<span data-ttu-id="57560-256">El WebView2 debe crearse en un subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="57560-256">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="57560-257">Específicamente un hilo con un bombeo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="57560-257">Specifically a thread with a message pump.</span></span> <span data-ttu-id="57560-258">Todas las devoluciones de llamada se producirán en ese subproceso y las llamadas a la vista en WebView deberán realizarse en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="57560-258">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="57560-259">No es seguro usar la vista en WebView desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="57560-259">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="57560-260">Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.</span><span class="sxs-lookup"><span data-stu-id="57560-260">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="57560-261">Es decir, si tiene un controlador de eventos ejecutándose y comienza un bucle de mensaje, no se empezarán a ejecutar de forma reentrante otros controladores de eventos o devoluciones de llamada de finalización.</span><span class="sxs-lookup"><span data-stu-id="57560-261">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="57560-262">Seguridad</span><span class="sxs-lookup"><span data-stu-id="57560-262">Security</span></span>

<span data-ttu-id="57560-263">Comprueba siempre la propiedad de origen de WebView antes de usar ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString o cualquier otro método para enviar información a WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-263">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="57560-264">Es posible que la vista Web haya navegado a otra página a través del usuario final interactuando con la página o script de la página que provoca la navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-264">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="57560-265">Del mismo modo, preste mucha atención a AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="57560-265">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="57560-266">Todas las navegaciones futuras ejecutarán esta secuencia de comandos y si proporciona acceso a información dirigida únicamente a un determinado origen, cualquier documento HTML puede tener acceso.</span><span class="sxs-lookup"><span data-stu-id="57560-266">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="57560-267">Al examinar el resultado de una llamada a un método ExecuteScript, un evento de WebMessageReceived, comprobar siempre el origen del remitente o cualquier otro mecanismo de recepción de la información de un documento HTML en una vista previa valide el URI del documento HTML es el que espera.</span><span class="sxs-lookup"><span data-stu-id="57560-267">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="57560-268">Al construir un mensaje para enviarlo a un WebView, prefiere usar PostWebMessageAsJson y construir el parámetro de cadena JSON con una biblioteca JSON.</span><span class="sxs-lookup"><span data-stu-id="57560-268">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="57560-269">Esto evitará cualquier accidente potencial de codificación de información en una cadena o script de JSON y asegúrese de que ninguna entrada controlada por el atacante pueda modificar el resto del mensaje JSON o ejecutar una secuencia de comandos arbitraria.</span><span class="sxs-lookup"><span data-stu-id="57560-269">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="57560-270">Tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="57560-270">String types</span></span>

<span data-ttu-id="57560-271">Los parámetros de salida de cadenas son LPWSTR null terminada.</span><span class="sxs-lookup"><span data-stu-id="57560-271">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="57560-272">El destinatario de la llamada asigna la cadena con CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="57560-272">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="57560-273">La propiedad se transfiere a la persona que llama y la persona que llama puede liberar la memoria usando CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="57560-273">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="57560-274">La cadena en los parámetros son cadenas terminadas en NULL LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="57560-274">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="57560-275">La persona que llama garantiza que la cadena es válida durante la llamada de función sincrónica.</span><span class="sxs-lookup"><span data-stu-id="57560-275">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="57560-276">Si el destinatario de la llamada tiene que conservar ese valor en algún punto después de que se complete la llamada de función, el destinatario de la llamada debe asignar su propia copia del valor de la cadena.</span><span class="sxs-lookup"><span data-stu-id="57560-276">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="57560-277">URI y análisis de JSON</span><span class="sxs-lookup"><span data-stu-id="57560-277">URI and JSON parsing</span></span>

<span data-ttu-id="57560-278">Varios métodos proporcionan o aceptan identificadores URI y JSON como cadenas.</span><span class="sxs-lookup"><span data-stu-id="57560-278">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="57560-279">Use su propia biblioteca preferida para analizar y generar estas cadenas.</span><span class="sxs-lookup"><span data-stu-id="57560-279">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="57560-280">Si WinRT está disponible para tu aplicación, puedes usar `RuntimeClass_Windows_Data_Json_JsonObject` y `IJsonObjectStatics` analizar o producir cadenas JSON, o bien, `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analizar y producir URI.</span><span class="sxs-lookup"><span data-stu-id="57560-280">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="57560-281">Ambos funcionan en las aplicaciones Win32.</span><span class="sxs-lookup"><span data-stu-id="57560-281">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="57560-282">Si usas IUri y CreateUri para analizar URI, es posible que desees usar los siguientes marcadores de creación de URI para que el comportamiento de CreateUri sea más parecido al de análisis de URI en la vista de vistas en vista previa:</span><span class="sxs-lookup"><span data-stu-id="57560-282">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="57560-283">Depuración</span><span class="sxs-lookup"><span data-stu-id="57560-283">Debugging</span></span>

<span data-ttu-id="57560-284">Abra DevTools con los métodos abreviados normales: `F12` o `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="57560-284">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="57560-285">Puede usar el `--auto-open-devtools-for-tabs` modificador de argumento de comando para que la ventana de DevTools se abra inmediatamente al crear una vista en vista previa.</span><span class="sxs-lookup"><span data-stu-id="57560-285">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="57560-286">Consulte la documentación de CreateCoreWebView2Host para obtener información sobre cómo proporcionar argumentos de la línea de comandos adicionales para el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="57560-286">See CreateCoreWebView2Host documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="57560-287">Consulte la clave del registro LoaderOverride para probar las diferentes compilaciones de WebView2 sin modificar la aplicación en la documentación de CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="57560-287">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Host documentation.</span></span>

## <span data-ttu-id="57560-288">Control de versiones</span><span class="sxs-lookup"><span data-stu-id="57560-288">Versioning</span></span>

<span data-ttu-id="57560-289">Después de haber usado una versión determinada del SDK para compilar la aplicación, es posible que la aplicación termine de funcionar con una versión anterior o posterior de los archivos binarios instalados en el explorador.</span><span class="sxs-lookup"><span data-stu-id="57560-289">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="57560-290">Hasta la versión 1.0.0.0 de WebView2, es posible que se produzcan cambios importantes durante las actualizaciones que impidan que el SDK funcione con diferentes versiones de los archivos binarios del explorador instalados.</span><span class="sxs-lookup"><span data-stu-id="57560-290">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="57560-291">Después de la versión 1.0.0.0, las diferentes versiones del SDK pueden funcionar con las distintas versiones del explorador instalado siguiendo estos procedimientos recomendados:</span><span class="sxs-lookup"><span data-stu-id="57560-291">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="57560-292">Para tener en cuenta los cambios importantes en la API, asegúrate de comprobar si se produjo un error al llamar a la CreateCoreWebView2Environment de exportación de DLL y al llamar a QueryInterface en cualquier objeto CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="57560-292">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="57560-293">Un valor devuelto de E_NOINTERFACE puede indicar que el SDK no es compatible con los archivos binarios del explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="57560-293">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="57560-294">Comprobar si hay un error en QueryInterface también tendrá en cuenta los casos en los que el SDK es más reciente que la versión del explorador Edge y la aplicación intenta usar una interfaz de la que no está consciente el explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="57560-294">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="57560-295">Cuando una interfaz no está disponible, puede considerar deshabilitar la característica asociada si es posible o informar al usuario final de que necesita actualizar su explorador.</span><span class="sxs-lookup"><span data-stu-id="57560-295">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="57560-296">Miembros</span><span class="sxs-lookup"><span data-stu-id="57560-296">Members</span></span>

#### <span data-ttu-id="57560-297">get_Settings</span><span class="sxs-lookup"><span data-stu-id="57560-297">get_Settings</span></span> 

<span data-ttu-id="57560-298">El objeto ICoreWebView2Settings contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="57560-298">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="57560-299">[get_Settings](#get_settings)pública HRESULT (configuración de ICoreWebView2Settings \* \*)</span><span class="sxs-lookup"><span data-stu-id="57560-299">public HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings \*\* settings)</span></span>

#### <span data-ttu-id="57560-300">get_Source</span><span class="sxs-lookup"><span data-stu-id="57560-300">get_Source</span></span> 

<span data-ttu-id="57560-301">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="57560-301">The URI of the current top level document.</span></span>

> <span data-ttu-id="57560-302">[get_Source](#get_source)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="57560-302">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="57560-303">Este valor puede cambiar potencialmente como parte del desencadenador de eventos SourceChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="57560-303">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="57560-304">Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="57560-304">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### <span data-ttu-id="57560-305">Busque</span><span class="sxs-lookup"><span data-stu-id="57560-305">Navigate</span></span> 

<span data-ttu-id="57560-306">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="57560-306">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="57560-307">[desplazarse](#navigate)con HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="57560-307">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="57560-308">Para obtener más información, consulta los eventos de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-308">See the navigation events for more information.</span></span> <span data-ttu-id="57560-309">Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-309">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
}
```

#### <span data-ttu-id="57560-310">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="57560-310">NavigateToString</span></span> 

<span data-ttu-id="57560-311">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="57560-311">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="57560-312">HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="57560-312">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="57560-313">El parámetro htmlContent no puede tener más de 2 MB de caracteres.</span><span class="sxs-lookup"><span data-stu-id="57560-313">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="57560-314">El origen de la nueva página será acerca de: Blank.</span><span class="sxs-lookup"><span data-stu-id="57560-314">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="57560-315">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-315">add_NavigationStarting</span></span> 

<span data-ttu-id="57560-316">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-316">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="57560-317">[add_NavigationStarting](#add_navigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-317">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-318">NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="57560-318">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="57560-319">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="57560-319">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
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

#### <span data-ttu-id="57560-320">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-320">remove_NavigationStarting</span></span> 

<span data-ttu-id="57560-321">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-321">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="57560-322">[remove_NavigationStarting](#remove_navigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-322">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-323">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="57560-323">add_ContentLoading</span></span> 

<span data-ttu-id="57560-324">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="57560-324">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="57560-325">[add_ContentLoading](#add_contentloading)de HRESULT público ([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-325">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-326">ContentLoading se activa antes de que se cargue ningún contenido, incluso los scripts agregados con AddScriptToExecuteOnDocumentCreated ContentLoading no se desencadenarán si se realiza una navegación de página (por ejemplo, a través de la navegación de fragmentos o el historial. navegaciones pushState).</span><span class="sxs-lookup"><span data-stu-id="57560-326">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="57560-327">Esto sigue los eventos NavigationStarting y SourceChanged, y precede a los eventos HistoryChanged y NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="57560-327">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="57560-328">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="57560-328">remove_ContentLoading</span></span> 

<span data-ttu-id="57560-329">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="57560-329">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="57560-330">[remove_ContentLoading](#remove_contentloading)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-330">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-331">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="57560-331">add_SourceChanged</span></span> 

<span data-ttu-id="57560-332">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="57560-332">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="57560-333">[add_SourceChanged](#add_sourcechanged)de HRESULT público ([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-333">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-334">SourceChanged se desencadena para navegar a un sitio diferente o a navegación de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="57560-334">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="57560-335">No se desencadenará para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="57560-335">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="57560-336">SourceChanged se desencadena antes de ContentLoading para la navegación a un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="57560-336">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="57560-337">Agregue un controlador de eventos para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-337">Add an event handler for the SourceChanged event.</span></span> 

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### <span data-ttu-id="57560-338">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="57560-338">remove_SourceChanged</span></span> 

<span data-ttu-id="57560-339">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-339">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="57560-340">[remove_SourceChanged](#remove_sourcechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-340">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-341">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="57560-341">add_HistoryChanged</span></span> 

<span data-ttu-id="57560-342">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="57560-342">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="57560-343">[add_HistoryChanged](#add_historychanged)de HRESULT público ([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-343">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-344">Usa Facturacióncambiar para comprobar si el valor get_CanGoBack/get_CanGoForward ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="57560-344">Use HistoryChange to check if get_CanGoBack/get_CanGoForward value has changed.</span></span> <span data-ttu-id="57560-345">HistoryChanged también se desencadena para usar GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="57560-345">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="57560-346">HistoryChanged se desencadena después de SourceChanged y ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="57560-346">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="57560-347">Agregue un controlador de eventos para el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-347">Add an event handler for the HistoryChanged event.</span></span> 

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="57560-348">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="57560-348">remove_HistoryChanged</span></span> 

<span data-ttu-id="57560-349">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-349">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="57560-350">[remove_HistoryChanged](#remove_historychanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-350">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-351">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="57560-351">add_NavigationCompleted</span></span> 

<span data-ttu-id="57560-352">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="57560-352">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="57560-353">[add_NavigationCompleted](#add_navigationcompleted)de HRESULT público ([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-353">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-354">El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.</span><span class="sxs-lookup"><span data-stu-id="57560-354">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="57560-355">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="57560-355">remove_NavigationCompleted</span></span> 

<span data-ttu-id="57560-356">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="57560-356">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="57560-357">[remove_NavigationCompleted](#remove_navigationcompleted)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-357">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-358">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-358">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="57560-359">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-359">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="57560-360">[add_FrameNavigationStarting](#add_framenavigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-360">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-361">FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="57560-361">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="57560-362">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="57560-362">This will fire for redirects as well.</span></span>

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### <span data-ttu-id="57560-363">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="57560-363">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="57560-364">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57560-364">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="57560-365">[remove_FrameNavigationStarting](#remove_framenavigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-365">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-366">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="57560-366">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="57560-367">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="57560-367">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="57560-368">[add_ScriptDialogOpening](#add_scriptdialogopening)de HRESULT público ([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-368">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-369">El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-369">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="57560-370">Este evento solo se desencadena si la propiedad ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled se establece en false.</span><span class="sxs-lookup"><span data-stu-id="57560-370">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="57560-371">El evento ScriptDialogOpening se puede usar para suprimir cuadros de diálogo o reemplazar los cuadros de diálogo predeterminados con cuadros de diálogo personalizados.</span><span class="sxs-lookup"><span data-stu-id="57560-371">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
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

#### <span data-ttu-id="57560-372">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="57560-372">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="57560-373">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="57560-373">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="57560-374">[remove_ScriptDialogOpening](#remove_scriptdialogopening)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-374">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-375">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="57560-375">add_PermissionRequested</span></span> 

<span data-ttu-id="57560-376">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-376">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="57560-377">[add_PermissionRequested](#add_permissionrequested)de HRESULT público ([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-377">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-378">Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="57560-378">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="57560-379">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="57560-379">remove_PermissionRequested</span></span> 

<span data-ttu-id="57560-380">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-380">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="57560-381">[remove_PermissionRequested](#remove_permissionrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-381">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-382">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="57560-382">add_ProcessFailed</span></span> 

<span data-ttu-id="57560-383">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="57560-383">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="57560-384">[add_ProcessFailed](#add_processfailed)de HRESULT público ([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-384">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-385">Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.</span><span class="sxs-lookup"><span data-stu-id="57560-385">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="57560-386">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="57560-386">remove_ProcessFailed</span></span> 

<span data-ttu-id="57560-387">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="57560-387">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="57560-388">[remove_ProcessFailed](#remove_processfailed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-388">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-389">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="57560-389">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="57560-390">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="57560-390">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="57560-391">[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)de HRESULT público (LPCWSTR JavaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="57560-391">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="57560-392">El script insertado se aplicará a todas las navegaciones del marco secundario y el documento de primer nivel superior hasta que se elimine con RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="57560-392">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="57560-393">Esto se aplica de forma asincrónica y debes esperar a que se ejecute el controlador de finalización para poder asegurarte de que el script está listo para ejecutarse en navegaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="57560-393">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="57560-394">Tenga en cuenta que si un documento HTML contiene algún tipo de espacio aislado a través de propiedades de [espacio aislado](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) o el [encabezado HTTP de seguridad de contenido](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , esto afectará a la secuencia de comandos que se ejecuta aquí.</span><span class="sxs-lookup"><span data-stu-id="57560-394">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="57560-395">Así, por ejemplo, si la palabra clave "Allow-modal" no se establece, se omitirán las llamadas a la `alert` función.</span><span class="sxs-lookup"><span data-stu-id="57560-395">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### <span data-ttu-id="57560-396">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="57560-396">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="57560-397">Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="57560-397">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="57560-398">HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR ID)</span><span class="sxs-lookup"><span data-stu-id="57560-398">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="57560-399">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="57560-399">ExecuteScript</span></span> 

<span data-ttu-id="57560-400">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-400">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="57560-401">[ExecuteScript](#executescript)de HRESULT público (LPCWSTR JavaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="57560-401">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="57560-402">Esto se ejecutará de forma asincrónica y cuando se complete, si se proporciona un controlador en el parámetro ExecuteScriptCompletedHandler, se llamará a su método Invoke con el resultado de evaluar el JavaScript proporcionado.</span><span class="sxs-lookup"><span data-stu-id="57560-402">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="57560-403">El valor del resultado es una cadena codificada por JSON.</span><span class="sxs-lookup"><span data-stu-id="57560-403">The result value is a JSON encoded string.</span></span> <span data-ttu-id="57560-404">Si el resultado es no definido, contiene un ciclo de referencia o, de lo contrario, no se puede codificar en JSON, el valor de JSON NULL se devolverá como la cadena "null".</span><span class="sxs-lookup"><span data-stu-id="57560-404">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="57560-405">Observe que una función que no tiene ningún valor explícito devuelto devuelve undefined.</span><span class="sxs-lookup"><span data-stu-id="57560-405">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="57560-406">Si el script ejecutado inicia una excepción no controlada, el resultado es también ' null '.</span><span class="sxs-lookup"><span data-stu-id="57560-406">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="57560-407">Este método se aplica de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="57560-407">This method is applied asynchronously.</span></span> <span data-ttu-id="57560-408">Si la llamada se realiza mientras la vista en la vista previa está en un documento y se realiza una navegación después de que se realiza la llamada, pero antes de que se ejecute JavaScript, no se ejecutará el script y se llamará al controlador con E_FAIL para su parámetro errorCode.</span><span class="sxs-lookup"><span data-stu-id="57560-408">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="57560-409">ExecuteScript funcionará incluso si IsScriptEnabled se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="57560-409">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
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

#### <span data-ttu-id="57560-410">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="57560-410">CapturePreview</span></span> 

<span data-ttu-id="57560-411">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="57560-411">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="57560-412">[CAPTUREPREVIEW](#capturepreview)HRESULT público ([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="57560-412">public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="57560-413">Especifique el formato de la imagen con el parámetro imageFormat.</span><span class="sxs-lookup"><span data-stu-id="57560-413">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="57560-414">Los datos binarios de la imagen resultantes se escriben en el parámetro imageStream proporcionado.</span><span class="sxs-lookup"><span data-stu-id="57560-414">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="57560-415">Cuando CapturePreview termina de escribir en la secuencia, se llama al método Invoke del parámetro handler proporcionado.</span><span class="sxs-lookup"><span data-stu-id="57560-415">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### <span data-ttu-id="57560-416">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="57560-416">Reload</span></span> 

<span data-ttu-id="57560-417">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="57560-417">Reload the current page.</span></span>

> <span data-ttu-id="57560-418">[recarga](#reload)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="57560-418">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="57560-419">Esto es similar a desplazarse hasta el URI del documento de nivel superior actual, incluidos todos los eventos de navegación que desencadenan y respetan cualquier entrada de la caché HTTP.</span><span class="sxs-lookup"><span data-stu-id="57560-419">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="57560-420">Sin embargo, el historial de atrás y reenvío no se modificará.</span><span class="sxs-lookup"><span data-stu-id="57560-420">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="57560-421">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="57560-421">PostWebMessageAsJson</span></span> 

<span data-ttu-id="57560-422">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-422">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="57560-423">HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="57560-423">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="57560-424">Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="57560-424">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="57560-425">JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="57560-425">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="57560-426">El argumentos del evento es una instancia de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="57560-426">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="57560-427">La opción ICoreWebView2Settings:: IsWebMessageEnabled debe ser true o este método dará un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="57560-427">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="57560-428">La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-428">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="57560-429">La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto.</span><span class="sxs-lookup"><span data-stu-id="57560-429">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="57560-430">Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host.</span><span class="sxs-lookup"><span data-stu-id="57560-430">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="57560-431">Este mensaje se envía de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="57560-431">This message is sent asynchronously.</span></span> <span data-ttu-id="57560-432">Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.</span><span class="sxs-lookup"><span data-stu-id="57560-432">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="57560-433">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="57560-433">PostWebMessageAsString</span></span> 

<span data-ttu-id="57560-434">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-434">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="57560-435">HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="57560-435">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="57560-436">Esto se comporta exactamente de la misma manera que PostWebMessageAsJson, pero la `window.chrome.webview` propiedad data del argumento de evento de mensaje será una cadena con el mismo valor que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="57560-436">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="57560-437">Use este en lugar de PostWebMessageAsJson si desea comunicarse a través de cadenas simples en lugar de objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="57560-437">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="57560-438">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="57560-438">add_WebMessageReceived</span></span> 

<span data-ttu-id="57560-439">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="57560-439">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="57560-440">[add_WebMessageReceived](#add_webmessagereceived)pública HRESULT (controlador[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-440">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-441">La función postmensaje es `void postMessage(object)` donde objeto es cualquier objeto compatible con la conversión de JSON.</span><span class="sxs-lookup"><span data-stu-id="57560-441">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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

 <span data-ttu-id="57560-442">Cuando se llama a PostMessage, se invocará el [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) establecido a través de este método SetWebMessageReceivedEventHandler con el parámetro de objeto PostMessage convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="57560-442">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

#### <span data-ttu-id="57560-443">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="57560-443">remove_WebMessageReceived</span></span> 

<span data-ttu-id="57560-444">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="57560-444">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="57560-445">[remove_WebMessageReceived](#remove_webmessagereceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-445">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-446">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="57560-446">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="57560-447">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="57560-447">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="57560-448">HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR NOMBREDEMÉTODO, LPCWSTR ParametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="57560-448">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="57560-449">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles.</span><span class="sxs-lookup"><span data-stu-id="57560-449">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="57560-450">El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="57560-450">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="57560-451">El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente.</span><span class="sxs-lookup"><span data-stu-id="57560-451">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="57560-452">Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="57560-452">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="57560-453">Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="57560-453">Invoke will be called with the method's return object as a JSON string.</span></span>

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
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### <span data-ttu-id="57560-454">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="57560-454">get_BrowserProcessId</span></span> 

<span data-ttu-id="57560-455">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="57560-455">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="57560-456">[get_BrowserProcessId](#get_browserprocessid)de HRESULT público (UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="57560-456">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="57560-457">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="57560-457">get_CanGoBack</span></span> 

<span data-ttu-id="57560-458">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-458">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="57560-459">[get_CanGoBack](#get_cangoback)de HRESULT público (bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="57560-459">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="57560-460">El evento HistoryChanged se activará si get_CanGoBack cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="57560-460">The HistoryChanged event will fire if get_CanGoBack changes value.</span></span>

#### <span data-ttu-id="57560-461">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="57560-461">get_CanGoForward</span></span> 

<span data-ttu-id="57560-462">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-462">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="57560-463">[get_CanGoForward](#get_cangoforward)de HRESULT público (bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="57560-463">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="57560-464">El evento HistoryChanged se activará si get_CanGoForward cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="57560-464">The HistoryChanged event will fire if get_CanGoForward changes value.</span></span>

#### <span data-ttu-id="57560-465">GoBack</span><span class="sxs-lookup"><span data-stu-id="57560-465">GoBack</span></span> 

<span data-ttu-id="57560-466">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-466">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="57560-467">HRESULT público [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="57560-467">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="57560-468">GoForward</span><span class="sxs-lookup"><span data-stu-id="57560-468">GoForward</span></span> 

<span data-ttu-id="57560-469">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="57560-469">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="57560-470">[HRESULT público](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="57560-470">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="57560-471">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="57560-471">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="57560-472">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="57560-472">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="57560-473">HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="57560-473">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="57560-474">El parámetro eventName es el nombre completo del evento en el formato `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="57560-474">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="57560-475">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista de los eventos de protocolo DevTools Descripción y los argumentos del evento.</span><span class="sxs-lookup"><span data-stu-id="57560-475">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="57560-476">Detener</span><span class="sxs-lookup"><span data-stu-id="57560-476">Stop</span></span> 

<span data-ttu-id="57560-477">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="57560-477">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="57560-478">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="57560-478">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="57560-479">No detiene las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="57560-479">Does not stop scripts.</span></span>

#### <span data-ttu-id="57560-480">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="57560-480">add_NewWindowRequested</span></span> 

<span data-ttu-id="57560-481">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-481">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="57560-482">[add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-482">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-483">Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.</span><span class="sxs-lookup"><span data-stu-id="57560-483">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="57560-484">La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.</span><span class="sxs-lookup"><span data-stu-id="57560-484">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="57560-485">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="57560-485">remove_NewWindowRequested</span></span> 

<span data-ttu-id="57560-486">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-486">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="57560-487">[remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-487">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-488">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="57560-488">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="57560-489">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-489">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="57560-490">[add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-490">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-491">El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="57560-491">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="57560-492">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="57560-492">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="57560-493">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="57560-493">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="57560-494">[remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-494">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-495">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="57560-495">get_DocumentTitle</span></span> 

<span data-ttu-id="57560-496">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="57560-496">The title for the current top level document.</span></span>

> <span data-ttu-id="57560-497">[get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="57560-497">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="57560-498">Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="57560-498">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="57560-499">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="57560-499">AddRemoteObject</span></span> 

<span data-ttu-id="57560-500">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="57560-500">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="57560-501">[ADDREMOTEOBJECT](#addremoteobject)HRESULT público (LPCWSTR Name, Variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="57560-501">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="57560-502">Los objetos de host se exponen como proxies de objetos remotos a través de `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="57560-502">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="57560-503">Los proxies de objetos remotos son promesas y se resolverán como un objeto que represente el objeto de host.</span><span class="sxs-lookup"><span data-stu-id="57560-503">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="57560-504">La promesa se rechaza si la aplicación no ha agregado un objeto con el nombre.</span><span class="sxs-lookup"><span data-stu-id="57560-504">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="57560-505">Cuando el código de JavaScript tiene acceso a una propiedad o método del objeto, se devuelve una promesa, que se resolverá con el valor devuelto por el host para la propiedad o el método, o se rechazará en caso de error, como no se trata de una propiedad o método en el objeto o los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="57560-505">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="57560-506">Por ejemplo, cuando el código de la aplicación hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="57560-506">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="57560-507">El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="57560-507">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="57560-508">Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant.</span><span class="sxs-lookup"><span data-stu-id="57560-508">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="57560-509">Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="57560-509">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="57560-510">El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId.</span><span class="sxs-lookup"><span data-stu-id="57560-510">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="57560-511">Las matrices anidadas se admiten hasta una profundidad de 3.</span><span class="sxs-lookup"><span data-stu-id="57560-511">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="57560-512">No se admiten las matrices de los tipos de referencia.</span><span class="sxs-lookup"><span data-stu-id="57560-512">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="57560-513">VT_EMPTY y VT_NULL se asignan a JavaScript como null.</span><span class="sxs-lookup"><span data-stu-id="57560-513">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="57560-514">En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="57560-514">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="57560-515">Además, todos los objetos remotos se exponen como `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="57560-515">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="57560-516">Aquí los objetos host se exponen como proxies de objetos remotos sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="57560-516">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="57560-517">No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host.</span><span class="sxs-lookup"><span data-stu-id="57560-517">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="57560-518">Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.remoteObjects.<name>` descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="57560-518">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="57560-519">Los proxies de objetos remotos sincrónicos y los proxies asincrónicos de objetos remotos pueden tener como proxy el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="57560-519">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="57560-520">Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto remoto, ya sean otros servidores proxy, sincrónicos o asíncronos.</span><span class="sxs-lookup"><span data-stu-id="57560-520">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="57560-521">Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-521">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="57560-522">Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="57560-522">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="57560-523">Los proxies de objetos remotos son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method.</span><span class="sxs-lookup"><span data-stu-id="57560-523">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="57560-524">Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local.</span><span class="sxs-lookup"><span data-stu-id="57560-524">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="57560-525">Además, cualquier propiedad o método de la matriz se `chrome.webview.remoteObjects.options.forceLocalProperties` ejecutará de forma local.</span><span class="sxs-lookup"><span data-stu-id="57560-525">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="57560-526">De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="57560-526">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="57560-527">Puede agregar más a esta matriz, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="57560-527">You can add more to this array as required.</span></span>

<span data-ttu-id="57560-528">Hay un método que puede resultar `chrome.webview.remoteObjects.cleanupSome` más conveniente para la recolección de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="57560-528">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="57560-529">Los proxies de objetos remotos también tienen los siguientes métodos que se ejecutan de forma local:</span><span class="sxs-lookup"><span data-stu-id="57560-529">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="57560-530">applyRemote, getRemote, setRemote: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="57560-530">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="57560-531">Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto.</span><span class="sxs-lookup"><span data-stu-id="57560-531">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="57560-532">Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy.</span><span class="sxs-lookup"><span data-stu-id="57560-532">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="57560-533">Pero `proxy.applyRemote('toString')` se ejecuta `toString` en el objeto remoto a través del proxy.</span><span class="sxs-lookup"><span data-stu-id="57560-533">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="57560-534">getLocal, setLocal: realizar obtención de propiedad o conjunto de propiedades de forma local.</span><span class="sxs-lookup"><span data-stu-id="57560-534">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="57560-535">Puede usar estos métodos para forzar o establecer una propiedad en el proxy del objeto remoto, en lugar de hacerlo en el objeto remoto al que representa.</span><span class="sxs-lookup"><span data-stu-id="57560-535">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="57560-536">Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto remoto a través del proxy.</span><span class="sxs-lookup"><span data-stu-id="57560-536">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="57560-537">Pero `proxy.getLocal('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="57560-537">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="57560-538">sincronizar: los proxies de objetos remotos asincrónicos exponen un método de sincronización que devuelve una promesa de un proxy de objetos remotos sincrónico para el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="57560-538">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="57560-539">Por ejemplo, `chrome.webview.remoteObjects.sample.methodCall()` devuelve un proxy asincrónico de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="57560-539">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="57560-540">Puede usar el `sync` método para obtener un proxy de objetos remotos sincrónico en su lugar:</span><span class="sxs-lookup"><span data-stu-id="57560-540">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="57560-541">Async: los proxies de objetos remotos sincrónicos exponen un método Async que bloquea y devuelve un proxy de objetos remotos asincrónicos para el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="57560-541">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="57560-542">Por ejemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` devuelve un proxy de objeto remoto sincrónico.</span><span class="sxs-lookup"><span data-stu-id="57560-542">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="57560-543">Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto remoto asincrónico para el mismo objeto remoto:</span><span class="sxs-lookup"><span data-stu-id="57560-543">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="57560-544">después: los proxies de objetos remotos asincrónicos tienen un método then.</span><span class="sxs-lookup"><span data-stu-id="57560-544">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="57560-545">Esto permite que sean esperados.</span><span class="sxs-lookup"><span data-stu-id="57560-545">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="57560-546">devolverá una promesa que se resolverá con una representación del objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="57560-546">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="57560-547">Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local.</span><span class="sxs-lookup"><span data-stu-id="57560-547">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="57560-548">Si el proxy representa una función, se devuelve un proxy que no es de espera.</span><span class="sxs-lookup"><span data-stu-id="57560-548">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="57560-549">Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como proxy de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="57560-549">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="57560-550">Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota.</span><span class="sxs-lookup"><span data-stu-id="57560-550">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="57560-551">Los proxies de objetos remotos asincrónicos devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="57560-551">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="57560-552">La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación.</span><span class="sxs-lookup"><span data-stu-id="57560-552">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="57560-553">Los proxy de objetos remotos sincrónicos funcionan de manera similar pero bloquean la ejecución remota y esperan a que se complete la operación remota.</span><span class="sxs-lookup"><span data-stu-id="57560-553">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="57560-554">Establecer una propiedad en un proxy de objetos remotos asincrónicos funciona de forma ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="57560-554">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="57560-555">El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá.</span><span class="sxs-lookup"><span data-stu-id="57560-555">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="57560-556">Este es un requisito del objeto proxy de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-556">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="57560-557">Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setRemote que devuelve una promesa según se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="57560-557">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="57560-558">La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="57560-558">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="57560-559">Por ejemplo, supongamos que tiene un objeto COM con la siguiente interfaz</span><span class="sxs-lookup"><span data-stu-id="57560-559">For example, suppose you have a COM object with the following interface</span></span>

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="57560-560">Podemos añadir una instancia de esta interfaz a nuestro JavaScript con `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="57560-560">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="57560-561">En este caso, lo hemos denominado `sample` :</span><span class="sxs-lookup"><span data-stu-id="57560-561">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="57560-562">A continuación, en el documento HTML podemos usar este objeto COM mediante `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="57560-562">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="57560-563">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="57560-563">RemoveRemoteObject</span></span> 

<span data-ttu-id="57560-564">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="57560-564">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="57560-565">[REMOVEREMOTEOBJECT](#removeremoteobject)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="57560-565">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="57560-566">Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="57560-566">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="57560-567">Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.</span><span class="sxs-lookup"><span data-stu-id="57560-567">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="57560-568">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="57560-568">OpenDevToolsWindow</span></span> 

<span data-ttu-id="57560-569">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="57560-569">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="57560-570">[OPENDEVTOOLSWINDOW](#opendevtoolswindow)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="57560-570">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="57560-571">No hace nada si se llama cuando la ventana de DevTools ya está abierta</span><span class="sxs-lookup"><span data-stu-id="57560-571">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="57560-572">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="57560-572">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="57560-573">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="57560-573">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="57560-574">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-574">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-575">Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="57560-575">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="57560-576">Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="57560-576">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="57560-577">El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.</span><span class="sxs-lookup"><span data-stu-id="57560-577">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="57560-578">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="57560-578">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="57560-579">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="57560-579">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="57560-580">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-580">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-581">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="57560-581">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="57560-582">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="57560-582">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="57560-583">[get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="57560-583">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="57560-584">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="57560-584">add_WebResourceRequested</span></span> 

<span data-ttu-id="57560-585">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-585">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="57560-586">[add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-586">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-587">Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="57560-587">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="57560-588">Debe agregar al menos un filtro para que se active el evento.</span><span class="sxs-lookup"><span data-stu-id="57560-588">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
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

#### <span data-ttu-id="57560-589">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="57560-589">remove_WebResourceRequested</span></span> 

<span data-ttu-id="57560-590">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-590">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="57560-591">[remove_WebResourceRequested](#remove_webresourcerequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-591">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-592">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="57560-592">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="57560-593">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-593">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="57560-594">[ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="57560-594">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="57560-595">El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno).</span><span class="sxs-lookup"><span data-stu-id="57560-595">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="57560-596">nullptr es equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="57560-596">nullptr is equivalent to L"".</span></span> <span data-ttu-id="57560-597">Consulta CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.</span><span class="sxs-lookup"><span data-stu-id="57560-597">See CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="57560-598">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="57560-598">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="57560-599">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-599">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="57560-600">[REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="57560-600">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="57560-601">Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="57560-601">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="57560-602">Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="57560-602">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="57560-603">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="57560-603">add_WindowCloseRequested</span></span> 

<span data-ttu-id="57560-604">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-604">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="57560-605">[add_WindowCloseRequested](#add_windowcloserequested)de HRESULT público ([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="57560-605">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="57560-606">Se desencadena cuando el contenido de la vista en WebView solicita cerrar la ventana, por ejemplo, después de que se llame a Window. Close.</span><span class="sxs-lookup"><span data-stu-id="57560-606">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="57560-607">La aplicación debe cerrar la ventana de WebView y de la aplicación relacionada si eso tiene sentido para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="57560-607">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="57560-608">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="57560-608">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="57560-609">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="57560-609">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="57560-610">[remove_WindowCloseRequested](#remove_windowcloserequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="57560-610">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="57560-611">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="57560-611">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="57560-612">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="57560-612">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="57560-613">[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) enum</span><span class="sxs-lookup"><span data-stu-id="57560-613">enum [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="57560-614">Los</span><span class="sxs-lookup"><span data-stu-id="57560-614">Values</span></span>                         | <span data-ttu-id="57560-615">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-615">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="57560-616">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="57560-616">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="57560-617">Formato de imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="57560-617">PNG image format.</span></span>
<span data-ttu-id="57560-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="57560-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="57560-619">Formato de imagen JPEG.</span><span class="sxs-lookup"><span data-stu-id="57560-619">JPEG image format.</span></span>

#### <span data-ttu-id="57560-620">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="57560-620">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="57560-621">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="57560-621">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="57560-622">[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) enum</span><span class="sxs-lookup"><span data-stu-id="57560-622">enum [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="57560-623">Los</span><span class="sxs-lookup"><span data-stu-id="57560-623">Values</span></span>                         | <span data-ttu-id="57560-624">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-624">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="57560-625">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="57560-625">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="57560-626">Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.</span><span class="sxs-lookup"><span data-stu-id="57560-626">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="57560-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="57560-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="57560-628">Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-628">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="57560-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="57560-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="57560-630">Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-630">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="57560-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="57560-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="57560-632">Un cuadro de diálogo invocado a través del evento beforeunload de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="57560-632">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="57560-633">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="57560-633">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="57560-634">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="57560-634">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="57560-635">[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) enum</span><span class="sxs-lookup"><span data-stu-id="57560-635">enum [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span></span>

 <span data-ttu-id="57560-636">Los</span><span class="sxs-lookup"><span data-stu-id="57560-636">Values</span></span>                         | <span data-ttu-id="57560-637">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-637">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="57560-638">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="57560-638">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="57560-639">Indica que el proceso del explorador ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="57560-639">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="57560-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="57560-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="57560-641">Indica que el proceso de representación ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="57560-641">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="57560-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="57560-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="57560-643">Indica que el proceso de representación deja de responder.</span><span class="sxs-lookup"><span data-stu-id="57560-643">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="57560-644">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="57560-644">CORE_WEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="57560-645">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="57560-645">The type of a permission request.</span></span>

> <span data-ttu-id="57560-646">[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) enum</span><span class="sxs-lookup"><span data-stu-id="57560-646">enum [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span></span>

 <span data-ttu-id="57560-647">Los</span><span class="sxs-lookup"><span data-stu-id="57560-647">Values</span></span>                         | <span data-ttu-id="57560-648">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-648">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="57560-649">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="57560-649">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="57560-650">Permiso desconocido.</span><span class="sxs-lookup"><span data-stu-id="57560-650">Unknown permission.</span></span>
<span data-ttu-id="57560-651">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="57560-651">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="57560-652">Permiso para capturar audio.</span><span class="sxs-lookup"><span data-stu-id="57560-652">Permission to capture audio.</span></span>
<span data-ttu-id="57560-653">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="57560-653">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="57560-654">Permiso para capturar video.</span><span class="sxs-lookup"><span data-stu-id="57560-654">Permission to capture video.</span></span>
<span data-ttu-id="57560-655">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="57560-655">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="57560-656">Permiso para acceder a la ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="57560-656">Permission to access geolocation.</span></span>
<span data-ttu-id="57560-657">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="57560-657">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="57560-658">Permiso para enviar notificaciones Web.</span><span class="sxs-lookup"><span data-stu-id="57560-658">Permission to send web notifications.</span></span>
<span data-ttu-id="57560-659">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="57560-659">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="57560-660">Permiso para acceder al sensor genérico.</span><span class="sxs-lookup"><span data-stu-id="57560-660">Permission to access generic sensor.</span></span>
<span data-ttu-id="57560-661">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="57560-661">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="57560-662">Permiso para leer el Portapapeles del sistema sin un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="57560-662">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="57560-663">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="57560-663">CORE_WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="57560-664">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="57560-664">Response to a permission request.</span></span>

> <span data-ttu-id="57560-665">[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) enum</span><span class="sxs-lookup"><span data-stu-id="57560-665">enum [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span></span>

 <span data-ttu-id="57560-666">Los</span><span class="sxs-lookup"><span data-stu-id="57560-666">Values</span></span>                         | <span data-ttu-id="57560-667">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="57560-668">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="57560-668">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="57560-669">Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.</span><span class="sxs-lookup"><span data-stu-id="57560-669">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="57560-670">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="57560-670">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="57560-671">Otorgue la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="57560-671">Grant the permission request.</span></span>
<span data-ttu-id="57560-672">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="57560-672">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="57560-673">Denegar la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="57560-673">Deny the permission request.</span></span>

#### <span data-ttu-id="57560-674">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="57560-674">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="57560-675">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="57560-675">Error status values for web navigations.</span></span>

> <span data-ttu-id="57560-676">[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) enum</span><span class="sxs-lookup"><span data-stu-id="57560-676">enum [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span></span>

 <span data-ttu-id="57560-677">Los</span><span class="sxs-lookup"><span data-stu-id="57560-677">Values</span></span>                         | <span data-ttu-id="57560-678">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-678">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="57560-679">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="57560-679">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="57560-680">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="57560-680">An unknown error occurred.</span></span>
<span data-ttu-id="57560-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="57560-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="57560-682">El nombre común del certificado SSL no coincide con la dirección Web.</span><span class="sxs-lookup"><span data-stu-id="57560-682">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="57560-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="57560-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="57560-684">El certificado SSL ha expirado.</span><span class="sxs-lookup"><span data-stu-id="57560-684">The SSL certificate has expired.</span></span>
<span data-ttu-id="57560-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="57560-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="57560-686">El certificado de cliente SSL contiene errores.</span><span class="sxs-lookup"><span data-stu-id="57560-686">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="57560-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="57560-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="57560-688">El certificado SSL ha sido revocado.</span><span class="sxs-lookup"><span data-stu-id="57560-688">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="57560-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="57560-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="57560-690">El certificado SSL no es válido &ndash; esto puede significar que el certificado no coincide con los pin de clave pública del nombre de host, que el certificado está firmado por una autoridad que no es de confianza o con un algoritmo de signo débil. el certificado alegó que los nombres DNS han infringido las restricciones de nombres, el certificado contiene una clave débil, el período de validez del certificado es demasiado largo, falta de información de revocación o de mecanismo de revocación, nombre de host no único, falta de información de transparencia del certificado o el certificado está encadenado a una [raíz de Symantec heredado](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="57560-690">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="57560-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="57560-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="57560-692">No se puede comunicar con el host.</span><span class="sxs-lookup"><span data-stu-id="57560-692">The host is unreachable.</span></span>
<span data-ttu-id="57560-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="57560-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="57560-694">Se agotó el tiempo de espera de la conexión.</span><span class="sxs-lookup"><span data-stu-id="57560-694">The connection has timed out.</span></span>
<span data-ttu-id="57560-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="57560-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="57560-696">El servidor ha devuelto una respuesta no válida o no reconocida.</span><span class="sxs-lookup"><span data-stu-id="57560-696">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="57560-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="57560-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="57560-698">La conexión ha sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="57560-698">The connection was aborted.</span></span>
<span data-ttu-id="57560-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="57560-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="57560-700">Se restableció la conexión.</span><span class="sxs-lookup"><span data-stu-id="57560-700">The connection was reset.</span></span>
<span data-ttu-id="57560-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="57560-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="57560-702">Se perdió la conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="57560-702">The Internet connection has been lost.</span></span>
<span data-ttu-id="57560-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="57560-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="57560-704">No se puede conectar al destino.</span><span class="sxs-lookup"><span data-stu-id="57560-704">Cannot connect to destination.</span></span>
<span data-ttu-id="57560-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="57560-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="57560-706">No se pudo resolver el nombre de host proporcionado.</span><span class="sxs-lookup"><span data-stu-id="57560-706">Could not resolve provided host name.</span></span>
<span data-ttu-id="57560-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="57560-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="57560-708">Se canceló la operación.</span><span class="sxs-lookup"><span data-stu-id="57560-708">The operation was canceled.</span></span>
<span data-ttu-id="57560-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="57560-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="57560-710">Error en la redirección de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="57560-710">The request redirect failed.</span></span>
<span data-ttu-id="57560-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="57560-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="57560-712">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="57560-712">An unexpected error occurred.</span></span>

#### <span data-ttu-id="57560-713">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="57560-713">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="57560-714">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="57560-714">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="57560-715">[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) enum</span><span class="sxs-lookup"><span data-stu-id="57560-715">enum [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span></span>

 <span data-ttu-id="57560-716">Los</span><span class="sxs-lookup"><span data-stu-id="57560-716">Values</span></span>                         | <span data-ttu-id="57560-717">Descripciones</span><span class="sxs-lookup"><span data-stu-id="57560-717">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="57560-718">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="57560-718">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="57560-719">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="57560-719">All resources.</span></span>
<span data-ttu-id="57560-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="57560-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="57560-721">Recursos de documentos.</span><span class="sxs-lookup"><span data-stu-id="57560-721">Document resources.</span></span>
<span data-ttu-id="57560-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="57560-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="57560-723">Recursos de CSS.</span><span class="sxs-lookup"><span data-stu-id="57560-723">CSS resources.</span></span>
<span data-ttu-id="57560-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="57560-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="57560-725">Recursos de imagen.</span><span class="sxs-lookup"><span data-stu-id="57560-725">Image resources.</span></span>
<span data-ttu-id="57560-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="57560-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="57560-727">Otros recursos multimedia, como los vídeos.</span><span class="sxs-lookup"><span data-stu-id="57560-727">Other media resources such as videos.</span></span>
<span data-ttu-id="57560-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="57560-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="57560-729">Recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="57560-729">Font resources.</span></span>
<span data-ttu-id="57560-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="57560-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="57560-731">Recursos de script.</span><span class="sxs-lookup"><span data-stu-id="57560-731">Script resources.</span></span>
<span data-ttu-id="57560-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="57560-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="57560-733">Solicitudes XML HTTP.</span><span class="sxs-lookup"><span data-stu-id="57560-733">XML HTTP requests.</span></span>
<span data-ttu-id="57560-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="57560-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="57560-735">Capture la comunicación de la API.</span><span class="sxs-lookup"><span data-stu-id="57560-735">Fetch API communication.</span></span>
<span data-ttu-id="57560-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="57560-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="57560-737">Recursos de TextTrack.</span><span class="sxs-lookup"><span data-stu-id="57560-737">TextTrack resources.</span></span>
<span data-ttu-id="57560-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="57560-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="57560-739">Comunicación de la API de EventSource.</span><span class="sxs-lookup"><span data-stu-id="57560-739">EventSource API communication.</span></span>
<span data-ttu-id="57560-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="57560-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="57560-741">Comunicación de API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="57560-741">WebSocket API communication.</span></span>
<span data-ttu-id="57560-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="57560-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="57560-743">Manifiestos de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="57560-743">Web App Manifests.</span></span>
<span data-ttu-id="57560-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="57560-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="57560-745">Intercambio de HTTP firmado.</span><span class="sxs-lookup"><span data-stu-id="57560-745">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="57560-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="57560-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="57560-747">Solicitudes de ping.</span><span class="sxs-lookup"><span data-stu-id="57560-747">Ping requests.</span></span>
<span data-ttu-id="57560-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="57560-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="57560-749">Informes de violación de CSP.</span><span class="sxs-lookup"><span data-stu-id="57560-749">CSP Violation Reports.</span></span>
<span data-ttu-id="57560-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="57560-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="57560-751">Otros recursos.</span><span class="sxs-lookup"><span data-stu-id="57560-751">Other resources.</span></span>
