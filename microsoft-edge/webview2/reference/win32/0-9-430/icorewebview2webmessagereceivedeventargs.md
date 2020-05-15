---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: f3002c6e7941cea1f632e1df4ee42a8f38a468b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655457"
---
# <span data-ttu-id="51a18-104">interfaz ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="51a18-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="51a18-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="51a18-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="51a18-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="51a18-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="51a18-107">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="51a18-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="51a18-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="51a18-108">Summary</span></span>

 <span data-ttu-id="51a18-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="51a18-109">Members</span></span>                        | <span data-ttu-id="51a18-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="51a18-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="51a18-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="51a18-111">get_Source</span></span>](#get_source) | <span data-ttu-id="51a18-112">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="51a18-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="51a18-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="51a18-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="51a18-114">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="51a18-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="51a18-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="51a18-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="51a18-116">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="51a18-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="51a18-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="51a18-117">Members</span></span>

#### <span data-ttu-id="51a18-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="51a18-118">get_Source</span></span> 

<span data-ttu-id="51a18-119">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="51a18-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="51a18-120">[get_Source](#get_source)de HRESULT público (código LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="51a18-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="51a18-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="51a18-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="51a18-122">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="51a18-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="51a18-123">[get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="51a18-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="51a18-124">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="51a18-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="51a18-125">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="51a18-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="51a18-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="51a18-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="51a18-127">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="51a18-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="51a18-128">[TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="51a18-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="51a18-129">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="51a18-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="51a18-130">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="51a18-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="51a18-131">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="51a18-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

