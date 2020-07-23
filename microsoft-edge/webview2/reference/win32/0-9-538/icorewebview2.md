---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2
ms.openlocfilehash: 81bc222324db9649439afa2a7c3c84f715fa2ae3
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894329"
---
# <span data-ttu-id="9d184-104">interfaz ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="9d184-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="9d184-105">WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.</span><span class="sxs-lookup"><span data-stu-id="9d184-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="9d184-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="9d184-106">Summary</span></span>

 <span data-ttu-id="9d184-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d184-107">Members</span></span>                        | <span data-ttu-id="9d184-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9d184-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="9d184-110">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="9d184-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="9d184-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9d184-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="9d184-112">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9d184-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="9d184-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="9d184-114">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="9d184-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="9d184-116">Agregue un controlador de eventos para el evento FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="9d184-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="9d184-118">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="9d184-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="9d184-120">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9d184-120">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="9d184-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="9d184-122">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="9d184-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="9d184-124">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="9d184-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="9d184-126">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="9d184-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="9d184-128">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="9d184-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9d184-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="9d184-130">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9d184-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="9d184-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9d184-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="9d184-132">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9d184-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="9d184-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="9d184-134">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="9d184-134">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="9d184-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9d184-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="9d184-136">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="9d184-136">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="9d184-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="9d184-138">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="9d184-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="9d184-140">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="9d184-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="9d184-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="9d184-142">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="9d184-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="9d184-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9d184-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="9d184-144">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="9d184-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="9d184-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9d184-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="9d184-146">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="9d184-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="9d184-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="9d184-148">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="9d184-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="9d184-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="9d184-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="9d184-150">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="9d184-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="9d184-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="9d184-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="9d184-152">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="9d184-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="9d184-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="9d184-154">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="9d184-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="9d184-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="9d184-156">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-156">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="9d184-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="9d184-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="9d184-158">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-158">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="9d184-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="9d184-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="9d184-160">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9d184-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="9d184-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="9d184-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="9d184-162">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-162">The title for the current top level document.</span></span>
