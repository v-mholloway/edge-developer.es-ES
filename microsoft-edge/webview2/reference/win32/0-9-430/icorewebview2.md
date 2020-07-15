---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 6fce29c2df69abc8d55d91c267b282702e567453
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881210"
---
# <span data-ttu-id="9e773-104">0.9.430: ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="9e773-104">0.9.430 - interface ICoreWebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="9e773-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9e773-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9e773-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9e773-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2
  : public IUnknown
```

<span data-ttu-id="9e773-107">WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.</span><span class="sxs-lookup"><span data-stu-id="9e773-107">WebView2 enables you to host web content using the latest Edge web browser technology.</span></span>

## <span data-ttu-id="9e773-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9e773-108">Summary</span></span>

 <span data-ttu-id="9e773-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e773-109">Members</span></span>                        | <span data-ttu-id="9e773-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e773-111">get_Settings</span><span class="sxs-lookup"><span data-stu-id="9e773-111">get_Settings</span></span>](#get_settings) | <span data-ttu-id="9e773-112">El objeto ICoreWebView2Settings contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="9e773-112">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>
[<span data-ttu-id="9e773-113">get_Source</span><span class="sxs-lookup"><span data-stu-id="9e773-113">get_Source</span></span>](#get_source) | <span data-ttu-id="9e773-114">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-114">The URI of the current top level document.</span></span>
[<span data-ttu-id="9e773-115">Busque</span><span class="sxs-lookup"><span data-stu-id="9e773-115">Navigate</span></span>](#navigate) | <span data-ttu-id="9e773-116">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="9e773-116">Cause a navigation of the top level document to the specified URI.</span></span>
[<span data-ttu-id="9e773-117">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="9e773-117">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="9e773-118">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="9e773-118">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="9e773-119">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-119">add_NavigationStarting</span></span>](#add_navigationstarting) | <span data-ttu-id="9e773-120">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-120">Add an event handler for the NavigationStarting event.</span></span>
[<span data-ttu-id="9e773-121">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-121">remove_NavigationStarting</span></span>](#remove_navigationstarting) | <span data-ttu-id="9e773-122">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-122">Remove an event handler previously added with add_NavigationStarting.</span></span>
[<span data-ttu-id="9e773-123">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9e773-123">add_ContentLoading</span></span>](#add_contentloading) | <span data-ttu-id="9e773-124">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9e773-124">Add an event handler for the ContentLoading event.</span></span>
[<span data-ttu-id="9e773-125">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9e773-125">remove_ContentLoading</span></span>](#remove_contentloading) | <span data-ttu-id="9e773-126">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9e773-126">Remove an event handler previously added with add_ContentLoading.</span></span>
[<span data-ttu-id="9e773-127">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-127">add_SourceChanged</span></span>](#add_sourcechanged) | <span data-ttu-id="9e773-128">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="9e773-128">SourceChanged fires when the Source property changes.</span></span>
[<span data-ttu-id="9e773-129">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-129">remove_SourceChanged</span></span>](#remove_sourcechanged) | <span data-ttu-id="9e773-130">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-130">Remove an event handler previously added with add_SourceChanged.</span></span>
[<span data-ttu-id="9e773-131">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-131">add_HistoryChanged</span></span>](#add_historychanged) | <span data-ttu-id="9e773-132">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9e773-132">HistoryChange listen to the change of navigation history for the top level document.</span></span>
[<span data-ttu-id="9e773-133">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-133">remove_HistoryChanged</span></span>](#remove_historychanged) | <span data-ttu-id="9e773-134">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-134">Remove an event handler previously added with add_HistoryChanged.</span></span>
[<span data-ttu-id="9e773-135">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9e773-135">add_NavigationCompleted</span></span>](#add_navigationcompleted) | <span data-ttu-id="9e773-136">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e773-136">Add an event handler for the NavigationCompleted event.</span></span>
[<span data-ttu-id="9e773-137">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9e773-137">remove_NavigationCompleted</span></span>](#remove_navigationcompleted) | <span data-ttu-id="9e773-138">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e773-138">Remove an event handler previously added with add_NavigationCompleted.</span></span>
[<span data-ttu-id="9e773-139">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-139">add_FrameNavigationStarting</span></span>](#add_framenavigationstarting) | <span data-ttu-id="9e773-140">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-140">Add an event handler for the FrameNavigationStarting event.</span></span>
[<span data-ttu-id="9e773-141">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-141">remove_FrameNavigationStarting</span></span>](#remove_framenavigationstarting) | <span data-ttu-id="9e773-142">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-142">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>
[<span data-ttu-id="9e773-143">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9e773-143">add_ScriptDialogOpening</span></span>](#add_scriptdialogopening) | <span data-ttu-id="9e773-144">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9e773-144">Add an event handler for the ScriptDialogOpening event.</span></span>
[<span data-ttu-id="9e773-145">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9e773-145">remove_ScriptDialogOpening</span></span>](#remove_scriptdialogopening) | <span data-ttu-id="9e773-146">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9e773-146">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>
[<span data-ttu-id="9e773-147">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-147">add_PermissionRequested</span></span>](#add_permissionrequested) | <span data-ttu-id="9e773-148">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-148">Add an event handler for the PermissionRequested event.</span></span>
[<span data-ttu-id="9e773-149">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-149">remove_PermissionRequested</span></span>](#remove_permissionrequested) | <span data-ttu-id="9e773-150">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-150">Remove an event handler previously added with add_PermissionRequested.</span></span>
[<span data-ttu-id="9e773-151">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9e773-151">add_ProcessFailed</span></span>](#add_processfailed) | <span data-ttu-id="9e773-152">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9e773-152">Add an event handler for the ProcessFailed event.</span></span>
[<span data-ttu-id="9e773-153">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9e773-153">remove_ProcessFailed</span></span>](#remove_processfailed) | <span data-ttu-id="9e773-154">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9e773-154">Remove an event handler previously added with add_ProcessFailed.</span></span>
[<span data-ttu-id="9e773-155">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9e773-155">AddScriptToExecuteOnDocumentCreated</span></span>](#addscripttoexecuteondocumentcreated) | <span data-ttu-id="9e773-156">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="9e773-156">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>
[<span data-ttu-id="9e773-157">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9e773-157">RemoveScriptToExecuteOnDocumentCreated</span></span>](#removescripttoexecuteondocumentcreated) | <span data-ttu-id="9e773-158">Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="9e773-158">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>
[<span data-ttu-id="9e773-159">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="9e773-159">ExecuteScript</span></span>](#executescript) | <span data-ttu-id="9e773-160">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-160">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="9e773-161">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="9e773-161">CapturePreview</span></span>](#capturepreview) | <span data-ttu-id="9e773-162">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="9e773-162">Capture an image of what WebView is displaying.</span></span>
[<span data-ttu-id="9e773-163">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="9e773-163">Reload</span></span>](#reload) | <span data-ttu-id="9e773-164">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-164">Reload the current page.</span></span>
[<span data-ttu-id="9e773-165">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="9e773-165">PostWebMessageAsJson</span></span>](#postwebmessageasjson) | <span data-ttu-id="9e773-166">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-166">Post the specified webMessage to the top level document in this WebView.</span></span>
[<span data-ttu-id="9e773-167">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="9e773-167">PostWebMessageAsString</span></span>](#postwebmessageasstring) | <span data-ttu-id="9e773-168">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-168">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>
[<span data-ttu-id="9e773-169">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9e773-169">add_WebMessageReceived</span></span>](#add_webmessagereceived) | <span data-ttu-id="9e773-170">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="9e773-170">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="9e773-171">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9e773-171">remove_WebMessageReceived</span></span>](#remove_webmessagereceived) | <span data-ttu-id="9e773-172">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="9e773-172">Remove an event handler previously added with add_WebMessageReceived.</span></span>
[<span data-ttu-id="9e773-173">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="9e773-173">CallDevToolsProtocolMethod</span></span>](#calldevtoolsprotocolmethod) | <span data-ttu-id="9e773-174">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="9e773-174">Call an asynchronous DevToolsProtocol method.</span></span>
[<span data-ttu-id="9e773-175">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="9e773-175">get_BrowserProcessId</span></span>](#get_browserprocessid) | <span data-ttu-id="9e773-176">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-176">The process id of the browser process that hosts the WebView.</span></span>
[<span data-ttu-id="9e773-177">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="9e773-177">get_CanGoBack</span></span>](#get_cangoback) | <span data-ttu-id="9e773-178">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-178">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="9e773-179">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="9e773-179">get_CanGoForward</span></span>](#get_cangoforward) | <span data-ttu-id="9e773-180">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-180">Returns true if the webview can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="9e773-181">GoBack</span><span class="sxs-lookup"><span data-stu-id="9e773-181">GoBack</span></span>](#goback) | <span data-ttu-id="9e773-182">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-182">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="9e773-183">GoForward</span><span class="sxs-lookup"><span data-stu-id="9e773-183">GoForward</span></span>](#goforward) | <span data-ttu-id="9e773-184">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-184">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="9e773-185">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="9e773-185">GetDevToolsProtocolEventReceiver</span></span>](#getdevtoolsprotocoleventreceiver) | <span data-ttu-id="9e773-186">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9e773-186">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>
[<span data-ttu-id="9e773-187">Detener</span><span class="sxs-lookup"><span data-stu-id="9e773-187">Stop</span></span>](#stop) | <span data-ttu-id="9e773-188">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="9e773-188">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="9e773-189">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-189">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="9e773-190">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-190">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="9e773-191">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-191">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="9e773-192">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-192">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="9e773-193">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-193">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="9e773-194">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-194">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="9e773-195">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-195">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="9e773-196">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-196">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="9e773-197">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="9e773-197">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="9e773-198">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-198">The title for the current top level document.</span></span>
[<span data-ttu-id="9e773-199">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="9e773-199">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="9e773-200">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="9e773-200">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="9e773-201">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="9e773-201">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="9e773-202">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="9e773-202">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="9e773-203">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="9e773-203">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="9e773-204">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-204">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="9e773-205">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-205">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="9e773-206">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="9e773-206">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="9e773-207">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-207">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="9e773-208">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e773-208">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="9e773-209">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="9e773-209">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="9e773-210">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9e773-210">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="9e773-211">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-211">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="9e773-212">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-212">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="9e773-213">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-213">remove_WebResourceRequested</span></span>](#remove_webresourcerequested) | <span data-ttu-id="9e773-214">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-214">Remove an event handler previously added with add_WebResourceRequested.</span></span>
[<span data-ttu-id="9e773-215">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9e773-215">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="9e773-216">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-216">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="9e773-217">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9e773-217">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="9e773-218">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-218">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>
[<span data-ttu-id="9e773-219">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-219">add_WindowCloseRequested</span></span>](#add_windowcloserequested) | <span data-ttu-id="9e773-220">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-220">Add an event handler for the WindowCloseRequested event.</span></span>
[<span data-ttu-id="9e773-221">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-221">remove_WindowCloseRequested</span></span>](#remove_windowcloserequested) | <span data-ttu-id="9e773-222">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-222">Remove an event handler previously added with add_WindowCloseRequested.</span></span>
[<span data-ttu-id="9e773-223">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="9e773-223">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span>](#core_webview2_capture_preview_image_format) | <span data-ttu-id="9e773-224">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9e773-224">Image format used by the ICoreWebView2::CapturePreview method.</span></span>
[<span data-ttu-id="9e773-225">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="9e773-225">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span>](#core_webview2_script_dialog_kind) | <span data-ttu-id="9e773-226">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9e773-226">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>
[<span data-ttu-id="9e773-227">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="9e773-227">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span>](#core_webview2_process_failed_kind) | <span data-ttu-id="9e773-228">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9e773-228">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>
[<span data-ttu-id="9e773-229">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="9e773-229">CORE_WEBVIEW2_PERMISSION_KIND</span></span>](#core_webview2_permission_kind) | <span data-ttu-id="9e773-230">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9e773-230">The type of a permission request.</span></span>
[<span data-ttu-id="9e773-231">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="9e773-231">CORE_WEBVIEW2_PERMISSION_STATE</span></span>](#core_webview2_permission_state) | <span data-ttu-id="9e773-232">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9e773-232">Response to a permission request.</span></span>
[<span data-ttu-id="9e773-233">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="9e773-233">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span>](#core_webview2_web_error_status) | <span data-ttu-id="9e773-234">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-234">Error status values for web navigations.</span></span>
[<span data-ttu-id="9e773-235">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="9e773-235">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span>](#core_webview2_web_resource_context) | <span data-ttu-id="9e773-236">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-236">Enum for web resource request contexts.</span></span>

## <span data-ttu-id="9e773-237">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="9e773-237">Navigation events</span></span>

<span data-ttu-id="9e773-238">La secuencia normal de eventos de navegación es NavigationStarting, SourceChanged, ContentLoading y, después, NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e773-238">The normal sequence of navigation events is NavigationStarting, SourceChanged, ContentLoading and then NavigationCompleted.</span></span>

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

<span data-ttu-id="9e773-240">Ten en cuenta que esto es para los eventos de navegación con el mismo evento NavigationId.</span><span class="sxs-lookup"><span data-stu-id="9e773-240">Note that this is for navigation events with the same NavigationId event arg.</span></span> <span data-ttu-id="9e773-241">Los eventos de navegación con diferentes argumentos de evento de NavigationId se pueden solapar.</span><span class="sxs-lookup"><span data-stu-id="9e773-241">Navigations events with different NavigationId event args may overlap.</span></span> <span data-ttu-id="9e773-242">Por ejemplo, si inicia una espera de navegación para su evento NavigationStarting y, a continuación, inicia otra navegación, verá el NavigationStarting para la primera navegación, seguida de la NavigationStarting del segundo Navigate, seguido de la NavigationCompleted de la primera navegación y, a continuación, todos los demás eventos de navegación correspondientes para la segunda navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-242">For instance, if you start a navigation wait for its NavigationStarting event and then start another navigation you'll see the NavigationStarting for the first navigate followed by the NavigationStarting of the second navigate, followed by the NavigationCompleted for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span> <span data-ttu-id="9e773-243">En casos de error puede haber o no un evento ContentLoading dependiendo de si la navegación continúa o no en una página de error.</span><span class="sxs-lookup"><span data-stu-id="9e773-243">In error cases there may or may not be a ContentLoading event depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="9e773-244">En el caso de una redirección HTTP, habrá varios eventos NavigationStarting en una fila, y los siguientes tendrán establecido el marcador IsRedirect.</span><span class="sxs-lookup"><span data-stu-id="9e773-244">In case of an HTTP redirect, there will be multiple NavigationStarting events in a row, with ones following the first will have their IsRedirect flag set.</span></span>

<span data-ttu-id="9e773-245">Para supervisar o cancelar la navegación dentro de los submarcos de la vista en WebView, use FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-245">To monitor or cancel navigations inside subframes in the WebView, use FrameNavigationStarting.</span></span>

## <span data-ttu-id="9e773-246">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="9e773-246">Process model</span></span>

<span data-ttu-id="9e773-247">WebView2 usa el mismo modelo de proceso que el explorador Web de Edge.</span><span class="sxs-lookup"><span data-stu-id="9e773-247">WebView2 uses the same process model as the Edge web browser.</span></span> <span data-ttu-id="9e773-248">Hay un proceso de explorador Edge por cada directorio de datos de usuario especificado en una sesión de usuario que servirá a cualquier proceso de llamada de WebView2 que especifique el directorio de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9e773-248">There is one Edge browser process per specified user data directory in a user session that will serve any WebView2 calling process that specifies that user data directory.</span></span> <span data-ttu-id="9e773-249">Esto significa que un proceso del navegador Edge puede estar atendiendo varios procesos de llamadas y un proceso de llamada puede estar usando varios procesos de explorador.</span><span class="sxs-lookup"><span data-stu-id="9e773-249">This means one Edge browser process may be serving multiple calling processes and one calling process may be using multiple Edge browser processes.</span></span>

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

<span data-ttu-id="9e773-251">Fuera de un proceso de explorador, habrá varios procesos de representación.</span><span class="sxs-lookup"><span data-stu-id="9e773-251">Off of a browser process there will be some number of renderer processes.</span></span> <span data-ttu-id="9e773-252">Estos se crean según sea necesario para dar servicio a varios marcos que se encuentren en diferentes vistas previas.</span><span class="sxs-lookup"><span data-stu-id="9e773-252">These are created as necessary to service potentially multiple frames in different WebViews.</span></span> <span data-ttu-id="9e773-253">La cantidad de procesos de representación varía en función de la característica de explorador de aislamiento del sitio y la cantidad de orígenes distintos desconectados representados en las vistas de web asociadas.</span><span class="sxs-lookup"><span data-stu-id="9e773-253">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated WebViews.</span></span>

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

<span data-ttu-id="9e773-255">Puede reaccionar ante los bloqueos y los bloqueos en estos procesos del explorador y el representador mediante el evento ProcessFailure.</span><span class="sxs-lookup"><span data-stu-id="9e773-255">You can react to crashes and hangs in these browser and renderer processes using the ProcessFailure event.</span></span>

<span data-ttu-id="9e773-256">Puede apagar de forma segura los procesos del explorador y el representador asociados con el método Close.</span><span class="sxs-lookup"><span data-stu-id="9e773-256">You can safely shutdown associated browser and renderer processes using the Close method.</span></span>

## <span data-ttu-id="9e773-257">Modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="9e773-257">Threading model</span></span>

<span data-ttu-id="9e773-258">El WebView2 debe crearse en un subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9e773-258">The WebView2 must be created on a UI thread.</span></span> <span data-ttu-id="9e773-259">Específicamente un hilo con un bombeo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9e773-259">Specifically a thread with a message pump.</span></span> <span data-ttu-id="9e773-260">Todas las devoluciones de llamada se producirán en ese subproceso y las llamadas a la vista en WebView deberán realizarse en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="9e773-260">All callbacks will occur on that thread and calls into the WebView must be done on that thread.</span></span> <span data-ttu-id="9e773-261">No es seguro usar la vista en WebView desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="9e773-261">It is not safe to use the WebView from another thread.</span></span>

<span data-ttu-id="9e773-262">Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.</span><span class="sxs-lookup"><span data-stu-id="9e773-262">Callbacks including event handlers and completion handlers execute serially.</span></span> <span data-ttu-id="9e773-263">Es decir, si tiene un controlador de eventos ejecutándose y comienza un bucle de mensaje, no se empezarán a ejecutar de forma reentrante otros controladores de eventos o devoluciones de llamada de finalización.</span><span class="sxs-lookup"><span data-stu-id="9e773-263">That is, if you have an event handler running and begin a message loop no other event handlers or completion callbacks will begin executing reentrantly.</span></span>

## <span data-ttu-id="9e773-264">Seguridad</span><span class="sxs-lookup"><span data-stu-id="9e773-264">Security</span></span>

<span data-ttu-id="9e773-265">Comprueba siempre la propiedad de origen de WebView antes de usar ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString o cualquier otro método para enviar información a WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-265">Always check the Source property of the WebView before using ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, or any other method to send information into the WebView.</span></span> <span data-ttu-id="9e773-266">Es posible que la vista Web haya navegado a otra página a través del usuario final interactuando con la página o script de la página que provoca la navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-266">The WebView may have navigated to another page via the end user interacting with the page or script in the page causing navigation.</span></span> <span data-ttu-id="9e773-267">Del mismo modo, preste mucha atención a AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="9e773-267">Similarly, be very careful with AddScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="9e773-268">Todas las navegaciones futuras ejecutarán esta secuencia de comandos y si proporciona acceso a información dirigida únicamente a un determinado origen, cualquier documento HTML puede tener acceso.</span><span class="sxs-lookup"><span data-stu-id="9e773-268">All future navigations will run this script and if it provides access to information intended only for a certain origin, any HTML document may have access.</span></span>

<span data-ttu-id="9e773-269">Al examinar el resultado de una llamada a un método ExecuteScript, un evento de WebMessageReceived, comprobar siempre el origen del remitente o cualquier otro mecanismo de recepción de la información de un documento HTML en una vista previa valide el URI del documento HTML es el que espera.</span><span class="sxs-lookup"><span data-stu-id="9e773-269">When examining the result of an ExecuteScript method call, a WebMessageReceived event, always check the Source of the sender, or any other mechanism of receiving information from an HTML document in a WebView validate the URI of the HTML document is what you expect.</span></span>

<span data-ttu-id="9e773-270">Al construir un mensaje para enviarlo a un WebView, prefiere usar PostWebMessageAsJson y construir el parámetro de cadena JSON con una biblioteca JSON.</span><span class="sxs-lookup"><span data-stu-id="9e773-270">When constructing a message to send into a WebView, prefer using PostWebMessageAsJson and construct the JSON string parameter using a JSON library.</span></span> <span data-ttu-id="9e773-271">Esto evitará cualquier accidente potencial de codificación de información en una cadena o script de JSON y asegúrese de que ninguna entrada controlada por el atacante pueda modificar el resto del mensaje JSON o ejecutar una secuencia de comandos arbitraria.</span><span class="sxs-lookup"><span data-stu-id="9e773-271">This will avoid any potential accidents of encoding information into a JSON string or script and ensure no attacker controlled input can modify the rest of the JSON message or run arbitrary script.</span></span>

## <span data-ttu-id="9e773-272">Tipos de cadena</span><span class="sxs-lookup"><span data-stu-id="9e773-272">String types</span></span>

<span data-ttu-id="9e773-273">Los parámetros de salida de cadenas son LPWSTR null terminada.</span><span class="sxs-lookup"><span data-stu-id="9e773-273">String out parameters are LPWSTR null terminated strings.</span></span> <span data-ttu-id="9e773-274">El destinatario de la llamada asigna la cadena con CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="9e773-274">The callee allocates the string using CoTaskMemAlloc.</span></span> <span data-ttu-id="9e773-275">La propiedad se transfiere a la persona que llama y la persona que llama puede liberar la memoria usando CoTaskMemFree.</span><span class="sxs-lookup"><span data-stu-id="9e773-275">Ownership is transferred to the caller and it is up to the caller to free the memory using CoTaskMemFree.</span></span>

<span data-ttu-id="9e773-276">La cadena en los parámetros son cadenas terminadas en NULL LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="9e773-276">String in parameters are LPCWSTR null terminated strings.</span></span> <span data-ttu-id="9e773-277">La persona que llama garantiza que la cadena es válida durante la llamada de función sincrónica.</span><span class="sxs-lookup"><span data-stu-id="9e773-277">The caller ensures the string is valid for the duration of the synchronous function call.</span></span> <span data-ttu-id="9e773-278">Si el destinatario de la llamada tiene que conservar ese valor en algún punto después de que se complete la llamada de función, el destinatario de la llamada debe asignar su propia copia del valor de la cadena.</span><span class="sxs-lookup"><span data-stu-id="9e773-278">If the callee needs to retain that value to some point after the function call completes, the callee must allocate its own copy of the string value.</span></span>

## <span data-ttu-id="9e773-279">URI y análisis de JSON</span><span class="sxs-lookup"><span data-stu-id="9e773-279">URI and JSON parsing</span></span>

<span data-ttu-id="9e773-280">Varios métodos proporcionan o aceptan identificadores URI y JSON como cadenas.</span><span class="sxs-lookup"><span data-stu-id="9e773-280">Various methods provide or accept URIs and JSON as strings.</span></span> <span data-ttu-id="9e773-281">Use su propia biblioteca preferida para analizar y generar estas cadenas.</span><span class="sxs-lookup"><span data-stu-id="9e773-281">Please use your own preferred library for parsing and generating these strings.</span></span>

<span data-ttu-id="9e773-282">Si WinRT está disponible para tu aplicación, puedes usar `RuntimeClass_Windows_Data_Json_JsonObject` y `IJsonObjectStatics` analizar o producir cadenas JSON, o bien, `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analizar y producir URI.</span><span class="sxs-lookup"><span data-stu-id="9e773-282">If WinRT is available for your app you can use `RuntimeClass_Windows_Data_Json_JsonObject` and `IJsonObjectStatics` to parse or produce JSON strings or `RuntimeClass_Windows_Foundation_Uri` and `IUriRuntimeClassFactory` to parse and produce URIs.</span></span> <span data-ttu-id="9e773-283">Ambos funcionan en las aplicaciones Win32.</span><span class="sxs-lookup"><span data-stu-id="9e773-283">Both of these work in Win32 apps.</span></span>

