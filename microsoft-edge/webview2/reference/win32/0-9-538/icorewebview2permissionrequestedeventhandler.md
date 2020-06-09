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
ms.openlocfilehash: dc6af50c8e02bf556a5d6245be03bbe030fee9d6
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699309"
---
# <span data-ttu-id="cb875-104">interfaz ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="cb875-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="cb875-105">La persona que llama implementa esta interfaz para recibir el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="cb875-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="cb875-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="cb875-106">Summary</span></span>

 <span data-ttu-id="cb875-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb875-107">Members</span></span>                        | <span data-ttu-id="cb875-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cb875-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cb875-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="cb875-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cb875-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cb875-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="cb875-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb875-111">Members</span></span>

#### <span data-ttu-id="cb875-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="cb875-112">Invoke</span></span> 

<span data-ttu-id="cb875-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="cb875-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="cb875-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="cb875-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

