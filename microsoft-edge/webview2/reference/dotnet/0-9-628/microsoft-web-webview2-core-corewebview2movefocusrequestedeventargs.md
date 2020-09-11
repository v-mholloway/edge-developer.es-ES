---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: c7f318f44ce0469a216fe8dda7870c4adbdebcc0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012669"
---
# <span data-ttu-id="c1981-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c1981-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

<span data-ttu-id="c1981-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c1981-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c1981-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c1981-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c1981-107">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="c1981-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="c1981-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c1981-108">Summary</span></span>

 <span data-ttu-id="c1981-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1981-109">Members</span></span>                        | <span data-ttu-id="c1981-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c1981-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1981-111">Handled</span><span class="sxs-lookup"><span data-stu-id="c1981-111">Handled</span></span>](#handled) | <span data-ttu-id="c1981-112">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="c1981-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="c1981-113">Razón</span><span class="sxs-lookup"><span data-stu-id="c1981-113">Reason</span></span>](#reason) | <span data-ttu-id="c1981-114">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="c1981-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="c1981-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1981-115">Members</span></span>

#### <span data-ttu-id="c1981-116">Handled</span><span class="sxs-lookup"><span data-stu-id="c1981-116">Handled</span></span> 

<span data-ttu-id="c1981-117">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="c1981-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="c1981-118">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="c1981-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="c1981-119">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="c1981-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="c1981-120">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c1981-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="c1981-121">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="c1981-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="c1981-122">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="c1981-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="c1981-123">Razón</span><span class="sxs-lookup"><span data-stu-id="c1981-123">Reason</span></span> 

<span data-ttu-id="c1981-124">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="c1981-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="c1981-125">[razón](#reason) de CoreWebView2MoveFocusReason pública</span><span class="sxs-lookup"><span data-stu-id="c1981-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

