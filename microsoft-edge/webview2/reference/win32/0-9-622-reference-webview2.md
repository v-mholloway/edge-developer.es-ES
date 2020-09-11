---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 C++ de Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 4b4d6079bf893dc160e95f26839e66e477dd70bd
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012709"
---
# <span data-ttu-id="2be67-104">Referencia (WebView2 Win32 C++)</span><span class="sxs-lookup"><span data-stu-id="2be67-104">Reference (WebView2 Win32 C++)</span></span>  

<span data-ttu-id="2be67-105">El control Microsoft Edge WebView2 permite hospedar contenido web en tu aplicación con [Microsoft Edge \ (cromo \)](https://www.microsoftedgeinsider.com) como motor de representación.</span><span class="sxs-lookup"><span data-stu-id="2be67-105">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="2be67-106">Para obtener más información, vea [información general sobre Microsoft Edge WebView2](../../index.md)) y [Cómo comenzar a usar WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="2be67-106">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="2be67-107">[ICoreWebView2](0-9-538/ICoreWebView2.md) es un buen lugar para comenzar a conocer los detalles de la API.</span><span class="sxs-lookup"><span data-stu-id="2be67-107">[ICoreWebView2](0-9-538/ICoreWebView2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="2be67-108">Global</span><span class="sxs-lookup"><span data-stu-id="2be67-108">Globals</span></span>  

*   [<span data-ttu-id="2be67-109">Global</span><span class="sxs-lookup"><span data-stu-id="2be67-109">Globals</span></span>](0-9-622/webview2-idl.md)  

## <span data-ttu-id="2be67-110">Interactúa</span><span class="sxs-lookup"><span data-stu-id="2be67-110">Interfaces</span></span>  
*   [<span data-ttu-id="2be67-111">ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="2be67-111">ICoreWebView2</span></span>](0-9-622/icorewebview2.md)
*   [<span data-ttu-id="2be67-112">ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="2be67-112">ICoreWebView2Controller</span></span>](0-9-622/icorewebview2controller.md)
*   [<span data-ttu-id="2be67-113">ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="2be67-113">ICoreWebView2Deferral</span></span>](0-9-622/icorewebview2deferral.md)
*   [<span data-ttu-id="2be67-114">ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="2be67-114">ICoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-622/icorewebview2devtoolsprotocoleventreceiver.md)
*   [<span data-ttu-id="2be67-115">ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="2be67-115">ICoreWebView2Environment</span></span>](0-9-622/icorewebview2environment.md)
*   [<span data-ttu-id="2be67-116">ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="2be67-116">ICoreWebView2EnvironmentOptions</span></span>](0-9-622/icorewebview2environmentoptions.md)
*   [<span data-ttu-id="2be67-117">ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="2be67-117">ICoreWebView2HttpHeadersCollectionIterator</span></span>](0-9-622/icorewebview2httpheaderscollectioniterator.md)
*   [<span data-ttu-id="2be67-118">ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="2be67-118">ICoreWebView2HttpRequestHeaders</span></span>](0-9-622/icorewebview2httprequestheaders.md)
*   [<span data-ttu-id="2be67-119">ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="2be67-119">ICoreWebView2HttpResponseHeaders</span></span>](0-9-622/icorewebview2httpresponseheaders.md)
*   [<span data-ttu-id="2be67-120">ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="2be67-120">ICoreWebView2Settings</span></span>](0-9-622/icorewebview2settings.md)
*   [<span data-ttu-id="2be67-121">ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="2be67-121">ICoreWebView2WebResourceRequest</span></span>](0-9-622/icorewebview2webresourcerequest.md)
*   [<span data-ttu-id="2be67-122">ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="2be67-122">ICoreWebView2WebResourceResponse</span></span>](0-9-622/icorewebview2webresourceresponse.md)
*   [<span data-ttu-id="2be67-123">ICoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="2be67-123">ICoreWebView2WindowFeatures</span></span>](0-9-622/icorewebview2windowfeatures.md)

### <span data-ttu-id="2be67-124">Argumentos de evento</span><span class="sxs-lookup"><span data-stu-id="2be67-124">Event arguments</span></span>

*   [<span data-ttu-id="2be67-125">ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-125">ICoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-622/icorewebview2acceleratorkeypressedeventargs.md)
*   [<span data-ttu-id="2be67-126">ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-126">ICoreWebView2ContentLoadingEventArgs</span></span>](0-9-622/icorewebview2contentloadingeventargs.md)
*   [<span data-ttu-id="2be67-127">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-127">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-622/icorewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [<span data-ttu-id="2be67-128">ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-128">ICoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-622/icorewebview2movefocusrequestedeventargs.md)
*   [<span data-ttu-id="2be67-129">ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-129">ICoreWebView2NavigationCompletedEventArgs</span></span>](0-9-622/icorewebview2navigationcompletedeventargs.md)
*   [<span data-ttu-id="2be67-130">ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-130">ICoreWebView2NavigationStartingEventArgs</span></span>](0-9-622/icorewebview2navigationstartingeventargs.md)
*   [<span data-ttu-id="2be67-131">ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-131">ICoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-622/icorewebview2newwindowrequestedeventargs.md)
*   [<span data-ttu-id="2be67-132">ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-132">ICoreWebView2PermissionRequestedEventArgs</span></span>](0-9-622/icorewebview2permissionrequestedeventargs.md)
*   [<span data-ttu-id="2be67-133">ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-133">ICoreWebView2ProcessFailedEventArgs</span></span>](0-9-622/icorewebview2processfailedeventargs.md)
*   [<span data-ttu-id="2be67-134">ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-134">ICoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-622/icorewebview2scriptdialogopeningeventargs.md)
*   [<span data-ttu-id="2be67-135">ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-135">ICoreWebView2SourceChangedEventArgs</span></span>](0-9-622/icorewebview2sourcechangedeventargs.md)
*   [<span data-ttu-id="2be67-136">ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-136">ICoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-622/icorewebview2webmessagereceivedeventargs.md)
*   [<span data-ttu-id="2be67-137">ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-137">ICoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-622/icorewebview2webresourcerequestedeventargs.md)

### <span data-ttu-id="2be67-138">Delegados</span><span class="sxs-lookup"><span data-stu-id="2be67-138">Delegates</span></span>

*   [<span data-ttu-id="2be67-139">ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-139">ICoreWebView2AcceleratorKeyPressedEventHandler</span></span>](0-9-622/icorewebview2acceleratorkeypressedeventhandler.md)
*   [<span data-ttu-id="2be67-140">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-140">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-9-622/icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md)
*   [<span data-ttu-id="2be67-141">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-141">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-9-622/icorewebview2calldevtoolsprotocolmethodcompletedhandler.md)
*   [<span data-ttu-id="2be67-142">ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-142">ICoreWebView2CapturePreviewCompletedHandler</span></span>](0-9-622/icorewebview2capturepreviewcompletedhandler.md)
*   [<span data-ttu-id="2be67-143">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-143">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-9-622/icorewebview2containsfullscreenelementchangedeventhandler.md)
*   [<span data-ttu-id="2be67-144">ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-144">ICoreWebView2ContentLoadingEventHandler</span></span>](0-9-622/icorewebview2contentloadingeventhandler.md)
*   [<span data-ttu-id="2be67-145">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-145">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span>](0-9-622/icorewebview2createcorewebview2controllercompletedhandler.md)
*   [<span data-ttu-id="2be67-146">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-146">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span>](0-9-622/icorewebview2createcorewebview2environmentcompletedhandler.md)
*   [<span data-ttu-id="2be67-147">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-147">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-9-622/icorewebview2devtoolsprotocoleventreceivedeventhandler.md)
*   [<span data-ttu-id="2be67-148">ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-148">ICoreWebView2DocumentTitleChangedEventHandler</span></span>](0-9-622/icorewebview2documenttitlechangedeventhandler.md)
*   [<span data-ttu-id="2be67-149">ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-149">ICoreWebView2ExecuteScriptCompletedHandler</span></span>](0-9-622/icorewebview2executescriptcompletedhandler.md)
*   [<span data-ttu-id="2be67-150">ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-150">ICoreWebView2FocusChangedEventHandler</span></span>](0-9-622/icorewebview2focuschangedeventhandler.md)
*   [<span data-ttu-id="2be67-151">ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-151">ICoreWebView2HistoryChangedEventHandler</span></span>](0-9-622/icorewebview2historychangedeventhandler.md)
*   [<span data-ttu-id="2be67-152">ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-152">ICoreWebView2MoveFocusRequestedEventHandler</span></span>](0-9-622/icorewebview2movefocusrequestedeventhandler.md)
*   [<span data-ttu-id="2be67-153">ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-153">ICoreWebView2NavigationCompletedEventHandler</span></span>](0-9-622/icorewebview2navigationcompletedeventhandler.md)
*   [<span data-ttu-id="2be67-154">ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-154">ICoreWebView2NavigationStartingEventHandler</span></span>](0-9-622/icorewebview2navigationstartingeventhandler.md)
*   [<span data-ttu-id="2be67-155">ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-155">ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span>](0-9-622/icorewebview2newbrowserversionavailableeventhandler.md)
*   [<span data-ttu-id="2be67-156">ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-156">ICoreWebView2NewWindowRequestedEventHandler</span></span>](0-9-622/icorewebview2newwindowrequestedeventhandler.md)
*   [<span data-ttu-id="2be67-157">ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-157">ICoreWebView2PermissionRequestedEventHandler</span></span>](0-9-622/icorewebview2permissionrequestedeventhandler.md)
*   [<span data-ttu-id="2be67-158">ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-158">ICoreWebView2ProcessFailedEventHandler</span></span>](0-9-622/icorewebview2processfailedeventhandler.md)
*   [<span data-ttu-id="2be67-159">ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-159">ICoreWebView2ScriptDialogOpeningEventHandler</span></span>](0-9-622/icorewebview2scriptdialogopeningeventhandler.md)
*   [<span data-ttu-id="2be67-160">ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-160">ICoreWebView2SourceChangedEventHandler</span></span>](0-9-622/icorewebview2sourcechangedeventhandler.md)
*   [<span data-ttu-id="2be67-161">ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-161">ICoreWebView2WebMessageReceivedEventHandler</span></span>](0-9-622/icorewebview2webmessagereceivedeventhandler.md)
*   [<span data-ttu-id="2be67-162">ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-162">ICoreWebView2WebResourceRequestedEventHandler</span></span>](0-9-622/icorewebview2webresourcerequestedeventhandler.md)
*   [<span data-ttu-id="2be67-163">ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-163">ICoreWebView2WindowCloseRequestedEventHandler</span></span>](0-9-622/icorewebview2windowcloserequestedeventhandler.md)
*   [<span data-ttu-id="2be67-164">ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-164">ICoreWebView2ZoomFactorChangedEventHandler</span></span>](0-9-622/icorewebview2zoomfactorchangedeventhandler.md)

### <span data-ttu-id="2be67-165">Experimental</span><span class="sxs-lookup"><span data-stu-id="2be67-165">Experimental</span></span>

*   [<span data-ttu-id="2be67-166">ICoreWebView2Experimental</span><span class="sxs-lookup"><span data-stu-id="2be67-166">ICoreWebView2Experimental</span></span>](0-9-622/icorewebview2experimental.md)
*   [<span data-ttu-id="2be67-167">ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="2be67-167">ICoreWebView2ExperimentalCompositionController</span></span>](0-9-622/icorewebview2experimentalcompositioncontroller.md)
*   [<span data-ttu-id="2be67-168">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-168">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span>](0-9-622/icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md)
*   [<span data-ttu-id="2be67-169">ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-169">ICoreWebView2ExperimentalCursorChangedEventHandler</span></span>](0-9-622/icorewebview2experimentalcursorchangedeventhandler.md)
*   [<span data-ttu-id="2be67-170">ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="2be67-170">ICoreWebView2ExperimentalEnvironment</span></span>](0-9-622/icorewebview2experimentalenvironment.md)
*   [<span data-ttu-id="2be67-171">ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="2be67-171">ICoreWebView2ExperimentalPointerInfo</span></span>](0-9-622/icorewebview2experimentalpointerinfo.md)
*   [<span data-ttu-id="2be67-172">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2be67-172">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span>](0-9-622/icorewebview2experimentalwebresourceresponsereceivedeventargs.md)
*   [<span data-ttu-id="2be67-173">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-173">ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span>](0-9-622/icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md)
*   [<span data-ttu-id="2be67-174">ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2be67-174">ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span>](0-9-622/icorewebview2experimentalwebresourceresponsereceivedeventhandler.md)
