---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885796"
---
# <span data-ttu-id="b55ca-104">0.8.355: IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="b55ca-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="b55ca-105">Argumentos de evento para el evento [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="b55ca-105">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="b55ca-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b55ca-106">Summary</span></span>

 <span data-ttu-id="b55ca-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b55ca-107">Members</span></span>                        | <span data-ttu-id="b55ca-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b55ca-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b55ca-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b55ca-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b55ca-110">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b55ca-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="b55ca-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="b55ca-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="b55ca-112">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b55ca-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="b55ca-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="b55ca-113">get_Message</span></span>](#get_message) | <span data-ttu-id="b55ca-114">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b55ca-114">The message of the dialog box.</span></span>
[<span data-ttu-id="b55ca-115">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b55ca-115">Accept</span></span>](#accept) | <span data-ttu-id="b55ca-116">El anfitrión puede llamarlo para responder con aceptar para confirmar y pedir diálogos, o no llamar a este método para indicar que es cancelado.</span><span class="sxs-lookup"><span data-stu-id="b55ca-116">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="b55ca-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="b55ca-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="b55ca-118">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b55ca-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="b55ca-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="b55ca-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="b55ca-120">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="b55ca-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="b55ca-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="b55ca-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="b55ca-122">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="b55ca-122">Set the ResultText property.</span></span>
[<span data-ttu-id="b55ca-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b55ca-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b55ca-124">Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b55ca-124">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="b55ca-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="b55ca-125">Members</span></span>

#### <span data-ttu-id="b55ca-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b55ca-126">get_Uri</span></span> 

<span data-ttu-id="b55ca-127">Identificador URI de la página que solicitó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b55ca-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="b55ca-128">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="b55ca-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b55ca-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="b55ca-129">get_Kind</span></span> 

<span data-ttu-id="b55ca-130">El cuadro de diálogo tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b55ca-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="b55ca-131">[get_Kind](#get_kind)de HRESULT público (WEBVIEW2_SCRIPT_DIALOG_KIND \* tipo)</span><span class="sxs-lookup"><span data-stu-id="b55ca-131">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="b55ca-132">get_Message</span><span class="sxs-lookup"><span data-stu-id="b55ca-132">get_Message</span></span> 

<span data-ttu-id="b55ca-133">Mensaje del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b55ca-133">The message of the dialog box.</span></span>

> <span data-ttu-id="b55ca-134">[get_Message](#get_message)de HRESULT público (mensaje LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="b55ca-134">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="b55ca-135">Desde JavaScript este es el primer parámetro que se pasa a Alert, confirm y prompt.</span><span class="sxs-lookup"><span data-stu-id="b55ca-135">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="b55ca-136">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b55ca-136">Accept</span></span> 

<span data-ttu-id="b55ca-137">El anfitrión puede llamarlo para responder con aceptar para confirmar y pedir diálogos, o no llamar a este método para indicar que es cancelado.</span><span class="sxs-lookup"><span data-stu-id="b55ca-137">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="b55ca-138">[aceptación](#accept)pública de HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="b55ca-138">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="b55ca-139">Desde JavaScript esto significa que la función CONFIRM devuelve true si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="b55ca-139">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="b55ca-140">Y para la función prompt, devuelve el valor de ResultText si se llama a Accept y devuelve false de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="b55ca-140">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="b55ca-141">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="b55ca-141">get_DefaultText</span></span> 

<span data-ttu-id="b55ca-142">El segundo parámetro que se pasa al cuadro de diálogo del símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b55ca-142">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="b55ca-143">[get_DefaultText](#get_defaulttext)de HRESULT público (LPWStr \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="b55ca-143">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="b55ca-144">Este es el valor predeterminado para usar en el resultado de la función pregunta.</span><span class="sxs-lookup"><span data-stu-id="b55ca-144">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="b55ca-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="b55ca-145">get_ResultText</span></span> 

<span data-ttu-id="b55ca-146">El valor devuelto por la función prompt de JavaScript, si se llama a Accept.</span><span class="sxs-lookup"><span data-stu-id="b55ca-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="b55ca-147">[get_ResultText](#get_resulttext)de HRESULT público (LPWStr \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="b55ca-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="b55ca-148">Esto se omite en los tipos de diálogo que no sean preguntar.</span><span class="sxs-lookup"><span data-stu-id="b55ca-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="b55ca-149">Si no se llama a Accept, se omite este valor y se devuelve false desde prompt.</span><span class="sxs-lookup"><span data-stu-id="b55ca-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="b55ca-150">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="b55ca-150">put_ResultText</span></span> 

<span data-ttu-id="b55ca-151">Establezca la propiedad ResultText.</span><span class="sxs-lookup"><span data-stu-id="b55ca-151">Set the ResultText property.</span></span>

> <span data-ttu-id="b55ca-152">[put_ResultText](#put_resulttext)pública HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="b55ca-152">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="b55ca-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b55ca-153">GetDeferral</span></span> 

<span data-ttu-id="b55ca-154">Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b55ca-154">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="b55ca-155">[GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="b55ca-155">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b55ca-156">Puedes usarlo para completar el evento en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="b55ca-156">You can use this to complete the event at a later time.</span></span>

