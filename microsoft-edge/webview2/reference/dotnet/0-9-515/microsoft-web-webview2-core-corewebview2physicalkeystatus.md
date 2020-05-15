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
ms.openlocfilehash: 28ed6db251095e2baf6474950c6839dc4a5a8633
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655508"
---
# <span data-ttu-id="8004c-104">Estructura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8004c-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="8004c-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8004c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8004c-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="8004c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8004c-107">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="8004c-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="8004c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="8004c-108">Summary</span></span>

 <span data-ttu-id="8004c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8004c-109">Members</span></span>                        | <span data-ttu-id="8004c-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8004c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8004c-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="8004c-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="8004c-112">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="8004c-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="8004c-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="8004c-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="8004c-114">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="8004c-114">The transition state.</span></span>
[<span data-ttu-id="8004c-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="8004c-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="8004c-116">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="8004c-116">The context code.</span></span>
[<span data-ttu-id="8004c-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="8004c-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="8004c-118">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="8004c-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="8004c-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="8004c-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="8004c-120">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="8004c-120">The scan code.</span></span>
[<span data-ttu-id="8004c-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="8004c-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="8004c-122">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="8004c-122">The previous key state.</span></span>

<span data-ttu-id="8004c-123">Para obtener más información, consulte la documentación de WM_KEYDOWN en [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="8004c-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="8004c-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="8004c-124">Members</span></span>

#### <span data-ttu-id="8004c-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="8004c-125">IsExtendedKey</span></span> 

<span data-ttu-id="8004c-126">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="8004c-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="8004c-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="8004c-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="8004c-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="8004c-128">IsKeyReleased</span></span> 

<span data-ttu-id="8004c-129">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="8004c-129">The transition state.</span></span>

> <span data-ttu-id="8004c-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="8004c-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="8004c-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="8004c-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="8004c-132">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="8004c-132">The context code.</span></span>

> <span data-ttu-id="8004c-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="8004c-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="8004c-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="8004c-134">RepeatCount</span></span> 

<span data-ttu-id="8004c-135">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="8004c-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="8004c-136">Public uint [RepeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="8004c-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="8004c-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="8004c-137">ScanCode</span></span> 

<span data-ttu-id="8004c-138">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="8004c-138">The scan code.</span></span>

> <span data-ttu-id="8004c-139">uint pública [Scancode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="8004c-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="8004c-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="8004c-140">WasKeyDown</span></span> 

<span data-ttu-id="8004c-141">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="8004c-141">The previous key state.</span></span>

> <span data-ttu-id="8004c-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="8004c-142">public int [WasKeyDown](#waskeydown)</span></span>

