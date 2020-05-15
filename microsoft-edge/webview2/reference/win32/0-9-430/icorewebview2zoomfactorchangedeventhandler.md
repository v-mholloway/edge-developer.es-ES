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
ms.openlocfilehash: dd9365fb8fb0215b3090928c8edb59575c6247fe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655412"
---
# <span data-ttu-id="0b83b-104">interfaz ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0b83b-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0b83b-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="0b83b-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="0b83b-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="0b83b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="0b83b-107">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="0b83b-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="0b83b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="0b83b-108">Summary</span></span>

 <span data-ttu-id="0b83b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b83b-109">Members</span></span>                        | <span data-ttu-id="0b83b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0b83b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b83b-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="0b83b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0b83b-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0b83b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="0b83b-113">Usa la propiedad ICoreWebView2Host. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="0b83b-113">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="0b83b-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b83b-114">Members</span></span>

#### <span data-ttu-id="0b83b-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="0b83b-115">Invoke</span></span> 

<span data-ttu-id="0b83b-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0b83b-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0b83b-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="0b83b-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="0b83b-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="0b83b-118">There are no event args and the args parameter will be null.</span></span>

