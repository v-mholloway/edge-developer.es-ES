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
ms.openlocfilehash: 1f7eb0237e43913ffcd147ff28dde0c14561643d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655456"
---
# <span data-ttu-id="edd07-104">interfaz ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="edd07-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="edd07-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="edd07-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="edd07-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="edd07-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="edd07-107">La persona que llama implementa esta interfaz para recibir el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="edd07-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="edd07-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="edd07-108">Summary</span></span>

 <span data-ttu-id="edd07-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="edd07-109">Members</span></span>                        | <span data-ttu-id="edd07-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="edd07-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="edd07-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="edd07-111">Invoke</span></span>](#invoke) | <span data-ttu-id="edd07-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="edd07-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="edd07-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="edd07-113">Members</span></span>

#### <span data-ttu-id="edd07-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="edd07-114">Invoke</span></span> 

<span data-ttu-id="edd07-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="edd07-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="edd07-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="edd07-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span></span>

