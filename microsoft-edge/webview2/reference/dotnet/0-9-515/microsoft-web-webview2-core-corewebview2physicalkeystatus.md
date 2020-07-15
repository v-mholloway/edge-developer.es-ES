---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: da7069fb4dad164720bb697a250a216a0bd452ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881203"
---
# <span data-ttu-id="352f7-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus struct</span><span class="sxs-lookup"><span data-stu-id="352f7-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="352f7-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="352f7-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="352f7-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="352f7-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="352f7-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="352f7-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="352f7-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="352f7-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="352f7-109">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="352f7-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="352f7-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="352f7-110">Summary</span></span>

 <span data-ttu-id="352f7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="352f7-111">Members</span></span>                        | <span data-ttu-id="352f7-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="352f7-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="352f7-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="352f7-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="352f7-114">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="352f7-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="352f7-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="352f7-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="352f7-116">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="352f7-116">The transition state.</span></span>
[<span data-ttu-id="352f7-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="352f7-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="352f7-118">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="352f7-118">The context code.</span></span>
[<span data-ttu-id="352f7-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="352f7-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="352f7-120">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="352f7-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="352f7-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="352f7-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="352f7-122">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="352f7-122">The scan code.</span></span>
[<span data-ttu-id="352f7-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="352f7-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="352f7-124">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="352f7-124">The previous key state.</span></span>

<span data-ttu-id="352f7-125">Para obtener más información, consulte la documentación de WM_KEYDOWN en [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="352f7-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="352f7-126">Miembros</span><span class="sxs-lookup"><span data-stu-id="352f7-126">Members</span></span>

#### <span data-ttu-id="352f7-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="352f7-127">IsExtendedKey</span></span> 

<span data-ttu-id="352f7-128">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="352f7-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="352f7-129">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="352f7-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="352f7-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="352f7-130">IsKeyReleased</span></span> 

<span data-ttu-id="352f7-131">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="352f7-131">The transition state.</span></span>

> <span data-ttu-id="352f7-132">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="352f7-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="352f7-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="352f7-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="352f7-134">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="352f7-134">The context code.</span></span>

> <span data-ttu-id="352f7-135">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="352f7-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="352f7-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="352f7-136">RepeatCount</span></span> 

<span data-ttu-id="352f7-137">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="352f7-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="352f7-138">Public uint [RepeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="352f7-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="352f7-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="352f7-139">ScanCode</span></span> 

<span data-ttu-id="352f7-140">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="352f7-140">The scan code.</span></span>

> <span data-ttu-id="352f7-141">uint pública [Scancode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="352f7-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="352f7-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="352f7-142">WasKeyDown</span></span> 

<span data-ttu-id="352f7-143">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="352f7-143">The previous key state.</span></span>

> <span data-ttu-id="352f7-144">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="352f7-144">public int [WasKeyDown](#waskeydown)</span></span>

