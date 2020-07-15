---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878774"
---
# <span data-ttu-id="969d1-104">Estructura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="969d1-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="969d1-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="969d1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="969d1-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="969d1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="969d1-107">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="969d1-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="969d1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="969d1-108">Summary</span></span>

 <span data-ttu-id="969d1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="969d1-109">Members</span></span>                        | <span data-ttu-id="969d1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="969d1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="969d1-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="969d1-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="969d1-112">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="969d1-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="969d1-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="969d1-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="969d1-114">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="969d1-114">The transition state.</span></span>
[<span data-ttu-id="969d1-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="969d1-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="969d1-116">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="969d1-116">The context code.</span></span>
[<span data-ttu-id="969d1-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="969d1-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="969d1-118">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="969d1-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="969d1-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="969d1-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="969d1-120">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="969d1-120">The scan code.</span></span>
[<span data-ttu-id="969d1-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="969d1-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="969d1-122">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="969d1-122">The previous key state.</span></span>

<span data-ttu-id="969d1-123">Para obtener más información, consulte la documentación de WM_KEYDOWN en [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="969d1-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="969d1-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="969d1-124">Members</span></span>

#### <span data-ttu-id="969d1-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="969d1-125">IsExtendedKey</span></span> 

<span data-ttu-id="969d1-126">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="969d1-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="969d1-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="969d1-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="969d1-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="969d1-128">IsKeyReleased</span></span> 

<span data-ttu-id="969d1-129">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="969d1-129">The transition state.</span></span>

> <span data-ttu-id="969d1-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="969d1-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="969d1-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="969d1-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="969d1-132">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="969d1-132">The context code.</span></span>

> <span data-ttu-id="969d1-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="969d1-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="969d1-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="969d1-134">RepeatCount</span></span> 

<span data-ttu-id="969d1-135">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="969d1-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="969d1-136">Public uint [RepeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="969d1-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="969d1-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="969d1-137">ScanCode</span></span> 

<span data-ttu-id="969d1-138">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="969d1-138">The scan code.</span></span>

> <span data-ttu-id="969d1-139">uint pública [Scancode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="969d1-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="969d1-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="969d1-140">WasKeyDown</span></span> 

<span data-ttu-id="969d1-141">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="969d1-141">The previous key state.</span></span>

> <span data-ttu-id="969d1-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="969d1-142">public int [WasKeyDown](#waskeydown)</span></span>

