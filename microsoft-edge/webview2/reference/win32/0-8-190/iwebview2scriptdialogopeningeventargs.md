---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 867a8f3656b04a566708fc6fc1a24e80b967c1e2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655092"
---
# <span data-ttu-id="60b22-104">interfaz IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="60b22-104">interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="60b22-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="60b22-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="60b22-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="60b22-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="60b22-107">Argumentos de evento para el evento [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="60b22-107">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="60b22-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="60b22-108">Summary</span></span>

 <span data-ttu-id="60b22-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="60b22-109">Members</span></span>                        | <span data-ttu-id="60b22-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="60b22-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="60b22-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="60b22-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="60b22-112">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="60b22-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="60b22-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="60b22-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="60b22-114">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60b22-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="60b22-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="60b22-115">get_Message</span></span>](#get_message) | <span data-ttu-id="60b22-116">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="60b22-116">The message of the dialog box.</span></span>
[<span data-ttu-id="60b22-117">Aceptar</span><span class="sxs-lookup"><span data-stu-id="60b22-117">Accept</span></span>](#accept) | <span data-ttu-id="60b22-118">El anfitrión puede llamarlo para responder con aceptar para confirmar y pedir diálogos, o no llamar a este método para indicar que es cancelado.</span><span class="sxs-lookup"><span data-stu-id="60b22-118">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="60b22-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="60b22-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="60b22-120">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60b22-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="60b22-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="60b22-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="60b22-122">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="60b22-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="60b22-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="60b22-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="60b22-124">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="60b22-124">Set the ResultText property.</span></span>
[<span data-ttu-id="60b22-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="60b22-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="60b22-126">Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="60b22-126">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="60b22-127">Miembros</span><span class="sxs-lookup"><span data-stu-id="60b22-127">Members</span></span>

#### <span data-ttu-id="60b22-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="60b22-128">get_Uri</span></span> 

<span data-ttu-id="60b22-129">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="60b22-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="60b22-130">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="60b22-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="60b22-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="60b22-131">get_Kind</span></span> 

<span data-ttu-id="60b22-132">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60b22-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="60b22-133">[get_Kind](#get_kind)de HRESULT público (WEBVIEW2_SCRIPT_DIALOG_KIND \* tipo)</span><span class="sxs-lookup"><span data-stu-id="60b22-133">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="60b22-134">get_Message</span><span class="sxs-lookup"><span data-stu-id="60b22-134">get_Message</span></span> 

<span data-ttu-id="60b22-135">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="60b22-135">The message of the dialog box.</span></span>

> <span data-ttu-id="60b22-136">[get_Message](#get_message)de HRESULT público (mensaje LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="60b22-136">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="60b22-137">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt.</span><span class="sxs-lookup"><span data-stu-id="60b22-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="60b22-138">Aceptar</span><span class="sxs-lookup"><span data-stu-id="60b22-138">Accept</span></span> 

<span data-ttu-id="60b22-139">El anfitrión puede llamarlo para responder con aceptar para confirmar y pedir diálogos, o no llamar a este método para indicar que es cancelado.</span><span class="sxs-lookup"><span data-stu-id="60b22-139">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="60b22-140">[aceptación](#accept)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="60b22-140">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="60b22-141">Desde JavaScript esto significa que la función CONFIRM devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="60b22-141">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="60b22-142">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="60b22-142">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="60b22-143">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="60b22-143">get_DefaultText</span></span> 

<span data-ttu-id="60b22-144">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="60b22-144">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="60b22-145">[get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="60b22-145">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="60b22-146">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="60b22-146">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="60b22-147">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="60b22-147">get_ResultText</span></span> 

<span data-ttu-id="60b22-148">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="60b22-148">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="60b22-149">[get_ResultText](#get_resulttext)de HRESULT público (LPWStr \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="60b22-149">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="60b22-150">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="60b22-150">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="60b22-151">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="60b22-151">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="60b22-152">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="60b22-152">put_ResultText</span></span> 

<span data-ttu-id="60b22-153">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="60b22-153">Set the ResultText property.</span></span>

> <span data-ttu-id="60b22-154">[put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="60b22-154">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="60b22-155">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="60b22-155">GetDeferral</span></span> 

<span data-ttu-id="60b22-156">Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="60b22-156">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="60b22-157">[GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="60b22-157">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="60b22-158">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="60b22-158">You can use this to complete the event at a later time.</span></span>

