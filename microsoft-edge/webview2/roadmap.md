---
description: Más información sobre lo que viene a continuación para WebView2
title: Guía básica para la vista de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: bc55c5a731ab6cba8f9be15208029aad0ad5357a
ms.sourcegitcommit: a75e062b71831ea850c85287a8d7d7ce3b55ec84
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659747"
---
# <span data-ttu-id="d5c2f-104">Guía básica de WebView2 de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d5c2f-104">Microsoft Edge WebView2 Roadmap</span></span>

##### <span data-ttu-id="d5c2f-105">Última actualización: 2020 de mayo de</span><span class="sxs-lookup"><span data-stu-id="d5c2f-105">Last Updated: May 2020</span></span>

<span data-ttu-id="d5c2f-106">El control WebView2 permite a los programadores incrustar tecnologías web en sus aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span> <span data-ttu-id="d5c2f-107">Este documento describe la guía básica para WebView2.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-107">This document outlines the prospective roadmap for WebView2.</span></span> 

> [!NOTE]
> <span data-ttu-id="d5c2f-108">WebView2 está en desarrollo activo y el plan seguirá evolucionando en función de los cambios en el mercado y los comentarios de los clientes, por lo que tenga en cuenta que los planes resaltados aquí no son exhaustivos y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-108">WebView2 is under active development and the roadmap will continue to evolve based on market changes and customer feedback, so please note that the plans outlined here aren't exhaustive and are subject to change.</span></span> 

<span data-ttu-id="d5c2f-109">Si tienes inquietudes o preguntas sobre la hoja de ruta, deja comentarios en el [repositorio de comentarios](https://github.com/MicrosoftEdge/WebViewFeedback).</span><span class="sxs-lookup"><span data-stu-id="d5c2f-109">If you have concerns or questions about the Roadmap, please leave feedback in the [feedback repo](https://github.com/MicrosoftEdge/WebViewFeedback).</span></span>

<span data-ttu-id="d5c2f-110">El equipo de WebView2 tiene una serie de esfuerzos importantes:</span><span class="sxs-lookup"><span data-stu-id="d5c2f-110">The WebView2 team has a few major efforts underway:</span></span>

1.  <span data-ttu-id="d5c2f-111">WebView2 Runtime Installer (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="d5c2f-111">WebView2 Runtime Installer (Q4 2020)</span></span>
2.  <span data-ttu-id="d5c2f-112">Versión fija (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="d5c2f-112">Fixed Version (Q4 2020)</span></span>
3.  <span data-ttu-id="d5c2f-113">Disponibilidad general</span><span class="sxs-lookup"><span data-stu-id="d5c2f-113">General Availability</span></span> 
    *   <span data-ttu-id="d5c2f-114">C/C++ Win32 (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="d5c2f-114">Win32 C/C++ (Q4 2020)</span></span>
    *   <span data-ttu-id="d5c2f-115">.NET (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="d5c2f-115">.NET (Q4 2020)</span></span>
    *   [<span data-ttu-id="d5c2f-116">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="d5c2f-116">WinUI 3.0</span></span>](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## <span data-ttu-id="d5c2f-117">WebView2 Runtime & Installer</span><span class="sxs-lookup"><span data-stu-id="d5c2f-117">WebView2 Runtime & Installer</span></span>

<span data-ttu-id="d5c2f-118">WebView2 modelo de distribución de [hoja perenne](./concepts/distribution.md#microsoft-edge-webview2-runtime) le permitirá dirigir o encadenar la instalación de WebView2 Runtime en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-118">WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) distribution model will allow you to target or chain install the WebView2 Runtime onto your user's machine.</span></span> <span data-ttu-id="d5c2f-119">Se espera que la versión preliminar del tiempo de ejecución y el instalador de WebView2 estén disponibles T3 2020 y GA en el cuarto trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-119">A preview of the WebView2 Runtime and installer is expected to be available Q3 2020 and GA in Q4 2020.</span></span>

## <span data-ttu-id="d5c2f-120">Versión fija</span><span class="sxs-lookup"><span data-stu-id="d5c2f-120">Fixed Version</span></span>

<span data-ttu-id="d5c2f-121">El modelo de distribución [fija](./concepts/distribution.md#roadmap) de WebView2 le permite empaquetar los archivos binarios de Microsoft Edge dentro de su aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-121">WebView2 [Fixed](./concepts/distribution.md#roadmap) distribution model allows you to package the Microsoft Edge binaries inside your native application.</span></span> <span data-ttu-id="d5c2f-122">En la actualidad, el trabajo de ingeniería está en camino con una vista previa anticipada para prepararse hacia el final del T3 2020 y GA Q4 2020.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-122">Engineering work is currently under way with a preview anticipated to be ready towards the end of  Q3 2020 and GA Q4 2020.</span></span>

## <span data-ttu-id="d5c2f-123">Disponibilidad general</span><span class="sxs-lookup"><span data-stu-id="d5c2f-123">General Availability</span></span> 

### <span data-ttu-id="d5c2f-124">C/C++ Win32</span><span class="sxs-lookup"><span data-stu-id="d5c2f-124">Win32 C/C++</span></span>

<span data-ttu-id="d5c2f-125">Se espera que el SDK de Win32 C/C++ se GA en el cuarto trimestre de 2020, poco después del tiempo de ejecución de WebView2 y el instalador GA.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-125">The Win32 C/C++ SDK is expected to GA in Q4 2020, shortly after the WebView2 Runtime and installer GA.</span></span>

### <span data-ttu-id="d5c2f-126">.NET</span><span class="sxs-lookup"><span data-stu-id="d5c2f-126">.NET</span></span>

<span data-ttu-id="d5c2f-127">El SDK de .NET contiene el SDK de Win32 C/C++.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-127">The .NET SDK wraps the Win32 C/C++ SDK.</span></span> <span data-ttu-id="d5c2f-128">Se espera que el SDK de .NET esté disponible poco después de Win32 C/C++ GA en el cuarto trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-128">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>

### <span data-ttu-id="d5c2f-129">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="d5c2f-129">WinUI 3.0</span></span>

<span data-ttu-id="d5c2f-130">Puedes poner WebView2 a las aplicaciones para UWP a través de la [interfaz de usuario de 3,0](/uwp/toolkits/winui3/), actualmente en Alpha.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-130">You can bring WebView2 to UWP applications through [Win UI 3.0](/uwp/toolkits/winui3/), currently in alpha.</span></span> <span data-ttu-id="d5c2f-131">Desproteja la [Guía básica de la biblioteca de Windows UI](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) para mantenerte al día.</span><span class="sxs-lookup"><span data-stu-id="d5c2f-131">Checkout the [Windows UI Library Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) to keep up to date.</span></span>  
