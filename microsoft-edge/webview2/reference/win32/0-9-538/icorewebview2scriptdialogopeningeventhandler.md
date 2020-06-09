---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: d594e009a7a125866268ea62a0bc6d235c282b46
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699457"
---
# <span data-ttu-id="c235c-104">interfaz ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="c235c-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="c235c-105">La persona que llama implementa esta interfaz para recibir el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="c235c-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="c235c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="c235c-106">Summary</span></span>

 <span data-ttu-id="c235c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c235c-107">Members</span></span>                        | <span data-ttu-id="c235c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c235c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c235c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c235c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c235c-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c235c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c235c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c235c-111">Members</span></span>

#### <span data-ttu-id="c235c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c235c-112">Invoke</span></span> 

<span data-ttu-id="c235c-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c235c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c235c-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c235c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

