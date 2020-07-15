---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core Reference
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 32092f4b434506229ffdd3612a68725b67f566a8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879978"
---
# <span data-ttu-id="9685f-104">0-9-515 - Referencia (WebView2)</span><span class="sxs-lookup"><span data-stu-id="9685f-104">0-9-515 - Reference (WebView2)</span></span>  

> [!NOTE]
> <span data-ttu-id="9685f-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="9685f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="9685f-106">Consulta la referencia de la [API de WebView2](../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9685f-106">Please refer to [WebView2 API reference](../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="9685f-107">El control Microsoft Edge WebView2 permite hospedar contenido web en tu aplicación con [Microsoft Edge \ (cromo \)](https://www.microsoftedgeinsider.com) como motor de representación.</span><span class="sxs-lookup"><span data-stu-id="9685f-107">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="9685f-108">Para obtener más información, vea [información general sobre Microsoft Edge WebView2](../../index.md)) y [Cómo comenzar a usar WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="9685f-108">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="9685f-109">[Microsoft. Web. WebView2. Core. CoreWebView2](0-9-515/microsoft-web-webview2-core-corewebview2.md) es un buen lugar para comenzar a conocer los detalles de la API.</span><span class="sxs-lookup"><span data-stu-id="9685f-109">[Microsoft.Web.WebView2.Core.CoreWebView2](0-9-515/microsoft-web-webview2-core-corewebview2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="9685f-110">Microsoft. Web. WebView2. Core</span><span class="sxs-lookup"><span data-stu-id="9685f-110">Microsoft.Web.WebView2.Core</span></span>
*   <span data-ttu-id="9685f-111">Espacio de nombres [Microsoft. Web. WebView2. Core](0-9-515/namespace-microsoft-web-webview2-core.md)</span><span class="sxs-lookup"><span data-stu-id="9685f-111">[Microsoft.Web.WebView2.Core](0-9-515/namespace-microsoft-web-webview2-core.md) namespace</span></span>
*   [<span data-ttu-id="9685f-112">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="9685f-112">CoreWebView2</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2.md)
*   [<span data-ttu-id="9685f-113">CoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="9685f-113">CoreWebView2Controller</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2controller.md)
*   [<span data-ttu-id="9685f-114">CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="9685f-114">CoreWebView2Deferral</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2deferral.md)
*   [<span data-ttu-id="9685f-115">CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="9685f-115">CoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceiver.md)
*   [<span data-ttu-id="9685f-116">CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="9685f-116">CoreWebView2Environment</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2environment.md)
*   [<span data-ttu-id="9685f-117">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="9685f-117">CoreWebView2EnvironmentOptions</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md)
*   [<span data-ttu-id="9685f-118">CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="9685f-118">CoreWebView2PhysicalKeyStatus</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2physicalkeystatus.md)
*   [<span data-ttu-id="9685f-119">CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="9685f-119">CoreWebView2Settings</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2settings.md)
*   [<span data-ttu-id="9685f-120">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="9685f-120">EdgeNotFoundException</span></span>](0-9-515/microsoft-web-webview2-core-edgenotfoundexception.md)

### <span data-ttu-id="9685f-121">Argumentos de evento</span><span class="sxs-lookup"><span data-stu-id="9685f-121">Event arguments</span></span>

*   [<span data-ttu-id="9685f-122">CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-122">CoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md)
*   [<span data-ttu-id="9685f-123">CoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-123">CoreWebView2ContentLoadingEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2contentloadingeventargs.md)
*   [<span data-ttu-id="9685f-124">CoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-124">CoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [<span data-ttu-id="9685f-125">CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-125">CoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md)
*   [<span data-ttu-id="9685f-126">CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-126">CoreWebView2NavigationCompletedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)
*   [<span data-ttu-id="9685f-127">CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-127">CoreWebView2NavigationStartingEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)
*   [<span data-ttu-id="9685f-128">CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-128">CoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2newwindowrequestedeventargs.md)
*   [<span data-ttu-id="9685f-129">CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-129">CoreWebView2PermissionRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2permissionrequestedeventargs.md)
*   [<span data-ttu-id="9685f-130">CoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-130">CoreWebView2ProcessFailedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2processfailedeventargs.md)
*   [<span data-ttu-id="9685f-131">CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-131">CoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2scriptdialogopeningeventargs.md)
*   [<span data-ttu-id="9685f-132">CoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-132">CoreWebView2SourceChangedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2sourcechangedeventargs.md)
*   [<span data-ttu-id="9685f-133">CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-133">CoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2webmessagereceivedeventargs.md)
*   [<span data-ttu-id="9685f-134">CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9685f-134">CoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-515/microsoft-web-webview2-core-corewebview2webresourcerequestedeventargs.md)
