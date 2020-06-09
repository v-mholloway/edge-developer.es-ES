---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 33450805c7f5117806feb1fb561cd7e0c364f00e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698102"
---
# <span data-ttu-id="7a9b4-104">interfaz ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="7a9b4-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7a9b4-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7a9b4-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="7a9b4-107">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="7a9b4-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7a9b4-108">Summary</span></span>

 <span data-ttu-id="7a9b4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a9b4-109">Members</span></span>                        | <span data-ttu-id="7a9b4-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7a9b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a9b4-111">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7a9b4-111">Accept</span></span>](#accept) | <span data-ttu-id="7a9b4-112">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-112">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="7a9b4-113">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="7a9b4-113">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="7a9b4-114">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="7a9b4-115">get_Kind</span><span class="sxs-lookup"><span data-stu-id="7a9b4-115">get_Kind</span></span>](#get_kind) | <span data-ttu-id="7a9b4-116">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="7a9b4-117">get_Message</span><span class="sxs-lookup"><span data-stu-id="7a9b4-117">get_Message</span></span>](#get_message) | <span data-ttu-id="7a9b4-118">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-118">The message of the dialog box.</span></span>
[<span data-ttu-id="7a9b4-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="7a9b4-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="7a9b4-120">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="7a9b4-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7a9b4-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="7a9b4-122">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="7a9b4-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7a9b4-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="7a9b4-124">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="7a9b4-124">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="7a9b4-125">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="7a9b4-125">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="7a9b4-126">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-126">Set the ResultText property.</span></span>

## <span data-ttu-id="7a9b4-127">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a9b4-127">Members</span></span>

#### <span data-ttu-id="7a9b4-128">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7a9b4-128">Accept</span></span> 

<span data-ttu-id="7a9b4-129">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-129">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="7a9b4-130">[aceptación](#accept)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="7a9b4-130">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="7a9b4-131">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-131">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="7a9b4-132">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-132">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="7a9b4-133">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="7a9b4-133">get_DefaultText</span></span> 

<span data-ttu-id="7a9b4-134">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-134">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="7a9b4-135">[get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-135">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="7a9b4-136">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-136">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="7a9b4-137">get_Kind</span><span class="sxs-lookup"><span data-stu-id="7a9b4-137">get_Kind</span></span> 

<span data-ttu-id="7a9b4-138">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-138">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="7a9b4-139">[get_Kind](#get_kind)de HRESULT público (COREWEBVIEW2_SCRIPT_DIALOG_KIND \* tipo)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-139">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="7a9b4-140">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-140">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="7a9b4-141">get_Message</span><span class="sxs-lookup"><span data-stu-id="7a9b4-141">get_Message</span></span> 

<span data-ttu-id="7a9b4-142">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-142">The message of the dialog box.</span></span>

> <span data-ttu-id="7a9b4-143">[get_Message](#get_message)de HRESULT público (mensaje LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-143">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="7a9b4-144">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-144">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="7a9b4-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="7a9b4-145">get_ResultText</span></span> 

<span data-ttu-id="7a9b4-146">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="7a9b4-147">[get_ResultText](#get_resulttext)de HRESULT público (LPWStr \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="7a9b4-148">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="7a9b4-149">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="7a9b4-150">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7a9b4-150">get_Uri</span></span> 

<span data-ttu-id="7a9b4-151">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-151">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="7a9b4-152">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-152">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="7a9b4-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7a9b4-153">GetDeferral</span></span> 

<span data-ttu-id="7a9b4-154">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="7a9b4-154">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="7a9b4-155">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="7a9b4-156">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-156">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="7a9b4-157">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="7a9b4-157">put_ResultText</span></span> 

<span data-ttu-id="7a9b4-158">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="7a9b4-158">Set the ResultText property.</span></span>

> <span data-ttu-id="7a9b4-159">[put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="7a9b4-159">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

