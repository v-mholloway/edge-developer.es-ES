---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2SourceChangedEventArgs
ms.openlocfilehash: 3e622a8fb5b8ed43e5a23eaab8bd0aa61ed7d193
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879404"
---
# <span data-ttu-id="e5884-104">interfaz ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e5884-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="e5884-105">Argumentos de evento para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="e5884-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="e5884-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e5884-106">Summary</span></span>

 <span data-ttu-id="e5884-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5884-107">Members</span></span>                        | <span data-ttu-id="e5884-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e5884-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5884-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="e5884-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="e5884-110">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="e5884-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="e5884-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e5884-111">Members</span></span>

#### <span data-ttu-id="e5884-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="e5884-112">get_IsNewDocument</span></span> 

<span data-ttu-id="e5884-113">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="e5884-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="e5884-114">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="e5884-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