[<span data-ttu-id="9d184-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="9d184-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="9d184-164">El objeto [ICoreWebView2Settings](icorewebview2settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="9d184-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="9d184-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="9d184-165">get_Source</span></span>](#get_source) | <span data-ttu-id="9d184-166">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="9d184-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="9d184-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="9d184-168">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d184-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="9d184-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="9d184-169">GoBack</span></span>](#goback) | <span data-ttu-id="9d184-170">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="9d184-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="9d184-171">GoForward</span></span>](#goforward) | <span data-ttu-id="9d184-172">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="9d184-173">Busque</span><span class="sxs-lookup"><span data-stu-id="9d184-173">Navigate</span></span>](#navigate) | <span data-ttu-id="9d184-174">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="9d184-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="9d184-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="9d184-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="9d184-176">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="9d184-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="9d184-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="9d184-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="9d184-178">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="9d184-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="9d184-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="9d184-180">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="9d184-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="9d184-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="9d184-182">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="9d184-183">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="9d184-183">Reload</span></span>](#reload) | <span data-ttu-id="9d184-184">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-184">Reload the current page.</span></span>
[<span data-ttu-id="9d184-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="9d184-186">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9d184-186">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="9d184-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9d184-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="9d184-188">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9d184-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="9d184-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="9d184-190">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="9d184-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="9d184-192">Quitar un controlador de eventos agregado previamente con add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="9d184-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="9d184-194">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="9d184-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="9d184-196">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="9d184-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="9d184-198">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="9d184-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="9d184-200">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="9d184-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="9d184-202">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="9d184-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="9d184-204">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="9d184-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9d184-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="9d184-206">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9d184-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="9d184-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9d184-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="9d184-208">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9d184-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="9d184-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="9d184-210">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="9d184-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9d184-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="9d184-212">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="9d184-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="9d184-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="9d184-214">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="9d184-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="9d184-216">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="9d184-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="9d184-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="9d184-218">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="9d184-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="9d184-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9d184-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="9d184-220">Quite el JavaScript correspondiente agregado `AddScriptToExecuteOnDocumentCreated` con el identificador de script especificado.</span><span class="sxs-lookup"><span data-stu-id="9d184-220">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>
[<span data-ttu-id="9d184-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9d184-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="9d184-222">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="9d184-223">Detener</span><span class="sxs-lookup"><span data-stu-id="9d184-223">Stop</span></span>](#stop) | <span data-ttu-id="9d184-224">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="9d184-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="9d184-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="9d184-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="9d184-226">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9d184-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="9d184-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="9d184-228">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="9d184-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="9d184-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="9d184-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="9d184-230">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="9d184-230">Reason for moving focus.</span></span>
[<span data-ttu-id="9d184-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="9d184-232">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9d184-232">The type of a permission request.</span></span>
[<span data-ttu-id="9d184-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="9d184-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="9d184-234">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9d184-234">Response to a permission request.</span></span>
[<span data-ttu-id="9d184-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="9d184-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="9d184-236">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="9d184-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="9d184-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="9d184-238">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9d184-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="9d184-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="9d184-240">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9d184-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="9d184-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="9d184-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="9d184-242">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="9d184-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="9d184-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="9d184-244">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="9d184-245">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="9d184-245">Navigation events</span></span>

<span data-ttu-id="9d184-246">La secuencia normal de eventos de navegación es NavigationStarting, SourceChanged, ContentLoading y, después, NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-246">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span> <span data-ttu-id="9d184-247">Los siguientes eventos describen el estado de la vista previa en cada navegación: NavigationStarting: WebView comienza a navegar y la navegación provocará una solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="9d184-247">The following events describe the state of WebView during each navigation: NavigationStarting: WebView is starting to navigate and the navigation will result in a network request.</span></span> <span data-ttu-id="9d184-248">El anfitrión puede no permitir la solicitud en este momento.</span><span class="sxs-lookup"><span data-stu-id="9d184-248">The host can disallow the request at this time.</span></span> <span data-ttu-id="9d184-249">SourceChanged: el origen de WebView se cambia a una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9d184-249">SourceChanged: The source of WebView is changed to a new URL.</span></span> <span data-ttu-id="9d184-250">También puede deberse a una navegación que no cause una solicitud de red, como la navegación de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="9d184-250">This may also be due to a navigation that doesn't cause a network request such as a fragment navigation.</span></span> <span data-ttu-id="9d184-251">HistoryChanged: el historial de WebView se ha actualizado como resultado de la navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-251">HistoryChanged: WebView's history has been updated as a result of the navigation.</span></span> <span data-ttu-id="9d184-252">ContentLoading: WebView ha empezado a cargar contenido nuevo.</span><span class="sxs-lookup"><span data-stu-id="9d184-252">ContentLoading: WebView has started loading new content.</span></span> <span data-ttu-id="9d184-253">NavigationCompleted: WebView terminó de cargar el contenido en la página nueva.</span><span class="sxs-lookup"><span data-stu-id="9d184-253">NavigationCompleted: WebView has completed loading content on the new page.</span></span> <span data-ttu-id="9d184-254">Los programadores pueden realizar un seguimiento de la navegación de cada documento nuevo por el identificador de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-254">Developers can track navigations to each new document by the navigation ID.</span></span> <span data-ttu-id="9d184-255">Los IDENTIFICADOres de navegación de WebView cada vez que hay una navegación correcta a un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="9d184-255">WebView's navigation ID changes every time there is a successful navigation to a new document.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="9d184-257">Ten en cuenta que esto es para los eventos de navegación con el mismo evento NavigationId.</span><span class="sxs-lookup"><span data-stu-id="9d184-257">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="9d184-258">Los eventos de navegación con diferentes argumentos de evento de NavigationId se pueden solapar.</span><span class="sxs-lookup"><span data-stu-id="9d184-258">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="9d184-259">Por ejemplo, si inicia una espera de navegación para su evento NavigationStarting y, a continuación, inicia otra navegación, verá el NavigationStarting para la primera navegación, seguida de la NavigationStarting del segundo Navigate, seguido de la NavigationCompleted de la primera navegación y, a continuación, todos los demás eventos de navegación correspondientes para la segunda navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-259">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="9d184-260">En casos de error puede haber o no un evento ContentLoading dependiendo de si la navegación continúa o no en una página de error.</span><span class="sxs-lookup"><span data-stu-id="9d184-260">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="9d184-261">En el caso de una redirección HTTP, habrá varios eventos NavigationStarting en una fila, y los que se detallan a continuación tendrán la marca IsRedirect, pero el identificador de navegación sigue siendo el mismo.</span><span class="sxs-lookup"><span data-stu-id="9d184-261">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set, however navigation ID remains the same.</span></span> <span data-ttu-id="9d184-262">Las mismas navegación de documento no producen un evento NavigationStarting y tampoco aumentan el identificador de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-262">Same document navigations do not result in NavigationStarting event and also do not increment the navigation ID.</span></span>

<span data-ttu-id="9d184-263">Para supervisar o cancelar la navegación dentro de los submarcos de la vista en WebView, use FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-263">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="9d184-264">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="9d184-264">Process model</span></span>

<span data-ttu-id="9d184-265">WebView2 usa el mismo modelo de proceso que el explorador Web de Edge.</span><span class="sxs-lookup"><span data-stu-id="9d184-265">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="9d184-266">Hay un proceso de explorador Edge por cada directorio de datos de usuario especificado en una sesión de usuario que servirá a cualquier proceso de llamada de WebView2 que especifique el directorio de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9d184-266">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="9d184-267">Esto significa que un proceso del navegador Edge puede estar atendiendo varios procesos de llamadas y un proceso de llamada puede estar usando varios procesos de explorador.</span><span class="sxs-lookup"><span data-stu-id="9d184-267">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="9d184-269">Fuera de un proceso de explorador, habrá varios procesos de representación.</span><span class="sxs-lookup"><span data-stu-id="9d184-269">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="9d184-270">Estos se crean según sea necesario para dar servicio a varios marcos que se encuentren en diferentes vistas previas.</span><span class="sxs-lookup"><span data-stu-id="9d184-270">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="9d184-271">La cantidad de procesos de representación varía en función de la característica de explorador de aislamiento del sitio y la cantidad de orígenes distintos desconectados representados en las vistas de web asociadas.</span><span class="sxs-lookup"><span data-stu-id="9d184-271">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="9d184-273">Puede reaccionar ante los bloqueos y los bloqueos en estos procesos del explorador y el representador mediante el evento ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="9d184-273">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="9d184-274">Puede apagar de forma segura los procesos del explorador y el representador asociados con el método Close.</span><span class="sxs-lookup"><span data-stu-id="9d184-274">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="9d184-275">Modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="9d184-275">Threading model</span></span>

<span data-ttu-id="9d184-276">El WebView2 debe crearse en un subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9d184-276">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="9d184-277">Específicamente un hilo con un bombeo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9d184-277">Specifically a thread with a message pump.</span></span> <span data-ttu-id="9d184-278">Todas las devoluciones de llamada se producirán en ese subproceso y las llamadas a la vista en WebView deberán realizarse en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="9d184-278">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="9d184-279">No es seguro usar la vista en WebView desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="9d184-279">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="9d184-280">Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.</span><span class="sxs-lookup"><span data-stu-id="9d184-280">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="9d184-281">Es decir, si tiene un controlador de eventos ejecutándose y comienza un bucle de mensaje, no se empezarán a ejecutar de forma reentrante otros controladores de eventos o devoluciones de llamada de finalización.</span><span class="sxs-lookup"><span data-stu-id="9d184-281">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="9d184-282">Tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="9d184-282">String types</span></span>

<span data-ttu-id="9d184-283">Los parámetros de salida de cadenas son LPWSTR null terminada.</span><span class="sxs-lookup"><span data-stu-id="9d184-283">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="9d184-284">El destinatario de la llamada asigna la cadena con CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="9d184-284">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="9d184-285">La propiedad se transfiere a la persona que llama y la persona que llama puede liberar la memoria usando CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="9d184-285">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="9d184-286">La cadena en los parámetros son cadenas terminadas en NULL LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="9d184-286">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="9d184-287">La persona que llama garantiza que la cadena es válida durante la llamada de función sincrónica.</span><span class="sxs-lookup"><span data-stu-id="9d184-287">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="9d184-288">Si el destinatario de la llamada tiene que conservar ese valor en algún punto después de que se complete la llamada de función, el destinatario de la llamada debe asignar su propia copia del valor de la cadena.</span><span class="sxs-lookup"><span data-stu-id="9d184-288">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="9d184-289">URI y análisis de JSON</span><span class="sxs-lookup"><span data-stu-id="9d184-289">URI and JSON parsing</span></span>

<span data-ttu-id="9d184-290">Varios métodos proporcionan o aceptan identificadores URI y JSON como cadenas.</span><span class="sxs-lookup"><span data-stu-id="9d184-290">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="9d184-291">Use su propia biblioteca preferida para analizar y generar estas cadenas.</span><span class="sxs-lookup"><span data-stu-id="9d184-291">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="9d184-292">Si WinRT está disponible para tu aplicación, puedes usar `RuntimeClass_Windows_Data_Json_JsonObject` y `IJsonObjectStatics` analizar o producir cadenas JSON, o bien, `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analizar y producir URI.</span><span class="sxs-lookup"><span data-stu-id="9d184-292">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="9d184-293">Ambos funcionan en las aplicaciones Win32.</span><span class="sxs-lookup"><span data-stu-id="9d184-293">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="9d184-294">Si usas IUri y CreateUri para analizar URI, es posible que desees usar los siguientes marcadores de creación de URI para que el comportamiento de CreateUri sea más parecido al de análisis de URI en la vista de vistas en vista previa:</span><span class="sxs-lookup"><span data-stu-id="9d184-294">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="9d184-295">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d184-295">Members</span></span>

#### <span data-ttu-id="9d184-296">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-296">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="9d184-297">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="9d184-297">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="9d184-298">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-298">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-299">Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9d184-299">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="9d184-300">Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9d184-300">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="9d184-301">El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d184-301">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="9d184-302">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9d184-302">add_ContentLoading</span></span> 

<span data-ttu-id="9d184-303">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9d184-303">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="9d184-304">[add_ContentLoading](#add_contentloading)de HRESULT público ([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-304">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-305">ContentLoading se activa antes de que se cargue ningún contenido, incluso los scripts agregados con AddScriptToExecuteOnDocumentCreated ContentLoading no se desencadenarán si se realiza una navegación de página (por ejemplo, a través de la navegación de fragmentos o el historial. navegaciones pushState).</span><span class="sxs-lookup"><span data-stu-id="9d184-305">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="9d184-306">Esto sigue los eventos NavigationStarting y SourceChanged, y precede a los eventos HistoryChanged y NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-306">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="9d184-307">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-307">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="9d184-308">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-308">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="9d184-309">[add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-309">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-310">El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-310">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="9d184-311">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-311">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="9d184-312">Agregue un controlador de eventos para el evento FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-312">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="9d184-313">[add_FrameNavigationCompleted](#add_framenavigationcompleted)de HRESULT público ([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-313">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-314">El evento FrameNavigationCompleted se desencadena cuando se ha cargado por completo un fotograma secundario (Body. onload) o la carga se ha detenido con error.</span><span class="sxs-lookup"><span data-stu-id="9d184-314">FrameNavigationCompleted event fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

```cpp
    // Register a handler for the FrameNavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    CHECK_FAILURE(m_webView->add_FrameNavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    std::wstring error_msg = WebErrorStatusToString(webErrorStatus);
                    MessageBox(nullptr,
                       (std::wstring(L"IFrame navigation failed with the ") +
                         L"give in error " + error_msg).c_str(),
                       L"Navigation Failure", MB_OK);
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_frameNavigationCompletedToken));
```

#### <span data-ttu-id="9d184-315">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-315">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="9d184-316">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-316">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="9d184-317">[add_FrameNavigationStarting](#add_framenavigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-317">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-318">FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="9d184-318">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="9d184-319">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="9d184-319">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="9d184-320">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-320">add_HistoryChanged</span></span> 

<span data-ttu-id="9d184-321">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9d184-321">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="9d184-322">[add_HistoryChanged](#add_historychanged)de HRESULT público ([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-322">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-323">Usa Facturacióncambiar para comprobar si el valor CanGoBack/CanGoForward ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9d184-323">Use HistoryChange to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="9d184-324">HistoryChanged también se desencadena para usar GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="9d184-324">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="9d184-325">HistoryChanged se desencadena después de SourceChanged y ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9d184-325">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="9d184-326">Agregue un controlador de eventos para el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-326">Add an event handler for the HistoryChanged event.</span></span> 
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
                m_toolbar->SetItemEnabled(Toolbar::Item_BackButton, canGoBack);
                m_toolbar->SetItemEnabled(Toolbar::Item_ForwardButton, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### <span data-ttu-id="9d184-327">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-327">add_NavigationCompleted</span></span> 

<span data-ttu-id="9d184-328">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-328">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="9d184-329">[add_NavigationCompleted](#add_navigationcompleted)de HRESULT público ([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-329">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-330">El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.</span><span class="sxs-lookup"><span data-stu-id="9d184-330">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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
                    COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
                m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
                m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### <span data-ttu-id="9d184-331">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-331">add_NavigationStarting</span></span> 

<span data-ttu-id="9d184-332">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-332">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="9d184-333">[add_NavigationStarting](#add_navigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-333">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-334">NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="9d184-334">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="9d184-335">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="9d184-335">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="9d184-336">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-336">add_NewWindowRequested</span></span> 

<span data-ttu-id="9d184-337">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-337">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="9d184-338">[add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-338">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-339">Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.</span><span class="sxs-lookup"><span data-stu-id="9d184-339">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="9d184-340">La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.</span><span class="sxs-lookup"><span data-stu-id="9d184-340">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));
                AppWindow* newAppWindow;

                wil::com_ptr<ICoreWebView2ExperimentalNewWindowRequestedEventArgs>
                    experimentalArgs;
                CHECK_FAILURE(args->QueryInterface(IID_PPV_ARGS(&experimentalArgs)));
                wil::com_ptr<ICoreWebView2ExperimentalWindowFeatures> windowFeatures;
                CHECK_FAILURE(experimentalArgs->get_WindowFeatures(&windowFeatures));

                RECT windowRect = {0};
                UINT32 left = 0;
                UINT32 top = 0;
                UINT32 height = 0;
                UINT32 width = 0;
                BOOL shouldHaveToolbar = true;

                BOOL hasPosition = FALSE;
                BOOL hasSize = FALSE;
                CHECK_FAILURE(windowFeatures->HasPosition(&hasPosition));
                CHECK_FAILURE(windowFeatures->HasSize(&hasSize));

                bool useDefaultWindow = true;

                if (!!hasPosition && !!hasSize)
                {
                    CHECK_FAILURE(windowFeatures->get_Left(&left));
                    CHECK_FAILURE(windowFeatures->get_Top(&top));
                    CHECK_FAILURE(windowFeatures->get_Height(&height));
                    CHECK_FAILURE(windowFeatures->get_Width(&width));
                    useDefaultWindow = false;
                }
                CHECK_FAILURE(windowFeatures->get_Toolbar(&shouldHaveToolbar));

                windowRect.left = left;
                windowRect.right = left + (width < s_minNewWindowSize ? s_minNewWindowSize : width);
                windowRect.top = top;
                windowRect.bottom = top + (height < s_minNewWindowSize ? s_minNewWindowSize : height);

                if (!useDefaultWindow)
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"", nullptr, true, windowRect, !!shouldHaveToolbar);
                }
                else
                {
                  newAppWindow = new AppWindow(m_creationModeId, L"");
                }
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

#### <span data-ttu-id="9d184-341">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-341">add_PermissionRequested</span></span> 

<span data-ttu-id="9d184-342">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-342">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="9d184-343">[add_PermissionRequested](#add_permissionrequested)de HRESULT público ([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-343">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-344">Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="9d184-344">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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
        COREWEBVIEW2_PERMISSION_KIND kind = COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
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

        COREWEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? COREWEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? COREWEBVIEW2_PERMISSION_STATE_DENY
            :                     COREWEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### <span data-ttu-id="9d184-345">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9d184-345">add_ProcessFailed</span></span> 

<span data-ttu-id="9d184-346">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9d184-346">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="9d184-347">[add_ProcessFailed](#add_processfailed)de HRESULT público ([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-347">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-348">Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.</span><span class="sxs-lookup"><span data-stu-id="9d184-348">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        COREWEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
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
        else if (failureType == COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process exited unexpectedly. Reload page?",
                L"Web page unresponsive", MB_YESNO);
            if (button == IDYES)
            {
                CHECK_FAILURE(m_webView->Reload());
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### <span data-ttu-id="9d184-349">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9d184-349">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="9d184-350">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9d184-350">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="9d184-351">[add_ScriptDialogOpening](#add_scriptdialogopening)de HRESULT público ([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-351">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-352">El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-352">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="9d184-353">Este evento solo se desencadena si la propiedad ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled se establece en false.</span><span class="sxs-lookup"><span data-stu-id="9d184-353">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="9d184-354">El evento ScriptDialogOpening se puede usar para suprimir cuadros de diálogo o reemplazar los cuadros de diálogo predeterminados con cuadros de diálogo personalizados.</span><span class="sxs-lookup"><span data-stu-id="9d184-354">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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
            COREWEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
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

#### <span data-ttu-id="9d184-355">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-355">add_SourceChanged</span></span> 

<span data-ttu-id="9d184-356">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="9d184-356">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="9d184-357">[add_SourceChanged](#add_sourcechanged)de HRESULT público ([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-357">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-358">SourceChanged se desencadena para navegar a un sitio diferente o a navegación de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="9d184-358">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="9d184-359">No se desencadenará para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-359">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="9d184-360">SourceChanged se desencadena antes de ContentLoading para la navegación a un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="9d184-360">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="9d184-361">Agregue un controlador de eventos para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-361">Add an event handler for the SourceChanged event.</span></span> 
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
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="9d184-362">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9d184-362">add_WebMessageReceived</span></span> 

<span data-ttu-id="9d184-363">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="9d184-363">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="9d184-364">[add_WebMessageReceived](#add_webmessagereceived)pública HRESULT (controlador[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-364">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-365">La función postmensaje es `void postMessage(object)` donde objeto es cualquier objeto compatible con la conversión de JSON.</span><span class="sxs-lookup"><span data-stu-id="9d184-365">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

```html
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
 <span data-ttu-id="9d184-366">Cuando se llama a PostMessage, se invocará el [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) establecido a través de este método SetWebMessageReceivedEventHandler con el parámetro de objeto PostMessage convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="9d184-366">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="9d184-367">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-367">add_WebResourceRequested</span></span> 

<span data-ttu-id="9d184-368">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-368">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="9d184-369">[add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-369">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-370">Se desencadena cuando WebView está realizando una solicitud de dirección URL a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="9d184-370">Fires when the WebView is performing a URL request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="9d184-371">Debe agregar al menos un filtro para que se active el evento.</span><span class="sxs-lookup"><span data-stu-id="9d184-371">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        COREWEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
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

#### <span data-ttu-id="9d184-372">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-372">add_WindowCloseRequested</span></span> 

<span data-ttu-id="9d184-373">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-373">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="9d184-374">[add_WindowCloseRequested](#add_windowcloserequested)de HRESULT público ([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9d184-374">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9d184-375">Se desencadena cuando el contenido de la vista en WebView solicita cerrar la ventana, por ejemplo, después de que se llame a Window. Close.</span><span class="sxs-lookup"><span data-stu-id="9d184-375">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="9d184-376">La aplicación debe cerrar la ventana de WebView y de la aplicación relacionada si eso tiene sentido para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d184-376">The app should close the WebView and related app window if that makes sense to the app.</span></span>

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>([this](
                                                                    ICoreWebView2* sender,
                                                                    IUnknown* args) {
            if (m_isPopupWindow)
            {
                CloseAppWindow();
            }
            return S_OK;
        }).Get(),
        nullptr));
```

#### <span data-ttu-id="9d184-377">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="9d184-377">AddHostObjectToScript</span></span> 

<span data-ttu-id="9d184-378">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="9d184-378">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="9d184-379">[ADDHOSTOBJECTTOSCRIPT](#addhostobjecttoscript)HRESULT público (LPCWSTR Name, Variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="9d184-379">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="9d184-380">Los objetos de host se exponen como proxies de objeto de host a través de `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="9d184-380">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="9d184-381">Los proxies de objeto host son promesas y se resolverán como un objeto que representa el objeto host.</span><span class="sxs-lookup"><span data-stu-id="9d184-381">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="9d184-382">La promesa se rechaza si la aplicación no ha agregado un objeto con el nombre.</span><span class="sxs-lookup"><span data-stu-id="9d184-382">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="9d184-383">Cuando el código de JavaScript tiene acceso a una propiedad o método del objeto, se devuelve una promesa, que se resolverá con el valor devuelto por el host para la propiedad o el método, o se rechazará en caso de error, como no se trata de una propiedad o método en el objeto o los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="9d184-383">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="9d184-384">Por ejemplo, cuando el código de la aplicación hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d184-384">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="9d184-385">El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="9d184-385">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="9d184-386">Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant.</span><span class="sxs-lookup"><span data-stu-id="9d184-386">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="9d184-387">Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="9d184-387">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="9d184-388">El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId.</span><span class="sxs-lookup"><span data-stu-id="9d184-388">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="9d184-389">Las matrices anidadas se admiten hasta una profundidad de 3.</span><span class="sxs-lookup"><span data-stu-id="9d184-389">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="9d184-390">No se admiten las matrices de los tipos de referencia.</span><span class="sxs-lookup"><span data-stu-id="9d184-390">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="9d184-391">VT_EMPTY y VT_NULL se asignan a JavaScript como null.</span><span class="sxs-lookup"><span data-stu-id="9d184-391">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="9d184-392">En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="9d184-392">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="9d184-393">Además, todos los objetos host se exponen como `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="9d184-393">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="9d184-394">Aquí los objetos host se exponen como proxies de objetos de host sincrónico.</span><span class="sxs-lookup"><span data-stu-id="9d184-394">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="9d184-395">No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host.</span><span class="sxs-lookup"><span data-stu-id="9d184-395">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="9d184-396">Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.hostObjects.<name>` descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9d184-396">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="9d184-397">Los proxies de objetos host sincrónicos y los proxies de objetos host asincrónicos pueden obtener el mismo objeto de host.</span><span class="sxs-lookup"><span data-stu-id="9d184-397">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="9d184-398">Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto host, ya sean otros servidores proxy, sincrónicos o asíncronos.</span><span class="sxs-lookup"><span data-stu-id="9d184-398">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="9d184-399">Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-399">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="9d184-400">Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="9d184-400">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="9d184-401">Los proxies de objetos de hospedaje son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method.</span><span class="sxs-lookup"><span data-stu-id="9d184-401">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="9d184-402">Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local.</span><span class="sxs-lookup"><span data-stu-id="9d184-402">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="9d184-403">Además, cualquier propiedad o método de la matriz se `chrome.webview.hostObjects.options.forceLocalProperties` ejecutará de forma local.</span><span class="sxs-lookup"><span data-stu-id="9d184-403">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="9d184-404">De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="9d184-404">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="9d184-405">Puede agregar más a esta matriz, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9d184-405">You can add more to this array as required.</span></span>

<span data-ttu-id="9d184-406">Hay un método que puede resultar `chrome.webview.hostObjects.cleanupSome` más conveniente para la recolección de objetos host.</span><span class="sxs-lookup"><span data-stu-id="9d184-406">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="9d184-407">Los proxies de objetos de hospedaje también tienen los siguientes métodos que se ejecutan de forma local:</span><span class="sxs-lookup"><span data-stu-id="9d184-407">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="9d184-408">applyHostFunction, getHostProperty, setHostProperty: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto host.</span><span class="sxs-lookup"><span data-stu-id="9d184-408">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="9d184-409">Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto.</span><span class="sxs-lookup"><span data-stu-id="9d184-409">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="9d184-410">Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy.</span><span class="sxs-lookup"><span data-stu-id="9d184-410">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="9d184-411">Pero `proxy.applyHostFunction('toString')` se ejecuta `toString` en el objeto de proxy del host.</span><span class="sxs-lookup"><span data-stu-id="9d184-411">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="9d184-412">getLocalProperty, setLocalProperty: propiedad get o conjunto de propiedades de forma local.</span><span class="sxs-lookup"><span data-stu-id="9d184-412">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="9d184-413">Puede usar estos métodos para forzar la obtención o la configuración de una propiedad en el proxy del objeto host, en lugar de en el objeto host que representa.</span><span class="sxs-lookup"><span data-stu-id="9d184-413">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="9d184-414">Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto de proxy del host.</span><span class="sxs-lookup"><span data-stu-id="9d184-414">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="9d184-415">Pero `proxy.getLocalProperty('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="9d184-415">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="9d184-416">sincronizar: los servidores proxy de objetos host asincrónicos exponen un método Sync que devuelve una promesa de un proxy de objeto host sincrónico para el mismo objeto host.</span><span class="sxs-lookup"><span data-stu-id="9d184-416">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="9d184-417">Por ejemplo, `chrome.webview.hostObjects.sample.methodCall()` devuelve un proxy de objeto host asincrónico.</span><span class="sxs-lookup"><span data-stu-id="9d184-417">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="9d184-418">Puede usar el `sync` método para obtener un proxy de objeto host sincrónico en su lugar:</span><span class="sxs-lookup"><span data-stu-id="9d184-418">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="9d184-419">Async: los proxies de objetos host sincrónicos exponen un método asincrónico que bloquea y devuelve un proxy de objeto host asincrónico para el mismo objeto host.</span><span class="sxs-lookup"><span data-stu-id="9d184-419">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="9d184-420">Por ejemplo, `chrome.webview.hostObjects.sync.sample.methodCall()` devuelve un proxy de objeto host sincrónico.</span><span class="sxs-lookup"><span data-stu-id="9d184-420">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="9d184-421">Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto host asincrónico para el mismo objeto host:</span><span class="sxs-lookup"><span data-stu-id="9d184-421">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="9d184-422">a continuación: los servidores proxy de objetos host asincrónicos tienen un método then.</span><span class="sxs-lookup"><span data-stu-id="9d184-422">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="9d184-423">Esto permite que sean esperados.</span><span class="sxs-lookup"><span data-stu-id="9d184-423">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="9d184-424">devolverá una promesa que se resolverá con una representación del objeto host.</span><span class="sxs-lookup"><span data-stu-id="9d184-424">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="9d184-425">Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local.</span><span class="sxs-lookup"><span data-stu-id="9d184-425">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="9d184-426">Si el proxy representa una función, se devuelve un proxy que no es de espera.</span><span class="sxs-lookup"><span data-stu-id="9d184-426">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="9d184-427">Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como servidores proxy de objeto host.</span><span class="sxs-lookup"><span data-stu-id="9d184-427">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="9d184-428">Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota.</span><span class="sxs-lookup"><span data-stu-id="9d184-428">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="9d184-429">Los proxies de objeto de host asincrónico devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9d184-429">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="9d184-430">La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación.</span><span class="sxs-lookup"><span data-stu-id="9d184-430">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="9d184-431">Los servidores proxy sincrónicos del objeto host funcionan de manera similar, pero bloquean la ejecución de JavaScript y espera a que se complete la operación remota.</span><span class="sxs-lookup"><span data-stu-id="9d184-431">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="9d184-432">Establecer una propiedad en un proxy de objeto de host asincrónico funciona de forma ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="9d184-432">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="9d184-433">El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá.</span><span class="sxs-lookup"><span data-stu-id="9d184-433">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="9d184-434">Este es un requisito del objeto proxy de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-434">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="9d184-435">Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setHostProperty que devuelve una promesa según se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9d184-435">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="9d184-436">La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9d184-436">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="9d184-437">Por ejemplo, supongamos que tiene un objeto COM con la siguiente interfaz</span><span class="sxs-lookup"><span data-stu-id="9d184-437">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IHostObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        [propget] HRESULT IndexedProperty(INT index, [out, retval] BSTR * stringResult);
        [propput] HRESULT IndexedProperty(INT index, [in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);

    };
```
 <span data-ttu-id="9d184-438">Podemos añadir una instancia de esta interfaz a nuestro JavaScript con `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="9d184-438">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="9d184-439">En este caso, lo hemos denominado `sample` :</span><span class="sxs-lookup"><span data-stu-id="9d184-439">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_hostObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddHostObjectToScript multiple times in a row without
            // calling RemoveHostObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(
                m_webView->AddHostObjectToScript(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```
 <span data-ttu-id="9d184-440">A continuación, en el documento HTML podemos usar este objeto COM mediante `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="9d184-440">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

```html
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = await chrome.webview.hostObjects.sample.property;
        document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
        const propertyValue = chrome.webview.hostObjects.sync.sample.property;
        document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyAsyncInput").value;
        // The following line will work but it will return immediately before the property value has actually been set.
        // If you need to set the property and wait for the property to change value, use the setRemote function.
        chrome.webview.hostObjects.sample.property = propertyValue;
        document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
        const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
        // If you care about waiting until the property has actually changed value use the setRemote function.
        await chrome.webview.hostObjects.sample.setRemote("property", propertyValue);
        document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
        const propertyValue = document.getElementById("setPropertySyncInput").value;
        chrome.webview.hostObjects.sync.sample.property = propertyValue;
        document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("getIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("getIndexedPropertyAsyncParam").value);
        const resultValue = await chrome.webview.hostObjects.sample.IndexedProperty[index];
        document.getElementById("getIndexedPropertyAsyncOutput").textContent = resultValue;
        });
        document.getElementById("setIndexedPropertyAsyncButton").addEventListener("click", async () => {
        const index = parseInt(document.getElementById("setIndexedPropertyAsyncParam1").value);
        const value = document.getElementById("setIndexedPropertyAsyncParam2").value;;
        chrome.webview.hostObjects.sample.IndexedProperty[index] = value;
        document.getElementById("setIndexedPropertyAsyncOutput").textContent = "Set";
        });
        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
        const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
        const resultValue = await chrome.webview.hostObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
        const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
        const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
        const resultValue = chrome.webview.hostObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
        document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
        chrome.webview.hostObjects.sample.CallCallbackAsynchronously(() => {
        document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
        });
        });
