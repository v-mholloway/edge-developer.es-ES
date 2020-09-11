---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012673"
---
# <span data-ttu-id="b2b6b-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="b2b6b-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpHeadersCollectionIterator class</span></span> 

<span data-ttu-id="b2b6b-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b2b6b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b2b6b-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b2b6b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b2b6b-107">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="b2b6b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b2b6b-108">Summary</span></span>

 <span data-ttu-id="b2b6b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2b6b-109">Members</span></span>                        | <span data-ttu-id="b2b6b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b2b6b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b2b6b-111">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="b2b6b-111">HasCurrentHeader</span></span>](#hascurrentheader) | <span data-ttu-id="b2b6b-112">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="b2b6b-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="b2b6b-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="b2b6b-114">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="b2b6b-115">Consulte CoreWebView2HttpRequestHeaders y CoreWebView2HttpResponseHeaders.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-115">See CoreWebView2HttpRequestHeaders and CoreWebView2HttpResponseHeaders.</span></span>

## <span data-ttu-id="b2b6b-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2b6b-116">Members</span></span>

#### <span data-ttu-id="b2b6b-117">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="b2b6b-117">HasCurrentHeader</span></span> 

<span data-ttu-id="b2b6b-118">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="b2b6b-119">Public bool [HasCurrentHeader](#hascurrentheader)</span><span class="sxs-lookup"><span data-stu-id="b2b6b-119">public bool [HasCurrentHeader](#hascurrentheader)</span></span>

<span data-ttu-id="b2b6b-120">Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="b2b6b-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="b2b6b-121">MoveNext</span></span> 

<span data-ttu-id="b2b6b-122">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="b2b6b-123">Public bool [MoveNext](#movenext)()</span><span class="sxs-lookup"><span data-stu-id="b2b6b-123">public bool [MoveNext](#movenext)()</span></span>

<span data-ttu-id="b2b6b-124">El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-124">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="b2b6b-125">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

