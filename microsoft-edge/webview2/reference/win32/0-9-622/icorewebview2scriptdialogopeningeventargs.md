---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: 442bd26caeb78804ceb202b302123b0ee1127f09
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012718"
---
# <span data-ttu-id="e879e-104">interfaz ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="e879e-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="e879e-105">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="e879e-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="e879e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e879e-106">Summary</span></span>

 <span data-ttu-id="e879e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e879e-107">Members</span></span>                        | <span data-ttu-id="e879e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e879e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e879e-109">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e879e-109">Accept</span></span>](#accept) | <span data-ttu-id="e879e-110">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="e879e-110">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="e879e-111">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="e879e-111">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="e879e-112">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e879e-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="e879e-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="e879e-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="e879e-114">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e879e-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="e879e-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="e879e-115">get_Message</span></span>](#get_message) | <span data-ttu-id="e879e-116">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e879e-116">The message of the dialog box.</span></span>
[<span data-ttu-id="e879e-117">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="e879e-117">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="e879e-118">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="e879e-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="e879e-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e879e-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e879e-120">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e879e-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="e879e-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e879e-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e879e-122">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="e879e-122">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="e879e-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="e879e-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="e879e-124">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="e879e-124">Set the ResultText property.</span></span>

## <span data-ttu-id="e879e-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="e879e-125">Members</span></span>

#### <span data-ttu-id="e879e-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e879e-126">Accept</span></span> 

<span data-ttu-id="e879e-127">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="e879e-127">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="e879e-128">[aceptación](#accept)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="e879e-128">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="e879e-129">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="e879e-129">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="e879e-130">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="e879e-130">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="e879e-131">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="e879e-131">get_DefaultText</span></span> 

<span data-ttu-id="e879e-132">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e879e-132">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="e879e-133">[get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="e879e-133">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="e879e-134">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="e879e-134">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="e879e-135">get_Kind</span><span class="sxs-lookup"><span data-stu-id="e879e-135">get_Kind</span></span> 

<span data-ttu-id="e879e-136">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e879e-136">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="e879e-137">[get_Kind](#get_kind)de HRESULT público (COREWEBVIEW2_SCRIPT_DIALOG_KIND \* tipo)</span><span class="sxs-lookup"><span data-stu-id="e879e-137">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="e879e-138">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="e879e-138">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="e879e-139">get_Message</span><span class="sxs-lookup"><span data-stu-id="e879e-139">get_Message</span></span> 

<span data-ttu-id="e879e-140">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e879e-140">The message of the dialog box.</span></span>

> <span data-ttu-id="e879e-141">[get_Message](#get_message)de HRESULT público (mensaje LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e879e-141">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="e879e-142">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="e879e-142">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="e879e-143">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="e879e-143">get_ResultText</span></span> 

<span data-ttu-id="e879e-144">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="e879e-144">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="e879e-145">[get_ResultText](#get_resulttext)de HRESULT público (LPWStr \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="e879e-145">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="e879e-146">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="e879e-146">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="e879e-147">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="e879e-147">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="e879e-148">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e879e-148">get_Uri</span></span> 

<span data-ttu-id="e879e-149">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e879e-149">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="e879e-150">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e879e-150">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e879e-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e879e-151">GetDeferral</span></span> 

<span data-ttu-id="e879e-152">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="e879e-152">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="e879e-153">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="e879e-153">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="e879e-154">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="e879e-154">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="e879e-155">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="e879e-155">put_ResultText</span></span> 

<span data-ttu-id="e879e-156">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="e879e-156">Set the ResultText property.</span></span>

> <span data-ttu-id="e879e-157">[put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="e879e-157">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

