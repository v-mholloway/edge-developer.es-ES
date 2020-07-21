---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1d3cae59c0906a94414ff135ef8d84fac7cc89b4
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885075"
---
# <span data-ttu-id="98008-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="98008-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="98008-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="98008-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="98008-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="98008-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="98008-107">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="98008-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="98008-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="98008-108">Summary</span></span>

 <span data-ttu-id="98008-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="98008-109">Members</span></span>                        | <span data-ttu-id="98008-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="98008-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="98008-111">Handled</span><span class="sxs-lookup"><span data-stu-id="98008-111">Handled</span></span>](#handled) | <span data-ttu-id="98008-112">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="98008-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="98008-113">Razón</span><span class="sxs-lookup"><span data-stu-id="98008-113">Reason</span></span>](#reason) | <span data-ttu-id="98008-114">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="98008-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="98008-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="98008-115">Members</span></span>

#### <span data-ttu-id="98008-116">Handled</span><span class="sxs-lookup"><span data-stu-id="98008-116">Handled</span></span> 

<span data-ttu-id="98008-117">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="98008-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="98008-118">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="98008-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="98008-119">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="98008-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="98008-120">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="98008-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="98008-121">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="98008-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="98008-122">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="98008-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="98008-123">Razón</span><span class="sxs-lookup"><span data-stu-id="98008-123">Reason</span></span> 

<span data-ttu-id="98008-124">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="98008-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="98008-125">[razón](#reason) de CoreWebView2MoveFocusReason pública</span><span class="sxs-lookup"><span data-stu-id="98008-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

