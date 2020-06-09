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
ms.openlocfilehash: 2f0a41c72c6ac6f7bcfbf7a5cbd5eef61ffa3a68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697269"
---
# <span data-ttu-id="9ab8a-104">interfaz ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="9ab8a-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="9ab8a-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="9ab8a-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="9ab8a-107">Iterador para una colección de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="9ab8a-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9ab8a-108">Summary</span></span>

 <span data-ttu-id="9ab8a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ab8a-109">Members</span></span>                        | <span data-ttu-id="9ab8a-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9ab8a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ab8a-111">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="9ab8a-111">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="9ab8a-112">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="9ab8a-113">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="9ab8a-113">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="9ab8a-114">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-114">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="9ab8a-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="9ab8a-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="9ab8a-116">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="9ab8a-117">Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) y [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="9ab8a-117">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="9ab8a-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="9ab8a-118">Members</span></span>

#### <span data-ttu-id="9ab8a-119">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="9ab8a-119">get_HasCurrentHeader</span></span> 

<span data-ttu-id="9ab8a-120">True cuando el iterador no se ha quedado sin encabezados.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-120">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="9ab8a-121">[get_HasCurrentHeader](#get_hascurrentheader)de HRESULT público (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="9ab8a-121">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="9ab8a-122">Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-122">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="9ab8a-123">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="9ab8a-123">GetCurrentHeader</span></span> 

<span data-ttu-id="9ab8a-124">Obtén el nombre y el valor del encabezado HTTP actual del iterador.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-124">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="9ab8a-125">[GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="9ab8a-125">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="9ab8a-126">Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-126">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="9ab8a-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="9ab8a-127">MoveNext</span></span> 

<span data-ttu-id="9ab8a-128">Mover el iterador al siguiente encabezado HTTP de la colección.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="9ab8a-129">HRESULT público [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="9ab8a-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="9ab8a-130">El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="9ab8a-131">Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