<span data-ttu-id="9e773-284">Si usas IUri y CreateUri para analizar URI, es posible que desees usar los siguientes marcadores de creación de URI para que el comportamiento de CreateUri sea más parecido al de análisis de URI en la vista de vistas en vista previa:</span><span class="sxs-lookup"><span data-stu-id="9e773-284">If you use IUri and CreateUri to parse URIs you may want to use the following URI creation flags to have CreateUri behavior more closely match the URI parsing in the WebView:</span></span> `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## <span data-ttu-id="9e773-285">Depuración</span><span class="sxs-lookup"><span data-stu-id="9e773-285">Debugging</span></span>

<span data-ttu-id="9e773-286">Abra DevTools con los métodos abreviados normales: `F12` o `Ctrl+Shift+I` .</span><span class="sxs-lookup"><span data-stu-id="9e773-286">Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`.</span></span> <span data-ttu-id="9e773-287">Puede usar el `--auto-open-devtools-for-tabs` modificador de argumento de comando para que la ventana de DevTools se abra inmediatamente al crear una vista en vista previa.</span><span class="sxs-lookup"><span data-stu-id="9e773-287">You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView.</span></span> <span data-ttu-id="9e773-288">Consulte la documentación de CreateCoreWebView2Host para obtener información sobre cómo proporcionar argumentos de la línea de comandos adicionales para el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="9e773-288">See CreateCoreWebView2Host documentation for how to provide additional command line arguments to the browser process.</span></span> <span data-ttu-id="9e773-289">Consulte la clave del registro LoaderOverride para probar las diferentes compilaciones de WebView2 sin modificar la aplicación en la documentación de CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="9e773-289">Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Host documentation.</span></span>

