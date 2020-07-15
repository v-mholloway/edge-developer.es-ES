---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ff4ebd8dc3a1c78424d57f6c7b5e6f7fc8e99049
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879320"
---
# <span data-ttu-id="1d74e-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="1d74e-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="1d74e-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1d74e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1d74e-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="1d74e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="1d74e-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1d74e-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1d74e-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="1d74e-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1d74e-109">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="1d74e-109">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="1d74e-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="1d74e-110">Summary</span></span>

 <span data-ttu-id="1d74e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d74e-111">Members</span></span>                        | <span data-ttu-id="1d74e-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1d74e-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1d74e-113">Source</span><span class="sxs-lookup"><span data-stu-id="1d74e-113">Source</span></span>](#source) | <span data-ttu-id="1d74e-114">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="1d74e-114">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="1d74e-115">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="1d74e-115">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="1d74e-116">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="1d74e-116">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="1d74e-117">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="1d74e-117">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="1d74e-118">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="1d74e-118">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="1d74e-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d74e-119">Members</span></span>

#### <span data-ttu-id="1d74e-120">Source</span><span class="sxs-lookup"><span data-stu-id="1d74e-120">Source</span></span> 

<span data-ttu-id="1d74e-121">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="1d74e-121">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="1d74e-122">[origen](#source) de cadena público</span><span class="sxs-lookup"><span data-stu-id="1d74e-122">public string [Source](#source)</span></span>

#### <span data-ttu-id="1d74e-123">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="1d74e-123">WebMessageAsJson</span></span> 

<span data-ttu-id="1d74e-124">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="1d74e-124">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="1d74e-125">cadena pública [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="1d74e-125">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="1d74e-126">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1d74e-126">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="1d74e-127">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="1d74e-127">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="1d74e-128">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="1d74e-128">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="1d74e-129">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="1d74e-129">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="1d74e-130">cadena pública [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="1d74e-130">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="1d74e-131">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1d74e-131">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="1d74e-132">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="1d74e-132">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="1d74e-133">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="1d74e-133">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

