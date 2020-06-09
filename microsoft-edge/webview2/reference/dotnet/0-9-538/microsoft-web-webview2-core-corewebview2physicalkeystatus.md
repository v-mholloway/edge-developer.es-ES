---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e0fb3f9ff7114b0c4f2a42893adabfd72e9616de
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699312"
---
# <span data-ttu-id="66679-104">Estructura Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="66679-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="66679-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="66679-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="66679-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="66679-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="66679-107">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="66679-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="66679-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="66679-108">Summary</span></span>

 <span data-ttu-id="66679-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="66679-109">Members</span></span>                        | <span data-ttu-id="66679-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="66679-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66679-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="66679-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="66679-112">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="66679-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="66679-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="66679-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="66679-114">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="66679-114">The transition state.</span></span>
[<span data-ttu-id="66679-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="66679-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="66679-116">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="66679-116">The context code.</span></span>
[<span data-ttu-id="66679-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="66679-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="66679-118">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="66679-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="66679-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="66679-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="66679-120">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="66679-120">The scan code.</span></span>
[<span data-ttu-id="66679-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="66679-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="66679-122">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="66679-122">The previous key state.</span></span>

<span data-ttu-id="66679-123">Para obtener más información, consulte la documentación de WM_KEYDOWN en [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="66679-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="66679-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="66679-124">Members</span></span>

#### <span data-ttu-id="66679-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="66679-125">IsExtendedKey</span></span> 

<span data-ttu-id="66679-126">Indica si la tecla es una tecla extendida.</span><span class="sxs-lookup"><span data-stu-id="66679-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="66679-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="66679-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="66679-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="66679-128">IsKeyReleased</span></span> 

<span data-ttu-id="66679-129">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="66679-129">The transition state.</span></span>

> <span data-ttu-id="66679-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="66679-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="66679-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="66679-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="66679-132">El código de contexto.</span><span class="sxs-lookup"><span data-stu-id="66679-132">The context code.</span></span>

> <span data-ttu-id="66679-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="66679-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="66679-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="66679-134">RepeatCount</span></span> 

<span data-ttu-id="66679-135">El número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="66679-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="66679-136">Public uint [RepeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="66679-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="66679-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="66679-137">ScanCode</span></span> 

<span data-ttu-id="66679-138">El código de análisis.</span><span class="sxs-lookup"><span data-stu-id="66679-138">The scan code.</span></span>

> <span data-ttu-id="66679-139">uint pública [Scancode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="66679-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="66679-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="66679-140">WasKeyDown</span></span> 

<span data-ttu-id="66679-141">El estado de clave anterior.</span><span class="sxs-lookup"><span data-stu-id="66679-141">The previous key state.</span></span>

> <span data-ttu-id="66679-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="66679-142">public int [WasKeyDown](#waskeydown)</span></span>

