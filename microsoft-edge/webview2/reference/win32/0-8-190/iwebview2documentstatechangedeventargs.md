---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 2ef38857b06c14eb9808452a33fa23b24855f055
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878564"
---
# <span data-ttu-id="d8387-104">0.8.355: IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d8387-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d8387-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d8387-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d8387-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="d8387-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="d8387-107">Argumentos de evento para el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="d8387-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="d8387-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="d8387-108">Summary</span></span>

 <span data-ttu-id="d8387-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8387-109">Members</span></span>                        | <span data-ttu-id="d8387-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d8387-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d8387-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="d8387-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="d8387-112">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="d8387-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="d8387-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d8387-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="d8387-114">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="d8387-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="d8387-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8387-115">Members</span></span>

#### <span data-ttu-id="d8387-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="d8387-116">get_IsNewDocument</span></span> 

<span data-ttu-id="d8387-117">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="d8387-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="d8387-118">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="d8387-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="d8387-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d8387-119">get_IsErrorPage</span></span> 

<span data-ttu-id="d8387-120">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="d8387-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="d8387-121">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="d8387-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

