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
ms.openlocfilehash: 8451620cc819a6c2934efe80b241e7127861d48e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655472"
---
# <span data-ttu-id="ffa47-104">interfaz ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="ffa47-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="ffa47-105">La persona que llama implementa esta interfaz para recibir el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="ffa47-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="ffa47-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ffa47-106">Summary</span></span>

 <span data-ttu-id="ffa47-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ffa47-107">Members</span></span>                        | <span data-ttu-id="ffa47-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ffa47-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ffa47-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ffa47-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ffa47-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ffa47-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ffa47-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ffa47-111">Members</span></span>

#### <span data-ttu-id="ffa47-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ffa47-112">Invoke</span></span> 

<span data-ttu-id="ffa47-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ffa47-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ffa47-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ffa47-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

