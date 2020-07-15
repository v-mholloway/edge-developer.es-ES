---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 29f4a09af459e80f8c299a66b24d061e79a96f92
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881028"
---
# 0.9.430: ICoreWebView2HttpHeadersCollectionIterator 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Iterador para una colección de encabezados HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Obtén el nombre y el valor del encabezado HTTP actual del iterador.
[get_HasCurrentHeader](#get_hascurrentheader) | True cuando el iterador no se ha quedado sin encabezados.
[MoveNext](#movenext) | Mover el iterador al siguiente encabezado HTTP de la colección.

Consulte [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) y [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md). 

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

#### GetCurrentHeader 

Obtén el nombre y el valor del encabezado HTTP actual del iterador.

> [GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr * Name, LPWStr * Value)

Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.

#### get_HasCurrentHeader 

True cuando el iterador no se ha quedado sin encabezados.

> [get_HasCurrentHeader](#get_hascurrentheader)de HRESULT público (bool * hasCurrent)

Si la colección sobre la que iteración del iterador está vacía o si el iterador ha pasado al final de la colección, entonces este valor es falso.

#### MoveNext 

Mover el iterador al siguiente encabezado HTTP de la colección.

> HRESULT público [MoveNext](#movenext)(bool * hasNext)

El parámetro hasNext se establecerá en FALSE si no hay más encabezados HTTP. Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.

