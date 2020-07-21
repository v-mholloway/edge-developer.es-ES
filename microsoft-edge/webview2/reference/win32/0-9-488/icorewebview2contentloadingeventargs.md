---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 32b0f46b00195a265238541f8715ec21ca3757a1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883878"
---
# <span data-ttu-id="6d640-104">0.9.515: ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="6d640-104">0.9.515 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="6d640-105">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="6d640-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="6d640-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6d640-106">Summary</span></span>

 <span data-ttu-id="6d640-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6d640-107">Members</span></span>                        | <span data-ttu-id="6d640-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6d640-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6d640-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="6d640-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="6d640-110">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="6d640-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="6d640-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6d640-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="6d640-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="6d640-112">The ID of the navigation.</span></span>

## <span data-ttu-id="6d640-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="6d640-113">Members</span></span>

#### <span data-ttu-id="6d640-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="6d640-114">get_IsErrorPage</span></span> 

<span data-ttu-id="6d640-115">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="6d640-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="6d640-116">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="6d640-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="6d640-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6d640-117">get_NavigationId</span></span> 

<span data-ttu-id="6d640-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="6d640-118">The ID of the navigation.</span></span>

> <span data-ttu-id="6d640-119">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="6d640-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

