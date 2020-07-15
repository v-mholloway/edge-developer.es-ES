---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 61805f34ac3ef3a51dcd5b746b77a7bdad8cdb5c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877605"
---
# <span data-ttu-id="7110f-104">interfaz ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7110f-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="7110f-105">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="7110f-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="7110f-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7110f-106">Summary</span></span>

 <span data-ttu-id="7110f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7110f-107">Members</span></span>                        | <span data-ttu-id="7110f-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7110f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7110f-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="7110f-109">get_Source</span></span>](#get_source) | <span data-ttu-id="7110f-110">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="7110f-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="7110f-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="7110f-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="7110f-112">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="7110f-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="7110f-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="7110f-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="7110f-114">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="7110f-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="7110f-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="7110f-115">Members</span></span>

#### <span data-ttu-id="7110f-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="7110f-116">get_Source</span></span> 

<span data-ttu-id="7110f-117">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="7110f-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="7110f-118">[get_Source](#get_source)de HRESULT público (código LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="7110f-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="7110f-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="7110f-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="7110f-120">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="7110f-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="7110f-121">[get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="7110f-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="7110f-122">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7110f-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="7110f-123">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="7110f-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="7110f-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="7110f-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="7110f-125">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="7110f-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="7110f-126">[TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="7110f-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="7110f-127">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="7110f-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="7110f-128">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="7110f-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="7110f-129">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="7110f-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

