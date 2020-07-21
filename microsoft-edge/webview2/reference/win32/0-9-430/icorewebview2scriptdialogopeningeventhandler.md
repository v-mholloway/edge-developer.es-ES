---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 31fea451b377b86eda0055a1074706ea12d9538e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884025"
---
# <span data-ttu-id="69e3e-104">0.9.430: ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="69e3e-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="69e3e-105">La persona que llama implementa esta interfaz para recibir el evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="69e3e-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="69e3e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="69e3e-106">Summary</span></span>

 <span data-ttu-id="69e3e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="69e3e-107">Members</span></span>                        | <span data-ttu-id="69e3e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="69e3e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="69e3e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="69e3e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="69e3e-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="69e3e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="69e3e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="69e3e-111">Members</span></span>

#### <span data-ttu-id="69e3e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="69e3e-112">Invoke</span></span> 

<span data-ttu-id="69e3e-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="69e3e-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="69e3e-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="69e3e-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

