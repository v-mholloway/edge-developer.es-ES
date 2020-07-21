---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 4e7cd20b982d829be6d304eea1f3f60759cc503f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884859"
---
# <span data-ttu-id="44b2f-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="44b2f-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="44b2f-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="44b2f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="44b2f-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="44b2f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="44b2f-107">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="44b2f-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="44b2f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="44b2f-108">Summary</span></span>

 <span data-ttu-id="44b2f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="44b2f-109">Members</span></span>                        | <span data-ttu-id="44b2f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="44b2f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="44b2f-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="44b2f-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="44b2f-112">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44b2f-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="44b2f-113">Tipos</span><span class="sxs-lookup"><span data-stu-id="44b2f-113">Kind</span></span>](#kind) | <span data-ttu-id="44b2f-114">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44b2f-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="44b2f-115">Mensaje</span><span class="sxs-lookup"><span data-stu-id="44b2f-115">Message</span></span>](#message) | <span data-ttu-id="44b2f-116">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="44b2f-116">The message of the dialog box.</span></span>
[<span data-ttu-id="44b2f-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="44b2f-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="44b2f-118">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="44b2f-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="44b2f-119">URI</span><span class="sxs-lookup"><span data-stu-id="44b2f-119">Uri</span></span>](#uri) | <span data-ttu-id="44b2f-120">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="44b2f-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="44b2f-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="44b2f-121">Accept</span></span>](#accept) | <span data-ttu-id="44b2f-122">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="44b2f-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="44b2f-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="44b2f-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="44b2f-124">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="44b2f-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="44b2f-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="44b2f-125">Members</span></span>

#### <span data-ttu-id="44b2f-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="44b2f-126">DefaultText</span></span> 

<span data-ttu-id="44b2f-127">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44b2f-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="44b2f-128">cadena pública [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="44b2f-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="44b2f-129">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="44b2f-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="44b2f-130">Tipos</span><span class="sxs-lookup"><span data-stu-id="44b2f-130">Kind</span></span> 

<span data-ttu-id="44b2f-131">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44b2f-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="44b2f-132">[tipo](#kind) de CoreWebView2ScriptDialogKind público</span><span class="sxs-lookup"><span data-stu-id="44b2f-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="44b2f-133">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="44b2f-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="44b2f-134">Mensaje</span><span class="sxs-lookup"><span data-stu-id="44b2f-134">Message</span></span> 

<span data-ttu-id="44b2f-135">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="44b2f-135">The message of the dialog box.</span></span>

> <span data-ttu-id="44b2f-136">[mensaje](#message) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="44b2f-136">public string [Message](#message)</span></span>

<span data-ttu-id="44b2f-137">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="44b2f-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="44b2f-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="44b2f-138">ResultText</span></span> 

<span data-ttu-id="44b2f-139">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="44b2f-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="44b2f-140">cadena pública [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="44b2f-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="44b2f-141">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="44b2f-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="44b2f-142">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="44b2f-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="44b2f-143">URI</span><span class="sxs-lookup"><span data-stu-id="44b2f-143">Uri</span></span> 

<span data-ttu-id="44b2f-144">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="44b2f-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="44b2f-145">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="44b2f-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="44b2f-146">Aceptar</span><span class="sxs-lookup"><span data-stu-id="44b2f-146">Accept</span></span> 

<span data-ttu-id="44b2f-147">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="44b2f-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="44b2f-148">[Accept](#accept)public void ()</span><span class="sxs-lookup"><span data-stu-id="44b2f-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="44b2f-149">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="44b2f-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="44b2f-150">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="44b2f-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="44b2f-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="44b2f-151">GetDeferral</span></span> 

<span data-ttu-id="44b2f-152">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="44b2f-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="44b2f-153">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="44b2f-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="44b2f-154">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="44b2f-154">You can use this to complete the event at a later time.</span></span>

