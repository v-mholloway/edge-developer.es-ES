---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c3ba6ac3a2478861abb7b26e726a9cbd606b0eb9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655245"
---
# <span data-ttu-id="9bb8f-104">interfaz ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="9bb8f-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9bb8f-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9bb8f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9bb8f-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9bb8f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="9bb8f-107">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="9bb8f-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="9bb8f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9bb8f-108">Summary</span></span>

 <span data-ttu-id="9bb8f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9bb8f-109">Members</span></span>                        | <span data-ttu-id="9bb8f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9bb8f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9bb8f-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="9bb8f-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="9bb8f-112">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="9bb8f-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="9bb8f-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="9bb8f-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="9bb8f-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="9bb8f-114">The ID of the navigation.</span></span>

## <span data-ttu-id="9bb8f-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="9bb8f-115">Members</span></span>

#### <span data-ttu-id="9bb8f-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="9bb8f-116">get_IsErrorPage</span></span> 

<span data-ttu-id="9bb8f-117">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="9bb8f-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="9bb8f-118">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="9bb8f-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="9bb8f-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="9bb8f-119">get_NavigationId</span></span> 

<span data-ttu-id="9bb8f-120">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="9bb8f-120">The ID of the navigation.</span></span>

> <span data-ttu-id="9bb8f-121">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="9bb8f-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