## <span data-ttu-id="9e773-290">Control de versiones</span><span class="sxs-lookup"><span data-stu-id="9e773-290">Versioning</span></span>

<span data-ttu-id="9e773-291">Después de haber usado una versión determinada del SDK para compilar la aplicación, es posible que la aplicación termine de funcionar con una versión anterior o posterior de los archivos binarios instalados en el explorador.</span><span class="sxs-lookup"><span data-stu-id="9e773-291">After you've used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.</span></span> <span data-ttu-id="9e773-292">Hasta la versión 1.0.0.0 de WebView2, es posible que se produzcan cambios importantes durante las actualizaciones que impidan que el SDK funcione con diferentes versiones de los archivos binarios del explorador instalados.</span><span class="sxs-lookup"><span data-stu-id="9e773-292">Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that will prevent your SDK from working with different versions of installed browser binaries.</span></span> <span data-ttu-id="9e773-293">Después de la versión 1.0.0.0, las diferentes versiones del SDK pueden funcionar con las distintas versiones del explorador instalado siguiendo estos procedimientos recomendados:</span><span class="sxs-lookup"><span data-stu-id="9e773-293">After version 1.0.0.0 different versions of the SDK can work with different versions of the installed browser by following these best practices:</span></span>

<span data-ttu-id="9e773-294">Para tener en cuenta los cambios importantes en la API, asegúrate de comprobar si se produjo un error al llamar a la CreateCoreWebView2Environment de exportación de DLL y al llamar a QueryInterface en cualquier objeto CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="9e773-294">To account for breaking changes to the API be sure to check for failure when calling the DLL export CreateCoreWebView2Environment and when calling QueryInterface on any CoreWebView2 object.</span></span> <span data-ttu-id="9e773-295">Un valor devuelto de E_NOINTERFACE puede indicar que el SDK no es compatible con los archivos binarios del explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="9e773-295">A return value of E_NOINTERFACE can indicate the SDK is not compatible with the Edge browser binaries.</span></span>

<span data-ttu-id="9e773-296">Comprobar si hay un error en QueryInterface también tendrá en cuenta los casos en los que el SDK es más reciente que la versión del explorador Edge y la aplicación intenta usar una interfaz de la que no está consciente el explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="9e773-296">Checking for failure from QueryInterface will also account for cases where the SDK is newer than the version of the Edge browser and your app attempts to use an interface of which the Edge browser is unaware.</span></span>

<span data-ttu-id="9e773-297">Cuando una interfaz no está disponible, puede considerar deshabilitar la característica asociada si es posible o informar al usuario final de que necesita actualizar su explorador.</span><span class="sxs-lookup"><span data-stu-id="9e773-297">When an interface is unavailable, you can consider disabling the associated feature if possible, or otherwise informing the end user they need to update their browser.</span></span>

## <span data-ttu-id="9e773-298">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e773-298">Members</span></span>

#### <span data-ttu-id="9e773-299">get_Settings</span><span class="sxs-lookup"><span data-stu-id="9e773-299">get_Settings</span></span> 

<span data-ttu-id="9e773-300">El objeto ICoreWebView2Settings contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="9e773-300">The ICoreWebView2Settings object contains various modifiable settings for the running WebView.</span></span>

