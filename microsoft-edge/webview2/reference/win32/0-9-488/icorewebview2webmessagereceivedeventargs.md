---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: c57c0df57915361e2d32024a5512616dea96a923
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655413"
---
# <span data-ttu-id="fc910-104">interfaz ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="fc910-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="fc910-105">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="fc910-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="fc910-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="fc910-106">Summary</span></span>

 <span data-ttu-id="fc910-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc910-107">Members</span></span>                        | <span data-ttu-id="fc910-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fc910-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc910-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="fc910-109">get_Source</span></span>](#get_source) | <span data-ttu-id="fc910-110">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="fc910-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="fc910-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="fc910-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="fc910-112">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="fc910-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="fc910-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="fc910-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="fc910-114">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="fc910-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="fc910-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc910-115">Members</span></span>

#### <span data-ttu-id="fc910-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="fc910-116">get_Source</span></span> 

<span data-ttu-id="fc910-117">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="fc910-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="fc910-118">[get_Source](#get_source)de HRESULT público (código LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="fc910-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="fc910-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="fc910-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="fc910-120">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="fc910-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="fc910-121">[get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="fc910-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="fc910-122">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fc910-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="fc910-123">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="fc910-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="fc910-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="fc910-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="fc910-125">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="fc910-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="fc910-126">[TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="fc910-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="fc910-127">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="fc910-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="fc910-128">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="fc910-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="fc910-129">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="fc910-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

