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
ms.openlocfilehash: 5230e4b4c7529924a958779665dd304ec9e6dd45
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699404"
---
# <span data-ttu-id="7c672-104">interfaz ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="7c672-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="7c672-105">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="7c672-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="7c672-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7c672-106">Summary</span></span>

 <span data-ttu-id="7c672-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c672-107">Members</span></span>                        | <span data-ttu-id="7c672-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7c672-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7c672-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="7c672-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="7c672-110">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="7c672-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="7c672-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="7c672-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="7c672-112">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="7c672-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="7c672-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="7c672-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="7c672-114">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="7c672-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="7c672-115">Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) y [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="7c672-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="7c672-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="7c672-116">Members</span></span>

#### <span data-ttu-id="7c672-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="7c672-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="7c672-118">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="7c672-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="7c672-119">[get_HasCurrentHeader](#get_hascurrentheader)de HRESULT público (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="7c672-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="7c672-120">Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.</span><span class="sxs-lookup"><span data-stu-id="7c672-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="7c672-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="7c672-121">GetCurrentHeader</span></span> 

<span data-ttu-id="7c672-122">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="7c672-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="7c672-123">[GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="7c672-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="7c672-124">Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.</span><span class="sxs-lookup"><span data-stu-id="7c672-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="7c672-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="7c672-125">MoveNext</span></span> 

<span data-ttu-id="7c672-126">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="7c672-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="7c672-127">HRESULT público [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="7c672-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="7c672-128">El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="7c672-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="7c672-129">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="7c672-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