> <span data-ttu-id="9e773-301">[get_Settings](#get_settings)pública HRESULT (configuración de ICoreWebView2Settings \* \*)</span><span class="sxs-lookup"><span data-stu-id="9e773-301">public HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings \*\* settings)</span></span>

#### <span data-ttu-id="9e773-302">get_Source</span><span class="sxs-lookup"><span data-stu-id="9e773-302">get_Source</span></span> 

<span data-ttu-id="9e773-303">Identificador URI del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-303">The URI of the current top level document.</span></span>

> <span data-ttu-id="9e773-304">[get_Source](#get_source)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="9e773-304">public HRESULT [get_Source](#get_source)(LPWSTR \* uri)</span></span>

<span data-ttu-id="9e773-305">Este valor puede cambiar potencialmente como parte del desencadenador de eventos SourceChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9e773-305">This value potentially changes as a part of the SourceChanged event firing for some cases such as navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="9e773-306">Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-306">It will remain the same for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span>

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

#### <span data-ttu-id="9e773-307">Busque</span><span class="sxs-lookup"><span data-stu-id="9e773-307">Navigate</span></span> 

<span data-ttu-id="9e773-308">Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.</span><span class="sxs-lookup"><span data-stu-id="9e773-308">Cause a navigation of the top level document to the specified URI.</span></span>

> <span data-ttu-id="9e773-309">[desplazarse](#navigate)con HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="9e773-309">public HRESULT [Navigate](#navigate)(LPCWSTR uri)</span></span>

<span data-ttu-id="9e773-310">Para obtener más información, consulta los eventos de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-310">See the navigation events for more information.</span></span> <span data-ttu-id="9e773-311">Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-311">Note that this starts a navigation and the corresponding NavigationStarting event will fire sometime after this Navigate call completes.</span></span>

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

#### <span data-ttu-id="9e773-312">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="9e773-312">NavigateToString</span></span> 

<span data-ttu-id="9e773-313">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="9e773-313">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="9e773-314">HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span><span class="sxs-lookup"><span data-stu-id="9e773-314">public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)</span></span>

<span data-ttu-id="9e773-315">El parámetro htmlContent no puede tener más de 2 MB de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9e773-315">The htmlContent parameter may not be larger than 2 MB of characters.</span></span> <span data-ttu-id="9e773-316">El origen de la nueva página será acerca de: Blank.</span><span class="sxs-lookup"><span data-stu-id="9e773-316">The origin of the new page will be about:blank.</span></span>

```cpp
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### <span data-ttu-id="9e773-317">add_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-317">add_NavigationStarting</span></span> 

<span data-ttu-id="9e773-318">Agregue un controlador de eventos para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-318">Add an event handler for the NavigationStarting event.</span></span>

> <span data-ttu-id="9e773-319">[add_NavigationStarting](#add_navigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-319">public HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-320">NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="9e773-320">NavigationStarting fires when the WebView main frame is requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="9e773-321">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="9e773-321">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="9e773-322">remove_NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-322">remove_NavigationStarting</span></span> 

<span data-ttu-id="9e773-323">Quitar un controlador de eventos agregado previamente con add_NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-323">Remove an event handler previously added with add_NavigationStarting.</span></span>

> <span data-ttu-id="9e773-324">[remove_NavigationStarting](#remove_navigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-324">public HRESULT [remove_NavigationStarting](#remove_navigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-325">add_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9e773-325">add_ContentLoading</span></span> 

<span data-ttu-id="9e773-326">Agregue un controlador de eventos para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9e773-326">Add an event handler for the ContentLoading event.</span></span>

> <span data-ttu-id="9e773-327">[add_ContentLoading](#add_contentloading)de HRESULT público ([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-327">public HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-328">ContentLoading se activa antes de que se cargue ningún contenido, incluso los scripts agregados con AddScriptToExecuteOnDocumentCreated ContentLoading no se desencadenarán si se realiza una navegación de página (por ejemplo, a través de la navegación de fragmentos o el historial. navegaciones pushState).</span><span class="sxs-lookup"><span data-stu-id="9e773-328">ContentLoading fires before any content is loaded, including scripts added with AddScriptToExecuteOnDocumentCreated ContentLoading will not fire if a same page navigation occurs (such as through fragment navigations or history.pushState navigations).</span></span> <span data-ttu-id="9e773-329">Esto sigue los eventos NavigationStarting y SourceChanged, y precede a los eventos HistoryChanged y NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e773-329">This follows the NavigationStarting and SourceChanged events and precedes the HistoryChanged and NavigationCompleted events.</span></span>

#### <span data-ttu-id="9e773-330">remove_ContentLoading</span><span class="sxs-lookup"><span data-stu-id="9e773-330">remove_ContentLoading</span></span> 

<span data-ttu-id="9e773-331">Quitar un controlador de eventos agregado previamente con add_ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9e773-331">Remove an event handler previously added with add_ContentLoading.</span></span>

> <span data-ttu-id="9e773-332">[remove_ContentLoading](#remove_contentloading)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-332">public HRESULT [remove_ContentLoading](#remove_contentloading)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-333">add_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-333">add_SourceChanged</span></span> 

<span data-ttu-id="9e773-334">SourceChanged se desencadena cuando cambia la propiedad de origen.</span><span class="sxs-lookup"><span data-stu-id="9e773-334">SourceChanged fires when the Source property changes.</span></span>

> <span data-ttu-id="9e773-335">[add_SourceChanged](#add_sourcechanged)de HRESULT público ([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-335">public HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-336">SourceChanged se desencadena para navegar a un sitio diferente o a navegación de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="9e773-336">SourceChanged fires for navigating to a different site or fragment navigations.</span></span> <span data-ttu-id="9e773-337">No se desencadenará para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-337">It will not fires for other types of navigations such as page reloads or history.pushState with the same URL as the current page.</span></span> <span data-ttu-id="9e773-338">SourceChanged se desencadena antes de ContentLoading para la navegación a un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="9e773-338">SourceChanged fires before ContentLoading for navigation to a new document.</span></span> <span data-ttu-id="9e773-339">Agregue un controlador de eventos para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-339">Add an event handler for the SourceChanged event.</span></span> 

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

#### <span data-ttu-id="9e773-340">remove_SourceChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-340">remove_SourceChanged</span></span> 

<span data-ttu-id="9e773-341">Quitar un controlador de eventos agregado previamente con add_SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-341">Remove an event handler previously added with add_SourceChanged.</span></span>

> <span data-ttu-id="9e773-342">[remove_SourceChanged](#remove_sourcechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-342">public HRESULT [remove_SourceChanged](#remove_sourcechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-343">add_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-343">add_HistoryChanged</span></span> 

<span data-ttu-id="9e773-344">Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9e773-344">HistoryChange listen to the change of navigation history for the top level document.</span></span>

> <span data-ttu-id="9e773-345">[add_HistoryChanged](#add_historychanged)de HRESULT público ([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-345">public HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-346">Usa Facturacióncambiar para comprobar si el valor get_CanGoBack/get_CanGoForward ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9e773-346">Use HistoryChange to check if get_CanGoBack/get_CanGoForward value has changed.</span></span> <span data-ttu-id="9e773-347">HistoryChanged también se desencadena para usar GoBack/GoForward.</span><span class="sxs-lookup"><span data-stu-id="9e773-347">HistoryChanged also fires for using GoBack/GoForward.</span></span> <span data-ttu-id="9e773-348">HistoryChanged se desencadena después de SourceChanged y ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9e773-348">HistoryChanged fires after SourceChanged and ContentLoading.</span></span> <span data-ttu-id="9e773-349">Agregue un controlador de eventos para el evento HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-349">Add an event handler for the HistoryChanged event.</span></span> 

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

#### <span data-ttu-id="9e773-350">remove_HistoryChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-350">remove_HistoryChanged</span></span> 

<span data-ttu-id="9e773-351">Quitar un controlador de eventos agregado previamente con add_HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-351">Remove an event handler previously added with add_HistoryChanged.</span></span>

> <span data-ttu-id="9e773-352">[remove_HistoryChanged](#remove_historychanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-352">public HRESULT [remove_HistoryChanged](#remove_historychanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-353">add_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9e773-353">add_NavigationCompleted</span></span> 

<span data-ttu-id="9e773-354">Agregue un controlador de eventos para el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e773-354">Add an event handler for the NavigationCompleted event.</span></span>

> <span data-ttu-id="9e773-355">[add_NavigationCompleted](#add_navigationcompleted)de HRESULT público ([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-355">public HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-356">El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.</span><span class="sxs-lookup"><span data-stu-id="9e773-356">NavigationCompleted event fires when the WebView has completely loaded (body.onload has fired) or loading stopped with error.</span></span>

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

#### <span data-ttu-id="9e773-357">remove_NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="9e773-357">remove_NavigationCompleted</span></span> 

<span data-ttu-id="9e773-358">Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e773-358">Remove an event handler previously added with add_NavigationCompleted.</span></span>

> <span data-ttu-id="9e773-359">[remove_NavigationCompleted](#remove_navigationcompleted)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-359">public HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-360">add_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-360">add_FrameNavigationStarting</span></span> 

<span data-ttu-id="9e773-361">Agregue un controlador de eventos para el evento FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-361">Add an event handler for the FrameNavigationStarting event.</span></span>

> <span data-ttu-id="9e773-362">[add_FrameNavigationStarting](#add_framenavigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-362">public HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-363">FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI.</span><span class="sxs-lookup"><span data-stu-id="9e773-363">FrameNavigationStarting fires when a child frame in the WebView requesting permission to navigate to a different URI.</span></span> <span data-ttu-id="9e773-364">Esto también se activará para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="9e773-364">This will fire for redirects as well.</span></span>

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

#### <span data-ttu-id="9e773-365">remove_FrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="9e773-365">remove_FrameNavigationStarting</span></span> 

<span data-ttu-id="9e773-366">Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9e773-366">Remove an event handler previously added with add_FrameNavigationStarting.</span></span>

> <span data-ttu-id="9e773-367">[remove_FrameNavigationStarting](#remove_framenavigationstarting)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-367">public HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-368">add_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9e773-368">add_ScriptDialogOpening</span></span> 

<span data-ttu-id="9e773-369">Agregue un controlador de eventos para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9e773-369">Add an event handler for the ScriptDialogOpening event.</span></span>

> <span data-ttu-id="9e773-370">[add_ScriptDialogOpening](#add_scriptdialogopening)de HRESULT público ([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-370">public HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-371">El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-371">The event fires when a JavaScript dialog (alert, confirm, or prompt) will show for the webview.</span></span> <span data-ttu-id="9e773-372">Este evento solo se desencadena si la propiedad ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled se establece en false.</span><span class="sxs-lookup"><span data-stu-id="9e773-372">This event only fires if the ICoreWebView2Settings::AreDefaultScriptDialogsEnabled property is set to false.</span></span> <span data-ttu-id="9e773-373">El evento ScriptDialogOpening se puede usar para suprimir cuadros de diálogo o reemplazar los cuadros de diálogo predeterminados con cuadros de diálogo personalizados.</span><span class="sxs-lookup"><span data-stu-id="9e773-373">The ScriptDialogOpening event can be used to suppress dialogs or replace default dialogs with custom dialogs.</span></span>

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

#### <span data-ttu-id="9e773-374">remove_ScriptDialogOpening</span><span class="sxs-lookup"><span data-stu-id="9e773-374">remove_ScriptDialogOpening</span></span> 

<span data-ttu-id="9e773-375">Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9e773-375">Remove an event handler previously added with add_ScriptDialogOpening.</span></span>

> <span data-ttu-id="9e773-376">[remove_ScriptDialogOpening](#remove_scriptdialogopening)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-376">public HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-377">add_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-377">add_PermissionRequested</span></span> 

<span data-ttu-id="9e773-378">Agregue un controlador de eventos para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-378">Add an event handler for the PermissionRequested event.</span></span>

> <span data-ttu-id="9e773-379">[add_PermissionRequested](#add_permissionrequested)de HRESULT público ([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-379">public HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-380">Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="9e773-380">Fires when content in a WebView requests permission to access some privileged resources.</span></span>

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

#### <span data-ttu-id="9e773-381">remove_PermissionRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-381">remove_PermissionRequested</span></span> 

<span data-ttu-id="9e773-382">Quitar un controlador de eventos agregado previamente con add_PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-382">Remove an event handler previously added with add_PermissionRequested.</span></span>

> <span data-ttu-id="9e773-383">[remove_PermissionRequested](#remove_permissionrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-383">public HRESULT [remove_PermissionRequested](#remove_permissionrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-384">add_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9e773-384">add_ProcessFailed</span></span> 

<span data-ttu-id="9e773-385">Agregue un controlador de eventos para el evento ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9e773-385">Add an event handler for the ProcessFailed event.</span></span>

> <span data-ttu-id="9e773-386">[add_ProcessFailed](#add_processfailed)de HRESULT público ([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-386">public HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-387">Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.</span><span class="sxs-lookup"><span data-stu-id="9e773-387">Fires when a WebView process terminated unexpectedly or become unresponsive.</span></span>

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

#### <span data-ttu-id="9e773-388">remove_ProcessFailed</span><span class="sxs-lookup"><span data-stu-id="9e773-388">remove_ProcessFailed</span></span> 

<span data-ttu-id="9e773-389">Quitar un controlador de eventos agregado previamente con add_ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="9e773-389">Remove an event handler previously added with add_ProcessFailed.</span></span>

> <span data-ttu-id="9e773-390">[remove_ProcessFailed](#remove_processfailed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-390">public HRESULT [remove_ProcessFailed](#remove_processfailed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-391">AddScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9e773-391">AddScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="9e773-392">Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.</span><span class="sxs-lookup"><span data-stu-id="9e773-392">Add the provided JavaScript to a list of scripts that should be executed after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is executed.</span></span>

> <span data-ttu-id="9e773-393">[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)de HRESULT público (LPCWSTR JavaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9e773-393">public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR javaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="9e773-394">El script insertado se aplicará a todas las navegaciones del marco secundario y el documento de primer nivel superior hasta que se elimine con RemoveScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="9e773-394">The injected script will apply to all future top level document and child frame navigations until removed with RemoveScriptToExecuteOnDocumentCreated.</span></span> <span data-ttu-id="9e773-395">Esto se aplica de forma asincrónica y debes esperar a que se ejecute el controlador de finalización para poder asegurarte de que el script está listo para ejecutarse en navegaciones futuras.</span><span class="sxs-lookup"><span data-stu-id="9e773-395">This is applied asynchronously and you must wait for the completion handler to run before you can be sure that the script is ready to execute on future navigations.</span></span>

<span data-ttu-id="9e773-396">Tenga en cuenta que si un documento HTML contiene algún tipo de espacio aislado a través de propiedades de [espacio aislado](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) o el [encabezado HTTP de seguridad de contenido](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , esto afectará a la secuencia de comandos que se ejecuta aquí.</span><span class="sxs-lookup"><span data-stu-id="9e773-396">Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here.</span></span> <span data-ttu-id="9e773-397">Así, por ejemplo, si la palabra clave "Allow-modal" no se establece, se omitirán las llamadas a la `alert` función.</span><span class="sxs-lookup"><span data-stu-id="9e773-397">So, for example, if the 'allow-modals' keyword is not set then calls to the `alert` function will be ignored.</span></span>

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

#### <span data-ttu-id="9e773-398">RemoveScriptToExecuteOnDocumentCreated</span><span class="sxs-lookup"><span data-stu-id="9e773-398">RemoveScriptToExecuteOnDocumentCreated</span></span> 

<span data-ttu-id="9e773-399">Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="9e773-399">Remove the corresponding JavaScript added via AddScriptToExecuteOnDocumentCreated.</span></span>

> <span data-ttu-id="9e773-400">HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR ID)</span><span class="sxs-lookup"><span data-stu-id="9e773-400">public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR id)</span></span>

#### <span data-ttu-id="9e773-401">ExecuteScript</span><span class="sxs-lookup"><span data-stu-id="9e773-401">ExecuteScript</span></span> 

<span data-ttu-id="9e773-402">Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-402">Execute JavaScript code from the javascript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="9e773-403">[ExecuteScript](#executescript)de HRESULT público (LPCWSTR JavaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9e773-403">public HRESULT [ExecuteScript](#executescript)(LPCWSTR javaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="9e773-404">Esto se ejecutará de forma asincrónica y cuando se complete, si se proporciona un controlador en el parámetro ExecuteScriptCompletedHandler, se llamará a su método Invoke con el resultado de evaluar el JavaScript proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9e773-404">This will execute asynchronously and when complete, if a handler is provided in the ExecuteScriptCompletedHandler parameter, its Invoke method will be called with the result of evaluating the provided JavaScript.</span></span> <span data-ttu-id="9e773-405">El valor del resultado es una cadena codificada por JSON.</span><span class="sxs-lookup"><span data-stu-id="9e773-405">The result value is a JSON encoded string.</span></span> <span data-ttu-id="9e773-406">Si el resultado es no definido, contiene un ciclo de referencia o, de lo contrario, no se puede codificar en JSON, el valor de JSON NULL se devolverá como la cadena "null".</span><span class="sxs-lookup"><span data-stu-id="9e773-406">If the result is undefined, contains a reference cycle, or otherwise cannot be encoded into JSON, the JSON null value will be returned as the string 'null'.</span></span> <span data-ttu-id="9e773-407">Observe que una función que no tiene ningún valor explícito devuelto devuelve undefined.</span><span class="sxs-lookup"><span data-stu-id="9e773-407">Note that a function that has no explicit return value returns undefined.</span></span> <span data-ttu-id="9e773-408">Si el script ejecutado inicia una excepción no controlada, el resultado es también ' null '.</span><span class="sxs-lookup"><span data-stu-id="9e773-408">If the executed script throws an unhandled exception, then the result is also 'null'.</span></span> <span data-ttu-id="9e773-409">Este método se aplica de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9e773-409">This method is applied asynchronously.</span></span> <span data-ttu-id="9e773-410">Si la llamada se realiza mientras la vista en la vista previa está en un documento y se realiza una navegación después de que se realiza la llamada, pero antes de que se ejecute JavaScript, no se ejecutará el script y se llamará al controlador con E_FAIL para su parámetro errorCode.</span><span class="sxs-lookup"><span data-stu-id="9e773-410">If the call is made while the webview is on one document, and a navigation occurs after the call is made but before the JavaScript is executed, then the script will not be executed and the handler will be called with E_FAIL for its errorCode parameter.</span></span> <span data-ttu-id="9e773-411">ExecuteScript funcionará incluso si IsScriptEnabled se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="9e773-411">ExecuteScript will work even if IsScriptEnabled is set to FALSE.</span></span>

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

#### <span data-ttu-id="9e773-412">CapturePreview</span><span class="sxs-lookup"><span data-stu-id="9e773-412">CapturePreview</span></span> 

<span data-ttu-id="9e773-413">Capture una imagen de lo que se muestra en la vista de página.</span><span class="sxs-lookup"><span data-stu-id="9e773-413">Capture an image of what WebView is displaying.</span></span>

> <span data-ttu-id="9e773-414">[CAPTUREPREVIEW](#capturepreview)HRESULT público ([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9e773-414">public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) imageFormat,IStream \* imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="9e773-415">Especifique el formato de la imagen con el parámetro imageFormat.</span><span class="sxs-lookup"><span data-stu-id="9e773-415">Specify the format of the image with the imageFormat parameter.</span></span> <span data-ttu-id="9e773-416">Los datos binarios de la imagen resultantes se escriben en el parámetro imageStream proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9e773-416">The resulting image binary data is written to the provided imageStream parameter.</span></span> <span data-ttu-id="9e773-417">Cuando CapturePreview termina de escribir en la secuencia, se llama al método Invoke del parámetro handler proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9e773-417">When CapturePreview finishes writing to the stream, the Invoke method on the provided handler parameter is called.</span></span>

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

#### <span data-ttu-id="9e773-418">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="9e773-418">Reload</span></span> 

<span data-ttu-id="9e773-419">Volver a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-419">Reload the current page.</span></span>

> <span data-ttu-id="9e773-420">[recarga](#reload)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="9e773-420">public HRESULT [Reload](#reload)()</span></span>

<span data-ttu-id="9e773-421">Esto es similar a desplazarse hasta el URI del documento de nivel superior actual, incluidos todos los eventos de navegación que desencadenan y respetan cualquier entrada de la caché HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e773-421">This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache.</span></span> <span data-ttu-id="9e773-422">Sin embargo, el historial de atrás y reenvío no se modificará.</span><span class="sxs-lookup"><span data-stu-id="9e773-422">But, the back/forward history will not be modified.</span></span>

#### <span data-ttu-id="9e773-423">PostWebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="9e773-423">PostWebMessageAsJson</span></span> 

<span data-ttu-id="9e773-424">Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-424">Post the specified webMessage to the top level document in this WebView.</span></span>

> <span data-ttu-id="9e773-425">HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="9e773-425">public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)</span></span>

<span data-ttu-id="9e773-426">Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9e773-426">The top level document's window.chrome.webview's message event fires.</span></span> <span data-ttu-id="9e773-427">JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9e773-427">JavaScript in that document may subscribe and unsubscribe to the event via the following:</span></span> 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 <span data-ttu-id="9e773-428">El argumentos del evento es una instancia de `MessageEvent` .</span><span class="sxs-lookup"><span data-stu-id="9e773-428">The event args is an instance of `MessageEvent`.</span></span> <span data-ttu-id="9e773-429">La opción ICoreWebView2Settings:: IsWebMessageEnabled debe ser true o este método dará un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="9e773-429">The ICoreWebView2Settings::IsWebMessageEnabled setting must be true or this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="9e773-430">La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-430">The event arg's data property is the webMessage string parameter parsed as a JSON string into a JavaScript object.</span></span> <span data-ttu-id="9e773-431">La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto.</span><span class="sxs-lookup"><span data-stu-id="9e773-431">The event arg's source property is a reference to the `window.chrome.webview` object.</span></span> <span data-ttu-id="9e773-432">Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host.</span><span class="sxs-lookup"><span data-stu-id="9e773-432">See SetWebMessageReceivedEventHandler for information on sending messages from the HTML document in the webview to the host.</span></span> <span data-ttu-id="9e773-433">Este mensaje se envía de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9e773-433">This message is sent asynchronously.</span></span> <span data-ttu-id="9e773-434">Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e773-434">If a navigation occurs before the message is posted to the page, then the message will not be sent.</span></span>

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

#### <span data-ttu-id="9e773-435">PostWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="9e773-435">PostWebMessageAsString</span></span> 

<span data-ttu-id="9e773-436">Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-436">This is a helper for posting a message that is a simple string rather than a JSON string representation of a JavaScript object.</span></span>

> <span data-ttu-id="9e773-437">HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="9e773-437">public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)</span></span>

<span data-ttu-id="9e773-438">Esto se comporta exactamente de la misma manera que PostWebMessageAsJson, pero la `window.chrome.webview` propiedad data del argumento de evento de mensaje será una cadena con el mismo valor que webMessageAsString.</span><span class="sxs-lookup"><span data-stu-id="9e773-438">This behaves in exactly the same manner as PostWebMessageAsJson but the `window.chrome.webview` message event arg's data property will be a string with the same value as webMessageAsString.</span></span> <span data-ttu-id="9e773-439">Use este en lugar de PostWebMessageAsJson si desea comunicarse a través de cadenas simples en lugar de objetos JSON.</span><span class="sxs-lookup"><span data-stu-id="9e773-439">Use this instead of PostWebMessageAsJson if you want to communicate via simple strings rather than JSON objects.</span></span>

#### <span data-ttu-id="9e773-440">add_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9e773-440">add_WebMessageReceived</span></span> 

<span data-ttu-id="9e773-441">Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="9e773-441">This event fires when the IsWebMessageEnabled setting is set and the top level document of the webview calls `window.chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="9e773-442">[add_WebMessageReceived](#add_webmessagereceived)pública HRESULT (controlador[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-442">public HRESULT [add_WebMessageReceived](#add_webmessagereceived)([ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-443">La función postmensaje es `void postMessage(object)` donde objeto es cualquier objeto compatible con la conversión de JSON.</span><span class="sxs-lookup"><span data-stu-id="9e773-443">The postMessage function is `void postMessage(object)` where object is any object supported by JSON conversion.</span></span>

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

 <span data-ttu-id="9e773-444">Cuando se llama a PostMessage, se invocará el [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) establecido a través de este método SetWebMessageReceivedEventHandler con el parámetro de objeto PostMessage convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="9e773-444">When postMessage is called, the [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) set via this SetWebMessageReceivedEventHandler method will be invoked with the postMessage's object parameter converted to a JSON string.</span></span>

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

#### <span data-ttu-id="9e773-445">remove_WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="9e773-445">remove_WebMessageReceived</span></span> 

<span data-ttu-id="9e773-446">Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="9e773-446">Remove an event handler previously added with add_WebMessageReceived.</span></span>

> <span data-ttu-id="9e773-447">[remove_WebMessageReceived](#remove_webmessagereceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-447">public HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-448">CallDevToolsProtocolMethod</span><span class="sxs-lookup"><span data-stu-id="9e773-448">CallDevToolsProtocolMethod</span></span> 

<span data-ttu-id="9e773-449">Llama a un método DevToolsProtocol asincrónico.</span><span class="sxs-lookup"><span data-stu-id="9e773-449">Call an asynchronous DevToolsProtocol method.</span></span>

> <span data-ttu-id="9e773-450">HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR NOMBREDEMÉTODO, LPCWSTR ParametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span><span class="sxs-lookup"><span data-stu-id="9e773-450">public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR methodName,LPCWSTR parametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="9e773-451">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles.</span><span class="sxs-lookup"><span data-stu-id="9e773-451">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list and description of available methods.</span></span> <span data-ttu-id="9e773-452">El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` .</span><span class="sxs-lookup"><span data-stu-id="9e773-452">The methodName parameter is the full name of the method in the format `{domain}.{method}`.</span></span> <span data-ttu-id="9e773-453">El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e773-453">The parametersAsJson parameter is a JSON formatted string containing the parameters for the corresponding method.</span></span> <span data-ttu-id="9e773-454">Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9e773-454">The handler's Invoke method will be called when the method asynchronously completes.</span></span> <span data-ttu-id="9e773-455">Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="9e773-455">Invoke will be called with the method's return object as a JSON string.</span></span>

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

#### <span data-ttu-id="9e773-456">get_BrowserProcessId</span><span class="sxs-lookup"><span data-stu-id="9e773-456">get_BrowserProcessId</span></span> 

<span data-ttu-id="9e773-457">El identificador de proceso del proceso del explorador que hospeda la vista Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-457">The process id of the browser process that hosts the WebView.</span></span>

> <span data-ttu-id="9e773-458">[get_BrowserProcessId](#get_browserprocessid)de HRESULT público (UINT32 \* Value)</span><span class="sxs-lookup"><span data-stu-id="9e773-458">public HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 \* value)</span></span>

#### <span data-ttu-id="9e773-459">get_CanGoBack</span><span class="sxs-lookup"><span data-stu-id="9e773-459">get_CanGoBack</span></span> 

<span data-ttu-id="9e773-460">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-460">Returns true if the webview can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="9e773-461">[get_CanGoBack](#get_cangoback)de HRESULT público (bool \* CanGoBack)</span><span class="sxs-lookup"><span data-stu-id="9e773-461">public HRESULT [get_CanGoBack](#get_cangoback)(BOOL \* canGoBack)</span></span>

<span data-ttu-id="9e773-462">El evento HistoryChanged se activará si get_CanGoBack cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="9e773-462">The HistoryChanged event will fire if get_CanGoBack changes value.</span></span>

#### <span data-ttu-id="9e773-463">get_CanGoForward</span><span class="sxs-lookup"><span data-stu-id="9e773-463">get_CanGoForward</span></span> 

<span data-ttu-id="9e773-464">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-464">Returns true if the webview can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="9e773-465">[get_CanGoForward](#get_cangoforward)de HRESULT público (bool \* CanGoForward)</span><span class="sxs-lookup"><span data-stu-id="9e773-465">public HRESULT [get_CanGoForward](#get_cangoforward)(BOOL \* canGoForward)</span></span>

<span data-ttu-id="9e773-466">El evento HistoryChanged se activará si get_CanGoForward cambia el valor.</span><span class="sxs-lookup"><span data-stu-id="9e773-466">The HistoryChanged event will fire if get_CanGoForward changes value.</span></span>

#### <span data-ttu-id="9e773-467">GoBack</span><span class="sxs-lookup"><span data-stu-id="9e773-467">GoBack</span></span> 

<span data-ttu-id="9e773-468">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-468">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="9e773-469">HRESULT público [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="9e773-469">public HRESULT [GoBack](#goback)()</span></span>

#### <span data-ttu-id="9e773-470">GoForward</span><span class="sxs-lookup"><span data-stu-id="9e773-470">GoForward</span></span> 

<span data-ttu-id="9e773-471">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="9e773-471">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="9e773-472">[HRESULT público](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="9e773-472">public HRESULT [GoForward](#goforward)()</span></span>

#### <span data-ttu-id="9e773-473">GetDevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="9e773-473">GetDevToolsProtocolEventReceiver</span></span> 

<span data-ttu-id="9e773-474">Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.</span><span class="sxs-lookup"><span data-stu-id="9e773-474">Get a DevTools Protocol event receiver that allows you to subscribe to a DevTools Protocol event.</span></span>

> <span data-ttu-id="9e773-475">HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \* \* Receiver)</span><span class="sxs-lookup"><span data-stu-id="9e773-475">public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) \*\* receiver)</span></span>

<span data-ttu-id="9e773-476">El parámetro eventName es el nombre completo del evento en el formato `{domain}.{event}` .</span><span class="sxs-lookup"><span data-stu-id="9e773-476">The eventName parameter is the full name of the event in the format `{domain}.{event}`.</span></span> <span data-ttu-id="9e773-477">Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista de los eventos de protocolo DevTools Descripción y los argumentos del evento.</span><span class="sxs-lookup"><span data-stu-id="9e773-477">See the [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs) for a list of DevTools Protocol events description, and event args.</span></span>

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

#### <span data-ttu-id="9e773-478">Detener</span><span class="sxs-lookup"><span data-stu-id="9e773-478">Stop</span></span> 

<span data-ttu-id="9e773-479">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="9e773-479">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="9e773-480">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="9e773-480">public HRESULT [Stop](#stop)()</span></span>

<span data-ttu-id="9e773-481">No detiene las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="9e773-481">Does not stop scripts.</span></span>

#### <span data-ttu-id="9e773-482">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-482">add_NewWindowRequested</span></span> 

<span data-ttu-id="9e773-483">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-483">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="9e773-484">[add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-484">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-485">Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.</span><span class="sxs-lookup"><span data-stu-id="9e773-485">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="9e773-486">La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.</span><span class="sxs-lookup"><span data-stu-id="9e773-486">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="9e773-487">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-487">remove_NewWindowRequested</span></span> 

<span data-ttu-id="9e773-488">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-488">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="9e773-489">[remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-489">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-490">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-490">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="9e773-491">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-491">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="9e773-492">[add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-492">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-493">El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9e773-493">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="9e773-494">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-494">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="9e773-495">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="9e773-495">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="9e773-496">[remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-496">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-497">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="9e773-497">get_DocumentTitle</span></span> 

<span data-ttu-id="9e773-498">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="9e773-498">The title for the current top level document.</span></span>

> <span data-ttu-id="9e773-499">[get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="9e773-499">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="9e773-500">Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="9e773-500">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

#### <span data-ttu-id="9e773-501">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="9e773-501">AddRemoteObject</span></span> 

<span data-ttu-id="9e773-502">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="9e773-502">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="9e773-503">[ADDREMOTEOBJECT](#addremoteobject)HRESULT público (LPCWSTR Name, Variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="9e773-503">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="9e773-504">Los objetos de host se exponen como proxies de objetos remotos a través de `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="9e773-504">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="9e773-505">Los proxies de objetos remotos son promesas y se resolverán como un objeto que represente el objeto de host.</span><span class="sxs-lookup"><span data-stu-id="9e773-505">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="9e773-506">La promesa se rechaza si la aplicación no ha agregado un objeto con el nombre.</span><span class="sxs-lookup"><span data-stu-id="9e773-506">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="9e773-507">Cuando el código de JavaScript tiene acceso a una propiedad o método del objeto, se devuelve una promesa, que se resolverá con el valor devuelto por el host para la propiedad o el método, o se rechazará en caso de error, como no se trata de una propiedad o método en el objeto o los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="9e773-507">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="9e773-508">Por ejemplo, cuando el código de la aplicación hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9e773-508">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="9e773-509">El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="9e773-509">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="9e773-510">Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant.</span><span class="sxs-lookup"><span data-stu-id="9e773-510">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="9e773-511">Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="9e773-511">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="9e773-512">El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId.</span><span class="sxs-lookup"><span data-stu-id="9e773-512">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="9e773-513">Las matrices anidadas se admiten hasta una profundidad de 3.</span><span class="sxs-lookup"><span data-stu-id="9e773-513">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="9e773-514">No se admiten las matrices de los tipos de referencia.</span><span class="sxs-lookup"><span data-stu-id="9e773-514">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="9e773-515">VT_EMPTY y VT_NULL se asignan a JavaScript como null.</span><span class="sxs-lookup"><span data-stu-id="9e773-515">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="9e773-516">En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="9e773-516">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="9e773-517">Además, todos los objetos remotos se exponen como `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="9e773-517">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="9e773-518">Aquí los objetos host se exponen como proxies de objetos remotos sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="9e773-518">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="9e773-519">No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host.</span><span class="sxs-lookup"><span data-stu-id="9e773-519">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="9e773-520">Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.remoteObjects.<name>` descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9e773-520">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="9e773-521">Los proxies de objetos remotos sincrónicos y los proxies asincrónicos de objetos remotos pueden tener como proxy el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="9e773-521">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="9e773-522">Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto remoto, ya sean otros servidores proxy, sincrónicos o asíncronos.</span><span class="sxs-lookup"><span data-stu-id="9e773-522">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="9e773-523">Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-523">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="9e773-524">Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="9e773-524">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="9e773-525">Los proxies de objetos remotos son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method.</span><span class="sxs-lookup"><span data-stu-id="9e773-525">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="9e773-526">Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local.</span><span class="sxs-lookup"><span data-stu-id="9e773-526">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="9e773-527">Además, cualquier propiedad o método de la matriz se `chrome.webview.remoteObjects.options.forceLocalProperties` ejecutará de forma local.</span><span class="sxs-lookup"><span data-stu-id="9e773-527">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="9e773-528">De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="9e773-528">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="9e773-529">Puede agregar más a esta matriz, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9e773-529">You can add more to this array as required.</span></span>

<span data-ttu-id="9e773-530">Hay un método que puede resultar `chrome.webview.remoteObjects.cleanupSome` más conveniente para la recolección de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="9e773-530">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="9e773-531">Los proxies de objetos remotos también tienen los siguientes métodos que se ejecutan de forma local:</span><span class="sxs-lookup"><span data-stu-id="9e773-531">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="9e773-532">applyRemote, getRemote, setRemote: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="9e773-532">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="9e773-533">Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto.</span><span class="sxs-lookup"><span data-stu-id="9e773-533">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="9e773-534">Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy.</span><span class="sxs-lookup"><span data-stu-id="9e773-534">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="9e773-535">Pero `proxy.applyRemote('toString')` se ejecuta `toString` en el objeto remoto a través del proxy.</span><span class="sxs-lookup"><span data-stu-id="9e773-535">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="9e773-536">getLocal, setLocal: realizar obtención de propiedad o conjunto de propiedades de forma local.</span><span class="sxs-lookup"><span data-stu-id="9e773-536">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="9e773-537">Puede usar estos métodos para forzar o establecer una propiedad en el proxy del objeto remoto, en lugar de hacerlo en el objeto remoto al que representa.</span><span class="sxs-lookup"><span data-stu-id="9e773-537">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="9e773-538">Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto remoto a través del proxy.</span><span class="sxs-lookup"><span data-stu-id="9e773-538">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="9e773-539">Pero `proxy.getLocal('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="9e773-539">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="9e773-540">sincronizar: los proxies de objetos remotos asincrónicos exponen un método de sincronización que devuelve una promesa de un proxy de objetos remotos sincrónico para el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="9e773-540">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="9e773-541">Por ejemplo, `chrome.webview.remoteObjects.sample.methodCall()` devuelve un proxy asincrónico de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="9e773-541">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="9e773-542">Puede usar el `sync` método para obtener un proxy de objetos remotos sincrónico en su lugar:</span><span class="sxs-lookup"><span data-stu-id="9e773-542">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="9e773-543">Async: los proxies de objetos remotos sincrónicos exponen un método Async que bloquea y devuelve un proxy de objetos remotos asincrónicos para el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="9e773-543">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="9e773-544">Por ejemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` devuelve un proxy de objeto remoto sincrónico.</span><span class="sxs-lookup"><span data-stu-id="9e773-544">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="9e773-545">Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto remoto asincrónico para el mismo objeto remoto:</span><span class="sxs-lookup"><span data-stu-id="9e773-545">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="9e773-546">después: los proxies de objetos remotos asincrónicos tienen un método then.</span><span class="sxs-lookup"><span data-stu-id="9e773-546">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="9e773-547">Esto permite que sean esperados.</span><span class="sxs-lookup"><span data-stu-id="9e773-547">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="9e773-548">devolverá una promesa que se resolverá con una representación del objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="9e773-548">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="9e773-549">Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local.</span><span class="sxs-lookup"><span data-stu-id="9e773-549">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="9e773-550">Si el proxy representa una función, se devuelve un proxy que no es de espera.</span><span class="sxs-lookup"><span data-stu-id="9e773-550">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="9e773-551">Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como proxy de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="9e773-551">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="9e773-552">Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota.</span><span class="sxs-lookup"><span data-stu-id="9e773-552">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="9e773-553">Los proxies de objetos remotos asincrónicos devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9e773-553">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="9e773-554">La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación.</span><span class="sxs-lookup"><span data-stu-id="9e773-554">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="9e773-555">Los proxy de objetos remotos sincrónicos funcionan de manera similar pero bloquean la ejecución remota y esperan a que se complete la operación remota.</span><span class="sxs-lookup"><span data-stu-id="9e773-555">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="9e773-556">Establecer una propiedad en un proxy de objetos remotos asincrónicos funciona de forma ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="9e773-556">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="9e773-557">El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá.</span><span class="sxs-lookup"><span data-stu-id="9e773-557">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="9e773-558">Este es un requisito del objeto proxy de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-558">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="9e773-559">Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setRemote que devuelve una promesa según se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9e773-559">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="9e773-560">La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9e773-560">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="9e773-561">Por ejemplo, supongamos que tiene un objeto COM con la siguiente interfaz</span><span class="sxs-lookup"><span data-stu-id="9e773-561">For example, suppose you have a COM object with the following interface</span></span>

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

 <span data-ttu-id="9e773-562">Podemos añadir una instancia de esta interfaz a nuestro JavaScript con `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="9e773-562">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="9e773-563">En este caso, lo hemos denominado `sample` :</span><span class="sxs-lookup"><span data-stu-id="9e773-563">In this case we name it `sample`:</span></span>

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

 <span data-ttu-id="9e773-564">A continuación, en el documento HTML podemos usar este objeto COM mediante `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="9e773-564">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

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

#### <span data-ttu-id="9e773-565">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="9e773-565">RemoveRemoteObject</span></span> 

<span data-ttu-id="9e773-566">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="9e773-566">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="9e773-567">[REMOVEREMOTEOBJECT](#removeremoteobject)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="9e773-567">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="9e773-568">Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="9e773-568">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="9e773-569">Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.</span><span class="sxs-lookup"><span data-stu-id="9e773-569">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="9e773-570">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="9e773-570">OpenDevToolsWindow</span></span> 

<span data-ttu-id="9e773-571">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="9e773-571">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="9e773-572">[OPENDEVTOOLSWINDOW](#opendevtoolswindow)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="9e773-572">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="9e773-573">No hace nada si se llama cuando la ventana de DevTools ya está abierta</span><span class="sxs-lookup"><span data-stu-id="9e773-573">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="9e773-574">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-574">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="9e773-575">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="9e773-575">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="9e773-576">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-576">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-577">Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9e773-577">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="9e773-578">Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9e773-578">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="9e773-579">El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.</span><span class="sxs-lookup"><span data-stu-id="9e773-579">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="9e773-580">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="9e773-580">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="9e773-581">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e773-581">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="9e773-582">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-582">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-583">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="9e773-583">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="9e773-584">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9e773-584">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="9e773-585">[get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="9e773-585">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="9e773-586">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-586">add_WebResourceRequested</span></span> 

<span data-ttu-id="9e773-587">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-587">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="9e773-588">[add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-588">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-589">Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="9e773-589">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="9e773-590">Debe agregar al menos un filtro para que se active el evento.</span><span class="sxs-lookup"><span data-stu-id="9e773-590">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="9e773-591">remove_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-591">remove_WebResourceRequested</span></span> 

<span data-ttu-id="9e773-592">Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-592">Remove an event handler previously added with add_WebResourceRequested.</span></span>

> <span data-ttu-id="9e773-593">[remove_WebResourceRequested](#remove_webresourcerequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-593">public HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-594">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9e773-594">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="9e773-595">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-595">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="9e773-596">[ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="9e773-596">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="9e773-597">El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno).</span><span class="sxs-lookup"><span data-stu-id="9e773-597">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="9e773-598">nullptr es equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="9e773-598">nullptr is equivalent to L"".</span></span> <span data-ttu-id="9e773-599">Consulta CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e773-599">See CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="9e773-600">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="9e773-600">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="9e773-601">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-601">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="9e773-602">[REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="9e773-602">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="9e773-603">Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="9e773-603">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="9e773-604">Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="9e773-604">Returns E_INVALIDARG for a filter that was never added.</span></span>

#### <span data-ttu-id="9e773-605">add_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-605">add_WindowCloseRequested</span></span> 

<span data-ttu-id="9e773-606">Agregue un controlador de eventos para el evento WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-606">Add an event handler for the WindowCloseRequested event.</span></span>

> <span data-ttu-id="9e773-607">[add_WindowCloseRequested](#add_windowcloserequested)de HRESULT público ([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="9e773-607">public HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="9e773-608">Se desencadena cuando el contenido de la vista en WebView solicita cerrar la ventana, por ejemplo, después de que se llame a Window. Close.</span><span class="sxs-lookup"><span data-stu-id="9e773-608">Fires when content inside the WebView requested to close the window, such as after window.close is called.</span></span> <span data-ttu-id="9e773-609">La aplicación debe cerrar la ventana de WebView y de la aplicación relacionada si eso tiene sentido para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9e773-609">The app should close the WebView and related app window if that makes sense to the app.</span></span>

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

#### <span data-ttu-id="9e773-610">remove_WindowCloseRequested</span><span class="sxs-lookup"><span data-stu-id="9e773-610">remove_WindowCloseRequested</span></span> 

<span data-ttu-id="9e773-611">Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.</span><span class="sxs-lookup"><span data-stu-id="9e773-611">Remove an event handler previously added with add_WindowCloseRequested.</span></span>

> <span data-ttu-id="9e773-612">[remove_WindowCloseRequested](#remove_windowcloserequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="9e773-612">public HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="9e773-613">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span><span class="sxs-lookup"><span data-stu-id="9e773-613">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT</span></span> 

<span data-ttu-id="9e773-614">Formato de imagen usado por el método ICoreWebView2:: CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="9e773-614">Image format used by the ICoreWebView2::CapturePreview method.</span></span>

> <span data-ttu-id="9e773-615">[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) enum</span><span class="sxs-lookup"><span data-stu-id="9e773-615">enum [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)</span></span>

 <span data-ttu-id="9e773-616">Los</span><span class="sxs-lookup"><span data-stu-id="9e773-616">Values</span></span>                         | <span data-ttu-id="9e773-617">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-617">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9e773-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span><span class="sxs-lookup"><span data-stu-id="9e773-618">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG</span></span>            | <span data-ttu-id="9e773-619">Formato de imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="9e773-619">PNG image format.</span></span>
<span data-ttu-id="9e773-620">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span><span class="sxs-lookup"><span data-stu-id="9e773-620">CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG</span></span>            | <span data-ttu-id="9e773-621">Formato de imagen JPEG.</span><span class="sxs-lookup"><span data-stu-id="9e773-621">JPEG image format.</span></span>

#### <span data-ttu-id="9e773-622">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span><span class="sxs-lookup"><span data-stu-id="9e773-622">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND</span></span> 

<span data-ttu-id="9e773-623">Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9e773-623">Kind of JavaScript dialog used in the ICoreWebView2ScriptDialogOpeningEventHandler interface.</span></span>

> <span data-ttu-id="9e773-624">[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) enum</span><span class="sxs-lookup"><span data-stu-id="9e773-624">enum [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)</span></span>

 <span data-ttu-id="9e773-625">Los</span><span class="sxs-lookup"><span data-stu-id="9e773-625">Values</span></span>                         | <span data-ttu-id="9e773-626">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-626">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9e773-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span><span class="sxs-lookup"><span data-stu-id="9e773-627">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT</span></span>            | <span data-ttu-id="9e773-628">Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.</span><span class="sxs-lookup"><span data-stu-id="9e773-628">A dialog invoked via the window.alert JavaScript function.</span></span>
<span data-ttu-id="9e773-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span><span class="sxs-lookup"><span data-stu-id="9e773-629">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM</span></span>            | <span data-ttu-id="9e773-630">Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-630">A dialog invoked via the window.confirm JavaScript function.</span></span>
<span data-ttu-id="9e773-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span><span class="sxs-lookup"><span data-stu-id="9e773-631">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT</span></span>            | <span data-ttu-id="9e773-632">Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-632">A dialog invoked via the window.prompt JavaScript function.</span></span>
<span data-ttu-id="9e773-633">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span><span class="sxs-lookup"><span data-stu-id="9e773-633">CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD</span></span>            | <span data-ttu-id="9e773-634">Un cuadro de diálogo invocado a través del evento beforeunload de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9e773-634">A dialog invoked via the beforeunload JavaScript event.</span></span>

#### <span data-ttu-id="9e773-635">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span><span class="sxs-lookup"><span data-stu-id="9e773-635">CORE_WEBVIEW2_PROCESS_FAILED_KIND</span></span> 

<span data-ttu-id="9e773-636">Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.</span><span class="sxs-lookup"><span data-stu-id="9e773-636">Kind of process failure used in the ICoreWebView2ProcessFailedEventHandler interface.</span></span>

> <span data-ttu-id="9e773-637">[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) enum</span><span class="sxs-lookup"><span data-stu-id="9e773-637">enum [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)</span></span>

 <span data-ttu-id="9e773-638">Los</span><span class="sxs-lookup"><span data-stu-id="9e773-638">Values</span></span>                         | <span data-ttu-id="9e773-639">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-639">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9e773-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="9e773-640">CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED</span></span>            | <span data-ttu-id="9e773-641">Indica que el proceso del explorador ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="9e773-641">Indicates the browser process terminated unexpectedly.</span></span>
<span data-ttu-id="9e773-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span><span class="sxs-lookup"><span data-stu-id="9e773-642">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED</span></span>            | <span data-ttu-id="9e773-643">Indica que el proceso de representación ha terminado de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="9e773-643">Indicates the render process terminated unexpectedly.</span></span>
<span data-ttu-id="9e773-644">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span><span class="sxs-lookup"><span data-stu-id="9e773-644">CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE</span></span>            | <span data-ttu-id="9e773-645">Indica que el proceso de representación deja de responder.</span><span class="sxs-lookup"><span data-stu-id="9e773-645">Indicates the render process becomes unresponsive.</span></span>

#### <span data-ttu-id="9e773-646">CORE_WEBVIEW2_PERMISSION_KIND</span><span class="sxs-lookup"><span data-stu-id="9e773-646">CORE_WEBVIEW2_PERMISSION_KIND</span></span> 

<span data-ttu-id="9e773-647">El tipo de una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9e773-647">The type of a permission request.</span></span>

> <span data-ttu-id="9e773-648">[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) enum</span><span class="sxs-lookup"><span data-stu-id="9e773-648">enum [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)</span></span>

 <span data-ttu-id="9e773-649">Los</span><span class="sxs-lookup"><span data-stu-id="9e773-649">Values</span></span>                         | <span data-ttu-id="9e773-650">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-650">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9e773-651">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="9e773-651">CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION</span></span>            | <span data-ttu-id="9e773-652">Permiso desconocido.</span><span class="sxs-lookup"><span data-stu-id="9e773-652">Unknown permission.</span></span>
<span data-ttu-id="9e773-653">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span><span class="sxs-lookup"><span data-stu-id="9e773-653">CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE</span></span>            | <span data-ttu-id="9e773-654">Permiso para capturar audio.</span><span class="sxs-lookup"><span data-stu-id="9e773-654">Permission to capture audio.</span></span>
<span data-ttu-id="9e773-655">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span><span class="sxs-lookup"><span data-stu-id="9e773-655">CORE_WEBVIEW2_PERMISSION_KIND_CAMERA</span></span>            | <span data-ttu-id="9e773-656">Permiso para capturar video.</span><span class="sxs-lookup"><span data-stu-id="9e773-656">Permission to capture video.</span></span>
<span data-ttu-id="9e773-657">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span><span class="sxs-lookup"><span data-stu-id="9e773-657">CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION</span></span>            | <span data-ttu-id="9e773-658">Permiso para acceder a la ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="9e773-658">Permission to access geolocation.</span></span>
<span data-ttu-id="9e773-659">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="9e773-659">CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS</span></span>            | <span data-ttu-id="9e773-660">Permiso para enviar notificaciones Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-660">Permission to send web notifications.</span></span>
<span data-ttu-id="9e773-661">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span><span class="sxs-lookup"><span data-stu-id="9e773-661">CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS</span></span>            | <span data-ttu-id="9e773-662">Permiso para acceder al sensor genérico.</span><span class="sxs-lookup"><span data-stu-id="9e773-662">Permission to access generic sensor.</span></span>
<span data-ttu-id="9e773-663">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span><span class="sxs-lookup"><span data-stu-id="9e773-663">CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ</span></span>            | <span data-ttu-id="9e773-664">Permiso para leer el Portapapeles del sistema sin un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="9e773-664">Permission to read system clipboard without a user gesture.</span></span>

#### <span data-ttu-id="9e773-665">CORE_WEBVIEW2_PERMISSION_STATE</span><span class="sxs-lookup"><span data-stu-id="9e773-665">CORE_WEBVIEW2_PERMISSION_STATE</span></span> 

<span data-ttu-id="9e773-666">Respuesta a una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9e773-666">Response to a permission request.</span></span>

> <span data-ttu-id="9e773-667">[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) enum</span><span class="sxs-lookup"><span data-stu-id="9e773-667">enum [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)</span></span>

 <span data-ttu-id="9e773-668">Los</span><span class="sxs-lookup"><span data-stu-id="9e773-668">Values</span></span>                         | <span data-ttu-id="9e773-669">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-669">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9e773-670">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="9e773-670">CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT</span></span>            | <span data-ttu-id="9e773-671">Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.</span><span class="sxs-lookup"><span data-stu-id="9e773-671">Use default browser behavior, which normally prompt users for decision.</span></span>
<span data-ttu-id="9e773-672">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span><span class="sxs-lookup"><span data-stu-id="9e773-672">CORE_WEBVIEW2_PERMISSION_STATE_ALLOW</span></span>            | <span data-ttu-id="9e773-673">Otorgue la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9e773-673">Grant the permission request.</span></span>
<span data-ttu-id="9e773-674">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span><span class="sxs-lookup"><span data-stu-id="9e773-674">CORE_WEBVIEW2_PERMISSION_STATE_DENY</span></span>            | <span data-ttu-id="9e773-675">Denegar la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="9e773-675">Deny the permission request.</span></span>

#### <span data-ttu-id="9e773-676">CORE_WEBVIEW2_WEB_ERROR_STATUS</span><span class="sxs-lookup"><span data-stu-id="9e773-676">CORE_WEBVIEW2_WEB_ERROR_STATUS</span></span> 

<span data-ttu-id="9e773-677">Valores de estado de error para navegaciones Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-677">Error status values for web navigations.</span></span>

> <span data-ttu-id="9e773-678">[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) enum</span><span class="sxs-lookup"><span data-stu-id="9e773-678">enum [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)</span></span>

 <span data-ttu-id="9e773-679">Los</span><span class="sxs-lookup"><span data-stu-id="9e773-679">Values</span></span>                         | <span data-ttu-id="9e773-680">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-680">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9e773-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="9e773-681">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN</span></span>            | <span data-ttu-id="9e773-682">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="9e773-682">An unknown error occurred.</span></span>
<span data-ttu-id="9e773-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span><span class="sxs-lookup"><span data-stu-id="9e773-683">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT</span></span>            | <span data-ttu-id="9e773-684">El nombre común del certificado SSL no coincide con la dirección Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-684">The SSL certificate common name does not match the web address.</span></span>
<span data-ttu-id="9e773-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span><span class="sxs-lookup"><span data-stu-id="9e773-685">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED</span></span>            | <span data-ttu-id="9e773-686">El certificado SSL ha expirado.</span><span class="sxs-lookup"><span data-stu-id="9e773-686">The SSL certificate has expired.</span></span>
<span data-ttu-id="9e773-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9e773-687">CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS</span></span>            | <span data-ttu-id="9e773-688">El certificado de cliente SSL contiene errores.</span><span class="sxs-lookup"><span data-stu-id="9e773-688">The SSL client certificate contains errors.</span></span>
<span data-ttu-id="9e773-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span><span class="sxs-lookup"><span data-stu-id="9e773-689">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED</span></span>            | <span data-ttu-id="9e773-690">El certificado SSL ha sido revocado.</span><span class="sxs-lookup"><span data-stu-id="9e773-690">The SSL certificate has been revoked.</span></span>
<span data-ttu-id="9e773-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span><span class="sxs-lookup"><span data-stu-id="9e773-691">CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID</span></span>            | <span data-ttu-id="9e773-692">El certificado SSL no es válido &ndash; esto puede significar que el certificado no coincide con los pin de clave pública del nombre de host, que el certificado está firmado por una autoridad que no es de confianza o con un algoritmo de signo débil. el certificado alegó que los nombres DNS han infringido las restricciones de nombres, el certificado contiene una clave débil, el período de validez del certificado es demasiado largo, falta de información de revocación o de mecanismo de revocación, nombre de host no único, falta de información de transparencia del certificado o el certificado está encadenado a una [raíz de Symantec heredado](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span><span class="sxs-lookup"><span data-stu-id="9e773-692">The SSL certificate is invalid &ndash; this could mean the certificate did not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the certificate's validity period is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).</span></span>
<span data-ttu-id="9e773-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span><span class="sxs-lookup"><span data-stu-id="9e773-693">CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE</span></span>            | <span data-ttu-id="9e773-694">No se puede comunicar con el host.</span><span class="sxs-lookup"><span data-stu-id="9e773-694">The host is unreachable.</span></span>
<span data-ttu-id="9e773-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9e773-695">CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT</span></span>            | <span data-ttu-id="9e773-696">Se agotó el tiempo de espera de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9e773-696">The connection has timed out.</span></span>
<span data-ttu-id="9e773-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span><span class="sxs-lookup"><span data-stu-id="9e773-697">CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE</span></span>            | <span data-ttu-id="9e773-698">El servidor ha devuelto una respuesta no válida o no reconocida.</span><span class="sxs-lookup"><span data-stu-id="9e773-698">The server returned an invalid or unrecognized response.</span></span>
<span data-ttu-id="9e773-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span><span class="sxs-lookup"><span data-stu-id="9e773-699">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED</span></span>            | <span data-ttu-id="9e773-700">La conexión ha sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="9e773-700">The connection was aborted.</span></span>
<span data-ttu-id="9e773-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span><span class="sxs-lookup"><span data-stu-id="9e773-701">CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET</span></span>            | <span data-ttu-id="9e773-702">Se restableció la conexión.</span><span class="sxs-lookup"><span data-stu-id="9e773-702">The connection was reset.</span></span>
<span data-ttu-id="9e773-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span><span class="sxs-lookup"><span data-stu-id="9e773-703">CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED</span></span>            | <span data-ttu-id="9e773-704">Se perdió la conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="9e773-704">The Internet connection has been lost.</span></span>
<span data-ttu-id="9e773-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span><span class="sxs-lookup"><span data-stu-id="9e773-705">CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT</span></span>            | <span data-ttu-id="9e773-706">No se puede conectar al destino.</span><span class="sxs-lookup"><span data-stu-id="9e773-706">Cannot connect to destination.</span></span>
<span data-ttu-id="9e773-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="9e773-707">CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED</span></span>            | <span data-ttu-id="9e773-708">No se pudo resolver el nombre de host proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9e773-708">Could not resolve provided host name.</span></span>
<span data-ttu-id="9e773-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span><span class="sxs-lookup"><span data-stu-id="9e773-709">CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED</span></span>            | <span data-ttu-id="9e773-710">Se canceló la operación.</span><span class="sxs-lookup"><span data-stu-id="9e773-710">The operation was canceled.</span></span>
<span data-ttu-id="9e773-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span><span class="sxs-lookup"><span data-stu-id="9e773-711">CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED</span></span>            | <span data-ttu-id="9e773-712">Error en la redirección de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e773-712">The request redirect failed.</span></span>
<span data-ttu-id="9e773-713">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span><span class="sxs-lookup"><span data-stu-id="9e773-713">CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR</span></span>            | <span data-ttu-id="9e773-714">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="9e773-714">An unexpected error occurred.</span></span>

#### <span data-ttu-id="9e773-715">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="9e773-715">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT</span></span> 

<span data-ttu-id="9e773-716">Enumeración de contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-716">Enum for web resource request contexts.</span></span>

> <span data-ttu-id="9e773-717">[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) enum</span><span class="sxs-lookup"><span data-stu-id="9e773-717">enum [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)</span></span>

 <span data-ttu-id="9e773-718">Los</span><span class="sxs-lookup"><span data-stu-id="9e773-718">Values</span></span>                         | <span data-ttu-id="9e773-719">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9e773-719">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="9e773-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span><span class="sxs-lookup"><span data-stu-id="9e773-720">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL</span></span>            | <span data-ttu-id="9e773-721">Todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="9e773-721">All resources.</span></span>
<span data-ttu-id="9e773-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="9e773-722">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT</span></span>            | <span data-ttu-id="9e773-723">Recursos de documentos.</span><span class="sxs-lookup"><span data-stu-id="9e773-723">Document resources.</span></span>
<span data-ttu-id="9e773-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span><span class="sxs-lookup"><span data-stu-id="9e773-724">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET</span></span>            | <span data-ttu-id="9e773-725">Recursos de CSS.</span><span class="sxs-lookup"><span data-stu-id="9e773-725">CSS resources.</span></span>
<span data-ttu-id="9e773-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span><span class="sxs-lookup"><span data-stu-id="9e773-726">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE</span></span>            | <span data-ttu-id="9e773-727">Recursos de imagen.</span><span class="sxs-lookup"><span data-stu-id="9e773-727">Image resources.</span></span>
<span data-ttu-id="9e773-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span><span class="sxs-lookup"><span data-stu-id="9e773-728">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA</span></span>            | <span data-ttu-id="9e773-729">Otros recursos multimedia, como los vídeos.</span><span class="sxs-lookup"><span data-stu-id="9e773-729">Other media resources such as videos.</span></span>
<span data-ttu-id="9e773-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span><span class="sxs-lookup"><span data-stu-id="9e773-730">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT</span></span>            | <span data-ttu-id="9e773-731">Recursos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9e773-731">Font resources.</span></span>
<span data-ttu-id="9e773-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="9e773-732">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT</span></span>            | <span data-ttu-id="9e773-733">Recursos de script.</span><span class="sxs-lookup"><span data-stu-id="9e773-733">Script resources.</span></span>
<span data-ttu-id="9e773-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="9e773-734">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST</span></span>            | <span data-ttu-id="9e773-735">Solicitudes XML HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e773-735">XML HTTP requests.</span></span>
<span data-ttu-id="9e773-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span><span class="sxs-lookup"><span data-stu-id="9e773-736">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH</span></span>            | <span data-ttu-id="9e773-737">Capture la comunicación de la API.</span><span class="sxs-lookup"><span data-stu-id="9e773-737">Fetch API communication.</span></span>
<span data-ttu-id="9e773-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span><span class="sxs-lookup"><span data-stu-id="9e773-738">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK</span></span>            | <span data-ttu-id="9e773-739">Recursos de TextTrack.</span><span class="sxs-lookup"><span data-stu-id="9e773-739">TextTrack resources.</span></span>
<span data-ttu-id="9e773-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span><span class="sxs-lookup"><span data-stu-id="9e773-740">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE</span></span>            | <span data-ttu-id="9e773-741">Comunicación de la API de EventSource.</span><span class="sxs-lookup"><span data-stu-id="9e773-741">EventSource API communication.</span></span>
<span data-ttu-id="9e773-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span><span class="sxs-lookup"><span data-stu-id="9e773-742">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET</span></span>            | <span data-ttu-id="9e773-743">Comunicación de API WebSocket.</span><span class="sxs-lookup"><span data-stu-id="9e773-743">WebSocket API communication.</span></span>
<span data-ttu-id="9e773-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span><span class="sxs-lookup"><span data-stu-id="9e773-744">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST</span></span>            | <span data-ttu-id="9e773-745">Manifiestos de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="9e773-745">Web App Manifests.</span></span>
<span data-ttu-id="9e773-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span><span class="sxs-lookup"><span data-stu-id="9e773-746">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE</span></span>            | <span data-ttu-id="9e773-747">Intercambio de HTTP firmado.</span><span class="sxs-lookup"><span data-stu-id="9e773-747">Signed HTTP Exchanges.</span></span>
<span data-ttu-id="9e773-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span><span class="sxs-lookup"><span data-stu-id="9e773-748">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING</span></span>            | <span data-ttu-id="9e773-749">Solicitudes de ping.</span><span class="sxs-lookup"><span data-stu-id="9e773-749">Ping requests.</span></span>
<span data-ttu-id="9e773-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span><span class="sxs-lookup"><span data-stu-id="9e773-750">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT</span></span>            | <span data-ttu-id="9e773-751">Informes de violación de CSP.</span><span class="sxs-lookup"><span data-stu-id="9e773-751">CSP Violation Reports.</span></span>
<span data-ttu-id="9e773-752">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span><span class="sxs-lookup"><span data-stu-id="9e773-752">CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER</span></span>            | <span data-ttu-id="9e773-753">Otros recursos.</span><span class="sxs-lookup"><span data-stu-id="9e773-753">Other resources.</span></span>
