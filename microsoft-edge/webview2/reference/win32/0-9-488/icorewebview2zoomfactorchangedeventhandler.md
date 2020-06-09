---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 64211bf99873ef2e2a41aaf2fb9453e892f6536a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698109"
---
# <span data-ttu-id="bdeea-104">interfaz ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="bdeea-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="bdeea-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="bdeea-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bdeea-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="bdeea-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="bdeea-107">La persona que llama implementa esta interfaz para recibir eventos ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="bdeea-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="bdeea-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="bdeea-108">Summary</span></span>

 <span data-ttu-id="bdeea-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bdeea-109">Members</span></span>                        | <span data-ttu-id="bdeea-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bdeea-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bdeea-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="bdeea-111">Invoke</span></span>](#invoke) | <span data-ttu-id="bdeea-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bdeea-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="bdeea-113">Usa la propiedad ICoreWebView2Controller. ZoomFactor para obtener el factor de zoom modificado.</span><span class="sxs-lookup"><span data-stu-id="bdeea-113">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="bdeea-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="bdeea-114">Members</span></span>

#### <span data-ttu-id="bdeea-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="bdeea-115">Invoke</span></span> 

<span data-ttu-id="bdeea-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bdeea-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bdeea-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="bdeea-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="bdeea-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="bdeea-118">There are no event args and the args parameter will be null.</span></span>

