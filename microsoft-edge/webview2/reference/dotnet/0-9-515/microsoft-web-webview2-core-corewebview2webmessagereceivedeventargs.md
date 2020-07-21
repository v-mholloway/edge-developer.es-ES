---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a3d1f899cb270f9a44d92d647ab2f5a4d5c3b02a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886370"
---
# <span data-ttu-id="73f69-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="73f69-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="73f69-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="73f69-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="73f69-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="73f69-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="73f69-107">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="73f69-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="73f69-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="73f69-108">Summary</span></span>

 <span data-ttu-id="73f69-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="73f69-109">Members</span></span>                        | <span data-ttu-id="73f69-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="73f69-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="73f69-111">Source</span><span class="sxs-lookup"><span data-stu-id="73f69-111">Source</span></span>](#source) | <span data-ttu-id="73f69-112">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="73f69-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="73f69-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="73f69-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="73f69-114">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="73f69-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="73f69-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="73f69-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="73f69-116">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="73f69-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="73f69-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="73f69-117">Members</span></span>

#### <span data-ttu-id="73f69-118">Source</span><span class="sxs-lookup"><span data-stu-id="73f69-118">Source</span></span> 

<span data-ttu-id="73f69-119">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="73f69-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="73f69-120">[origen](#source) de cadena público</span><span class="sxs-lookup"><span data-stu-id="73f69-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="73f69-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="73f69-121">WebMessageAsJson</span></span> 

<span data-ttu-id="73f69-122">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="73f69-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="73f69-123">cadena pública [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="73f69-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="73f69-124">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="73f69-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="73f69-125">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="73f69-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="73f69-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="73f69-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="73f69-127">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="73f69-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="73f69-128">cadena pública [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="73f69-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="73f69-129">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="73f69-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="73f69-130">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="73f69-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="73f69-131">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="73f69-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

