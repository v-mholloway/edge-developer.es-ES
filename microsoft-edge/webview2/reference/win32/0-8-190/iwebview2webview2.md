---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884739"
---
# <span data-ttu-id="40365-104">0.8.355: IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="40365-104">0.8.355 - interface IWebView2WebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="40365-105">Funcionalidad adicional implementada por el objeto WebView principal.</span><span class="sxs-lookup"><span data-stu-id="40365-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="40365-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="40365-106">Summary</span></span>

 <span data-ttu-id="40365-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="40365-107">Members</span></span>                        | <span data-ttu-id="40365-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="40365-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="40365-109">Detener</span><span class="sxs-lookup"><span data-stu-id="40365-109">Stop</span></span>](#stop) | <span data-ttu-id="40365-110">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="40365-110">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="40365-111">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="40365-111">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="40365-112">Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="40365-112">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="40365-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="40365-113">Members</span></span>

#### <span data-ttu-id="40365-114">Detener</span><span class="sxs-lookup"><span data-stu-id="40365-114">Stop</span></span> 

<span data-ttu-id="40365-115">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="40365-115">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="40365-116">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="40365-116">public HRESULT [Stop](#stop)()</span></span>

