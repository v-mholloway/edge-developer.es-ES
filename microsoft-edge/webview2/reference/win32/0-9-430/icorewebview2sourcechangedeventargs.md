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
ms.openlocfilehash: 69c569be7e712d0f5cfddbaa180419be8d475ad0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655459"
---
# <span data-ttu-id="42e11-104">interfaz ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="42e11-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="42e11-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="42e11-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="42e11-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="42e11-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="42e11-107">Argumentos de evento para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="42e11-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="42e11-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="42e11-108">Summary</span></span>

 <span data-ttu-id="42e11-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="42e11-109">Members</span></span>                        | <span data-ttu-id="42e11-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="42e11-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="42e11-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="42e11-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="42e11-112">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="42e11-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="42e11-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="42e11-113">Members</span></span>

#### <span data-ttu-id="42e11-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="42e11-114">get_IsNewDocument</span></span> 

<span data-ttu-id="42e11-115">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="42e11-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="42e11-116">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="42e11-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

