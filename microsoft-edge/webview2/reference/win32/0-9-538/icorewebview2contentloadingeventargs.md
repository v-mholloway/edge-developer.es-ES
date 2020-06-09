---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8acec97ec6060cd53adc3821f6a51db2048935fb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699382"
---
# <span data-ttu-id="9b191-104">interfaz ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="9b191-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="9b191-105">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9b191-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="9b191-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="9b191-106">Summary</span></span>

 <span data-ttu-id="9b191-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b191-107">Members</span></span>                        | <span data-ttu-id="9b191-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9b191-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9b191-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="9b191-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="9b191-110">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="9b191-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="9b191-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="9b191-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="9b191-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="9b191-112">The ID of the navigation.</span></span>

## <span data-ttu-id="9b191-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b191-113">Members</span></span>

#### <span data-ttu-id="9b191-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="9b191-114">get_IsErrorPage</span></span> 

<span data-ttu-id="9b191-115">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="9b191-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="9b191-116">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="9b191-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="9b191-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="9b191-117">get_NavigationId</span></span> 

<span data-ttu-id="9b191-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="9b191-118">The ID of the navigation.</span></span>

> <span data-ttu-id="9b191-119">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="9b191-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

