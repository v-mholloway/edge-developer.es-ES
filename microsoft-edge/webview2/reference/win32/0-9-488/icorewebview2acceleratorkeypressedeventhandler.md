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
ms.openlocfilehash: 5cbf358780d196168976fc0812c9845d0ec59b24
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655186"
---
# <span data-ttu-id="49415-104">interfaz ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="49415-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="49415-105">La persona que llama implementa esta interfaz para recibir el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="49415-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="49415-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="49415-106">Summary</span></span>

 <span data-ttu-id="49415-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="49415-107">Members</span></span>                        | <span data-ttu-id="49415-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="49415-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49415-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="49415-109">Invoke</span></span>](#invoke) | <span data-ttu-id="49415-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="49415-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="49415-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="49415-111">Members</span></span>

#### <span data-ttu-id="49415-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="49415-112">Invoke</span></span> 

<span data-ttu-id="49415-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="49415-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="49415-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="49415-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

