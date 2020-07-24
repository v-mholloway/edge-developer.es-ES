---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2
ms.openlocfilehash: a1da6789027234130c58078871d7da23b4e285ba
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895500"
---
# <span data-ttu-id="17243-104">interfaz ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="17243-104">interface ICoreWebView2</span></span> 

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="17243-105">WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.</span><span class="sxs-lookup"><span data-stu-id="17243-105">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="17243-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="17243-106">Summary</span></span>

 <span data-ttu-id="17243-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="17243-107">Members</span></span>                        | <span data-ttu-id="17243-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17243-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="17243-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="17243-110">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="17243-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="17243-111">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="17243-111">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="17243-112">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17243-112">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="17243-113">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17243-113">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="17243-114">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-114">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="17243-115">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-115">add_FrameNavigationCompleted</span></span>](#add_framenavigationcompleted) | <span data-ttu-id="17243-116">Agregue un controlador de eventos para el evento FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-116">Add an event handler for the FrameNavigationCompleted event.</span></span>
[<span data-ttu-id="17243-117">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-117">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="17243-118">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-118">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="17243-119">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="17243-119">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="17243-120">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="17243-120">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="17243-121">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-121">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="17243-122">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-122">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="17243-123">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-123">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="17243-124">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-124">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="17243-125">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17243-125">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="17243-126">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-126">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="17243-127">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="17243-127">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="17243-128">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-128">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="17243-129">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="17243-129">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="17243-130">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="17243-130">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="17243-131">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="17243-131">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="17243-132">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="17243-132">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="17243-133">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="17243-133">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="17243-134">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="17243-134">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="17243-135">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="17243-135">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="17243-136">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="17243-136">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="17243-137">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="17243-137">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="17243-138">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-138">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="17243-139">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="17243-139">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="17243-140">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-140">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="17243-141">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="17243-141">AddHostObjectToScript</span></span>](#addhostobjecttoscript) | <span data-ttu-id="17243-142">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="17243-142">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="17243-143">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="17243-143">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="17243-144">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="17243-144">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="17243-145">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="17243-145">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="17243-146">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-146">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="17243-147">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="17243-147">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="17243-148">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="17243-148">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="17243-149">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="17243-149">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="17243-150">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="17243-150">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="17243-151">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="17243-151">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="17243-152">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-152">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="17243-153">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="17243-153">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="17243-154">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="17243-154">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="17243-155">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="17243-155">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="17243-156">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-156">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="17243-157">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="17243-157">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="17243-158">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-158">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="17243-159">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="17243-159">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="17243-160">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="17243-160">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="17243-161">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="17243-161">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="17243-162">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="17243-162">The title for the current top level document.</span></span>
[<span data-ttu-id="17243-163">get_Settings</span><span class="sxs-lookup"><span data-stu-id="17243-163">get_Settings</span></span>](#get_settings) | <span data-ttu-id="17243-164">El objeto [ICoreWebView2Settings](icorewebview2settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="17243-164">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="17243-165">get_Source</span><span class="sxs-lookup"><span data-stu-id="17243-165">get_Source</span></span>](#get_source) | <span data-ttu-id="17243-166">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="17243-166">The URI of the current top level document.</span></span>
[<span data-ttu-id="17243-167">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="17243-167">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="17243-168">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="17243-168">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="17243-169">GoBack</span><span class="sxs-lookup"><span data-stu-id="17243-169">GoBack</span></span>](#goback) | <span data-ttu-id="17243-170">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-170">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="17243-171">GoForward</span><span class="sxs-lookup"><span data-stu-id="17243-171">GoForward</span></span>](#goforward) | <span data-ttu-id="17243-172">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-172">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="17243-173">Busque</span><span class="sxs-lookup"><span data-stu-id="17243-173">Navigate</span></span>](#navigate) | <span data-ttu-id="17243-174">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="17243-174">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="17243-175">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="17243-175">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="17243-176">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="17243-176">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="17243-177">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="17243-177">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="17243-178">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-178">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="17243-179">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="17243-179">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="17243-180">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-180">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="17243-181">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="17243-181">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="17243-182">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-182">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="17243-183">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="17243-183">Reload</span></span>](#reload) | <span data-ttu-id="17243-184">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="17243-184">Reload the current page.</span></span>
[<span data-ttu-id="17243-185">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="17243-185">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="17243-186">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17243-186">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="17243-187">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="17243-187">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="17243-188">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17243-188">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="17243-189">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17243-189">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="17243-190">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-190">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="17243-191">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-191">remove_FrameNavigationCompleted</span></span>](#remove_framenavigationcompleted) | <span data-ttu-id="17243-192">Quitar un controlador de eventos agregado previamente con add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-192">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>
[<span data-ttu-id="17243-193">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-193">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="17243-194">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-194">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="17243-195">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="17243-195">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="17243-196">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-196">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="17243-197">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-197">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="17243-198">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-198">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="17243-199">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-199">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="17243-200">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-200">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="17243-201">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17243-201">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="17243-202">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-202">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="17243-203">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="17243-203">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="17243-204">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-204">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="17243-205">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="17243-205">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="17243-206">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="17243-206">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="17243-207">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="17243-207">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="17243-208">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="17243-208">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="17243-209">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="17243-209">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="17243-210">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-210">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="17243-211">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="17243-211">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="17243-212">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="17243-212">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="17243-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="17243-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="17243-214">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="17243-215">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="17243-215">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="17243-216">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-216">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="17243-217">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="17243-217">RemoveHostObjectFromScript</span></span>](#removehostobjectfromscript) | <span data-ttu-id="17243-218">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="17243-218">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="17243-219">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="17243-219">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="17243-220">Quite el JavaScript correspondiente agregado `AddScriptToExecuteOnDocumentCreated` con el identificador de script especificado.</span><span class="sxs-lookup"><span data-stu-id="17243-220">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>
[<span data-ttu-id="17243-221">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="17243-221">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="17243-222">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-222">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="17243-223">Detener</span><span class="sxs-lookup"><span data-stu-id="17243-223">Stop</span></span>](#stop) | <span data-ttu-id="17243-224">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="17243-224">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="17243-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="17243-225">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#corewebview2_capture_preview_image_format) | <span data-ttu-id="17243-226">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="17243-226">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="17243-227">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-227">COREWEBVIEW2_KEY_EVENT_KIND</span></span>](#corewebview2_key_event_kind) | <span data-ttu-id="17243-228">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="17243-228">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="17243-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="17243-229">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span>](#corewebview2_move_focus_reason) | <span data-ttu-id="17243-230">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="17243-230">Reason for moving focus.</span></span>
[<span data-ttu-id="17243-231">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-231">COREWEBVIEW2_PERMISSION_KIND</span></span>](#corewebview2_permission_kind) | <span data-ttu-id="17243-232">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="17243-232">The type of a permission request.</span></span>
[<span data-ttu-id="17243-233">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="17243-233">COREWEBVIEW2_PERMISSION_STATE</span></span>](#corewebview2_permission_state) | <span data-ttu-id="17243-234">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="17243-234">Response to a permission request.</span></span>
[<span data-ttu-id="17243-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="17243-235">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#corewebview2_physical_key_status) | <span data-ttu-id="17243-236">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="17243-236">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>
[<span data-ttu-id="17243-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-237">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span>](#corewebview2_process_failed_kind) | <span data-ttu-id="17243-238">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="17243-238">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="17243-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-239">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#corewebview2_script_dialog_kind) | <span data-ttu-id="17243-240">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="17243-240">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="17243-241">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="17243-241">COREWEBVIEW2_WEB_ERROR_STATUS</span></span>](#corewebview2_web_error_status) | <span data-ttu-id="17243-242">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="17243-242">Error status values for web navigations.</span></span>
[<span data-ttu-id="17243-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="17243-243">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#corewebview2_web_resource_context) | <span data-ttu-id="17243-244">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="17243-244">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="17243-245">Miembros</span><span class="sxs-lookup"><span data-stu-id="17243-245">Members</span></span>

#### <span data-ttu-id="17243-246">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="17243-246">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="17243-247">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="17243-247">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="17243-248">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-248">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](icorewebview2containsfullscreenelementchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-249">Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="17243-249">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="17243-250">Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="17243-250">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="17243-251">El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.</span><span class="sxs-lookup"><span data-stu-id="17243-251">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="17243-252">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="17243-252">add_ContentLoading</span></span> 

<span data-ttu-id="17243-253">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17243-253">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="17243-254">[add_ContentLoading](#add_contentloading)de HRESULT público ([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-254">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](icorewebview2contentloadingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-255">ContentLoading se activa antes de que se cargue ningún contenido, incluso los scripts agregados con AddScriptToExecuteOnDocumentCreated ContentLoading no se desencadenarán si se realiza una navegación de página (por ejemplo, a través de la navegación de fragmentos o el historial. navegaciones pushState).</span><span class="sxs-lookup"><span data-stu-id="17243-255">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="17243-256">Esto sigue los eventos NavigationStarting y SourceChanged, y precede a los eventos HistoryChanged y NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-256">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="17243-257">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17243-257">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="17243-258">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-258">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="17243-259">[add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-259">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](icorewebview2documenttitlechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-260">El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-260">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="17243-261">add_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-261">add_FrameNavigationCompleted</span></span> 

<span data-ttu-id="17243-262">Agregue un controlador de eventos para el evento FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-262">Add an event handler for the FrameNavigationCompleted event.</span></span>

> <span data-ttu-id="17243-263">[add_FrameNavigationCompleted](#add_framenavigationcompleted)de HRESULT público ([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-263">public HRESULT [add_FrameNavigationCompleted](#add_framenavigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-264">El evento FrameNavigationCompleted se desencadena cuando se ha cargado por completo un fotograma secundario (Body. onload) o la carga se ha detenido con error.</span><span class="sxs-lookup"><span data-stu-id="17243-264">FrameNavigationCompleted event fires when a child frame has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="17243-265">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-265">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="17243-266">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-266">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="17243-267">[add_FrameNavigationStarting](#add_framenavigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-267">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-268">FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="17243-268">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="17243-269">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="17243-269">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="17243-270">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="17243-270">add_HistoryChanged</span></span> 

<span data-ttu-id="17243-271">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="17243-271">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="17243-272">[add_HistoryChanged](#add_historychanged)de HRESULT público ([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-272">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](icorewebview2historychangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-273">Usa Facturacióncambiar para comprobar si el valor CanGoBack/CanGoForward ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="17243-273">Use HistoryChange to check if CanGoBack/CanGoForward value has changed.</span></span> <span data-ttu-id="17243-274">HistoryChanged también se desencadena para usar GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="17243-274">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="17243-275">HistoryChanged se desencadena después de SourceChanged y ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17243-275">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="17243-276">Agregue un controlador de eventos para el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-276">Add an event handler for the HistoryChanged event.</span></span> 
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

#### <span data-ttu-id="17243-277">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-277">add_NavigationCompleted</span></span> 

<span data-ttu-id="17243-278">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-278">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="17243-279">[add_NavigationCompleted](#add_navigationcompleted)de HRESULT público ([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-279">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](icorewebview2navigationcompletedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-280">El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.</span><span class="sxs-lookup"><span data-stu-id="17243-280">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="17243-281">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-281">add_NavigationStarting</span></span> 

<span data-ttu-id="17243-282">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-282">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="17243-283">[add_NavigationStarting](#add_navigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-283">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](icorewebview2navigationstartingeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-284">NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="17243-284">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="17243-285">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="17243-285">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="17243-286">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17243-286">add_NewWindowRequested</span></span> 

<span data-ttu-id="17243-287">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-287">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="17243-288">[add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-288">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](icorewebview2newwindowrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-289">Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.</span><span class="sxs-lookup"><span data-stu-id="17243-289">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="17243-290">La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.</span><span class="sxs-lookup"><span data-stu-id="17243-290">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="17243-291">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="17243-291">add_PermissionRequested</span></span> 

<span data-ttu-id="17243-292">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-292">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="17243-293">[add_PermissionRequested](#add_permissionrequested)de HRESULT público ([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-293">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](icorewebview2permissionrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-294">Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="17243-294">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="17243-295">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="17243-295">add_ProcessFailed</span></span> 

<span data-ttu-id="17243-296">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="17243-296">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="17243-297">[add_ProcessFailed](#add_processfailed)de HRESULT público ([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-297">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](icorewebview2processfailedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-298">Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.</span><span class="sxs-lookup"><span data-stu-id="17243-298">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="17243-299">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="17243-299">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="17243-300">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="17243-300">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="17243-301">[add_ScriptDialogOpening](#add_scriptdialogopening)de HRESULT público ([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-301">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](icorewebview2scriptdialogopeningeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-302">El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-302">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="17243-303">Este evento solo se desencadena si la propiedad ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled se establece en false.</span><span class="sxs-lookup"><span data-stu-id="17243-303">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="17243-304">El evento ScriptDialogOpening se puede usar para suprimir cuadros de diálogo o reemplazar los cuadros de diálogo predeterminados con cuadros de diálogo personalizados.</span><span class="sxs-lookup"><span data-stu-id="17243-304">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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

#### <span data-ttu-id="17243-305">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="17243-305">add_SourceChanged</span></span> 

<span data-ttu-id="17243-306">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="17243-306">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="17243-307">[add_SourceChanged](#add_sourcechanged)de HRESULT público ([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-307">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](icorewebview2sourcechangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-308">SourceChanged se desencadena para navegar a un sitio diferente o a navegación de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="17243-308">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="17243-309">No se desencadenará para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="17243-309">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="17243-310">SourceChanged se desencadena antes de ContentLoading para la navegación a un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="17243-310">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="17243-311">Agregue un controlador de eventos para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-311">Add an event handler for the SourceChanged event.</span></span> 
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

#### <span data-ttu-id="17243-312">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="17243-312">add_WebMessageReceived</span></span> 

<span data-ttu-id="17243-313">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="17243-313">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="17243-314">[add_WebMessageReceived](#add_webmessagereceived)pública HRESULT (controlador[ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-314">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-315">La función postmensaje es `void postMessage(object)` donde objeto es cualquier objeto compatible con la conversión de JSON.</span><span class="sxs-lookup"><span data-stu-id="17243-315">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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
 <span data-ttu-id="17243-316">Cuando se llama a PostMessage, se invocará el [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) establecido a través de este método SetWebMessageReceivedEventHandler con el parámetro de objeto PostMessage convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="17243-316">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](icorewebview2webmessagereceivedeventhandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="17243-317">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="17243-317">add_WebResourceRequested</span></span> 

<span data-ttu-id="17243-318">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-318">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="17243-319">[add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-319">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](icorewebview2webresourcerequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-320">Se desencadena cuando WebView está realizando una solicitud de dirección URL a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="17243-320">Fires when the WebView is performing a URL request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="17243-321">Debe agregar al menos un filtro para que se active el evento.</span><span class="sxs-lookup"><span data-stu-id="17243-321">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="17243-322">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="17243-322">add_WindowCloseRequested</span></span> 

<span data-ttu-id="17243-323">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-323">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="17243-324">[add_WindowCloseRequested](#add_windowcloserequested)de HRESULT público ([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="17243-324">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](icorewebview2windowcloserequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17243-325">Se desencadena cuando el contenido de la vista en WebView solicita cerrar la ventana, por ejemplo, después de que se llame a Window. Close.</span><span class="sxs-lookup"><span data-stu-id="17243-325">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="17243-326">La aplicación debe cerrar la ventana de WebView y de la aplicación relacionada si eso tiene sentido para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="17243-326">The app should close the WebView and related app window if that makes sense to the app.</span></span>

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

#### <span data-ttu-id="17243-327">AddHostObjectToScript</span><span class="sxs-lookup"><span data-stu-id="17243-327">AddHostObjectToScript</span></span> 

<span data-ttu-id="17243-328">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="17243-328">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="17243-329">[ADDHOSTOBJECTTOSCRIPT](#addhostobjecttoscript)HRESULT público (LPCWSTR Name, Variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="17243-329">public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT \* object)</span></span>

<span data-ttu-id="17243-330">Los objetos de host se exponen como proxies de objeto de host a través de `window.chrome.webview.hostObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="17243-330">Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.<name>`.</span></span> <span data-ttu-id="17243-331">Los proxies de objeto host son promesas y se resolverán como un objeto que representa el objeto host.</span><span class="sxs-lookup"><span data-stu-id="17243-331">Host object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="17243-332">La promesa se rechaza si la aplicación no ha agregado un objeto con el nombre.</span><span class="sxs-lookup"><span data-stu-id="17243-332">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="17243-333">Cuando el código de JavaScript tiene acceso a una propiedad o método del objeto, se devuelve una promesa, que se resolverá con el valor devuelto por el host para la propiedad o el método, o se rechazará en caso de error, como no se trata de una propiedad o método en el objeto o los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="17243-333">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="17243-334">Por ejemplo, cuando el código de la aplicación hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="17243-334">For example, when the application code does the following:</span></span>

```
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddHostObjectToScript(L"host_object", &host);
```

<span data-ttu-id="17243-335">El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="17243-335">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span>

```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

<span data-ttu-id="17243-336">Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant.</span><span class="sxs-lookup"><span data-stu-id="17243-336">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="17243-337">Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="17243-337">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="17243-338">El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId.</span><span class="sxs-lookup"><span data-stu-id="17243-338">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="17243-339">Las matrices anidadas se admiten hasta una profundidad de 3.</span><span class="sxs-lookup"><span data-stu-id="17243-339">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="17243-340">No se admiten las matrices de los tipos de referencia.</span><span class="sxs-lookup"><span data-stu-id="17243-340">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="17243-341">VT_EMPTY y VT_NULL se asignan a JavaScript como null.</span><span class="sxs-lookup"><span data-stu-id="17243-341">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="17243-342">En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="17243-342">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="17243-343">Además, todos los objetos host se exponen como `window.chrome.webview.hostObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="17243-343">Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.<name>`.</span></span> <span data-ttu-id="17243-344">Aquí los objetos host se exponen como proxies de objetos de host sincrónico.</span><span class="sxs-lookup"><span data-stu-id="17243-344">Here the host objects are exposed as synchronous host object proxies.</span></span> <span data-ttu-id="17243-345">No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host.</span><span class="sxs-lookup"><span data-stu-id="17243-345">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="17243-346">Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.hostObjects.<name>` descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="17243-346">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.<name>` API described above.</span></span>

<span data-ttu-id="17243-347">Los proxies de objetos host sincrónicos y los proxies de objetos host asincrónicos pueden obtener el mismo objeto de host.</span><span class="sxs-lookup"><span data-stu-id="17243-347">Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object.</span></span> <span data-ttu-id="17243-348">Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto host, ya sean otros servidores proxy, sincrónicos o asíncronos.</span><span class="sxs-lookup"><span data-stu-id="17243-348">Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="17243-349">Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-349">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="17243-350">Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="17243-350">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="17243-351">Los proxies de objetos de hospedaje son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method.</span><span class="sxs-lookup"><span data-stu-id="17243-351">Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="17243-352">Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local.</span><span class="sxs-lookup"><span data-stu-id="17243-352">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="17243-353">Además, cualquier propiedad o método de la matriz se `chrome.webview.hostObjects.options.forceLocalProperties` ejecutará de forma local.</span><span class="sxs-lookup"><span data-stu-id="17243-353">Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="17243-354">De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="17243-354">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="17243-355">Puede agregar más a esta matriz, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="17243-355">You can add more to this array as required.</span></span>

<span data-ttu-id="17243-356">Hay un método que puede resultar `chrome.webview.hostObjects.cleanupSome` más conveniente para la recolección de objetos host.</span><span class="sxs-lookup"><span data-stu-id="17243-356">There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.</span></span>

<span data-ttu-id="17243-357">Los proxies de objetos de hospedaje también tienen los siguientes métodos que se ejecutan de forma local:</span><span class="sxs-lookup"><span data-stu-id="17243-357">Host object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="17243-358">applyHostFunction, getHostProperty, setHostProperty: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto host.</span><span class="sxs-lookup"><span data-stu-id="17243-358">applyHostFunction, getHostProperty, setHostProperty: Perform a method invocation, property get, or property set on the host object.</span></span> <span data-ttu-id="17243-359">Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto.</span><span class="sxs-lookup"><span data-stu-id="17243-359">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="17243-360">Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy.</span><span class="sxs-lookup"><span data-stu-id="17243-360">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="17243-361">Pero `proxy.applyHostFunction('toString')` se ejecuta `toString` en el objeto de proxy del host.</span><span class="sxs-lookup"><span data-stu-id="17243-361">But `proxy.applyHostFunction('toString')` runs `toString` on the host proxied object instead.</span></span>

* <span data-ttu-id="17243-362">getLocalProperty, setLocalProperty: propiedad get o conjunto de propiedades de forma local.</span><span class="sxs-lookup"><span data-stu-id="17243-362">getLocalProperty, setLocalProperty: Perform property get, or property set locally.</span></span> <span data-ttu-id="17243-363">Puede usar estos métodos para forzar la obtención o la configuración de una propiedad en el proxy del objeto host, en lugar de en el objeto host que representa.</span><span class="sxs-lookup"><span data-stu-id="17243-363">You can use these methods to force getting or setting a property on the host object proxy itself rather than on the host object it represents.</span></span> <span data-ttu-id="17243-364">Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto de proxy del host.</span><span class="sxs-lookup"><span data-stu-id="17243-364">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the host proxied object.</span></span> <span data-ttu-id="17243-365">Pero `proxy.getLocalProperty('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="17243-365">But `proxy.getLocalProperty('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="17243-366">sincronizar: los servidores proxy de objetos host asincrónicos exponen un método Sync que devuelve una promesa de un proxy de objeto host sincrónico para el mismo objeto host.</span><span class="sxs-lookup"><span data-stu-id="17243-366">sync: Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.</span></span> <span data-ttu-id="17243-367">Por ejemplo, `chrome.webview.hostObjects.sample.methodCall()` devuelve un proxy de objeto host asincrónico.</span><span class="sxs-lookup"><span data-stu-id="17243-367">For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.</span></span> <span data-ttu-id="17243-368">Puede usar el `sync` método para obtener un proxy de objeto host sincrónico en su lugar:</span><span class="sxs-lookup"><span data-stu-id="17243-368">You can use the `sync` method to obtain a synchronous host object proxy instead:</span></span> `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* <span data-ttu-id="17243-369">Async: los proxies de objetos host sincrónicos exponen un método asincrónico que bloquea y devuelve un proxy de objeto host asincrónico para el mismo objeto host.</span><span class="sxs-lookup"><span data-stu-id="17243-369">async: Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.</span></span> <span data-ttu-id="17243-370">Por ejemplo, `chrome.webview.hostObjects.sync.sample.methodCall()` devuelve un proxy de objeto host sincrónico.</span><span class="sxs-lookup"><span data-stu-id="17243-370">For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.</span></span> <span data-ttu-id="17243-371">Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto host asincrónico para el mismo objeto host:</span><span class="sxs-lookup"><span data-stu-id="17243-371">Calling the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object:</span></span> `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="17243-372">a continuación: los servidores proxy de objetos host asincrónicos tienen un método then.</span><span class="sxs-lookup"><span data-stu-id="17243-372">then: Asynchronous host object proxies have a then method.</span></span> <span data-ttu-id="17243-373">Esto permite que sean esperados.</span><span class="sxs-lookup"><span data-stu-id="17243-373">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="17243-374">devolverá una promesa que se resolverá con una representación del objeto host.</span><span class="sxs-lookup"><span data-stu-id="17243-374">will return a promise that resolves with a representation of the host object.</span></span> <span data-ttu-id="17243-375">Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local.</span><span class="sxs-lookup"><span data-stu-id="17243-375">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="17243-376">Si el proxy representa una función, se devuelve un proxy que no es de espera.</span><span class="sxs-lookup"><span data-stu-id="17243-376">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="17243-377">Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como servidores proxy de objeto host.</span><span class="sxs-lookup"><span data-stu-id="17243-377">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as host object proxies.</span></span>

<span data-ttu-id="17243-378">Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota.</span><span class="sxs-lookup"><span data-stu-id="17243-378">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="17243-379">Los proxies de objeto de host asincrónico devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="17243-379">Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="17243-380">La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación.</span><span class="sxs-lookup"><span data-stu-id="17243-380">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="17243-381">Los servidores proxy sincrónicos del objeto host funcionan de manera similar, pero bloquean la ejecución de JavaScript y espera a que se complete la operación remota.</span><span class="sxs-lookup"><span data-stu-id="17243-381">Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="17243-382">Establecer una propiedad en un proxy de objeto de host asincrónico funciona de forma ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="17243-382">Setting a property on an asynchronous host object proxy works slightly differently.</span></span> <span data-ttu-id="17243-383">El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá.</span><span class="sxs-lookup"><span data-stu-id="17243-383">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="17243-384">Este es un requisito del objeto proxy de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-384">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="17243-385">Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setHostProperty que devuelve una promesa según se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="17243-385">If you need to asynchronously wait for the property set to complete, use the setHostProperty method which returns a promise as described above.</span></span> <span data-ttu-id="17243-386">La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="17243-386">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="17243-387">Por ejemplo, supongamos que tiene un objeto COM con la siguiente interfaz</span><span class="sxs-lookup"><span data-stu-id="17243-387">For example, suppose you have a COM object with the following interface</span></span>

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
 <span data-ttu-id="17243-388">Podemos añadir una instancia de esta interfaz a nuestro JavaScript con `AddHostObjectToScript` .</span><span class="sxs-lookup"><span data-stu-id="17243-388">We can add an instance of this interface into our JavaScript with `AddHostObjectToScript`.</span></span> <span data-ttu-id="17243-389">En este caso, lo hemos denominado `sample` :</span><span class="sxs-lookup"><span data-stu-id="17243-389">In this case we name it `sample`:</span></span>

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
 <span data-ttu-id="17243-390">A continuación, en el documento HTML podemos usar este objeto COM mediante `chrome.webview.hostObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="17243-390">Then in the HTML document we can use this COM object via `chrome.webview.hostObjects.sample`:</span></span>

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
<span data-ttu-id="17243-391">La exposición de objetos de host a script tiene riesgo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="17243-391">Exposing host objects to script has security risk.</span></span> <span data-ttu-id="17243-392">Siga los [procedimientos recomendados](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span><span class="sxs-lookup"><span data-stu-id="17243-392">Please follow [best practices](https://docs.microsoft.com/microsoft-edge/webview2/concepts/security).</span></span>

#### <span data-ttu-id="17243-393">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="17243-393">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="17243-394">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="17243-394">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="17243-395">[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)de HRESULT público (LPCWSTR JavaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="17243-395">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript, [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="17243-396">Este método inyecta un script que se ejecuta en todos los documentos de nivel superior y en los elementos de navegación de la página de Marcos secundarios.</span><span class="sxs-lookup"><span data-stu-id="17243-396">This method injects a script that runs on all top-level document and child frame page navigations.</span></span> <span data-ttu-id="17243-397">Este método se ejecuta de forma asincrónica y debes esperar a que finalice el controlador de finalización antes de que el script insertado esté listo para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="17243-397">This method runs asynchronously, and you must wait for the completion handler to finish before the injected script is ready to run.</span></span> <span data-ttu-id="17243-398">Cuando se completa este método, `Invoke` se llama al método del controlador con el `id` de la secuencia de comandos insertada.</span><span class="sxs-lookup"><span data-stu-id="17243-398">When this method completes, the handler's `Invoke` method is called with the `id` of the injected script.</span></span> `id` <span data-ttu-id="17243-399">es una cadena.</span><span class="sxs-lookup"><span data-stu-id="17243-399">is a string.</span></span> <span data-ttu-id="17243-400">Para quitar la secuencia de comandos insertada, use `RemoveScriptToExecuteOnDocumentCreated` .</span><span class="sxs-lookup"><span data-stu-id="17243-400">To remove the injected script, use `RemoveScriptToExecuteOnDocumentCreated`.</span></span>

<span data-ttu-id="17243-401">Tenga en cuenta que si un documento HTML contiene algún tipo de espacio aislado a través de propiedades de [espacio aislado](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) o el [encabezado HTTP de seguridad de contenido](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) , esto afectará a la secuencia de comandos que se ejecuta aquí.</span><span class="sxs-lookup"><span data-stu-id="17243-401">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="17243-402">Así, por ejemplo, si la palabra clave "Allow-modal" no se establece, se omitirán las llamadas a la `alert` función.</span><span class="sxs-lookup"><span data-stu-id="17243-402">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="17243-403">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="17243-403">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="17243-404">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-404">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="17243-405">[ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="17243-405">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="17243-406">El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno).</span><span class="sxs-lookup"><span data-stu-id="17243-406">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="17243-407">nullptr es equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="17243-407">nullptr is equivalent to L"".</span></span> <span data-ttu-id="17243-408">Consulta COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.</span><span class="sxs-lookup"><span data-stu-id="17243-408">See COREWEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="17243-409">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="17243-409">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="17243-410">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="17243-410">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="17243-411">HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR NOMBREDEMÉTODO, LPCWSTR ParametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="17243-411">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName, LPCWSTR parametersAsJson, [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](icorewebview2calldevtoolsprotocolmethodcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="17243-412">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles.</span><span class="sxs-lookup"><span data-stu-id="17243-412">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="17243-413">El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="17243-413">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="17243-414">El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17243-414">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="17243-415">Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="17243-415">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="17243-416">Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="17243-416">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="17243-417">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="17243-417">CapturePreview</span></span> 

<span data-ttu-id="17243-418">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="17243-418">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="17243-419">[CAPTUREPREVIEW](#capturepreview)HRESULT público ([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) ImageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="17243-419">public HRESULT [CapturePreview](#capturepreview)([COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) imageFormat, IStream \* imageStream, [ICoreWebView2CapturePreviewCompletedHandler](icorewebview2capturepreviewcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="17243-420">Especifique el formato de la imagen con el parámetro imageFormat.</span><span class="sxs-lookup"><span data-stu-id="17243-420">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="17243-421">Los datos binarios de la imagen resultantes se escriben en el parámetro imageStream proporcionado.</span><span class="sxs-lookup"><span data-stu-id="17243-421">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="17243-422">Cuando CapturePreview termina de escribir en la secuencia, se llama al método Invoke del parámetro handler proporcionado.</span><span class="sxs-lookup"><span data-stu-id="17243-422">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="17243-423">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="17243-423">ExecuteScript</span></span> 

<span data-ttu-id="17243-424">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-424">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="17243-425">[ExecuteScript](#executescript)de HRESULT público (LPCWSTR JavaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="17243-425">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript, [ICoreWebView2ExecuteScriptCompletedHandler](icorewebview2executescriptcompletedhandler.md) \* handler)</span></span>

<span data-ttu-id="17243-426">Esto se ejecutará de forma asincrónica y cuando se complete, si se proporciona un controlador en el parámetro ExecuteScriptCompletedHandler, se llamará a su método Invoke con el resultado de evaluar el JavaScript proporcionado.</span><span class="sxs-lookup"><span data-stu-id="17243-426">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="17243-427">El valor del resultado es una cadena codificada por JSON.</span><span class="sxs-lookup"><span data-stu-id="17243-427">The result value is a JSON encoded string.</span></span> <span data-ttu-id="17243-428">Si el resultado es no definido, contiene un ciclo de referencia o, de lo contrario, no se puede codificar en JSON, el valor de JSON NULL se devolverá como la cadena "null".</span><span class="sxs-lookup"><span data-stu-id="17243-428">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="17243-429">Observe que una función que no tiene ningún valor explícito devuelto devuelve undefined.</span><span class="sxs-lookup"><span data-stu-id="17243-429">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="17243-430">Si el script ejecutado inicia una excepción no controlada, el resultado es también ' null '.</span><span class="sxs-lookup"><span data-stu-id="17243-430">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="17243-431">Este método se aplica de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="17243-431">This method is applied asynchronously.</span></span> <span data-ttu-id="17243-432">Si se llama al método después del evento NavigationStarting durante una navegación, el script se ejecutará en el nuevo documento al cargarlo, en el momento en que se active ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17243-432">If the method is called after NavigationStarting event during a navigation, the script will be executed in the new document when loading it, around the time ContentLoading is fired.</span></span> <span data-ttu-id="17243-433">ExecuteScript funcionará incluso si IsScriptEnabled se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="17243-433">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="17243-434">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="17243-434">get_BrowserProcessId</span></span> 

<span data-ttu-id="17243-435">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="17243-435">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="17243-436">[get_BrowserProcessId](#get_browserprocessid)de HRESULT público (UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="17243-436">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="17243-437">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="17243-437">get_CanGoBack</span></span> 

<span data-ttu-id="17243-438">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-438">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="17243-439">[get_CanGoBack](#get_cangoback)de HRESULT público (bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="17243-439">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="17243-440">El evento HistoryChanged se desencadenará si CanGoBack cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="17243-440">The HistoryChanged event will fire if CanGoBack changes value.</span></span>

#### <span data-ttu-id="17243-441">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="17243-441">get_CanGoForward</span></span> 

<span data-ttu-id="17243-442">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-442">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="17243-443">[get_CanGoForward](#get_cangoforward)de HRESULT público (bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="17243-443">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="17243-444">El evento HistoryChanged se desencadenará si CanGoForward cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="17243-444">The HistoryChanged event will fire if CanGoForward changes value.</span></span>

#### <span data-ttu-id="17243-445">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="17243-445">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="17243-446">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="17243-446">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="17243-447">[get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="17243-447">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="17243-448">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="17243-448">get_DocumentTitle</span></span> 

<span data-ttu-id="17243-449">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="17243-449">The title for the current top level document.</span></span>

> <span data-ttu-id="17243-450">[get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="17243-450">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="17243-451">Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="17243-451">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="17243-452">get_Settings</span><span class="sxs-lookup"><span data-stu-id="17243-452">get_Settings</span></span> 

<span data-ttu-id="17243-453">El objeto [ICoreWebView2Settings](icorewebview2settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="17243-453">The [ICoreWebView2Settings](icorewebview2settings.md) object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="17243-454">[get_Settings](#get_settings)pública HRESULT (configuración de[ICoreWebView2Settings](icorewebview2settings.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="17243-454">public HRESULT [get_Settings](#get_settings)([ICoreWebView2Settings](icorewebview2settings.md) \*\* settings)</span></span>

#### <span data-ttu-id="17243-455">get_Source</span><span class="sxs-lookup"><span data-stu-id="17243-455">get_Source</span></span> 

<span data-ttu-id="17243-456">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="17243-456">The URI of the current top level document.</span></span>

> <span data-ttu-id="17243-457">[get_Source](#get_source)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="17243-457">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="17243-458">Este valor puede cambiar potencialmente como parte del desencadenador de eventos SourceChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="17243-458">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="17243-459">Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="17243-459">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="17243-460">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="17243-460">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="17243-461">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="17243-461">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="17243-462">HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="17243-462">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName, [ICoreWebView2DevToolsProtocolEventReceiver](icorewebview2devtoolsprotocoleventreceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="17243-463">El parámetro eventName es el nombre completo del evento en el formato `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="17243-463">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="17243-464">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista de los eventos de protocolo DevTools Descripción y los argumentos del evento.</span><span class="sxs-lookup"><span data-stu-id="17243-464">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="17243-465">GoBack</span><span class="sxs-lookup"><span data-stu-id="17243-465">GoBack</span></span> 

<span data-ttu-id="17243-466">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-466">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="17243-467">HRESULT público [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="17243-467">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="17243-468">GoForward</span><span class="sxs-lookup"><span data-stu-id="17243-468">GoForward</span></span> 

<span data-ttu-id="17243-469">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-469">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="17243-470">[HRESULT público](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="17243-470">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="17243-471">Busque</span><span class="sxs-lookup"><span data-stu-id="17243-471">Navigate</span></span> 

<span data-ttu-id="17243-472">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="17243-472">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="17243-473">[desplazarse](#navigate)con HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="17243-473">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="17243-474">Para obtener más información, consulta los eventos de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-474">See the navigation events for more information.</span></span> <span data-ttu-id="17243-475">Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.</span><span class="sxs-lookup"><span data-stu-id="17243-475">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

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

#### <span data-ttu-id="17243-476">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="17243-476">NavigateToString</span></span> 

<span data-ttu-id="17243-477">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="17243-477">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="17243-478">HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="17243-478">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="17243-479">El parámetro htmlContent no puede tener más de 2 MB de caracteres.</span><span class="sxs-lookup"><span data-stu-id="17243-479">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="17243-480">El origen de la nueva página será acerca de: Blank.</span><span class="sxs-lookup"><span data-stu-id="17243-480">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="17243-481">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="17243-481">OpenDevToolsWindow</span></span> 

<span data-ttu-id="17243-482">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-482">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="17243-483">[OPENDEVTOOLSWINDOW](#opendevtoolswindow)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="17243-483">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="17243-484">No hace nada si se llama cuando la ventana de DevTools ya está abierta</span><span class="sxs-lookup"><span data-stu-id="17243-484">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="17243-485">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="17243-485">PostWebMessageAsJson</span></span> 

<span data-ttu-id="17243-486">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-486">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="17243-487">HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="17243-487">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="17243-488">Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="17243-488">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="17243-489">JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="17243-489">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span>

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

<span data-ttu-id="17243-490">El argumentos del evento es una instancia de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="17243-490">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="17243-491">La opción ICoreWebView2Settings:: IsWebMessageEnabled debe ser true o este método dará un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="17243-491">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="17243-492">La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-492">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="17243-493">La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto.</span><span class="sxs-lookup"><span data-stu-id="17243-493">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="17243-494">Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host.</span><span class="sxs-lookup"><span data-stu-id="17243-494">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="17243-495">Este mensaje se envía de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="17243-495">This message is sent asynchronously.</span></span> <span data-ttu-id="17243-496">Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.</span><span class="sxs-lookup"><span data-stu-id="17243-496">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="17243-497">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="17243-497">PostWebMessageAsString</span></span> 

<span data-ttu-id="17243-498">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-498">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="17243-499">HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="17243-499">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="17243-500">Esto se comporta exactamente de la misma manera que PostWebMessageAsJson, pero la `window.chrome.webview` propiedad data del argumento de evento de mensaje será una cadena con el mismo valor que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="17243-500">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="17243-501">Use este en lugar de PostWebMessageAsJson si desea comunicarse a través de cadenas simples en lugar de objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="17243-501">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="17243-502">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="17243-502">Reload</span></span> 

<span data-ttu-id="17243-503">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="17243-503">Reload the current page.</span></span>

> <span data-ttu-id="17243-504">[recarga](#reload)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="17243-504">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="17243-505">Esto es similar a desplazarse hasta el URI del documento de nivel superior actual, incluidos todos los eventos de navegación que desencadenan y respetan cualquier entrada de la caché HTTP.</span><span class="sxs-lookup"><span data-stu-id="17243-505">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="17243-506">Sin embargo, el historial de atrás y reenvío no se modificará.</span><span class="sxs-lookup"><span data-stu-id="17243-506">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="17243-507">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="17243-507">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="17243-508">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17243-508">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="17243-509">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-509">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-510">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="17243-510">remove_ContentLoading</span></span> 

<span data-ttu-id="17243-511">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="17243-511">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="17243-512">[remove_ContentLoading](#remove_contentloading)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-512">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-513">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17243-513">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="17243-514">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-514">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="17243-515">[remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-515">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-516">remove_FrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-516">remove_FrameNavigationCompleted</span></span> 

<span data-ttu-id="17243-517">Quitar un controlador de eventos agregado previamente con add_FrameNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-517">Remove an event handler previously added with add_FrameNavigationCompleted.</span></span>

> <span data-ttu-id="17243-518">[remove_FrameNavigationCompleted](#remove_framenavigationcompleted)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-518">public HRESULT [remove_FrameNavigationCompleted](#remove_framenavigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-519">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-519">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="17243-520">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-520">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="17243-521">[remove_FrameNavigationStarting](#remove_framenavigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-521">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-522">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="17243-522">remove_HistoryChanged</span></span> 

<span data-ttu-id="17243-523">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-523">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="17243-524">[remove_HistoryChanged](#remove_historychanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-524">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-525">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="17243-525">remove_NavigationCompleted</span></span> 

<span data-ttu-id="17243-526">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17243-526">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="17243-527">[remove_NavigationCompleted](#remove_navigationcompleted)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-527">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-528">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="17243-528">remove_NavigationStarting</span></span> 

<span data-ttu-id="17243-529">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="17243-529">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="17243-530">[remove_NavigationStarting](#remove_navigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-530">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-531">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17243-531">remove_NewWindowRequested</span></span> 

<span data-ttu-id="17243-532">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-532">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="17243-533">[remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-533">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-534">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="17243-534">remove_PermissionRequested</span></span> 

<span data-ttu-id="17243-535">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-535">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="17243-536">[remove_PermissionRequested](#remove_permissionrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-536">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-537">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="17243-537">remove_ProcessFailed</span></span> 

<span data-ttu-id="17243-538">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="17243-538">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="17243-539">[remove_ProcessFailed](#remove_processfailed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-539">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-540">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="17243-540">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="17243-541">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="17243-541">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="17243-542">[remove_ScriptDialogOpening](#remove_scriptdialogopening)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-542">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-543">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="17243-543">remove_SourceChanged</span></span> 

<span data-ttu-id="17243-544">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="17243-544">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="17243-545">[remove_SourceChanged](#remove_sourcechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-545">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-546">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="17243-546">remove_WebMessageReceived</span></span> 

<span data-ttu-id="17243-547">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="17243-547">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="17243-548">[remove_WebMessageReceived](#remove_webmessagereceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-548">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-549">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="17243-549">remove_WebResourceRequested</span></span> 

<span data-ttu-id="17243-550">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-550">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="17243-551">[remove_WebResourceRequested](#remove_webresourcerequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-551">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-552">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="17243-552">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="17243-553">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-553">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="17243-554">[remove_WindowCloseRequested](#remove_windowcloserequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="17243-554">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17243-555">RemoveHostObjectFromScript</span><span class="sxs-lookup"><span data-stu-id="17243-555">RemoveHostObjectFromScript</span></span> 

<span data-ttu-id="17243-556">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="17243-556">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="17243-557">[REMOVEHOSTOBJECTFROMSCRIPT](#removehostobjectfromscript)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="17243-557">public HRESULT [RemoveHostObjectFromScript](#removehostobjectfromscript)(LPCWSTR name)</span></span>

<span data-ttu-id="17243-558">Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="17243-558">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="17243-559">Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.</span><span class="sxs-lookup"><span data-stu-id="17243-559">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="17243-560">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="17243-560">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="17243-561">Quite el JavaScript correspondiente agregado `AddScriptToExecuteOnDocumentCreated` con el identificador de script especificado.</span><span class="sxs-lookup"><span data-stu-id="17243-561">Remove the corresponding JavaScript added using `AddScriptToExecuteOnDocumentCreated` with the specified script id.</span></span>

> <span data-ttu-id="17243-562">HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR ID)</span><span class="sxs-lookup"><span data-stu-id="17243-562">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="17243-563">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="17243-563">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="17243-564">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="17243-564">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="17243-565">[REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="17243-565">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri, [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="17243-566">Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="17243-566">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="17243-567">Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="17243-567">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="17243-568">Detener</span><span class="sxs-lookup"><span data-stu-id="17243-568">Stop</span></span> 

<span data-ttu-id="17243-569">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="17243-569">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="17243-570">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="17243-570">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="17243-571">No detiene las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="17243-571">Does not stop scripts.</span></span>

#### <span data-ttu-id="17243-572">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="17243-572">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="17243-573">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="17243-573">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="17243-574">[COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format) enum</span><span class="sxs-lookup"><span data-stu-id="17243-574">enum [COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#corewebview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="17243-575">Los</span><span class="sxs-lookup"><span data-stu-id="17243-575">Values</span></span>                         | <span data-ttu-id="17243-576">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-576">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-577">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="17243-577">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="17243-578">Formato de imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="17243-578">PNG image format.</span></span>
<span data-ttu-id="17243-579">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="17243-579">COREWEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="17243-580">Formato de imagen JPEG.</span><span class="sxs-lookup"><span data-stu-id="17243-580">JPEG image format.</span></span>

#### <span data-ttu-id="17243-581">COREWEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-581">COREWEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="17243-582">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="17243-582">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="17243-583">[COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind) enum</span><span class="sxs-lookup"><span data-stu-id="17243-583">enum [COREWEBVIEW2_KEY_EVENT_KIND](#corewebview2_key_event_kind)</span></span>

 <span data-ttu-id="17243-584">Los</span><span class="sxs-lookup"><span data-stu-id="17243-584">Values</span></span>                         | <span data-ttu-id="17243-585">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-585">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-586">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="17243-586">COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="17243-587">Corresponde a WM_KEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="17243-587">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="17243-588">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="17243-588">COREWEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="17243-589">Corresponde a WM_KEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="17243-589">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="17243-590">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="17243-590">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="17243-591">Corresponde a WM_SYSKEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="17243-591">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="17243-592">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="17243-592">COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="17243-593">Corresponde a WM_SYSKEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="17243-593">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="17243-594">COREWEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="17243-594">COREWEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="17243-595">Motivo de mover el foco.</span><span class="sxs-lookup"><span data-stu-id="17243-595">Reason for moving focus.</span></span>

> <span data-ttu-id="17243-596">[COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason) enum</span><span class="sxs-lookup"><span data-stu-id="17243-596">enum [COREWEBVIEW2_MOVE_FOCUS_REASON](#corewebview2_move_focus_reason)</span></span>

 <span data-ttu-id="17243-597">Los</span><span class="sxs-lookup"><span data-stu-id="17243-597">Values</span></span>                         | <span data-ttu-id="17243-598">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-598">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-599">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="17243-599">COREWEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="17243-600">El ajuste del foco a WebView.</span><span class="sxs-lookup"><span data-stu-id="17243-600">Code setting focus into WebView.</span></span>
<span data-ttu-id="17243-601">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="17243-601">COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="17243-602">Moviendo el foco debido a una resaltado de pestañas hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="17243-602">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="17243-603">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="17243-603">COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="17243-604">Moviendo el foco debido a un recorrido de tabulación hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="17243-604">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="17243-605">COREWEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-605">COREWEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="17243-606">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="17243-606">The type of a permission request.</span></span>

> <span data-ttu-id="17243-607">[COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind) enum</span><span class="sxs-lookup"><span data-stu-id="17243-607">enum [COREWEBVIEW2_PERMISSION_KIND](#corewebview2_permission_kind)</span></span>

 <span data-ttu-id="17243-608">Los</span><span class="sxs-lookup"><span data-stu-id="17243-608">Values</span></span>                         | <span data-ttu-id="17243-609">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-609">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-610">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="17243-610">COREWEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="17243-611">Permiso desconocido.</span><span class="sxs-lookup"><span data-stu-id="17243-611">Unknown permission.</span></span>
<span data-ttu-id="17243-612">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="17243-612">COREWEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="17243-613">Permiso para capturar audio.</span><span class="sxs-lookup"><span data-stu-id="17243-613">Permission to capture audio.</span></span>
<span data-ttu-id="17243-614">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="17243-614">COREWEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="17243-615">Permiso para capturar video.</span><span class="sxs-lookup"><span data-stu-id="17243-615">Permission to capture video.</span></span>
<span data-ttu-id="17243-616">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="17243-616">COREWEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="17243-617">Permiso para acceder a la ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="17243-617">Permission to access geolocation.</span></span>
<span data-ttu-id="17243-618">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="17243-618">COREWEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="17243-619">Permiso para enviar notificaciones Web.</span><span class="sxs-lookup"><span data-stu-id="17243-619">Permission to send web notifications.</span></span>
<span data-ttu-id="17243-620">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="17243-620">COREWEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="17243-621">Permiso para acceder al sensor genérico.</span><span class="sxs-lookup"><span data-stu-id="17243-621">Permission to access generic sensor.</span></span>
<span data-ttu-id="17243-622">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="17243-622">COREWEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="17243-623">Permiso para leer el Portapapeles del sistema sin un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="17243-623">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="17243-624">COREWEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="17243-624">COREWEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="17243-625">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="17243-625">Response to a permission request.</span></span>

> <span data-ttu-id="17243-626">[COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state) enum</span><span class="sxs-lookup"><span data-stu-id="17243-626">enum [COREWEBVIEW2_PERMISSION_STATE](#corewebview2_permission_state)</span></span>

 <span data-ttu-id="17243-627">Los</span><span class="sxs-lookup"><span data-stu-id="17243-627">Values</span></span>                         | <span data-ttu-id="17243-628">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-628">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-629">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="17243-629">COREWEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="17243-630">Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.</span><span class="sxs-lookup"><span data-stu-id="17243-630">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="17243-631">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="17243-631">COREWEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="17243-632">Otorgue la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="17243-632">Grant the permission request.</span></span>
<span data-ttu-id="17243-633">COREWEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="17243-633">COREWEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="17243-634">Denegar la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="17243-634">Deny the permission request.</span></span>

#### <span data-ttu-id="17243-635">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="17243-635">COREWEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="17243-636">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="17243-636">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="17243-637">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="17243-637">typedef [COREWEBVIEW2_PHYSICAL_KEY_STATUS](#corewebview2_physical_key_status)</span></span>

<span data-ttu-id="17243-638">Para obtener más información, consulte la documentación de WM_KEYDOWN en[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="17243-638">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

#### <span data-ttu-id="17243-639">COREWEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-639">COREWEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="17243-640">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="17243-640">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="17243-641">[COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind) enum</span><span class="sxs-lookup"><span data-stu-id="17243-641">enum [COREWEBVIEW2_PROCESS_FAILED_KIND](#corewebview2_process_failed_kind)</span></span>

 <span data-ttu-id="17243-642">Los</span><span class="sxs-lookup"><span data-stu-id="17243-642">Values</span></span>                         | <span data-ttu-id="17243-643">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-643">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-644">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="17243-644">COREWEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="17243-645">Indica que el proceso del explorador ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="17243-645">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="17243-646">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="17243-646">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="17243-647">Indica que el proceso de representación ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="17243-647">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="17243-648">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="17243-648">COREWEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="17243-649">Indica que el proceso de representación deja de responder.</span><span class="sxs-lookup"><span data-stu-id="17243-649">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="17243-650">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="17243-650">COREWEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="17243-651">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="17243-651">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="17243-652">[COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind) enum</span><span class="sxs-lookup"><span data-stu-id="17243-652">enum [COREWEBVIEW2_SCRIPT_DIALOG_KIND](#corewebview2_script_dialog_kind)</span></span>

 <span data-ttu-id="17243-653">Los</span><span class="sxs-lookup"><span data-stu-id="17243-653">Values</span></span>                         | <span data-ttu-id="17243-654">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-654">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-655">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="17243-655">COREWEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="17243-656">Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.</span><span class="sxs-lookup"><span data-stu-id="17243-656">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="17243-657">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="17243-657">COREWEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="17243-658">Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-658">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="17243-659">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="17243-659">COREWEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="17243-660">Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-660">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="17243-661">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="17243-661">COREWEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="17243-662">Un cuadro de diálogo invocado a través del evento beforeunload de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17243-662">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="17243-663">COREWEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="17243-663">COREWEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="17243-664">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="17243-664">Error status values for web navigations.</span></span>

> <span data-ttu-id="17243-665">[COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status) enum</span><span class="sxs-lookup"><span data-stu-id="17243-665">enum [COREWEBVIEW2_WEB_ERROR_STATUS](#corewebview2_web_error_status)</span></span>

 <span data-ttu-id="17243-666">Los</span><span class="sxs-lookup"><span data-stu-id="17243-666">Values</span></span>                         | <span data-ttu-id="17243-667">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-667">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-668">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="17243-668">COREWEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="17243-669">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="17243-669">An unknown error occurred.</span></span>
<span data-ttu-id="17243-670">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="17243-670">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="17243-671">El nombre común del certificado SSL no coincide con la dirección Web.</span><span class="sxs-lookup"><span data-stu-id="17243-671">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="17243-672">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="17243-672">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="17243-673">El certificado SSL ha expirado.</span><span class="sxs-lookup"><span data-stu-id="17243-673">The SSL certificate has expired.</span></span>
<span data-ttu-id="17243-674">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="17243-674">COREWEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="17243-675">El certificado de cliente SSL contiene errores.</span><span class="sxs-lookup"><span data-stu-id="17243-675">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="17243-676">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="17243-676">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="17243-677">El certificado SSL ha sido revocado.</span><span class="sxs-lookup"><span data-stu-id="17243-677">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="17243-678">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="17243-678">COREWEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="17243-679">El certificado SSL no es válido &ndash; esto puede significar que el certificado no coincide con los pin de clave pública del nombre de host, que el certificado está firmado por una autoridad que no es de confianza o con un algoritmo de signo débil. el certificado alegó que los nombres DNS han infringido las restricciones de nombres, el certificado contiene una clave débil, el período de validez del certificado es demasiado largo, falta de información de revocación o de mecanismo de revocación, nombre de host no único, falta de información de transparencia del certificado o el certificado está encadenado a una [raíz de Symantec heredado](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="17243-679">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="17243-680">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="17243-680">COREWEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="17243-681">No se puede comunicar con el host.</span><span class="sxs-lookup"><span data-stu-id="17243-681">The host is unreachable.</span></span>
<span data-ttu-id="17243-682">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="17243-682">COREWEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="17243-683">Se agotó el tiempo de espera de la conexión.</span><span class="sxs-lookup"><span data-stu-id="17243-683">The connection has timed out.</span></span>
<span data-ttu-id="17243-684">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="17243-684">COREWEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="17243-685">El servidor ha devuelto una respuesta no válida o no reconocida.</span><span class="sxs-lookup"><span data-stu-id="17243-685">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="17243-686">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="17243-686">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="17243-687">La conexión ha sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="17243-687">The connection was aborted.</span></span>
<span data-ttu-id="17243-688">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="17243-688">COREWEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="17243-689">Se restableció la conexión.</span><span class="sxs-lookup"><span data-stu-id="17243-689">The connection was reset.</span></span>
<span data-ttu-id="17243-690">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="17243-690">COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="17243-691">Se perdió la conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="17243-691">The Internet connection has been lost.</span></span>
<span data-ttu-id="17243-692">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="17243-692">COREWEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="17243-693">No se puede conectar al destino.</span><span class="sxs-lookup"><span data-stu-id="17243-693">Cannot connect to destination.</span></span>
<span data-ttu-id="17243-694">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="17243-694">COREWEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="17243-695">No se pudo resolver el nombre de host proporcionado.</span><span class="sxs-lookup"><span data-stu-id="17243-695">Could not resolve provided host name.</span></span>
<span data-ttu-id="17243-696">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="17243-696">COREWEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="17243-697">Se canceló la operación.</span><span class="sxs-lookup"><span data-stu-id="17243-697">The operation was canceled.</span></span>
<span data-ttu-id="17243-698">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="17243-698">COREWEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="17243-699">Error en la redirección de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17243-699">The request redirect failed.</span></span>
<span data-ttu-id="17243-700">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="17243-700">COREWEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="17243-701">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="17243-701">An unexpected error occurred.</span></span>

#### <span data-ttu-id="17243-702">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="17243-702">COREWEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="17243-703">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="17243-703">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="17243-704">[COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context) enum</span><span class="sxs-lookup"><span data-stu-id="17243-704">enum [COREWEBVIEW2_WEB_RESOURCE_CONTEXT](#corewebview2_web_resource_context)</span></span>

 <span data-ttu-id="17243-705">Los</span><span class="sxs-lookup"><span data-stu-id="17243-705">Values</span></span>                         | <span data-ttu-id="17243-706">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17243-706">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="17243-707">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="17243-707">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="17243-708">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="17243-708">All resources.</span></span>
<span data-ttu-id="17243-709">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="17243-709">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="17243-710">Recursos de documentos.</span><span class="sxs-lookup"><span data-stu-id="17243-710">Document resources.</span></span>
<span data-ttu-id="17243-711">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="17243-711">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="17243-712">Recursos de CSS.</span><span class="sxs-lookup"><span data-stu-id="17243-712">CSS resources.</span></span>
<span data-ttu-id="17243-713">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="17243-713">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="17243-714">Recursos de imagen.</span><span class="sxs-lookup"><span data-stu-id="17243-714">Image resources.</span></span>
<span data-ttu-id="17243-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="17243-715">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="17243-716">Otros recursos multimedia, como los vídeos.</span><span class="sxs-lookup"><span data-stu-id="17243-716">Other media resources such as videos.</span></span>
<span data-ttu-id="17243-717">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="17243-717">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="17243-718">Recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="17243-718">Font resources.</span></span>
<span data-ttu-id="17243-719">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="17243-719">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="17243-720">Recursos de script.</span><span class="sxs-lookup"><span data-stu-id="17243-720">Script resources.</span></span>
<span data-ttu-id="17243-721">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="17243-721">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="17243-722">Solicitudes XML HTTP.</span><span class="sxs-lookup"><span data-stu-id="17243-722">XML HTTP requests.</span></span>
<span data-ttu-id="17243-723">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="17243-723">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="17243-724">Capture la comunicación de la API.</span><span class="sxs-lookup"><span data-stu-id="17243-724">Fetch API communication.</span></span>
<span data-ttu-id="17243-725">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="17243-725">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="17243-726">Recursos de TextTrack.</span><span class="sxs-lookup"><span data-stu-id="17243-726">TextTrack resources.</span></span>
<span data-ttu-id="17243-727">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="17243-727">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="17243-728">Comunicación de la API de EventSource.</span><span class="sxs-lookup"><span data-stu-id="17243-728">EventSource API communication.</span></span>
<span data-ttu-id="17243-729">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="17243-729">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="17243-730">Comunicación de API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="17243-730">WebSocket API communication.</span></span>
<span data-ttu-id="17243-731">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="17243-731">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="17243-732">Manifiestos de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="17243-732">Web App Manifests.</span></span>
<span data-ttu-id="17243-733">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="17243-733">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="17243-734">Intercambio de HTTP firmado.</span><span class="sxs-lookup"><span data-stu-id="17243-734">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="17243-735">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="17243-735">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="17243-736">Solicitudes de ping.</span><span class="sxs-lookup"><span data-stu-id="17243-736">Ping requests.</span></span>
<span data-ttu-id="17243-737">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="17243-737">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="17243-738">Informes de violación de CSP.</span><span class="sxs-lookup"><span data-stu-id="17243-738">CSP Violation Reports.</span></span>
<span data-ttu-id="17243-739">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="17243-739">COREWEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="17243-740">Otros recursos.</span><span class="sxs-lookup"><span data-stu-id="17243-740">Other resources.</span></span>

