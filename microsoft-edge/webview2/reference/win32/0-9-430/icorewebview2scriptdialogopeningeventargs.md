---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: cd8f96787d289ab0fe649244ce665445efdbcecf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884046"
---
# <span data-ttu-id="f80cd-104">0.9.430: ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="f80cd-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="f80cd-105">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="f80cd-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="f80cd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="f80cd-106">Summary</span></span>

 <span data-ttu-id="f80cd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f80cd-107">Members</span></span>                        | <span data-ttu-id="f80cd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f80cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f80cd-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f80cd-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f80cd-110">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f80cd-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="f80cd-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="f80cd-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="f80cd-112">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f80cd-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="f80cd-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="f80cd-113">get_Message</span></span>](#get_message) | <span data-ttu-id="f80cd-114">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f80cd-114">The message of the dialog box.</span></span>
[<span data-ttu-id="f80cd-115">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f80cd-115">Accept</span></span>](#accept) | <span data-ttu-id="f80cd-116">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="f80cd-116">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="f80cd-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="f80cd-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="f80cd-118">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f80cd-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="f80cd-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="f80cd-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="f80cd-120">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="f80cd-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="f80cd-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="f80cd-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="f80cd-122">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="f80cd-122">Set the ResultText property.</span></span>
[<span data-ttu-id="f80cd-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f80cd-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f80cd-124">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="f80cd-124">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="f80cd-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="f80cd-125">Members</span></span>

#### <span data-ttu-id="f80cd-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f80cd-126">get_Uri</span></span> 

<span data-ttu-id="f80cd-127">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f80cd-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="f80cd-128">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="f80cd-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f80cd-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="f80cd-129">get_Kind</span></span> 

<span data-ttu-id="f80cd-130">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f80cd-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="f80cd-131">[get_Kind](#get_kind)de HRESULT público (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* tipo)</span><span class="sxs-lookup"><span data-stu-id="f80cd-131">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="f80cd-132">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="f80cd-132">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="f80cd-133">get_Message</span><span class="sxs-lookup"><span data-stu-id="f80cd-133">get_Message</span></span> 

<span data-ttu-id="f80cd-134">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f80cd-134">The message of the dialog box.</span></span>

> <span data-ttu-id="f80cd-135">[get_Message](#get_message)de HRESULT público (mensaje LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="f80cd-135">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="f80cd-136">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="f80cd-136">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="f80cd-137">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f80cd-137">Accept</span></span> 

<span data-ttu-id="f80cd-138">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="f80cd-138">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="f80cd-139">[aceptación](#accept)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="f80cd-139">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="f80cd-140">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="f80cd-140">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="f80cd-141">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f80cd-141">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="f80cd-142">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="f80cd-142">get_DefaultText</span></span> 

<span data-ttu-id="f80cd-143">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f80cd-143">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="f80cd-144">[get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="f80cd-144">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="f80cd-145">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="f80cd-145">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="f80cd-146">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="f80cd-146">get_ResultText</span></span> 

<span data-ttu-id="f80cd-147">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="f80cd-147">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="f80cd-148">[get_ResultText](#get_resulttext)de HRESULT público (LPWStr \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="f80cd-148">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="f80cd-149">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="f80cd-149">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="f80cd-150">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="f80cd-150">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="f80cd-151">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="f80cd-151">put_ResultText</span></span> 

<span data-ttu-id="f80cd-152">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="f80cd-152">Set the ResultText property.</span></span>

> <span data-ttu-id="f80cd-153">[put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="f80cd-153">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="f80cd-154">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f80cd-154">GetDeferral</span></span> 

<span data-ttu-id="f80cd-155">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="f80cd-155">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="f80cd-156">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="f80cd-156">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f80cd-157">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="f80cd-157">You can use this to complete the event at a later time.</span></span>

