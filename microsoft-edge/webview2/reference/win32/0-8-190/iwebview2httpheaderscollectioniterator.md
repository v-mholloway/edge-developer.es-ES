---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 4b9ad48d9b09343bad04d4acbe7c49750e76427d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655433"
---
# <span data-ttu-id="914d6-104">interfaz IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="914d6-104">interface IWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="914d6-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="914d6-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="914d6-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="914d6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="914d6-107">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="914d6-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="914d6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="914d6-108">Summary</span></span>

 <span data-ttu-id="914d6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="914d6-109">Members</span></span>                        | <span data-ttu-id="914d6-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="914d6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="914d6-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="914d6-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="914d6-112">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="914d6-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="914d6-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="914d6-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="914d6-114">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="914d6-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="914d6-115">Consulte [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) y [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="914d6-115">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="914d6-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="914d6-116">Members</span></span>

#### <span data-ttu-id="914d6-117">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="914d6-117">GetCurrentHeader</span></span> 

<span data-ttu-id="914d6-118">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="914d6-118">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="914d6-119">[GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="914d6-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="914d6-120">Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.</span><span class="sxs-lookup"><span data-stu-id="914d6-120">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="914d6-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="914d6-121">MoveNext</span></span> 

<span data-ttu-id="914d6-122">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="914d6-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="914d6-123">HRESULT público [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="914d6-123">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="914d6-124">El parámetro has_next se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="914d6-124">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="914d6-125">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="914d6-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

