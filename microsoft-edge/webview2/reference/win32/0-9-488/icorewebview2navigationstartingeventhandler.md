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
ms.openlocfilehash: 81d3fe4620dcb439933d661d7b061819b5e07a00
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655380"
---
# <span data-ttu-id="95963-104">interfaz ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="95963-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="95963-105">La persona que llama implementa esta interfaz para recibir el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="95963-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="95963-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="95963-106">Summary</span></span>

 <span data-ttu-id="95963-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="95963-107">Members</span></span>                        | <span data-ttu-id="95963-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="95963-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95963-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="95963-109">Invoke</span></span>](#invoke) | <span data-ttu-id="95963-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="95963-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="95963-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="95963-111">Members</span></span>

#### <span data-ttu-id="95963-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="95963-112">Invoke</span></span> 

<span data-ttu-id="95963-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="95963-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="95963-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="95963-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>

