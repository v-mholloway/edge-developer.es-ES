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
ms.openlocfilehash: e8563bdd77972945a1e4b81662071d07d1efeb02
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699339"
---
# <span data-ttu-id="fea15-104">Estructura Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4</span><span class="sxs-lookup"><span data-stu-id="fea15-104">Microsoft.Web.WebView2.Core.CoreWebView2Matrix4x4 struct</span></span> 

> [!NOTE]
> <span data-ttu-id="fea15-105">Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="fea15-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="fea15-106">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fea15-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fea15-107">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="fea15-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fea15-108">Esta transformación se usa para calcular las coordenadas correctas al llamar a CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="fea15-108">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span>

## <span data-ttu-id="fea15-109">Resumen</span><span class="sxs-lookup"><span data-stu-id="fea15-109">Summary</span></span>

 <span data-ttu-id="fea15-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fea15-110">Members</span></span>                        | <span data-ttu-id="fea15-111">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fea15-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fea15-112">_11</span><span class="sxs-lookup"><span data-stu-id="fea15-112">_11</span></span>](#_11) | <span data-ttu-id="fea15-113">El valor de la primera fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-113">The value in the first row and first column of the matrix.</span></span>
[<span data-ttu-id="fea15-114">_12</span><span class="sxs-lookup"><span data-stu-id="fea15-114">_12</span></span>](#_12) | <span data-ttu-id="fea15-115">El valor de la primera fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-115">The value in the first row and second column of the matrix.</span></span>
[<span data-ttu-id="fea15-116">_13</span><span class="sxs-lookup"><span data-stu-id="fea15-116">_13</span></span>](#_13) | <span data-ttu-id="fea15-117">El valor de la primera fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-117">The value in the first row and third column of the matrix.</span></span>
[<span data-ttu-id="fea15-118">_14</span><span class="sxs-lookup"><span data-stu-id="fea15-118">_14</span></span>](#_14) | <span data-ttu-id="fea15-119">El valor de la primera fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-119">The value in the first row and fourth column of the matrix.</span></span>
[<span data-ttu-id="fea15-120">_21</span><span class="sxs-lookup"><span data-stu-id="fea15-120">_21</span></span>](#_21) | <span data-ttu-id="fea15-121">El valor de la segunda fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-121">The value in the second row and first column of the matrix.</span></span>
[<span data-ttu-id="fea15-122">_22</span><span class="sxs-lookup"><span data-stu-id="fea15-122">_22</span></span>](#_22) | <span data-ttu-id="fea15-123">El valor de la segunda fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-123">The value in the second row and second column of the matrix.</span></span>
[<span data-ttu-id="fea15-124">_23</span><span class="sxs-lookup"><span data-stu-id="fea15-124">_23</span></span>](#_23) | <span data-ttu-id="fea15-125">El valor de la segunda fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-125">The value in the second row and third column of the matrix.</span></span>
[<span data-ttu-id="fea15-126">_24</span><span class="sxs-lookup"><span data-stu-id="fea15-126">_24</span></span>](#_24) | <span data-ttu-id="fea15-127">El valor de la segunda fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-127">The value in the second row and fourth column of the matrix.</span></span>
[<span data-ttu-id="fea15-128">_31</span><span class="sxs-lookup"><span data-stu-id="fea15-128">_31</span></span>](#_31) | <span data-ttu-id="fea15-129">El valor de la tercera fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-129">The value in the third row and first column of the matrix.</span></span>
[<span data-ttu-id="fea15-130">_32</span><span class="sxs-lookup"><span data-stu-id="fea15-130">_32</span></span>](#_32) | <span data-ttu-id="fea15-131">El valor de la tercera fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-131">The value in the third row and second column of the matrix.</span></span>
[<span data-ttu-id="fea15-132">_33</span><span class="sxs-lookup"><span data-stu-id="fea15-132">_33</span></span>](#_33) | <span data-ttu-id="fea15-133">El valor de la tercera fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-133">The value in the third row and third column of the matrix.</span></span>
[<span data-ttu-id="fea15-134">_34</span><span class="sxs-lookup"><span data-stu-id="fea15-134">_34</span></span>](#_34) | <span data-ttu-id="fea15-135">El valor de la tercera fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-135">The value in the third row and fourth column of the matrix.</span></span>
[<span data-ttu-id="fea15-136">_41</span><span class="sxs-lookup"><span data-stu-id="fea15-136">_41</span></span>](#_41) | <span data-ttu-id="fea15-137">El valor de la cuarta fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-137">The value in the fourth row and first column of the matrix.</span></span>
[<span data-ttu-id="fea15-138">_42</span><span class="sxs-lookup"><span data-stu-id="fea15-138">_42</span></span>](#_42) | <span data-ttu-id="fea15-139">El valor de la cuarta fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-139">The value in the fourth row and second column of the matrix.</span></span>
[<span data-ttu-id="fea15-140">_43</span><span class="sxs-lookup"><span data-stu-id="fea15-140">_43</span></span>](#_43) | <span data-ttu-id="fea15-141">El valor de la cuarta fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-141">The value in the fourth row and third column of the matrix.</span></span>
[<span data-ttu-id="fea15-142">_44</span><span class="sxs-lookup"><span data-stu-id="fea15-142">_44</span></span>](#_44) | <span data-ttu-id="fea15-143">El valor de la cuarta fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-143">The value in the fourth row and fourth column of the matrix.</span></span>

<span data-ttu-id="fea15-144">Es equivalente a una D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="fea15-144">This is equivalent to a D2D1_MATRIX_4X4_F.</span></span>

## <span data-ttu-id="fea15-145">Miembros</span><span class="sxs-lookup"><span data-stu-id="fea15-145">Members</span></span>

#### <span data-ttu-id="fea15-146">_11</span><span class="sxs-lookup"><span data-stu-id="fea15-146">_11</span></span> 

<span data-ttu-id="fea15-147">El valor de la primera fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-147">The value in the first row and first column of the matrix.</span></span>

> <span data-ttu-id="fea15-148">[_11](#_11) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-148">public Single [_11](#_11)</span></span>

#### <span data-ttu-id="fea15-149">_12</span><span class="sxs-lookup"><span data-stu-id="fea15-149">_12</span></span> 

<span data-ttu-id="fea15-150">El valor de la primera fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-150">The value in the first row and second column of the matrix.</span></span>

> <span data-ttu-id="fea15-151">[_12](#_12) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-151">public Single [_12](#_12)</span></span>

#### <span data-ttu-id="fea15-152">_13</span><span class="sxs-lookup"><span data-stu-id="fea15-152">_13</span></span> 

<span data-ttu-id="fea15-153">El valor de la primera fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-153">The value in the first row and third column of the matrix.</span></span>

> <span data-ttu-id="fea15-154">[_13](#_13) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-154">public Single [_13](#_13)</span></span>

#### <span data-ttu-id="fea15-155">_14</span><span class="sxs-lookup"><span data-stu-id="fea15-155">_14</span></span> 

<span data-ttu-id="fea15-156">El valor de la primera fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-156">The value in the first row and fourth column of the matrix.</span></span>

> <span data-ttu-id="fea15-157">[_14](#_14) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-157">public Single [_14](#_14)</span></span>

#### <span data-ttu-id="fea15-158">_21</span><span class="sxs-lookup"><span data-stu-id="fea15-158">_21</span></span> 

<span data-ttu-id="fea15-159">El valor de la segunda fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-159">The value in the second row and first column of the matrix.</span></span>

> <span data-ttu-id="fea15-160">[_21](#_21) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-160">public Single [_21](#_21)</span></span>

#### <span data-ttu-id="fea15-161">_22</span><span class="sxs-lookup"><span data-stu-id="fea15-161">_22</span></span> 

<span data-ttu-id="fea15-162">El valor de la segunda fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-162">The value in the second row and second column of the matrix.</span></span>

> <span data-ttu-id="fea15-163">[_22](#_22) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-163">public Single [_22](#_22)</span></span>

#### <span data-ttu-id="fea15-164">_23</span><span class="sxs-lookup"><span data-stu-id="fea15-164">_23</span></span> 

<span data-ttu-id="fea15-165">El valor de la segunda fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-165">The value in the second row and third column of the matrix.</span></span>

> <span data-ttu-id="fea15-166">[_23](#_23) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-166">public Single [_23](#_23)</span></span>

#### <span data-ttu-id="fea15-167">_24</span><span class="sxs-lookup"><span data-stu-id="fea15-167">_24</span></span> 

<span data-ttu-id="fea15-168">El valor de la segunda fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-168">The value in the second row and fourth column of the matrix.</span></span>

> <span data-ttu-id="fea15-169">[_24](#_24) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-169">public Single [_24](#_24)</span></span>

#### <span data-ttu-id="fea15-170">_31</span><span class="sxs-lookup"><span data-stu-id="fea15-170">_31</span></span> 

<span data-ttu-id="fea15-171">El valor de la tercera fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-171">The value in the third row and first column of the matrix.</span></span>

> <span data-ttu-id="fea15-172">[_31](#_31) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-172">public Single [_31](#_31)</span></span>

#### <span data-ttu-id="fea15-173">_32</span><span class="sxs-lookup"><span data-stu-id="fea15-173">_32</span></span> 

<span data-ttu-id="fea15-174">El valor de la tercera fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-174">The value in the third row and second column of the matrix.</span></span>

> <span data-ttu-id="fea15-175">[_32](#_32) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-175">public Single [_32](#_32)</span></span>

#### <span data-ttu-id="fea15-176">_33</span><span class="sxs-lookup"><span data-stu-id="fea15-176">_33</span></span> 

<span data-ttu-id="fea15-177">El valor de la tercera fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-177">The value in the third row and third column of the matrix.</span></span>

> <span data-ttu-id="fea15-178">[_33](#_33) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-178">public Single [_33](#_33)</span></span>

#### <span data-ttu-id="fea15-179">_34</span><span class="sxs-lookup"><span data-stu-id="fea15-179">_34</span></span> 

<span data-ttu-id="fea15-180">El valor de la tercera fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-180">The value in the third row and fourth column of the matrix.</span></span>

> <span data-ttu-id="fea15-181">[_34](#_34) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-181">public Single [_34](#_34)</span></span>

#### <span data-ttu-id="fea15-182">_41</span><span class="sxs-lookup"><span data-stu-id="fea15-182">_41</span></span> 

<span data-ttu-id="fea15-183">El valor de la cuarta fila y la primera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-183">The value in the fourth row and first column of the matrix.</span></span>

> <span data-ttu-id="fea15-184">[_41](#_41) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-184">public Single [_41](#_41)</span></span>

#### <span data-ttu-id="fea15-185">_42</span><span class="sxs-lookup"><span data-stu-id="fea15-185">_42</span></span> 

<span data-ttu-id="fea15-186">El valor de la cuarta fila y la segunda columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-186">The value in the fourth row and second column of the matrix.</span></span>

> <span data-ttu-id="fea15-187">[_42](#_42) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-187">public Single [_42](#_42)</span></span>

#### <span data-ttu-id="fea15-188">_43</span><span class="sxs-lookup"><span data-stu-id="fea15-188">_43</span></span> 

<span data-ttu-id="fea15-189">El valor de la cuarta fila y la tercera columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-189">The value in the fourth row and third column of the matrix.</span></span>

> <span data-ttu-id="fea15-190">[_43](#_43) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-190">public Single [_43](#_43)</span></span>

#### <span data-ttu-id="fea15-191">_44</span><span class="sxs-lookup"><span data-stu-id="fea15-191">_44</span></span> 

<span data-ttu-id="fea15-192">El valor de la cuarta fila y la cuarta columna de la matriz.</span><span class="sxs-lookup"><span data-stu-id="fea15-192">The value in the fourth row and fourth column of the matrix.</span></span>

> <span data-ttu-id="fea15-193">[_44](#_44) única pública</span><span class="sxs-lookup"><span data-stu-id="fea15-193">public Single [_44](#_44)</span></span>

