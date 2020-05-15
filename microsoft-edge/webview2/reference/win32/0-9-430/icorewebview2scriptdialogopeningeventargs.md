---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8ed1a10a65a07fc359deea18b8aadd4df3a7b055
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655503"
---
# <span data-ttu-id="7d1fb-104">interfaz ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="7d1fb-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7d1fb-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7d1fb-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="7d1fb-107">Argumentos de evento para el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="7d1fb-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7d1fb-108">Summary</span></span>

 <span data-ttu-id="7d1fb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d1fb-109">Members</span></span>                        | <span data-ttu-id="7d1fb-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7d1fb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7d1fb-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7d1fb-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="7d1fb-112">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="7d1fb-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="7d1fb-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="7d1fb-114">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="7d1fb-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="7d1fb-115">get_Message</span></span>](#get_message) | <span data-ttu-id="7d1fb-116">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-116">The message of the dialog box.</span></span>
[<span data-ttu-id="7d1fb-117">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7d1fb-117">Accept</span></span>](#accept) | <span data-ttu-id="7d1fb-118">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="7d1fb-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="7d1fb-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="7d1fb-120">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="7d1fb-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="7d1fb-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="7d1fb-122">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="7d1fb-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="7d1fb-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="7d1fb-124">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-124">Set the ResultText property.</span></span>
[<span data-ttu-id="7d1fb-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7d1fb-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="7d1fb-126">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="7d1fb-127">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d1fb-127">Members</span></span>

#### <span data-ttu-id="7d1fb-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7d1fb-128">get_Uri</span></span> 

<span data-ttu-id="7d1fb-129">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="7d1fb-130">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="7d1fb-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="7d1fb-131">get_Kind</span></span> 

<span data-ttu-id="7d1fb-132">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="7d1fb-133">[get_Kind](#get_kind)de HRESULT público (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* tipo)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="7d1fb-134">Aceptar, confirmar, solicitar o beforeunload.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="7d1fb-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="7d1fb-135">get_Message</span></span> 

<span data-ttu-id="7d1fb-136">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-136">The message of the dialog box.</span></span>

> <span data-ttu-id="7d1fb-137">[get_Message](#get_message)de HRESULT público (mensaje LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="7d1fb-138">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt, y está vacío para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="7d1fb-139">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7d1fb-139">Accept</span></span> 

<span data-ttu-id="7d1fb-140">El anfitrión puede llamarlo para responder con aceptar para confirmar, preguntar y beforeunload cuadros de diálogo, o no llamar a este método para indicar la cancelación.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="7d1fb-141">[aceptación](#accept)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="7d1fb-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="7d1fb-142">Desde JavaScript, esto significa que la función confirm y beforeunload devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="7d1fb-143">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="7d1fb-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="7d1fb-144">get_DefaultText</span></span> 

<span data-ttu-id="7d1fb-145">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="7d1fb-146">[get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="7d1fb-147">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="7d1fb-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="7d1fb-148">get_ResultText</span></span> 

<span data-ttu-id="7d1fb-149">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="7d1fb-150">[get_ResultText](#get_resulttext)de HRESULT público (LPWStr \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="7d1fb-151">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="7d1fb-152">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="7d1fb-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="7d1fb-153">put_ResultText</span></span> 

<span data-ttu-id="7d1fb-154">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-154">Set the ResultText property.</span></span>

> <span data-ttu-id="7d1fb-155">[put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="7d1fb-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7d1fb-156">GetDeferral</span></span> 

<span data-ttu-id="7d1fb-157">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="7d1fb-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="7d1fb-158">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="7d1fb-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="7d1fb-159">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="7d1fb-159">You can use this to complete the event at a later time.</span></span>

