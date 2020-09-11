---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 36b5475b7af4537b640aac4bfec43f4850413b88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010484"
---
# <span data-ttu-id="61ce9-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="61ce9-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="61ce9-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="61ce9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="61ce9-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="61ce9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="61ce9-107">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="61ce9-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="61ce9-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="61ce9-108">Summary</span></span>

 <span data-ttu-id="61ce9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="61ce9-109">Members</span></span>                        | <span data-ttu-id="61ce9-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="61ce9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61ce9-111">Source</span><span class="sxs-lookup"><span data-stu-id="61ce9-111">Source</span></span>](#source) | <span data-ttu-id="61ce9-112">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="61ce9-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="61ce9-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="61ce9-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="61ce9-114">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="61ce9-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="61ce9-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="61ce9-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="61ce9-116">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="61ce9-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="61ce9-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="61ce9-117">Members</span></span>

#### <span data-ttu-id="61ce9-118">Source</span><span class="sxs-lookup"><span data-stu-id="61ce9-118">Source</span></span> 

<span data-ttu-id="61ce9-119">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="61ce9-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="61ce9-120">[origen](#source) de cadena público</span><span class="sxs-lookup"><span data-stu-id="61ce9-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="61ce9-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="61ce9-121">WebMessageAsJson</span></span> 

<span data-ttu-id="61ce9-122">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="61ce9-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="61ce9-123">cadena pública [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="61ce9-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="61ce9-124">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="61ce9-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="61ce9-125">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="61ce9-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="61ce9-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="61ce9-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="61ce9-127">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="61ce9-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="61ce9-128">cadena pública [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="61ce9-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="61ce9-129">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="61ce9-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="61ce9-130">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="61ce9-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="61ce9-131">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="61ce9-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

