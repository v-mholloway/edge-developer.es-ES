---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: dbcc5b10ce1973df61554f3f27174f600fb25280
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885984"
---
# <span data-ttu-id="a4346-104">0.8.355: IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="a4346-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="a4346-105">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="a4346-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="a4346-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a4346-106">Summary</span></span>

 <span data-ttu-id="a4346-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a4346-107">Members</span></span>                        | <span data-ttu-id="a4346-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a4346-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a4346-109">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="a4346-109">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="a4346-110">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="a4346-110">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="a4346-111">MoveNext</span><span class="sxs-lookup"><span data-stu-id="a4346-111">MoveNext</span></span>](#movenext) | <span data-ttu-id="a4346-112">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4346-112">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="a4346-113">Consulte [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) y [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="a4346-113">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="a4346-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="a4346-114">Members</span></span>

#### <span data-ttu-id="a4346-115">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="a4346-115">GetCurrentHeader</span></span> 

<span data-ttu-id="a4346-116">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="a4346-116">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="a4346-117">[GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="a4346-117">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="a4346-118">Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.</span><span class="sxs-lookup"><span data-stu-id="a4346-118">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="a4346-119">MoveNext</span><span class="sxs-lookup"><span data-stu-id="a4346-119">MoveNext</span></span> 

<span data-ttu-id="a4346-120">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="a4346-120">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="a4346-121">HRESULT público [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="a4346-121">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="a4346-122">El parámetro has_next se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="a4346-122">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="a4346-123">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="a4346-123">After this occurs the GetCurrentHeader method will fail if called.</span></span>

