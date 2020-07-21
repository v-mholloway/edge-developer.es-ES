---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 7bccd93aeec2c5cfbc181ce5ab1cf58e29da48ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884298"
---
# <span data-ttu-id="aad91-104">0.9.430: ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="aad91-104">0.9.430 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="aad91-105">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="aad91-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="aad91-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="aad91-106">Summary</span></span>

 <span data-ttu-id="aad91-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="aad91-107">Members</span></span>                        | <span data-ttu-id="aad91-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="aad91-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aad91-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="aad91-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="aad91-110">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="aad91-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="aad91-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="aad91-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="aad91-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="aad91-112">The ID of the navigation.</span></span>

## <span data-ttu-id="aad91-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="aad91-113">Members</span></span>

#### <span data-ttu-id="aad91-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="aad91-114">get_IsErrorPage</span></span> 

<span data-ttu-id="aad91-115">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="aad91-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="aad91-116">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="aad91-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="aad91-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="aad91-117">get_NavigationId</span></span> 

<span data-ttu-id="aad91-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="aad91-118">The ID of the navigation.</span></span>

> <span data-ttu-id="aad91-119">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="aad91-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