```
<span data-ttu-id="9d184-441">La exposición de objetos de host a script tiene riesgo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d184-441">Exposing host objects to script has security risk.</span></span> <span data-ttu-id="9d184-442">Siga los [procedimientos recomendados](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span><span class="sxs-lookup"><span data-stu-id="9d184-442">Please follow [best practices](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span></span>

#### <span data-ttu-id="9d184-443">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9d184-443">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="9d184-444">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="9d184-444">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="9d184-445">[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)de HRESULT público (LPCWSTR JavaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9d184-445">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="9d184-446">Este método inyecta un script que se ejecuta en todos los documentos de nivel superior y en los elementos de navegación de la página de Marcos secundarios.</span><span class="sxs-lookup"><span data-stu-id="9d184-446">This method injects a script that runs on all top-level document and child frame page navigations.</span></span> <span data-ttu-id="9d184-447">Este método se ejecuta de forma asincrónica y debes esperar a que finalice el controlador de finalización antes de que el script insertado esté listo para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="9d184-447">This method runs asynchronously, and you must wait for the completion handler to finish before the injected script is ready to run.</span></span> <span data-ttu-id="9d184-448">Cuando se completa este método, `Invoke` se llama al método del controlador con el `id` de la secuencia de comandos insertada.</span><span class="sxs-lookup"><span data-stu-id="9d184-448">When this method completes, the handler's `Invoke` method is called with the `id` of the injected script.</span></span> `id` <span data-ttu-id="9d184-449">es una cadena.</span><span class="sxs-lookup"><span data-stu-id="9d184-449">is a string.</span></span> <span data-ttu-id="9d184-450">Para quitar la secuencia de comandos insertada, use `RemoveScriptToExecuteOnDocumentCreated` .</span><span class="sxs-lookup"><span data-stu-id="9d184-450">To remove the injected script, use `RemoveScriptToExecuteOnDocumentCreated`.</span></span>

<span data-ttu-id="9d184-451">Tenga en cuenta que si un documento HTML contiene algún tipo de espacio aislado a través de propiedades de [espacio aislado](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) o el [encabezado HTTP de seguridad de contenido](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) , esto afectará a la secuencia de comandos que se ejecuta aquí.</span><span class="sxs-lookup"><span data-stu-id="9d184-451">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="9d184-452">Así, por ejemplo, si la palabra clave "Allow-modal" no se establece, se omitirán las llamadas a la `alert` función.</span><span class="sxs-lookup"><span data-stu-id="9d184-452">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="9d184-453">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9d184-453">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="9d184-454">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-454">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="9d184-455">[ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="9d184-455">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="9d184-456">El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno).</span><span class="sxs-lookup"><span data-stu-id="9d184-456">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="9d184-457">nullptr es equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="9d184-457">nullptr is equivalent to L"".</span></span> <span data-ttu-id="9d184-458">Consulta COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d184-458">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="9d184-459">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="9d184-459">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="9d184-460">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="9d184-460">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="9d184-461">HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR NOMBREDEMÉTODO, LPCWSTR ParametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9d184-461">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="9d184-462">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles.</span><span class="sxs-lookup"><span data-stu-id="9d184-462">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="9d184-463">El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="9d184-463">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="9d184-464">El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9d184-464">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="9d184-465">Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9d184-465">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="9d184-466">Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="9d184-466">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="9d184-467">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="9d184-467">CapturePreview</span></span> 

<span data-ttu-id="9d184-468">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="9d184-468">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="9d184-469">[CAPTUREPREVIEW](#capturepreview)HRESULT público ([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9d184-469">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="9d184-470">Especifique el formato de la imagen con el parámetro imageFormat.</span><span class="sxs-lookup"><span data-stu-id="9d184-470">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="9d184-471">Los datos binarios de la imagen resultantes se escriben en el parámetro imageStream proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9d184-471">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="9d184-472">Cuando CapturePreview termina de escribir en la secuencia, se llama al método Invoke del parámetro handler proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9d184-472">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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
            COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
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

#### <span data-ttu-id="9d184-473">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="9d184-473">ExecuteScript</span></span> 

<span data-ttu-id="9d184-474">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-474">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="9d184-475">[ExecuteScript](#executescript)de HRESULT público (LPCWSTR JavaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9d184-475">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="9d184-476">Esto se ejecutará de forma asincrónica y cuando se complete, si se proporciona un controlador en el parámetro ExecuteScriptCompletedHandler, se llamará a su método Invoke con el resultado de evaluar el JavaScript proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9d184-476">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="9d184-477">El valor del resultado es una cadena codificada por JSON.</span><span class="sxs-lookup"><span data-stu-id="9d184-477">The result value is a JSON encoded string.</span></span> <span data-ttu-id="9d184-478">Si el resultado es no definido, contiene un ciclo de referencia o, de lo contrario, no se puede codificar en JSON, el valor de JSON NULL se devolverá como la cadena "null".</span><span class="sxs-lookup"><span data-stu-id="9d184-478">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="9d184-479">Observe que una función que no tiene ningún valor explícito devuelto devuelve undefined.</span><span class="sxs-lookup"><span data-stu-id="9d184-479">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="9d184-480">Si el script ejecutado inicia una excepción no controlada, el resultado es también ' null '.</span><span class="sxs-lookup"><span data-stu-id="9d184-480">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="9d184-481">Este método se aplica de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9d184-481">This method is applied asynchronously.</span></span> <span data-ttu-id="9d184-482">Si se llama al método después del evento NavigationStarting durante una navegación, el script se ejecutará en el nuevo documento al cargarlo, en el momento en que se active ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9d184-482">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="9d184-483">ExecuteScript funcionará incluso si IsScriptEnabled se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="9d184-483">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="9d184-484">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="9d184-484">get_BrowserProcessId</span></span> 

<span data-ttu-id="9d184-485">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-485">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="9d184-486">[get_BrowserProcessId](#get_browserprocessid)de HRESULT público (UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="9d184-486">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="9d184-487">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="9d184-487">get_CanGoBack</span></span> 

<span data-ttu-id="9d184-488">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-488">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="9d184-489">[get_CanGoBack](#get_cangoback)de HRESULT público (bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="9d184-489">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="9d184-490">El evento HistoryChanged se desencadenará si CanGoBack cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="9d184-490">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="9d184-491">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="9d184-491">get_CanGoForward</span></span> 

<span data-ttu-id="9d184-492">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-492">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="9d184-493">[get_CanGoForward](#get_cangoforward)de HRESULT público (bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="9d184-493">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="9d184-494">El evento HistoryChanged se desencadenará si CanGoForward cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="9d184-494">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="9d184-495">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="9d184-495">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="9d184-496">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9d184-496">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="9d184-497">[get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="9d184-497">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="9d184-498">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="9d184-498">get_DocumentTitle</span></span> 

<span data-ttu-id="9d184-499">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-499">The title for the current top level document.</span></span>

> <span data-ttu-id="9d184-500">[get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="9d184-500">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="9d184-501">Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="9d184-501">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="9d184-502">get_Settings</span><span class="sxs-lookup"><span data-stu-id="9d184-502">get_Settings</span></span> 

<span data-ttu-id="9d184-503">El objeto [ICoreWebView2Settings](icorewebview2settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="9d184-503">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="9d184-504">[get_Settings](#get_settings)pública HRESULT (configuración de[ICoreWebView2Settings](icorewebview2settings.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="9d184-504">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="9d184-505">get_Source</span><span class="sxs-lookup"><span data-stu-id="9d184-505">get_Source</span></span> 

<span data-ttu-id="9d184-506">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-506">The URI of the current top level document.</span></span>

> <span data-ttu-id="9d184-507">[get_Source](#get_source)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="9d184-507">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="9d184-508">Este valor puede cambiar potencialmente como parte del desencadenador de eventos SourceChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9d184-508">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="9d184-509">Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-509">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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
                SetWindowText(GetAddressBar(), uri.get());

                return S_OK;
            })
            .Get(),
        &m_sourceChangedToken));
```

