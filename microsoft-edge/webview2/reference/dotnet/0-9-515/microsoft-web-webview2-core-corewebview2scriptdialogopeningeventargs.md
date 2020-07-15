---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b7071a312ce1fa3ca006a6805a1f712a51d0dab0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879117"
---
# <span data-ttu-id="cec96-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="cec96-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="cec96-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="cec96-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cec96-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="cec96-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="cec96-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cec96-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cec96-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="cec96-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cec96-109">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="cec96-109">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="cec96-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="cec96-110">Summary</span></span>

 <span data-ttu-id="cec96-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cec96-111">Members</span></span>                        | <span data-ttu-id="cec96-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cec96-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cec96-113">DefaultText</span><span class="sxs-lookup"><span data-stu-id="cec96-113">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="cec96-114">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cec96-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="cec96-115">Tipos</span><span class="sxs-lookup"><span data-stu-id="cec96-115">Kind</span></span>](#kind) | <span data-ttu-id="cec96-116">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cec96-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="cec96-117">Mensaje</span><span class="sxs-lookup"><span data-stu-id="cec96-117">Message</span></span>](#message) | <span data-ttu-id="cec96-118">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cec96-118">The message of the dialog box.</span></span>
[<span data-ttu-id="cec96-119">ResultText</span><span class="sxs-lookup"><span data-stu-id="cec96-119">ResultText</span></span>](#resulttext) | <span data-ttu-id="cec96-120">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="cec96-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="cec96-121">URI</span><span class="sxs-lookup"><span data-stu-id="cec96-121">Uri</span></span>](#uri) | <span data-ttu-id="cec96-122">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cec96-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="cec96-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cec96-123">Accept</span></span>](#accept) | <span data-ttu-id="cec96-124">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="cec96-124">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="cec96-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cec96-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="cec96-126">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="cec96-126">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="cec96-127">Miembros</span><span class="sxs-lookup"><span data-stu-id="cec96-127">Members</span></span>

#### <span data-ttu-id="cec96-128">DefaultText</span><span class="sxs-lookup"><span data-stu-id="cec96-128">DefaultText</span></span> 

<span data-ttu-id="cec96-129">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cec96-129">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="cec96-130">cadena pública [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="cec96-130">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="cec96-131">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="cec96-131">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="cec96-132">Tipos</span><span class="sxs-lookup"><span data-stu-id="cec96-132">Kind</span></span> 

<span data-ttu-id="cec96-133">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cec96-133">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="cec96-134">[tipo](#kind) de CoreWebView2ScriptDialogKind público</span><span class="sxs-lookup"><span data-stu-id="cec96-134">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="cec96-135">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="cec96-135">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="cec96-136">Mensaje</span><span class="sxs-lookup"><span data-stu-id="cec96-136">Message</span></span> 

<span data-ttu-id="cec96-137">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cec96-137">The message of the dialog box.</span></span>

> <span data-ttu-id="cec96-138">[mensaje](#message) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="cec96-138">public string [Message](#message)</span></span>

<span data-ttu-id="cec96-139">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="cec96-139">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="cec96-140">ResultText</span><span class="sxs-lookup"><span data-stu-id="cec96-140">ResultText</span></span> 

<span data-ttu-id="cec96-141">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="cec96-141">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="cec96-142">cadena pública [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="cec96-142">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="cec96-143">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="cec96-143">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="cec96-144">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="cec96-144">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="cec96-145">URI</span><span class="sxs-lookup"><span data-stu-id="cec96-145">Uri</span></span> 

<span data-ttu-id="cec96-146">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cec96-146">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="cec96-147">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="cec96-147">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="cec96-148">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cec96-148">Accept</span></span> 

<span data-ttu-id="cec96-149">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="cec96-149">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="cec96-150">[Accept](#accept)public void ()</span><span class="sxs-lookup"><span data-stu-id="cec96-150">public void [Accept](#accept)()</span></span>

<span data-ttu-id="cec96-151">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="cec96-151">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="cec96-152">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="cec96-152">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="cec96-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cec96-153">GetDeferral</span></span> 

<span data-ttu-id="cec96-154">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="cec96-154">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="cec96-155">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="cec96-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="cec96-156">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="cec96-156">You can use this to complete the event at a later time.</span></span>

