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
ms.openlocfilehash: 1359e9472455acf2949cc329de4280ad970a3b68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697311"
---
# <span data-ttu-id="698f8-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="698f8-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="698f8-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="698f8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="698f8-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="698f8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="698f8-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="698f8-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="698f8-108">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="698f8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="698f8-109">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="698f8-109">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="698f8-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="698f8-110">Summary</span></span>

 <span data-ttu-id="698f8-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="698f8-111">Members</span></span>                        | <span data-ttu-id="698f8-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="698f8-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="698f8-113">DefaultText</span><span class="sxs-lookup"><span data-stu-id="698f8-113">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="698f8-114">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="698f8-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="698f8-115">Tipos</span><span class="sxs-lookup"><span data-stu-id="698f8-115">Kind</span></span>](#kind) | <span data-ttu-id="698f8-116">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="698f8-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="698f8-117">Mensaje</span><span class="sxs-lookup"><span data-stu-id="698f8-117">Message</span></span>](#message) | <span data-ttu-id="698f8-118">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="698f8-118">The message of the dialog box.</span></span>
[<span data-ttu-id="698f8-119">ResultText</span><span class="sxs-lookup"><span data-stu-id="698f8-119">ResultText</span></span>](#resulttext) | <span data-ttu-id="698f8-120">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="698f8-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="698f8-121">URI</span><span class="sxs-lookup"><span data-stu-id="698f8-121">Uri</span></span>](#uri) | <span data-ttu-id="698f8-122">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="698f8-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="698f8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="698f8-123">Accept</span></span>](#accept) | <span data-ttu-id="698f8-124">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="698f8-124">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="698f8-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="698f8-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="698f8-126">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="698f8-126">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="698f8-127">Miembros</span><span class="sxs-lookup"><span data-stu-id="698f8-127">Members</span></span>

#### <span data-ttu-id="698f8-128">DefaultText</span><span class="sxs-lookup"><span data-stu-id="698f8-128">DefaultText</span></span> 

<span data-ttu-id="698f8-129">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="698f8-129">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="698f8-130">cadena pública [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="698f8-130">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="698f8-131">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="698f8-131">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="698f8-132">Tipos</span><span class="sxs-lookup"><span data-stu-id="698f8-132">Kind</span></span> 

<span data-ttu-id="698f8-133">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="698f8-133">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="698f8-134">[tipo](#kind) de CoreWebView2ScriptDialogKind público</span><span class="sxs-lookup"><span data-stu-id="698f8-134">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="698f8-135">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="698f8-135">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="698f8-136">Mensaje</span><span class="sxs-lookup"><span data-stu-id="698f8-136">Message</span></span> 

<span data-ttu-id="698f8-137">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="698f8-137">The message of the dialog box.</span></span>

> <span data-ttu-id="698f8-138">[mensaje](#message) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="698f8-138">public string [Message](#message)</span></span>

<span data-ttu-id="698f8-139">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="698f8-139">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="698f8-140">ResultText</span><span class="sxs-lookup"><span data-stu-id="698f8-140">ResultText</span></span> 

<span data-ttu-id="698f8-141">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="698f8-141">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="698f8-142">cadena pública [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="698f8-142">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="698f8-143">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="698f8-143">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="698f8-144">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="698f8-144">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="698f8-145">URI</span><span class="sxs-lookup"><span data-stu-id="698f8-145">Uri</span></span> 

<span data-ttu-id="698f8-146">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="698f8-146">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="698f8-147">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="698f8-147">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="698f8-148">Aceptar</span><span class="sxs-lookup"><span data-stu-id="698f8-148">Accept</span></span> 

<span data-ttu-id="698f8-149">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="698f8-149">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="698f8-150">[Accept](#accept)public void ()</span><span class="sxs-lookup"><span data-stu-id="698f8-150">public void [Accept](#accept)()</span></span>

<span data-ttu-id="698f8-151">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="698f8-151">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="698f8-152">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="698f8-152">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="698f8-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="698f8-153">GetDeferral</span></span> 

<span data-ttu-id="698f8-154">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="698f8-154">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="698f8-155">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="698f8-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="698f8-156">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="698f8-156">You can use this to complete the event at a later time.</span></span>