#### <span data-ttu-id="9d184-510">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="9d184-510">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="9d184-511">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d184-511">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="9d184-512">HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="9d184-512">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="9d184-513">El parámetro eventName es el nombre completo del evento en el formato `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="9d184-513">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="9d184-514">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista de los eventos de protocolo DevTools Descripción y los argumentos del evento.</span><span class="sxs-lookup"><span data-stu-id="9d184-514">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="9d184-515">GoBack</span><span class="sxs-lookup"><span data-stu-id="9d184-515">GoBack</span></span> 

<span data-ttu-id="9d184-516">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-516">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="9d184-517">HRESULT público [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="9d184-517">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="9d184-518">GoForward</span><span class="sxs-lookup"><span data-stu-id="9d184-518">GoForward</span></span> 

<span data-ttu-id="9d184-519">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-519">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="9d184-520">[HRESULT público](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="9d184-520">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="9d184-521">Busque</span><span class="sxs-lookup"><span data-stu-id="9d184-521">Navigate</span></span> 

<span data-ttu-id="9d184-522">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="9d184-522">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="9d184-523">[desplazarse](#navigate)con HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9d184-523">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="9d184-524">Para obtener más información, consulta los eventos de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-524">See the navigation events for more information.</span></span> <span data-ttu-id="9d184-525">Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.</span><span class="sxs-lookup"><span data-stu-id="9d184-525">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(GetAddressBar());
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(GetAddressBar(), buffer, length + 1);

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

#### <span data-ttu-id="9d184-526">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="9d184-526">NavigateToString</span></span> 

<span data-ttu-id="9d184-527">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="9d184-527">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="9d184-528">HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="9d184-528">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="9d184-529">El parámetro htmlContent no puede tener más de 2 MB de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d184-529">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="9d184-530">El origen de la nueva página será acerca de: Blank.</span><span class="sxs-lookup"><span data-stu-id="9d184-530">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="9d184-531">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="9d184-531">OpenDevToolsWindow</span></span> 

<span data-ttu-id="9d184-532">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-532">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="9d184-533">[OPENDEVTOOLSWINDOW](#opendevtoolswindow)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="9d184-533">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="9d184-534">No hace nada si se llama cuando la ventana de DevTools ya está abierta</span><span class="sxs-lookup"><span data-stu-id="9d184-534">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="9d184-535">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="9d184-535">PostWebMessageAsJson</span></span> 

<span data-ttu-id="9d184-536">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-536">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="9d184-537">HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="9d184-537">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="9d184-538">Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9d184-538">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="9d184-539">JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9d184-539">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="9d184-540">El argumentos del evento es una instancia de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="9d184-540">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="9d184-541">La opción ICoreWebView2Settings:: IsWebMessageEnabled debe ser true o este método dará un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9d184-541">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="9d184-542">La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-542">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="9d184-543">La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto.</span><span class="sxs-lookup"><span data-stu-id="9d184-543">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="9d184-544">Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host.</span><span class="sxs-lookup"><span data-stu-id="9d184-544">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="9d184-545">Este mensaje se envía de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9d184-545">This message is sent asynchronously.</span></span> <span data-ttu-id="9d184-546">Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9d184-546">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="9d184-547">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="9d184-547">PostWebMessageAsString</span></span> 

<span data-ttu-id="9d184-548">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-548">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="9d184-549">HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="9d184-549">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="9d184-550">Esto se comporta exactamente de la misma manera que PostWebMessageAsJson, pero la `window.chrome.webview` propiedad data del argumento de evento de mensaje será una cadena con el mismo valor que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="9d184-550">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="9d184-551">Use este en lugar de PostWebMessageAsJson si desea comunicarse a través de cadenas simples en lugar de objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="9d184-551">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="9d184-552">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="9d184-552">Reload</span></span> 

<span data-ttu-id="9d184-553">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="9d184-553">Reload the current page.</span></span>

> <span data-ttu-id="9d184-554">[recarga](#reload)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="9d184-554">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="9d184-555">Esto es similar a desplazarse hasta el URI del documento de nivel superior actual, incluidos todos los eventos de navegación que desencadenan y respetan cualquier entrada de la caché HTTP.</span><span class="sxs-lookup"><span data-stu-id="9d184-555">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="9d184-556">Sin embargo, el historial de atrás y reenvío no se modificará.</span><span class="sxs-lookup"><span data-stu-id="9d184-556">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="9d184-557">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-557">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="9d184-558">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9d184-558">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="9d184-559">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-559">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-560">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9d184-560">remove_ContentLoading</span></span> 

<span data-ttu-id="9d184-561">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9d184-561">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="9d184-562">[remove_ContentLoading](#remove_contentloading)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-562">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-563">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-563">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="9d184-564">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-564">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="9d184-565">[remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-565">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-566">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-566">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="9d184-567">Quitar un controlador de eventos agregado previamente con add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-567">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="9d184-568">[remove_FrameNavigationCompleted](#remove_framenavigationcompleted)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-568">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-569">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-569">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="9d184-570">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-570">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="9d184-571">[remove_FrameNavigationStarting](#remove_framenavigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-571">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-572">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-572">remove_HistoryChanged</span></span> 

<span data-ttu-id="9d184-573">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-573">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="9d184-574">[remove_HistoryChanged](#remove_historychanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-574">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-575">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9d184-575">remove_NavigationCompleted</span></span> 

<span data-ttu-id="9d184-576">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9d184-576">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="9d184-577">[remove_NavigationCompleted](#remove_navigationcompleted)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-577">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-578">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9d184-578">remove_NavigationStarting</span></span> 

<span data-ttu-id="9d184-579">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9d184-579">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="9d184-580">[remove_NavigationStarting](#remove_navigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-580">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-581">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-581">remove_NewWindowRequested</span></span> 

<span data-ttu-id="9d184-582">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-582">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="9d184-583">[remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-583">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-584">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-584">remove_PermissionRequested</span></span> 

<span data-ttu-id="9d184-585">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-585">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="9d184-586">[remove_PermissionRequested](#remove_permissionrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-586">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-587">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9d184-587">remove_ProcessFailed</span></span> 

<span data-ttu-id="9d184-588">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9d184-588">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="9d184-589">[remove_ProcessFailed](#remove_processfailed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-589">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-590">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9d184-590">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="9d184-591">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9d184-591">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="9d184-592">[remove_ScriptDialogOpening](#remove_scriptdialogopening)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-592">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-593">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9d184-593">remove_SourceChanged</span></span> 

<span data-ttu-id="9d184-594">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9d184-594">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="9d184-595">[remove_SourceChanged](#remove_sourcechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-595">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-596">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9d184-596">remove_WebMessageReceived</span></span> 

<span data-ttu-id="9d184-597">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="9d184-597">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="9d184-598">[remove_WebMessageReceived](#remove_webmessagereceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-598">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-599">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-599">remove_WebResourceRequested</span></span> 

<span data-ttu-id="9d184-600">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-600">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="9d184-601">[remove_WebResourceRequested](#remove_webresourcerequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-601">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-602">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9d184-602">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="9d184-603">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-603">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="9d184-604">[remove_WindowCloseRequested](#remove_windowcloserequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9d184-604">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9d184-605">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="9d184-605">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="9d184-606">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="9d184-606">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="9d184-607">[REMOVEHOSTOBJECTFROMSCRIPT](#removehostobjectfromscript)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="9d184-607">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="9d184-608">Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="9d184-608">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="9d184-609">Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.</span><span class="sxs-lookup"><span data-stu-id="9d184-609">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="9d184-610">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9d184-610">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="9d184-611">Quite el JavaScript correspondiente agregado `AddScriptToExecuteOnDocumentCreated` con el identificador de script especificado.</span><span class="sxs-lookup"><span data-stu-id="9d184-611">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>

> <span data-ttu-id="9d184-612">HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR ID)</span><span class="sxs-lookup"><span data-stu-id="9d184-612">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="9d184-613">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9d184-613">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="9d184-614">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9d184-614">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="9d184-615">[REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="9d184-615">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="9d184-616">Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="9d184-616">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="9d184-617">Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="9d184-617">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="9d184-618">Detener</span><span class="sxs-lookup"><span data-stu-id="9d184-618">Stop</span></span> 

<span data-ttu-id="9d184-619">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="9d184-619">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="9d184-620">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="9d184-620">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="9d184-621">No detiene las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="9d184-621">Does not stop scripts.</span></span>

#### <span data-ttu-id="9d184-622">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="9d184-622">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="9d184-623">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9d184-623">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="9d184-624">[COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-624">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="9d184-625">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-625">Values</span></span>                         | <span data-ttu-id="9d184-626">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-626">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-627">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="9d184-627">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="9d184-628">Formato de imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="9d184-628">PNG image format.</span></span>
<span data-ttu-id="9d184-629">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="9d184-629">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="9d184-630">Formato de imagen JPEG.</span><span class="sxs-lookup"><span data-stu-id="9d184-630">JPEG image format.</span></span>

#### <span data-ttu-id="9d184-631">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-631">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="9d184-632">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="9d184-632">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="9d184-633">[COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-633">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="9d184-634">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-634">Values</span></span>                         | <span data-ttu-id="9d184-635">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-635">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-636">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="9d184-636">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="9d184-637">Corresponde a WM_KEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="9d184-637">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="9d184-638">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="9d184-638">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="9d184-639">Corresponde a WM_KEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="9d184-639">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="9d184-640">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="9d184-640">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="9d184-641">Corresponde a WM_SYSKEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="9d184-641">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="9d184-642">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="9d184-642">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="9d184-643">Corresponde a WM_SYSKEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="9d184-643">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="9d184-644">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="9d184-644">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="9d184-645">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="9d184-645">Reason for moving focus.</span></span>

> <span data-ttu-id="9d184-646">[COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-646">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="9d184-647">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-647">Values</span></span>                         | <span data-ttu-id="9d184-648">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-648">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-649">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="9d184-649">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="9d184-650">El ajuste del foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="9d184-650">Code setting focus into WebView.</span></span>
<span data-ttu-id="9d184-651">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="9d184-651">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="9d184-652">Moviendo el foco debido a una resaltado de pestañas hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="9d184-652">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="9d184-653">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="9d184-653">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="9d184-654">Moviendo el foco debido a un recorrido de tabulación hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="9d184-654">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="9d184-655">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-655">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="9d184-656">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9d184-656">The type of a permission request.</span></span>

> <span data-ttu-id="9d184-657">[COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-657">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="9d184-658">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-658">Values</span></span>                         | <span data-ttu-id="9d184-659">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-659">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-660">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="9d184-660">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="9d184-661">Permiso desconocido.</span><span class="sxs-lookup"><span data-stu-id="9d184-661">Unknown permission.</span></span>
<span data-ttu-id="9d184-662">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="9d184-662">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="9d184-663">Permiso para capturar audio.</span><span class="sxs-lookup"><span data-stu-id="9d184-663">Permission to capture audio.</span></span>
<span data-ttu-id="9d184-664">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="9d184-664">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="9d184-665">Permiso para capturar video.</span><span class="sxs-lookup"><span data-stu-id="9d184-665">Permission to capture video.</span></span>
<span data-ttu-id="9d184-666">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="9d184-666">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="9d184-667">Permiso para acceder a la ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="9d184-667">Permission to access geolocation.</span></span>
<span data-ttu-id="9d184-668">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="9d184-668">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="9d184-669">Permiso para enviar notificaciones Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-669">Permission to send web notifications.</span></span>
<span data-ttu-id="9d184-670">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="9d184-670">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="9d184-671">Permiso para acceder al sensor genérico.</span><span class="sxs-lookup"><span data-stu-id="9d184-671">Permission to access generic sensor.</span></span>
<span data-ttu-id="9d184-672">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="9d184-672">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="9d184-673">Permiso para leer el Portapapeles del sistema sin un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="9d184-673">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="9d184-674">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="9d184-674">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="9d184-675">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9d184-675">Response to a permission request.</span></span>

> <span data-ttu-id="9d184-676">[COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-676">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="9d184-677">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-677">Values</span></span>                         | <span data-ttu-id="9d184-678">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-678">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-679">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="9d184-679">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="9d184-680">Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.</span><span class="sxs-lookup"><span data-stu-id="9d184-680">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="9d184-681">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="9d184-681">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="9d184-682">Otorgue la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9d184-682">Grant the permission request.</span></span>
<span data-ttu-id="9d184-683">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="9d184-683">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="9d184-684">Denegar la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9d184-684">Deny the permission request.</span></span>

#### <span data-ttu-id="9d184-685">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="9d184-685">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="9d184-686">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="9d184-686">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="9d184-687">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="9d184-687">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="9d184-688">Para obtener más información, consulte la documentación de WM_KEYDOWN en[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="9d184-688">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="9d184-689">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-689">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="9d184-690">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9d184-690">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="9d184-691">[COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-691">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="9d184-692">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-692">Values</span></span>                         | <span data-ttu-id="9d184-693">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-693">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-694">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="9d184-694">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="9d184-695">Indica que el proceso del explorador ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="9d184-695">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="9d184-696">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="9d184-696">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="9d184-697">Indica que el proceso de representación ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="9d184-697">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="9d184-698">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="9d184-698">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="9d184-699">Indica que el proceso de representación deja de responder.</span><span class="sxs-lookup"><span data-stu-id="9d184-699">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="9d184-700">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="9d184-700">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="9d184-701">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9d184-701">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="9d184-702">[COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-702">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="9d184-703">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-703">Values</span></span>                         | <span data-ttu-id="9d184-704">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-704">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-705">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="9d184-705">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="9d184-706">Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.</span><span class="sxs-lookup"><span data-stu-id="9d184-706">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="9d184-707">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="9d184-707">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="9d184-708">Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-708">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="9d184-709">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="9d184-709">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="9d184-710">Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-710">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="9d184-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="9d184-711">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="9d184-712">Un cuadro de diálogo invocado a través del evento beforeunload de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d184-712">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="9d184-713">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="9d184-713">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="9d184-714">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-714">Error status values for web navigations.</span></span>

> <span data-ttu-id="9d184-715">[COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-715">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="9d184-716">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-716">Values</span></span>                         | <span data-ttu-id="9d184-717">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-717">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-718">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="9d184-718">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="9d184-719">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="9d184-719">An unknown error occurred.</span></span>
<span data-ttu-id="9d184-720">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="9d184-720">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="9d184-721">El nombre común del certificado SSL no coincide con la dirección Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-721">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="9d184-722">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="9d184-722">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="9d184-723">El certificado SSL ha expirado.</span><span class="sxs-lookup"><span data-stu-id="9d184-723">The SSL certificate has expired.</span></span>
<span data-ttu-id="9d184-724">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9d184-724">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="9d184-725">El certificado de cliente SSL contiene errores.</span><span class="sxs-lookup"><span data-stu-id="9d184-725">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="9d184-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="9d184-726">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="9d184-727">El certificado SSL ha sido revocado.</span><span class="sxs-lookup"><span data-stu-id="9d184-727">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="9d184-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="9d184-728">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="9d184-729">El certificado SSL no es válido &ndash; esto puede significar que el certificado no coincide con los pin de clave pública del nombre de host, que el certificado está firmado por una autoridad que no es de confianza o con un algoritmo de signo débil. el certificado alegó que los nombres DNS han infringido las restricciones de nombres, el certificado contiene una clave débil, el período de validez del certificado es demasiado largo, falta de información de revocación o de mecanismo de revocación, nombre de host no único, falta de información de transparencia del certificado o el certificado está encadenado a una [raíz de Symantec heredado](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="9d184-729">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="9d184-730">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="9d184-730">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="9d184-731">No se puede comunicar con el host.</span><span class="sxs-lookup"><span data-stu-id="9d184-731">The host is unreachable.</span></span>
<span data-ttu-id="9d184-732">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9d184-732">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="9d184-733">Se agotó el tiempo de espera de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9d184-733">The connection has timed out.</span></span>
<span data-ttu-id="9d184-734">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="9d184-734">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="9d184-735">El servidor ha devuelto una respuesta no válida o no reconocida.</span><span class="sxs-lookup"><span data-stu-id="9d184-735">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="9d184-736">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="9d184-736">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="9d184-737">La conexión ha sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="9d184-737">The connection was aborted.</span></span>
<span data-ttu-id="9d184-738">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="9d184-738">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="9d184-739">Se restableció la conexión.</span><span class="sxs-lookup"><span data-stu-id="9d184-739">The connection was reset.</span></span>
<span data-ttu-id="9d184-740">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="9d184-740">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="9d184-741">Se perdió la conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="9d184-741">The Internet connection has been lost.</span></span>
<span data-ttu-id="9d184-742">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="9d184-742">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="9d184-743">No se puede conectar al destino.</span><span class="sxs-lookup"><span data-stu-id="9d184-743">Cannot connect to destination.</span></span>
<span data-ttu-id="9d184-744">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="9d184-744">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="9d184-745">No se pudo resolver el nombre de host proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9d184-745">Could not resolve provided host name.</span></span>
<span data-ttu-id="9d184-746">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="9d184-746">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="9d184-747">Se canceló la operación.</span><span class="sxs-lookup"><span data-stu-id="9d184-747">The operation was canceled.</span></span>
<span data-ttu-id="9d184-748">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="9d184-748">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="9d184-749">Error en la redirección de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d184-749">The request redirect failed.</span></span>
<span data-ttu-id="9d184-750">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="9d184-750">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="9d184-751">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="9d184-751">An unexpected error occurred.</span></span>

#### <span data-ttu-id="9d184-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="9d184-752">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="9d184-753">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-753">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="9d184-754">[COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) enum</span><span class="sxs-lookup"><span data-stu-id="9d184-754">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="9d184-755">Los</span><span class="sxs-lookup"><span data-stu-id="9d184-755">Values</span></span>                         | <span data-ttu-id="9d184-756">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9d184-756">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9d184-757">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="9d184-757">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="9d184-758">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="9d184-758">All resources.</span></span>
<span data-ttu-id="9d184-759">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="9d184-759">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="9d184-760">Recursos de documentos.</span><span class="sxs-lookup"><span data-stu-id="9d184-760">Document resources.</span></span>
<span data-ttu-id="9d184-761">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="9d184-761">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="9d184-762">Recursos de CSS.</span><span class="sxs-lookup"><span data-stu-id="9d184-762">CSS resources.</span></span>
<span data-ttu-id="9d184-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="9d184-763">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="9d184-764">Recursos de imagen.</span><span class="sxs-lookup"><span data-stu-id="9d184-764">Image resources.</span></span>
<span data-ttu-id="9d184-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="9d184-765">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="9d184-766">Otros recursos multimedia, como los vídeos.</span><span class="sxs-lookup"><span data-stu-id="9d184-766">Other media resources such as videos.</span></span>
<span data-ttu-id="9d184-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="9d184-767">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="9d184-768">Recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9d184-768">Font resources.</span></span>
<span data-ttu-id="9d184-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="9d184-769">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="9d184-770">Recursos de script.</span><span class="sxs-lookup"><span data-stu-id="9d184-770">Script resources.</span></span>
<span data-ttu-id="9d184-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="9d184-771">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="9d184-772">Solicitudes XML HTTP.</span><span class="sxs-lookup"><span data-stu-id="9d184-772">XML HTTP requests.</span></span>
<span data-ttu-id="9d184-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="9d184-773">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="9d184-774">Capture la comunicación de la API.</span><span class="sxs-lookup"><span data-stu-id="9d184-774">Fetch API communication.</span></span>
<span data-ttu-id="9d184-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="9d184-775">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="9d184-776">Recursos de TextTrack.</span><span class="sxs-lookup"><span data-stu-id="9d184-776">TextTrack resources.</span></span>
<span data-ttu-id="9d184-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="9d184-777">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="9d184-778">Comunicación de la API de EventSource.</span><span class="sxs-lookup"><span data-stu-id="9d184-778">EventSource API communication.</span></span>
<span data-ttu-id="9d184-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="9d184-779">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="9d184-780">Comunicación de API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="9d184-780">WebSocket API communication.</span></span>
<span data-ttu-id="9d184-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="9d184-781">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="9d184-782">Manifiestos de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="9d184-782">Web App Manifests.</span></span>
<span data-ttu-id="9d184-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="9d184-783">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="9d184-784">Intercambio de HTTP firmado.</span><span class="sxs-lookup"><span data-stu-id="9d184-784">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="9d184-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="9d184-785">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="9d184-786">Solicitudes de ping.</span><span class="sxs-lookup"><span data-stu-id="9d184-786">Ping requests.</span></span>
<span data-ttu-id="9d184-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="9d184-787">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="9d184-788">Informes de violación de CSP.</span><span class="sxs-lookup"><span data-stu-id="9d184-788">CSP Violation Reports.</span></span>
<span data-ttu-id="9d184-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="9d184-789">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="9d184-790">Otros recursos.</span><span class="sxs-lookup"><span data-stu-id="9d184-790">Other resources.</span></span>

