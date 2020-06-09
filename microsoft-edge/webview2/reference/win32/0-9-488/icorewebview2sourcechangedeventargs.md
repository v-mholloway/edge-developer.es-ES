---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8ea9437530a7f64cc045bfbaa1cc3cc55da77732
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698144"
---
# <span data-ttu-id="f8e64-104">interfaz ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8e64-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="f8e64-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f8e64-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f8e64-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="f8e64-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="f8e64-107">Argumentos de evento para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="f8e64-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="f8e64-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="f8e64-108">Summary</span></span>

 <span data-ttu-id="f8e64-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8e64-109">Members</span></span>                        | <span data-ttu-id="f8e64-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f8e64-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8e64-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="f8e64-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="f8e64-112">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="f8e64-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="f8e64-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="f8e64-113">Members</span></span>

#### <span data-ttu-id="f8e64-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="f8e64-114">get_IsNewDocument</span></span> 

<span data-ttu-id="f8e64-115">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="f8e64-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="f8e64-116">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="f8e64-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

