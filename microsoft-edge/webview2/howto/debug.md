---
description: Más información sobre cómo depurar controles WebView2.
title: Depurar WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 7e3ee11de443713a14684023fcd90de3cb1d265a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697752"
---
# <span data-ttu-id="201f8-104">Cómo depurar al desarrollar con controles WebView2</span><span class="sxs-lookup"><span data-stu-id="201f8-104">How to debug when developing with WebView2 controls</span></span>  

<span data-ttu-id="201f8-105">El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características de desarrollo de aplicaciones nativas y Web y las herramientas de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="201f8-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="201f8-106">En este artículo se describen las distintas herramientas que se deben usar al desarrollar con controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="201f8-106">This article outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="201f8-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="201f8-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="201f8-108">Use [las herramientas de desarrollador de Microsoft Edge (cromo)](/microsoft-edge/devtools-guide-chromium) para depurar contenido web que se muestra en controles WebView2, de la misma manera que si estuviera usando Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="201f8-108">Use [Microsoft Edge (Chromium) Developer Tools](/microsoft-edge/devtools-guide-chromium) to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="201f8-109">Para abrir la DevTools, establezca el foco en la ventana WebView y, a continuación, use cualquiera de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="201f8-109">To open the DevTools, set focus on the WebView window and then use any of the following options.</span></span>  
*   <span data-ttu-id="201f8-110">Seleccione `F12` .</span><span class="sxs-lookup"><span data-stu-id="201f8-110">Select `F12`.</span></span>  
*   <span data-ttu-id="201f8-111">Seleccione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="201f8-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="201f8-112">Abra el menú contextual \ (haga clic con el botón derecho \) > seleccione `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="201f8-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   <span data-ttu-id="201f8-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="201f8-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="201f8-115">Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="201f8-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="201f8-116">Use `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar esta situación.</span><span class="sxs-lookup"><span data-stu-id="201f8-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid this situation.</span></span>  

## <span data-ttu-id="201f8-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="201f8-117">Visual Studio</span></span>  

<span data-ttu-id="201f8-118">Use el depurador de scripts en Visual Studio 2019 versión 16,4 Preview 2 o una versión posterior para depurar el script en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="201f8-118">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="201f8-119">Compruebe que el componente **diagnóstico de JavaScript** en **desarrollo de escritorio con** la carga de trabajo de C++ está instalado.</span><span class="sxs-lookup"><span data-stu-id="201f8-119">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnósticos de JavaScript de Visual Studio":::
   <span data-ttu-id="201f8-121">Diagnósticos de JavaScript de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="201f8-121">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="201f8-122">Para habilitar la depuración de scripts WebView2, abra el menú contextual \ (haga clic con el botón derecho \) en el proyecto > seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="201f8-122">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  <span data-ttu-id="201f8-123">En **propiedades de configuración**, seleccione **depuración**.</span><span class="sxs-lookup"><span data-stu-id="201f8-123">On **Configuration Properties**, select **Debugging**.</span></span>  <span data-ttu-id="201f8-124">En la propiedad **tipo de depuración** , elija **JavaScript (WebView2)** de la lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="201f8-124">On the **Debugger Type** property, choose **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador de JavaScript de Visual Studio":::
   <span data-ttu-id="201f8-126">Depurador de JavaScript de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="201f8-126">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## <span data-ttu-id="201f8-127">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="201f8-127">Visual Studio Code</span></span>  

<span data-ttu-id="201f8-128">Puede usar código de Visual Studio para depurar scripts que se ejecutan en controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="201f8-128">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="201f8-129">Para obtener más información, consulte [aplicaciones de WebView de Microsoft Edge (cromo)](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span><span class="sxs-lookup"><span data-stu-id="201f8-129">For more information, see [Microsoft Edge (Chromium) WebView Applications](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="201f8-130">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="201f8-130">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="201f8-131">Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.</span><span class="sxs-lookup"><span data-stu-id="201f8-131">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="201f8-132">Visita el [repositorio de comentarios](https://aka.ms/webviewfeedback) para enviar solicitudes de características o informes de errores.</span><span class="sxs-lookup"><span data-stu-id="201f8-132">Visit the [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  
