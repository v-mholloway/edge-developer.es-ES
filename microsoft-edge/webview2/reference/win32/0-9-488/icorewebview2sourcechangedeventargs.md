---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9a98e2afa5b15452d7521183abebc019d51e3a3c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885460"
---
# <span data-ttu-id="e1007-104">0.9.515: ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e1007-104">0.9.515 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="e1007-105">Argumentos de evento para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="e1007-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="e1007-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e1007-106">Summary</span></span>

 <span data-ttu-id="e1007-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1007-107">Members</span></span>                        | <span data-ttu-id="e1007-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e1007-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1007-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="e1007-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="e1007-110">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="e1007-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="e1007-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1007-111">Members</span></span>

#### <span data-ttu-id="e1007-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="e1007-112">get_IsNewDocument</span></span> 

<span data-ttu-id="e1007-113">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="e1007-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="e1007-114">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="e1007-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

