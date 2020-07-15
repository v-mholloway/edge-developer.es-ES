---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 0a5e847c2f7f83bcc253406718d4c0782b84922b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877955"
---
# <span data-ttu-id="b59a2-104">0.9.430: ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b59a2-104">0.9.430 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b59a2-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b59a2-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b59a2-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="b59a2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b59a2-107">La persona que llama implementa esta interfaz para recibir eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="b59a2-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="b59a2-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b59a2-108">Summary</span></span>

 <span data-ttu-id="b59a2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b59a2-109">Members</span></span>                        | <span data-ttu-id="b59a2-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b59a2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b59a2-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b59a2-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b59a2-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b59a2-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b59a2-113">Use la propiedad DocumentTitle para obtener el título modificado.</span><span class="sxs-lookup"><span data-stu-id="b59a2-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="b59a2-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="b59a2-114">Members</span></span>

#### <span data-ttu-id="b59a2-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="b59a2-115">Invoke</span></span> 

<span data-ttu-id="b59a2-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b59a2-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b59a2-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b59a2-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="b59a2-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="b59a2-118">There are no event args and the args parameter will be null.</span></span>

