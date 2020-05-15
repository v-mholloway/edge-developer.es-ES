---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: b44724f8e18e11374f88ed2cd22711f06f59f12d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655313"
---
# <span data-ttu-id="13a1d-104">interfaz ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="13a1d-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="13a1d-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="13a1d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="13a1d-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="13a1d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="13a1d-107">La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="13a1d-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="13a1d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="13a1d-108">Summary</span></span>

 <span data-ttu-id="13a1d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="13a1d-109">Members</span></span>                        | <span data-ttu-id="13a1d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="13a1d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="13a1d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="13a1d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="13a1d-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="13a1d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="13a1d-113">Use el método get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) para obtener el nuevo número de versión.</span><span class="sxs-lookup"><span data-stu-id="13a1d-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="13a1d-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="13a1d-114">Members</span></span>

#### <span data-ttu-id="13a1d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="13a1d-115">Invoke</span></span> 

<span data-ttu-id="13a1d-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="13a1d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="13a1d-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="13a1d-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

