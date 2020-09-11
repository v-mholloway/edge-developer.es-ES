---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 17ed4a578234a056a7e6ff347829a12e39fa93bd
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010925"
---
# <span data-ttu-id="6ee04-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus struct</span><span class="sxs-lookup"><span data-stu-id="6ee04-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="6ee04-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6ee04-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6ee04-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6ee04-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6ee04-107">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="6ee04-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="6ee04-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6ee04-108">Summary</span></span>

 <span data-ttu-id="6ee04-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ee04-109">Members</span></span>                        | <span data-ttu-id="6ee04-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6ee04-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6ee04-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="6ee04-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="6ee04-112">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="6ee04-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="6ee04-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="6ee04-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="6ee04-114">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="6ee04-114">The transition state.</span></span>
[<span data-ttu-id="6ee04-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="6ee04-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="6ee04-116">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="6ee04-116">The context code.</span></span>
[<span data-ttu-id="6ee04-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="6ee04-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="6ee04-118">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="6ee04-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="6ee04-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="6ee04-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="6ee04-120">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="6ee04-120">The scan code.</span></span>
[<span data-ttu-id="6ee04-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="6ee04-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="6ee04-122">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="6ee04-122">The previous key state.</span></span>

<span data-ttu-id="6ee04-123">Para obtener más información, consulte la documentación de WM_KEYDOWN en [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="6ee04-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="6ee04-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ee04-124">Members</span></span>

#### <span data-ttu-id="6ee04-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="6ee04-125">IsExtendedKey</span></span> 

<span data-ttu-id="6ee04-126">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="6ee04-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="6ee04-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="6ee04-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="6ee04-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="6ee04-128">IsKeyReleased</span></span> 

<span data-ttu-id="6ee04-129">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="6ee04-129">The transition state.</span></span>

> <span data-ttu-id="6ee04-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="6ee04-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="6ee04-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="6ee04-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="6ee04-132">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="6ee04-132">The context code.</span></span>

> <span data-ttu-id="6ee04-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="6ee04-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="6ee04-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="6ee04-134">RepeatCount</span></span> 

<span data-ttu-id="6ee04-135">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="6ee04-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="6ee04-136">Public uint [RepeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="6ee04-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="6ee04-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="6ee04-137">ScanCode</span></span> 

<span data-ttu-id="6ee04-138">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="6ee04-138">The scan code.</span></span>

> <span data-ttu-id="6ee04-139">uint pública [Scancode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="6ee04-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="6ee04-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="6ee04-140">WasKeyDown</span></span> 

<span data-ttu-id="6ee04-141">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="6ee04-141">The previous key state.</span></span>

> <span data-ttu-id="6ee04-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="6ee04-142">public int [WasKeyDown](#waskeydown)</span></span>

