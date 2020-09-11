---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: da1b9f3dbf9ba0ebd309e1017fe4e7f7e6526941
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011331"
---
# 0.9.579: ICoreWebView2HttpHeadersCollectionIterator 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Iterador para una colección de encabezados HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_HasCurrentHeader](#get_hascurrentheader) | True cuando el iterador no se ha quedado sin encabezados.
[GetCurrentHeader](#getcurrentheader) | Obtén el nombre y el valor del encabezado HTTP actual del iterador.
[MoveNext](#movenext) | Mover el iterador al siguiente encabezado HTTP de la colección.

Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) y [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md). 
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

## Miembros

#### get_HasCurrentHeader 

True cuando el iterador no se ha quedado sin encabezados.

> [get_HasCurrentHeader](#get_hascurrentheader)de HRESULT público (bool * hasCurrent)

Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.

#### GetCurrentHeader 

Obtén el nombre y el valor del encabezado HTTP actual del iterador.

> [GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr * Name, LPWStr * Value)

Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.

#### MoveNext 

Mover el iterador al siguiente encabezado HTTP de la colección.

> HRESULT público [MoveNext](#movenext)(bool * hasNext)

El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP. Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.

