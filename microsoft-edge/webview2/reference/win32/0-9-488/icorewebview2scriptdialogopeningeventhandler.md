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
ms.openlocfilehash: 68cde818ee62462aac663b66dcfc0a1ec95bf08e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697801"
---
# <span data-ttu-id="1032b-104">interfaz ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="1032b-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1032b-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1032b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1032b-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="1032b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="1032b-107">La persona que llama implementa esta interfaz para recibir el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="1032b-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="1032b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="1032b-108">Summary</span></span>

 <span data-ttu-id="1032b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1032b-109">Members</span></span>                        | <span data-ttu-id="1032b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1032b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1032b-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="1032b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="1032b-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1032b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="1032b-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="1032b-113">Members</span></span>

#### <span data-ttu-id="1032b-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="1032b-114">Invoke</span></span> 

<span data-ttu-id="1032b-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1032b-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1032b-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="1032b-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

