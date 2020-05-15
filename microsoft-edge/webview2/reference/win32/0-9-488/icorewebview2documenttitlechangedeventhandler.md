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
ms.openlocfilehash: 25e6318a695d67995f6fbf1b2ad4b02e1a982860
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655335"
---
# <span data-ttu-id="1b12f-104">interfaz ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1b12f-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1b12f-105">La persona que llama implementa esta interfaz para recibir eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="1b12f-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="1b12f-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="1b12f-106">Summary</span></span>

 <span data-ttu-id="1b12f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b12f-107">Members</span></span>                        | <span data-ttu-id="1b12f-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1b12f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b12f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b12f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1b12f-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b12f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1b12f-111">Use la propiedad DocumentTitle para obtener el título modificado.</span><span class="sxs-lookup"><span data-stu-id="1b12f-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="1b12f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b12f-112">Members</span></span>

#### <span data-ttu-id="1b12f-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="1b12f-113">Invoke</span></span> 

<span data-ttu-id="1b12f-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1b12f-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1b12f-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1b12f-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="1b12f-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="1b12f-116">There are no event args and the args parameter will be null.</span></span>

