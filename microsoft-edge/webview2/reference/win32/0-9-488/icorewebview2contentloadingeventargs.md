---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a5dd8dc0b504faad7c02669ae464ca1ef75c88af
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880783"
---
# <span data-ttu-id="3121f-104">0.9.515: ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3121f-104">0.9.515 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="3121f-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3121f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3121f-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="3121f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="3121f-107">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="3121f-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="3121f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="3121f-108">Summary</span></span>

 <span data-ttu-id="3121f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3121f-109">Members</span></span>                        | <span data-ttu-id="3121f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3121f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3121f-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3121f-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="3121f-112">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="3121f-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="3121f-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3121f-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="3121f-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="3121f-114">The ID of the navigation.</span></span>

## <span data-ttu-id="3121f-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="3121f-115">Members</span></span>

#### <span data-ttu-id="3121f-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="3121f-116">get_IsErrorPage</span></span> 

<span data-ttu-id="3121f-117">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="3121f-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="3121f-118">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="3121f-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="3121f-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="3121f-119">get_NavigationId</span></span> 

<span data-ttu-id="3121f-120">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="3121f-120">The ID of the navigation.</span></span>

> <span data-ttu-id="3121f-121">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="3121f-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

