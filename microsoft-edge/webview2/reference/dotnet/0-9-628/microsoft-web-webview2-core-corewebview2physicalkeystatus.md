---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: adecd3b23369935b1dc5729e894eaf1c295a06d3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012638"
---
# <span data-ttu-id="85468-104">Estructura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="85468-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="85468-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="85468-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="85468-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="85468-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="85468-107">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="85468-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="85468-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="85468-108">Summary</span></span>

 <span data-ttu-id="85468-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="85468-109">Members</span></span>                        | <span data-ttu-id="85468-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="85468-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="85468-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="85468-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="85468-112">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="85468-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="85468-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="85468-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="85468-114">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="85468-114">The transition state.</span></span>
[<span data-ttu-id="85468-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="85468-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="85468-116">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="85468-116">The context code.</span></span>
[<span data-ttu-id="85468-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="85468-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="85468-118">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="85468-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="85468-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="85468-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="85468-120">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="85468-120">The scan code.</span></span>
[<span data-ttu-id="85468-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="85468-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="85468-122">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="85468-122">The previous key state.</span></span>

<span data-ttu-id="85468-123">Para obtener más información, consulte la documentación de WM_KEYDOWN en [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="85468-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="85468-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="85468-124">Members</span></span>

#### <span data-ttu-id="85468-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="85468-125">IsExtendedKey</span></span> 

<span data-ttu-id="85468-126">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="85468-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="85468-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="85468-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="85468-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="85468-128">IsKeyReleased</span></span> 

<span data-ttu-id="85468-129">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="85468-129">The transition state.</span></span>

> <span data-ttu-id="85468-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="85468-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="85468-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="85468-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="85468-132">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="85468-132">The context code.</span></span>

> <span data-ttu-id="85468-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="85468-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="85468-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="85468-134">RepeatCount</span></span> 

<span data-ttu-id="85468-135">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="85468-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="85468-136">Public uint [RepeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="85468-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="85468-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="85468-137">ScanCode</span></span> 

<span data-ttu-id="85468-138">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="85468-138">The scan code.</span></span>

> <span data-ttu-id="85468-139">uint pública [Scancode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="85468-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="85468-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="85468-140">WasKeyDown</span></span> 

<span data-ttu-id="85468-141">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="85468-141">The previous key state.</span></span>

> <span data-ttu-id="85468-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="85468-142">public int [WasKeyDown](#waskeydown)</span></span>

