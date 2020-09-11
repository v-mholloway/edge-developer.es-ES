---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: d70673714e3641e19f5c3d6367278c0c7bd2729b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010302"
---
# <span data-ttu-id="80793-104">0.9.579: ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="80793-104">0.9.579 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="80793-105">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="80793-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="80793-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="80793-106">Summary</span></span>

 <span data-ttu-id="80793-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="80793-107">Members</span></span>                        | <span data-ttu-id="80793-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="80793-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="80793-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="80793-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="80793-110">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="80793-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="80793-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="80793-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="80793-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="80793-112">The ID of the navigation.</span></span>

## <span data-ttu-id="80793-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="80793-113">Members</span></span>

#### <span data-ttu-id="80793-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="80793-114">get_IsErrorPage</span></span> 

<span data-ttu-id="80793-115">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="80793-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="80793-116">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="80793-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="80793-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="80793-117">get_NavigationId</span></span> 

<span data-ttu-id="80793-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="80793-118">The ID of the navigation.</span></span>

> <span data-ttu-id="80793-119">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="80793-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

