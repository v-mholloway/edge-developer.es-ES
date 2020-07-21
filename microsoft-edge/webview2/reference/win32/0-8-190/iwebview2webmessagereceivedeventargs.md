---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 4dfe2296312ac3ff3e9c67667c660aafcea38211
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885761"
---
# <span data-ttu-id="aed7a-104">0.8.355: IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aed7a-104">0.8.355 - interface IWebView2WebMessageReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="aed7a-105">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="aed7a-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="aed7a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="aed7a-106">Summary</span></span>

 <span data-ttu-id="aed7a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="aed7a-107">Members</span></span>                        | <span data-ttu-id="aed7a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="aed7a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aed7a-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="aed7a-109">get_Source</span></span>](#get_source) | <span data-ttu-id="aed7a-110">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="aed7a-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="aed7a-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="aed7a-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="aed7a-112">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="aed7a-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="aed7a-113">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="aed7a-113">get_WebMessageAsString</span></span>](#get_webmessageasstring) | <span data-ttu-id="aed7a-114">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="aed7a-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="aed7a-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="aed7a-115">Members</span></span>

#### <span data-ttu-id="aed7a-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="aed7a-116">get_Source</span></span> 

<span data-ttu-id="aed7a-117">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="aed7a-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="aed7a-118">[get_Source](#get_source)de HRESULT público (código LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="aed7a-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="aed7a-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="aed7a-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="aed7a-120">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="aed7a-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="aed7a-121">[get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="aed7a-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="aed7a-122">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aed7a-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="aed7a-123">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="aed7a-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="aed7a-124">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="aed7a-124">get_WebMessageAsString</span></span> 

<span data-ttu-id="aed7a-125">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="aed7a-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="aed7a-126">[get_WebMessageAsString](#get_webmessageasstring)de HRESULT público (LPWStr \* WebMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="aed7a-126">public HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="aed7a-127">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="aed7a-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="aed7a-128">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="aed7a-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="aed7a-129">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="aed7a-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

