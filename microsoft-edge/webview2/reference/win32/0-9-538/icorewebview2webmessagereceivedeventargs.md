---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 58bb4b7f34b2917ec16ead051d1df8d6e6885f6d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010386"
---
# <span data-ttu-id="d1cdd-104">0.9.579: ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d1cdd-104">0.9.579 - interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="d1cdd-105">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="d1cdd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="d1cdd-106">Summary</span></span>

 <span data-ttu-id="d1cdd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1cdd-107">Members</span></span>                        | <span data-ttu-id="d1cdd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d1cdd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1cdd-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="d1cdd-109">get_Source</span></span>](#get_source) | <span data-ttu-id="d1cdd-110">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="d1cdd-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d1cdd-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="d1cdd-112">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="d1cdd-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d1cdd-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="d1cdd-114">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="d1cdd-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1cdd-115">Members</span></span>

#### <span data-ttu-id="d1cdd-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="d1cdd-116">get_Source</span></span> 

<span data-ttu-id="d1cdd-117">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="d1cdd-118">[get_Source](#get_source)de HRESULT público (código LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="d1cdd-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="d1cdd-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d1cdd-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="d1cdd-120">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="d1cdd-121">[get_WebMessageAsJson](#get_webmessageasjson)de HRESULT público (LPWStr \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="d1cdd-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="d1cdd-122">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="d1cdd-123">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="d1cdd-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="d1cdd-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d1cdd-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="d1cdd-125">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="d1cdd-126">[TRYGETWEBMESSAGEASSTRING](#trygetwebmessageasstring)HRESULT público (LPWStr \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="d1cdd-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="d1cdd-127">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="d1cdd-128">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="d1cdd-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="d1cdd-129">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="d1cdd-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

