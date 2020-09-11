---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 229389c6859363ef9a7c3fbf7719dbe30a061875
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012773"
---
# <span data-ttu-id="43467-104">interfaz ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="43467-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="43467-105">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="43467-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="43467-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="43467-106">Summary</span></span>

 <span data-ttu-id="43467-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="43467-107">Members</span></span>                        | <span data-ttu-id="43467-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="43467-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="43467-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="43467-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="43467-110">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="43467-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="43467-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="43467-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="43467-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="43467-112">The ID of the navigation.</span></span>

## <span data-ttu-id="43467-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="43467-113">Members</span></span>

#### <span data-ttu-id="43467-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="43467-114">get_IsErrorPage</span></span> 

<span data-ttu-id="43467-115">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="43467-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="43467-116">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="43467-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="43467-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="43467-117">get_NavigationId</span></span> 

<span data-ttu-id="43467-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="43467-118">The ID of the navigation.</span></span>

> <span data-ttu-id="43467-119">[get_NavigationId](#get_navigationid)(HRESULT) público (UINT64 \* NavigationId)</span><span class="sxs-lookup"><span data-stu-id="43467-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

