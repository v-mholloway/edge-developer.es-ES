---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 571aae9e1e00938c9bf0f3fb872fccf340269105
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877458"
---
# <span data-ttu-id="255a3-104">interfaz ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="255a3-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="255a3-105">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="255a3-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="255a3-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="255a3-106">Summary</span></span>

 <span data-ttu-id="255a3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="255a3-107">Members</span></span>                        | <span data-ttu-id="255a3-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="255a3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="255a3-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="255a3-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="255a3-110">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="255a3-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="255a3-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="255a3-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="255a3-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="255a3-112">The ID of the navigation.</span></span>

## <span data-ttu-id="255a3-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="255a3-113">Members</span></span>

#### <span data-ttu-id="255a3-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="255a3-114">get_IsErrorPage</span></span> 

<span data-ttu-id="255a3-115">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="255a3-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="255a3-116">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="255a3-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="255a3-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="255a3-117">get_NavigationId</span></span> 

<span data-ttu-id="255a3-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="255a3-118">The ID of the navigation.</span></span>

> <span data-ttu-id="255a3-119">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="255a3-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

