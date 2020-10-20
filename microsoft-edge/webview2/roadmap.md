---
description: Más información sobre lo que viene a continuación para WebView2
title: Guía básica para la vista de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 52a2f6d9ef3447955554a5507c3eaab39e6b6a9e
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120371"
---
# <span data-ttu-id="41d6e-104">Guía básica de WebView2 de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41d6e-104">Microsoft Edge WebView2 roadmap</span></span>  

##### <span data-ttu-id="41d6e-105">Última actualización: 2020 de octubre</span><span class="sxs-lookup"><span data-stu-id="41d6e-105">Last Updated: Oct 2020</span></span>  

<span data-ttu-id="41d6e-106">El control WebView2 permite a los programadores incrustar tecnologías web en sus aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="41d6e-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="41d6e-107">En la siguiente página se describe la guía básica para WebView2.</span><span class="sxs-lookup"><span data-stu-id="41d6e-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="41d6e-108">WebView2 está en desarrollo activo y el plan continúa evolucionando en función de los cambios en el mercado y los comentarios de los clientes, por lo que tenga en cuenta que los planes resaltados aquí no son exhaustivos y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="41d6e-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="41d6e-109">Si tiene inquietudes o preguntas sobre la hoja de ruta, envíe sus comentarios en el [repositorio de comentarios][GithubMicrosoftedgeWebviewfeedbackMain].</span><span class="sxs-lookup"><span data-stu-id="41d6e-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="41d6e-110">El equipo de WebView2 está planeando los siguientes esfuerzos importantes para futuras actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="41d6e-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="41d6e-111">Instalador de tiempo de ejecución de WebView2</span><span class="sxs-lookup"><span data-stu-id="41d6e-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="41d6e-112">Cuarto trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="41d6e-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="41d6e-113">Versión fija</span><span class="sxs-lookup"><span data-stu-id="41d6e-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="41d6e-114">Cuarto trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="41d6e-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="41d6e-115">Disponibilidad general</span><span class="sxs-lookup"><span data-stu-id="41d6e-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="41d6e-116">C/C++ \ Win32 \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="41d6e-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="41d6e-117">.NET \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="41d6e-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="41d6e-118">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="41d6e-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="41d6e-119">Tiempo de ejecución y instalador de WebView2</span><span class="sxs-lookup"><span data-stu-id="41d6e-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="41d6e-120">El [modelo de distribución de hoja perenne][ConceptDistributionEvergreenModel] le permite dirigir o encadenar la instalación del WebView2 en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="41d6e-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="41d6e-121">El tiempo de ejecución de WebView2 perenne y el instalador han alcanzado la disponibilidad general \ (GA \).</span><span class="sxs-lookup"><span data-stu-id="41d6e-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <span data-ttu-id="41d6e-122">Versión fija</span><span class="sxs-lookup"><span data-stu-id="41d6e-122">Fixed version</span></span>  

<span data-ttu-id="41d6e-123">El [modelo de distribución de versiones fijo][ConceptsDistributionFixedVersionModel] le permite empaquetar los archivos binarios de Microsoft Edge dentro de su aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="41d6e-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="41d6e-124">Actualmente se encuentra en vista previa y destinada a GA Q4 2020.</span><span class="sxs-lookup"><span data-stu-id="41d6e-124">It is currently under preview and targeted to GA Q4 2020.</span></span>  

## <span data-ttu-id="41d6e-125">Disponibilidad general</span><span class="sxs-lookup"><span data-stu-id="41d6e-125">General availability</span></span>  

### <span data-ttu-id="41d6e-126">C/C++ Win32</span><span class="sxs-lookup"><span data-stu-id="41d6e-126">Win32 C/C++</span></span>  

<span data-ttu-id="41d6e-127">El SDK Win32 C/C++ ha llegado a GA.</span><span class="sxs-lookup"><span data-stu-id="41d6e-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <span data-ttu-id="41d6e-128">.NET</span><span class="sxs-lookup"><span data-stu-id="41d6e-128">.NET</span></span>  

<span data-ttu-id="41d6e-129">El SDK de .NET contiene el SDK de Win32 C/C++.</span><span class="sxs-lookup"><span data-stu-id="41d6e-129">The .NET SDK wraps the Win32 C/C++ SDK.</span></span>  <span data-ttu-id="41d6e-130">Se espera que el SDK de .NET esté disponible poco después de Win32 C/C++ GA en el cuarto trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="41d6e-130">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>  

### <span data-ttu-id="41d6e-131">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="41d6e-131">WinUI 3.0</span></span>  

<span data-ttu-id="41d6e-132">Puedes acceder a WebView2 en tus aplicaciones para UWP usando la [interfaz de usuario de 3,0][UwpToolkitsWinui3Index], actualmente en Alpha.</span><span class="sxs-lookup"><span data-stu-id="41d6e-132">You are able to access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="41d6e-133">Para obtener más información sobre cómo mantenerse al día, consulte [Guía básica de la biblioteca de Windows UI][GithubMicrosoftUiXamlRoadmap].</span><span class="sxs-lookup"><span data-stu-id="41d6e-133">For more information about keeping up to date, see [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribución de versiones corregidas: distribución de aplicaciones con WebView2 | Microsoft docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Biblioteca de interfaces de usuario de Windows 3,0 Preview 1 (mayo de 2020) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Guía básica de la biblioteca de la interfaz de usuario de Windows-Microsoft/Microsoft-UI-XAML | GitHub"  
