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
ms.openlocfilehash: c720b700257554891f13477f5f3508e331ac6b25
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698207"
---
# <span data-ttu-id="a5348-104">interfaz ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a5348-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a5348-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a5348-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a5348-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a5348-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="a5348-107">Argumentos de evento para el evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="a5348-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="a5348-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a5348-108">Summary</span></span>

 <span data-ttu-id="a5348-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5348-109">Members</span></span>                        | <span data-ttu-id="a5348-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a5348-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a5348-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a5348-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="a5348-112">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="a5348-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="a5348-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a5348-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="a5348-114">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="a5348-114">The ID of the navigation.</span></span>

## <span data-ttu-id="a5348-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5348-115">Members</span></span>

#### <span data-ttu-id="a5348-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a5348-116">get_IsErrorPage</span></span> 

<span data-ttu-id="a5348-117">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="a5348-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="a5348-118">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="a5348-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="a5348-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a5348-119">get_NavigationId</span></span> 

<span data-ttu-id="a5348-120">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="a5348-120">The ID of the navigation.</span></span>

> <span data-ttu-id="a5348-121">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="a5348-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

