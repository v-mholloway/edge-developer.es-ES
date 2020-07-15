---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: 56eacc7b06a3de5b29d316df032448b076b33e8f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879040"
---
# <span data-ttu-id="1e94e-104">interfaz ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="1e94e-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="1e94e-105">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="1e94e-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="1e94e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="1e94e-106">Summary</span></span>

 <span data-ttu-id="1e94e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e94e-107">Members</span></span>                        | <span data-ttu-id="1e94e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1e94e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1e94e-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="1e94e-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="1e94e-110">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="1e94e-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="1e94e-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="1e94e-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="1e94e-112">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="1e94e-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="1e94e-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="1e94e-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="1e94e-114">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="1e94e-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="1e94e-115">Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) y [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="1e94e-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="1e94e-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e94e-116">Members</span></span>

#### <span data-ttu-id="1e94e-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="1e94e-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="1e94e-118">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="1e94e-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="1e94e-119">[get_HasCurrentHeader](#get_hascurrentheader)de HRESULT público (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="1e94e-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="1e94e-120">Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.</span><span class="sxs-lookup"><span data-stu-id="1e94e-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="1e94e-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="1e94e-121">GetCurrentHeader</span></span> 

<span data-ttu-id="1e94e-122">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="1e94e-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="1e94e-123">[GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="1e94e-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="1e94e-124">Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.</span><span class="sxs-lookup"><span data-stu-id="1e94e-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="1e94e-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="1e94e-125">MoveNext</span></span> 

<span data-ttu-id="1e94e-126">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="1e94e-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="1e94e-127">HRESULT público [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="1e94e-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="1e94e-128">El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="1e94e-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="1e94e-129">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="1e94e-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

