---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c619c066151941f1177d55c973569c89f03daa2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880167"
---
# <span data-ttu-id="0b1fd-104">0.9.430: ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0b1fd-104">0.9.430 - interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="0b1fd-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="0b1fd-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="0b1fd-107">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="0b1fd-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="0b1fd-108">Summary</span></span>

 <span data-ttu-id="0b1fd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b1fd-109">Members</span></span>                        | <span data-ttu-id="0b1fd-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0b1fd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b1fd-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="0b1fd-111">get_Source</span></span>](#get_source) | <span data-ttu-id="0b1fd-112">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="0b1fd-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="0b1fd-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="0b1fd-114">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="0b1fd-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="0b1fd-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="0b1fd-116">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="0b1fd-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b1fd-117">Members</span></span>

#### <span data-ttu-id="0b1fd-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="0b1fd-118">get_Source</span></span> 

<span data-ttu-id="0b1fd-119">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="0b1fd-120">[get_Source](#get_source)de HRESULT público (código LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="0b1fd-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="0b1fd-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="0b1fd-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="0b1fd-122">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="0b1fd-123">[get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="0b1fd-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="0b1fd-124">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="0b1fd-125">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="0b1fd-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="0b1fd-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="0b1fd-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="0b1fd-127">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="0b1fd-128">[TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="0b1fd-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="0b1fd-129">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="0b1fd-130">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="0b1fd-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="0b1fd-131">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="0b1fd-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

