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
ms.openlocfilehash: 73af2e217ca645536623eca18ceafad3270529cd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655365"
---
# <span data-ttu-id="9725e-104">interfaz ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9725e-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="9725e-105">La persona que llama implementa esta interfaz para recibir el evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="9725e-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="9725e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="9725e-106">Summary</span></span>

 <span data-ttu-id="9725e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9725e-107">Members</span></span>                        | <span data-ttu-id="9725e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9725e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9725e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9725e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9725e-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9725e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9725e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9725e-111">Members</span></span>

#### <span data-ttu-id="9725e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9725e-112">Invoke</span></span> 

<span data-ttu-id="9725e-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9725e-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9725e-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9725e-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

