---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a0372e9319a3dd260092b8bc96c693976b7f1fec
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880323"
---
# <span data-ttu-id="03481-104">0.9.515: ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="03481-104">0.9.515 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="03481-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="03481-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="03481-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="03481-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="03481-107">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="03481-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="03481-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="03481-108">Summary</span></span>

 <span data-ttu-id="03481-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="03481-109">Members</span></span>                        | <span data-ttu-id="03481-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="03481-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="03481-111">Aceptar</span><span class="sxs-lookup"><span data-stu-id="03481-111">Accept</span></span>](#accept) | <span data-ttu-id="03481-112">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="03481-112">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="03481-113">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="03481-113">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="03481-114">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="03481-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="03481-115">get_Kind</span><span class="sxs-lookup"><span data-stu-id="03481-115">get_Kind</span></span>](#get_kind) | <span data-ttu-id="03481-116">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="03481-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="03481-117">get_Message</span><span class="sxs-lookup"><span data-stu-id="03481-117">get_Message</span></span>](#get_message) | <span data-ttu-id="03481-118">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="03481-118">The message of the dialog box.</span></span>
[<span data-ttu-id="03481-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="03481-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="03481-120">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="03481-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="03481-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="03481-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="03481-122">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="03481-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="03481-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="03481-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="03481-124">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="03481-124">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="03481-125">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="03481-125">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="03481-126">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="03481-126">Set the ResultText property.</span></span>

## <span data-ttu-id="03481-127">Miembros</span><span class="sxs-lookup"><span data-stu-id="03481-127">Members</span></span>

#### <span data-ttu-id="03481-128">Aceptar</span><span class="sxs-lookup"><span data-stu-id="03481-128">Accept</span></span> 

<span data-ttu-id="03481-129">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="03481-129">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="03481-130">[aceptación](#accept)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="03481-130">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="03481-131">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="03481-131">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="03481-132">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="03481-132">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="03481-133">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="03481-133">get_DefaultText</span></span> 

<span data-ttu-id="03481-134">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="03481-134">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="03481-135">[get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="03481-135">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="03481-136">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="03481-136">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="03481-137">get_Kind</span><span class="sxs-lookup"><span data-stu-id="03481-137">get_Kind</span></span> 

<span data-ttu-id="03481-138">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="03481-138">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="03481-139">[get_Kind](#get_kind)de HRESULT público (COREWEBVIEW2_SCRIPT_DIALOG_KIND \* tipo)</span><span class="sxs-lookup"><span data-stu-id="03481-139">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="03481-140">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="03481-140">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="03481-141">get_Message</span><span class="sxs-lookup"><span data-stu-id="03481-141">get_Message</span></span> 

<span data-ttu-id="03481-142">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="03481-142">The message of the dialog box.</span></span>

> <span data-ttu-id="03481-143">[get_Message](#get_message)de HRESULT público (mensaje LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="03481-143">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="03481-144">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="03481-144">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="03481-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="03481-145">get_ResultText</span></span> 

<span data-ttu-id="03481-146">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="03481-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="03481-147">[get_ResultText](#get_resulttext)de HRESULT público (LPWStr \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="03481-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="03481-148">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="03481-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="03481-149">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="03481-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="03481-150">get_Uri</span><span class="sxs-lookup"><span data-stu-id="03481-150">get_Uri</span></span> 

<span data-ttu-id="03481-151">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="03481-151">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="03481-152">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="03481-152">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="03481-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="03481-153">GetDeferral</span></span> 

<span data-ttu-id="03481-154">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="03481-154">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="03481-155">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="03481-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="03481-156">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="03481-156">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="03481-157">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="03481-157">put_ResultText</span></span> 

<span data-ttu-id="03481-158">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="03481-158">Set the ResultText property.</span></span>

> <span data-ttu-id="03481-159">[put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="03481-159">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

