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
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655354"
---
# <span data-ttu-id="21440-104">interfaz ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="21440-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="21440-105">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="21440-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="21440-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="21440-106">Summary</span></span>

 <span data-ttu-id="21440-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="21440-107">Members</span></span>                        | <span data-ttu-id="21440-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="21440-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21440-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="21440-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="21440-110">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="21440-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="21440-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="21440-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="21440-112">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="21440-112">The ID of the navigation.</span></span>

## <span data-ttu-id="21440-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="21440-113">Members</span></span>

#### <span data-ttu-id="21440-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="21440-114">get_IsErrorPage</span></span> 

<span data-ttu-id="21440-115">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="21440-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="21440-116">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="21440-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="21440-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="21440-117">get_NavigationId</span></span> 

<span data-ttu-id="21440-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="21440-118">The ID of the navigation.</span></span>

> <span data-ttu-id="21440-119">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="21440-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

