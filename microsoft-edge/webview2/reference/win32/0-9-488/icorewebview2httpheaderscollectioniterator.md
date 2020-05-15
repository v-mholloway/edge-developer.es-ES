---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: cc3cf67a03f81acc546ab17fded5d7430496033f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655211"
---
# <span data-ttu-id="12e54-104">interfaz ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="12e54-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="12e54-105">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="12e54-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="12e54-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="12e54-106">Summary</span></span>

 <span data-ttu-id="12e54-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="12e54-107">Members</span></span>                        | <span data-ttu-id="12e54-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="12e54-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="12e54-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="12e54-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="12e54-110">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="12e54-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="12e54-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="12e54-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="12e54-112">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="12e54-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="12e54-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="12e54-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="12e54-114">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="12e54-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="12e54-115">Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) y [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="12e54-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
```cpp
std::wstring RequestHeadersToJsonString(ICoreWebView2HttpRequestHeaders* requestHeaders)
{
    wil::com_ptr<ICoreWebView2HttpHeadersCollectionIterator> iterator;
    CHECK_FAILURE(requestHeaders->GetIterator(&iterator));
    BOOL hasCurrent = FALSE;
    std::wstring result = L"[";

    while (SUCCEEDED(iterator->get_HasCurrentHeader(&hasCurrent)) && hasCurrent)
    {
        wil::unique_cotaskmem_string name;
        wil::unique_cotaskmem_string value;

        CHECK_FAILURE(iterator->GetCurrentHeader(&name, &value));
        result += L"{\"name\": " + EncodeQuote(name.get())
            + L", \"value\": " + EncodeQuote(value.get()) + L"}";

        BOOL hasNext = FALSE;
        CHECK_FAILURE(iterator->MoveNext(&hasNext));
        if (hasNext)
        {
            result += L", ";
        }
    }

    return result + L"]";
}
```

## <span data-ttu-id="12e54-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="12e54-116">Members</span></span>

#### <span data-ttu-id="12e54-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="12e54-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="12e54-118">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="12e54-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="12e54-119">[get_HasCurrentHeader](#get_hascurrentheader)de HRESULT público (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="12e54-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="12e54-120">Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.</span><span class="sxs-lookup"><span data-stu-id="12e54-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="12e54-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="12e54-121">GetCurrentHeader</span></span> 

<span data-ttu-id="12e54-122">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="12e54-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="12e54-123">[GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="12e54-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="12e54-124">Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.</span><span class="sxs-lookup"><span data-stu-id="12e54-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="12e54-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="12e54-125">MoveNext</span></span> 

<span data-ttu-id="12e54-126">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="12e54-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="12e54-127">HRESULT público [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="12e54-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="12e54-128">El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="12e54-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="12e54-129">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="12e54-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

