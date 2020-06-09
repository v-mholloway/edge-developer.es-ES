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
ms.openlocfilehash: 4ae58375f0158a3876b284e16a579149dc6db9a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699432"
---
# <span data-ttu-id="51076-104">interfaz ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="51076-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="51076-105">Argumentos de evento para el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="51076-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="51076-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="51076-106">Summary</span></span>

 <span data-ttu-id="51076-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="51076-107">Members</span></span>                        | <span data-ttu-id="51076-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="51076-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="51076-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="51076-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="51076-110">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="51076-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="51076-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="51076-111">Members</span></span>

#### <span data-ttu-id="51076-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="51076-112">get_IsNewDocument</span></span> 

<span data-ttu-id="51076-113">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="51076-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="51076-114">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="51076-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

