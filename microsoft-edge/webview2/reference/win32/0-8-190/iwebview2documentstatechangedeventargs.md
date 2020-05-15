---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 342716da2cded9c903f1edd13fb3400c779a9b39
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655316"
---
# <span data-ttu-id="efb5e-104">interfaz IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="efb5e-104">interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="efb5e-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="efb5e-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="efb5e-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="efb5e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="efb5e-107">Argumentos de evento para el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="efb5e-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="efb5e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="efb5e-108">Summary</span></span>

 <span data-ttu-id="efb5e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="efb5e-109">Members</span></span>                        | <span data-ttu-id="efb5e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="efb5e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="efb5e-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="efb5e-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="efb5e-112">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="efb5e-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="efb5e-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="efb5e-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="efb5e-114">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="efb5e-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="efb5e-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="efb5e-115">Members</span></span>

#### <span data-ttu-id="efb5e-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="efb5e-116">get_IsNewDocument</span></span> 

<span data-ttu-id="efb5e-117">True si la página a la que se navega es un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="efb5e-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="efb5e-118">[get_IsNewDocument](#get_isnewdocument)de HRESULT público (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="efb5e-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="efb5e-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="efb5e-119">get_IsErrorPage</span></span> 

<span data-ttu-id="efb5e-120">True si el contenido cargado es una página de error.</span><span class="sxs-lookup"><span data-stu-id="efb5e-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="efb5e-121">[get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="efb5e-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

