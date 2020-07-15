---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 40215d0c32b30000a93f59343547d60fc377ba03
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877325"
---
# <span data-ttu-id="cda6a-104">0.9.515: ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cda6a-104">0.9.515 - interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="cda6a-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="cda6a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="cda6a-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="cda6a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="cda6a-107">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="cda6a-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="cda6a-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="cda6a-108">Summary</span></span>

 <span data-ttu-id="cda6a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cda6a-109">Members</span></span>                        | <span data-ttu-id="cda6a-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cda6a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cda6a-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="cda6a-111">get_Source</span></span>](#get_source) | <span data-ttu-id="cda6a-112">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="cda6a-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="cda6a-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="cda6a-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="cda6a-114">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="cda6a-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="cda6a-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="cda6a-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="cda6a-116">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="cda6a-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="cda6a-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="cda6a-117">Members</span></span>

#### <span data-ttu-id="cda6a-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="cda6a-118">get_Source</span></span> 

<span data-ttu-id="cda6a-119">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="cda6a-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="cda6a-120">[get_Source](#get_source)de HRESULT público (código LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="cda6a-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="cda6a-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="cda6a-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="cda6a-122">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="cda6a-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="cda6a-123">[get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="cda6a-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="cda6a-124">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cda6a-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="cda6a-125">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="cda6a-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="cda6a-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="cda6a-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="cda6a-127">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="cda6a-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="cda6a-128">[TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="cda6a-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="cda6a-129">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="cda6a-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="cda6a-130">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="cda6a-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="cda6a-131">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="cda6a-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

