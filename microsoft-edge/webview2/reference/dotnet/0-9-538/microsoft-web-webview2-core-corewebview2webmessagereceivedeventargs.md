---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9babcaff5b90e22ea6bac5d5703a54caef6d349d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699476"
---
# <span data-ttu-id="8dbe1-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8dbe1-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="8dbe1-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8dbe1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8dbe1-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="8dbe1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8dbe1-107">Argumentos de evento para el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="8dbe1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="8dbe1-108">Summary</span></span>

 <span data-ttu-id="8dbe1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8dbe1-109">Members</span></span>                        | <span data-ttu-id="8dbe1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8dbe1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8dbe1-111">Source</span><span class="sxs-lookup"><span data-stu-id="8dbe1-111">Source</span></span>](#source) | <span data-ttu-id="8dbe1-112">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="8dbe1-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="8dbe1-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="8dbe1-114">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="8dbe1-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="8dbe1-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="8dbe1-116">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="8dbe1-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="8dbe1-117">Members</span></span>

#### <span data-ttu-id="8dbe1-118">Source</span><span class="sxs-lookup"><span data-stu-id="8dbe1-118">Source</span></span> 

<span data-ttu-id="8dbe1-119">El URI del documento que envió este mensaje Web.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="8dbe1-120">[origen](#source) de cadena público</span><span class="sxs-lookup"><span data-stu-id="8dbe1-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="8dbe1-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="8dbe1-121">WebMessageAsJson</span></span> 

<span data-ttu-id="8dbe1-122">Mensaje publicado desde el contenido de WebView en el host convertido en una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="8dbe1-123">cadena pública [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="8dbe1-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="8dbe1-124">Usa esta para comunicarte a través de objetos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="8dbe1-125">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsJson:</span><span class="sxs-lookup"><span data-stu-id="8dbe1-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="8dbe1-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="8dbe1-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="8dbe1-127">Si el mensaje publicado desde el contenido de WebView en el host es de tipo cadena, este método devolverá el valor de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="8dbe1-128">cadena pública [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="8dbe1-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="8dbe1-129">Si el mensaje publicado es algún otro tipo de JavaScript, este método producirá un error con E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="8dbe1-130">Use esta para comunicarse a través de cadenas simples.</span><span class="sxs-lookup"><span data-stu-id="8dbe1-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="8dbe1-131">Por ejemplo, las siguientes llamadas PostMessage provocan los siguientes valores de WebMessageAsString:</span><span class="sxs-lookup"><span data-stu-id="8dbe1-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

