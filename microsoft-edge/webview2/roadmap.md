---
description: Obtenga información sobre lo que viene a continuación para WebView2
title: Guía básica para Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: 7b67e4a6844ead0f845667a70df8657745ece938
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643423"
---
# <a name="microsoft-edge-webview2-roadmap"></a><span data-ttu-id="d36ca-104">Microsoft Edge Guía básica de WebView2</span><span class="sxs-lookup"><span data-stu-id="d36ca-104">Microsoft Edge WebView2 roadmap</span></span>  

> [!NOTE]
> <span data-ttu-id="d36ca-105">Last Updated: July 2021</span><span class="sxs-lookup"><span data-stu-id="d36ca-105">Last Updated:  July 2021</span></span>  

<span data-ttu-id="d36ca-106">El control WebView2 permite a los desarrolladores insertar tecnologías web en sus aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="d36ca-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="d36ca-107">En la página siguiente se describe el plan de ruta posible para WebView2.</span><span class="sxs-lookup"><span data-stu-id="d36ca-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="d36ca-108">WebView2 está en desarrollo activo y la hoja de ruta sigue evolucionando en función de los cambios del mercado y los comentarios de los clientes, por lo que tenga en cuenta que los planes descritos aquí no son exhaustivos y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="d36ca-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="d36ca-109">Si tiene dudas o dudas sobre la guía básica, proporcione sus comentarios en el repositorio [de comentarios][GithubMicrosoftedgeWebviewfeedbackMain].</span><span class="sxs-lookup"><span data-stu-id="d36ca-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="d36ca-110">El equipo de WebView2 está planeando los siguientes esfuerzos principales para futuras actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="d36ca-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

* <span data-ttu-id="d36ca-111">Vista previa de UWP</span><span class="sxs-lookup"><span data-stu-id="d36ca-111">UWP Preview</span></span>
* <span data-ttu-id="d36ca-112">Vista previa de MacOS</span><span class="sxs-lookup"><span data-stu-id="d36ca-112">MacOS Preview</span></span>
* <span data-ttu-id="d36ca-113">Xbox Preview</span><span class="sxs-lookup"><span data-stu-id="d36ca-113">Xbox Preview</span></span>
* <span data-ttu-id="d36ca-114">HoloLens Vista previa</span><span class="sxs-lookup"><span data-stu-id="d36ca-114">HoloLens Preview</span></span>

## <a name="webview2-runtime-and-installer"></a><span data-ttu-id="d36ca-115">WebView2 Runtime and Installer</span><span class="sxs-lookup"><span data-stu-id="d36ca-115">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="d36ca-116">[El modelo de distribución Evergreen][ConceptDistributionEvergreenModel] permite dirigir o encadenar la instalación de WebView2 Runtime en la máquina del usuario.</span><span class="sxs-lookup"><span data-stu-id="d36ca-116">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="d36ca-117">El tiempo de ejecución e instalador de Evergreen WebView2 ha alcanzado la disponibilidad general \(GA\).</span><span class="sxs-lookup"><span data-stu-id="d36ca-117">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <a name="fixed-version"></a><span data-ttu-id="d36ca-118">Versión fija</span><span class="sxs-lookup"><span data-stu-id="d36ca-118">Fixed version</span></span>  

<span data-ttu-id="d36ca-119">[El modelo de distribución de versiones][ConceptsDistributionFixedVersionModel] fijas permite empaquetar los archivos binarios Microsoft Edge dentro de la aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="d36ca-119">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="d36ca-120">La versión fija ha alcanzado la disponibilidad general \(GA\).</span><span class="sxs-lookup"><span data-stu-id="d36ca-120">The Fixed Version has reached General Availability \(GA\).</span></span>  

## <a name="general-availability"></a><span data-ttu-id="d36ca-121">Disponibilidad general</span><span class="sxs-lookup"><span data-stu-id="d36ca-121">General availability</span></span>  

### <a name="win32-cc"></a><span data-ttu-id="d36ca-122">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="d36ca-122">Win32 C/C++</span></span>  

<span data-ttu-id="d36ca-123">El SDK de C/C++ de Win32 ha llegado a GA.</span><span class="sxs-lookup"><span data-stu-id="d36ca-123">The Win32 C/C++ SDK has reached GA.</span></span>  

### <a name="net"></a><span data-ttu-id="d36ca-124">.NET</span><span class="sxs-lookup"><span data-stu-id="d36ca-124">.NET</span></span>  

<span data-ttu-id="d36ca-125">El SDK de .NET ha llegado a GA.</span><span class="sxs-lookup"><span data-stu-id="d36ca-125">The .NET SDK has reached GA.</span></span> 

### <a name="windows-ui-library-3"></a><span data-ttu-id="d36ca-126">Windows Biblioteca de interfaz de usuario 3</span><span class="sxs-lookup"><span data-stu-id="d36ca-126">Windows UI Library 3</span></span>

<span data-ttu-id="d36ca-127">Puedes tener acceso a los controles WebView2 en tus aplicaciones mediante [Windows ui library 3 (WinUI3)][UwpToolkitsWinui3Index] con el SDK Windows app.</span><span class="sxs-lookup"><span data-stu-id="d36ca-127">You can access WebView2 controls in your applications using [Windows UI Library 3 (WinUI3)][UwpToolkitsWinui3Index] with the Windows App SDK.</span></span> <span data-ttu-id="d36ca-128">Esto se encuentra actualmente en versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="d36ca-128">This is currently in preview.</span></span> <span data-ttu-id="d36ca-129">Para obtener más información, vaya a la [guía básica Windows SDK de aplicaciones.][WindowsAppSDK|::ref1::|]</span><span class="sxs-lookup"><span data-stu-id="d36ca-129">For more information, navigate to the [Windows App SDK roadmap][WindowsAppSDK|::ref1::|].</span></span>

 
<!-- links -->  

[WindowsAppSDKRoadmap]: https://github.com/microsoft/WindowsAppSDK/blob/main/docs/roadmap.md "Guía básica"
[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribución evergreen: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribución de versiones fijas: distribución de aplicaciones con WebView2 | Microsoft Docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows Biblioteca de interfaz de usuario 3.0 Versión preliminar 1 (mayo de 2020) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Guía básica de la biblioteca de la interfaz de usuario: microsoft/microsoft-ui-xaml | GitHub"  
