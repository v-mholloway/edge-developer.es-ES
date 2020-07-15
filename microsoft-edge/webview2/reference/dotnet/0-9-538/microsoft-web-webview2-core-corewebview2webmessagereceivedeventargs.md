---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 01c6a22ec84b85437920dceb66072089fd6d0d93
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879663"
---
# <span data-ttu-id="5241b-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5241b-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="5241b-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="5241b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="5241b-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="5241b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="5241b-107">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="5241b-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="5241b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="5241b-108">Summary</span></span>

 <span data-ttu-id="5241b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5241b-109">Members</span></span>                        | <span data-ttu-id="5241b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5241b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5241b-111">Source</span><span class="sxs-lookup"><span data-stu-id="5241b-111">Source</span></span>](#source) | <span data-ttu-id="5241b-112">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="5241b-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="5241b-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="5241b-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="5241b-114">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="5241b-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="5241b-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="5241b-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="5241b-116">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="5241b-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="5241b-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="5241b-117">Members</span></span>

#### <span data-ttu-id="5241b-118">Source</span><span class="sxs-lookup"><span data-stu-id="5241b-118">Source</span></span> 

<span data-ttu-id="5241b-119">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="5241b-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="5241b-120">[origen](#source) de cadena público</span><span class="sxs-lookup"><span data-stu-id="5241b-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="5241b-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="5241b-121">WebMessageAsJson</span></span> 

<span data-ttu-id="5241b-122">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="5241b-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="5241b-123">cadena pública [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="5241b-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="5241b-124">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5241b-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="5241b-125">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="5241b-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="5241b-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="5241b-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="5241b-127">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="5241b-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="5241b-128">cadena pública [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="5241b-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="5241b-129">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5241b-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="5241b-130">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="5241b-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="5241b-131">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="5241b-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

