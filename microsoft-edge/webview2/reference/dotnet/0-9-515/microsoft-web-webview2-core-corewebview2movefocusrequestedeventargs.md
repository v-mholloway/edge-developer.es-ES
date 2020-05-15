---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3c88108f0e1df89c62c8713ff37f35d0c759cf6c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655448"
---
# <span data-ttu-id="c8887-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c8887-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

<span data-ttu-id="c8887-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c8887-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c8887-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="c8887-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c8887-107">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="c8887-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c8887-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c8887-108">Summary</span></span>

 <span data-ttu-id="c8887-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8887-109">Members</span></span>                        | <span data-ttu-id="c8887-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c8887-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c8887-111">Handled</span><span class="sxs-lookup"><span data-stu-id="c8887-111">Handled</span></span>](#handled) | <span data-ttu-id="c8887-112">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="c8887-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="c8887-113">Razón</span><span class="sxs-lookup"><span data-stu-id="c8887-113">Reason</span></span>](#reason) | <span data-ttu-id="c8887-114">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="c8887-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="c8887-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8887-115">Members</span></span>

#### <span data-ttu-id="c8887-116">Handled</span><span class="sxs-lookup"><span data-stu-id="c8887-116">Handled</span></span> 

<span data-ttu-id="c8887-117">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="c8887-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="c8887-118">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="c8887-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="c8887-119">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="c8887-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="c8887-120">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c8887-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="c8887-121">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="c8887-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="c8887-122">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="c8887-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="c8887-123">Razón</span><span class="sxs-lookup"><span data-stu-id="c8887-123">Reason</span></span> 

<span data-ttu-id="c8887-124">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="c8887-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="c8887-125">[razón](#reason) de CoreWebView2MoveFocusReason pública</span><span class="sxs-lookup"><span data-stu-id="c8887-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

