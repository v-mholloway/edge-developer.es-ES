---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: a02a7ac3e31f959e80d5a3bdc41e39f653b9949c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655409"
---
# <span data-ttu-id="2acb9-104">interfaz IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="2acb9-104">interface IWebView2NewVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="2acb9-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="2acb9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2acb9-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2acb9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="2acb9-107">La persona que llama implementa esta interfaz para recibir eventos NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="2acb9-107">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="2acb9-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2acb9-108">Summary</span></span>

 <span data-ttu-id="2acb9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2acb9-109">Members</span></span>                        | <span data-ttu-id="2acb9-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2acb9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2acb9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="2acb9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="2acb9-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2acb9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2acb9-113">Use el método get_NewVersion de [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) para obtener el nuevo número de versión.</span><span class="sxs-lookup"><span data-stu-id="2acb9-113">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="2acb9-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="2acb9-114">Members</span></span>

#### <span data-ttu-id="2acb9-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="2acb9-115">Invoke</span></span> 

<span data-ttu-id="2acb9-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2acb9-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2acb9-117">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2acb9-117">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

