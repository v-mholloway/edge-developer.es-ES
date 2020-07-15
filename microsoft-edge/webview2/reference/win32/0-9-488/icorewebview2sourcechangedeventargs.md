---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9ea8f860d637c5d9e49e68917d167380c0418b87
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877374"
---
# <span data-ttu-id="1588b-104">0.9.515: ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1588b-104">0.9.515 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="1588b-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1588b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1588b-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="1588b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="1588b-107">Argumentos de evento para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="1588b-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="1588b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="1588b-108">Summary</span></span>

 <span data-ttu-id="1588b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1588b-109">Members</span></span>                        | <span data-ttu-id="1588b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1588b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1588b-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="1588b-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="1588b-112">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="1588b-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="1588b-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="1588b-113">Members</span></span>

#### <span data-ttu-id="1588b-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="1588b-114">get_IsNewDocument</span></span> 

<span data-ttu-id="1588b-115">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="1588b-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="1588b-116">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="1588b-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

