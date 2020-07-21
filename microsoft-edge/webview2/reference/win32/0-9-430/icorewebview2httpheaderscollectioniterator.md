---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 640926481e99c6571c0cbf9c345efa56d97e3f66
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885600"
---
# <span data-ttu-id="82a98-104">0.9.430: ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="82a98-104">0.9.430 - interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="82a98-105">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="82a98-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="82a98-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="82a98-106">Summary</span></span>

 <span data-ttu-id="82a98-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="82a98-107">Members</span></span>                        | <span data-ttu-id="82a98-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="82a98-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82a98-109">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="82a98-109">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="82a98-110">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="82a98-110">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="82a98-111">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="82a98-111">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="82a98-112">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="82a98-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="82a98-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="82a98-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="82a98-114">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="82a98-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="82a98-115">Consulte [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) y [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="82a98-115">See [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) and [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span></span> 

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

## <span data-ttu-id="82a98-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="82a98-116">Members</span></span>

#### <span data-ttu-id="82a98-117">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="82a98-117">GetCurrentHeader</span></span> 

<span data-ttu-id="82a98-118">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="82a98-118">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="82a98-119">[GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="82a98-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="82a98-120">Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.</span><span class="sxs-lookup"><span data-stu-id="82a98-120">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="82a98-121">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="82a98-121">get_HasCurrentHeader</span></span> 

<span data-ttu-id="82a98-122">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="82a98-122">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="82a98-123">[get_HasCurrentHeader](#get_hascurrentheader)de HRESULT público (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="82a98-123">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="82a98-124">Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.</span><span class="sxs-lookup"><span data-stu-id="82a98-124">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="82a98-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="82a98-125">MoveNext</span></span> 

<span data-ttu-id="82a98-126">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="82a98-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="82a98-127">HRESULT público [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="82a98-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="82a98-128">El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="82a98-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="82a98-129">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="82a98-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

