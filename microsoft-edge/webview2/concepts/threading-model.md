---
description: Modelo de subprocesamiento
title: Modelo de subprocesamiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013740"
---
# <span data-ttu-id="4d34b-104">Modelo de subprocesamiento</span><span class="sxs-lookup"><span data-stu-id="4d34b-104">Threading model</span></span> 

<span data-ttu-id="4d34b-105">El control WebView2 se basa en el [modelo de objetos componentes (com)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) y debe ejecutarse en un único subproceso [apartamentos (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) .</span><span class="sxs-lookup"><span data-stu-id="4d34b-105">The WebView2 control is based on the [Component Object Model (COM)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) and must run on a [Single Threaded Apartments (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) thread.</span></span>

## <span data-ttu-id="4d34b-106">Seguridad de los subprocesos</span><span class="sxs-lookup"><span data-stu-id="4d34b-106">Thread safety</span></span>  

<span data-ttu-id="4d34b-107">El WebView2 debe crearse en un subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d34b-107">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="4d34b-108">Específicamente un hilo con un bombeo de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4d34b-108">Specifically a thread with a message pump.</span></span>  <span data-ttu-id="4d34b-109">Todas las devoluciones de llamada se producen en ese subproceso y las solicitudes en el WebView2 deben realizarse en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="4d34b-109">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="4d34b-110">No es seguro usar WebView2 desde otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="4d34b-110">It is not safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="4d34b-111">La única excepción es para la `Content` propiedad de `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="4d34b-111">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="4d34b-112">La `Content` propiedad Stream se lee desde un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4d34b-112">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="4d34b-113">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el rendimiento en el subproceso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d34b-113">The stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span>  

## <span data-ttu-id="4d34b-114">Ingreso</span><span class="sxs-lookup"><span data-stu-id="4d34b-114">Reentrancy</span></span>  

<span data-ttu-id="4d34b-115">Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.</span><span class="sxs-lookup"><span data-stu-id="4d34b-115">Callbacks including event handlers and completion handlers run serially.</span></span>  <span data-ttu-id="4d34b-116">Si tiene un controlador de eventos ejecutándose y comienza un bucle de mensajes, ningún otro controlador de eventos ni las devoluciones de llamada de finalización pueden comenzar a ejecutarse de forma reentrante.</span><span class="sxs-lookup"><span data-stu-id="4d34b-116">If you have an event handler running and begin a message loop, no other event handlers or completion callbacks are able to begin running in a reentrant manner.</span></span>  

## <span data-ttu-id="4d34b-117">Aplazamientos</span><span class="sxs-lookup"><span data-stu-id="4d34b-117">Deferrals</span></span>  

<span data-ttu-id="4d34b-118">Algunos eventos WebView2 leen valores establecidos en sus argumentos de evento o realizan alguna acción después de que finalice el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="4d34b-118">Some WebView2 events read values set on their event args or perform some action after the event handler completes.</span></span>  <span data-ttu-id="4d34b-119">Si también necesitas ejecutar una operación asincrónica como un controlador de eventos, puedes usar el `GetDeferral` método en los argumentos del evento de los eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="4d34b-119">If you also need to run an asynchronous operation such an event handler, you may use the `GetDeferral` method on the event args of the associated events.</span></span>  <span data-ttu-id="4d34b-120">El objeto de aplazamiento devuelto garantiza que el controlador de eventos no se considere completo hasta que `Complete` se solicite el método del `Deferral` .</span><span class="sxs-lookup"><span data-stu-id="4d34b-120">The returned Deferral object ensures the event handler is not considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="4d34b-121">Por ejemplo, puedes usar el `NewWindowRequested` evento para proporcionar una `CoreWebView2` para conectarte como una ventana secundaria cuando se completa el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="4d34b-121">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="4d34b-122">Pero si necesita crear de forma asincrónica el `CoreWebView2` , solicite el `GetDeferral` método en el `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="4d34b-122">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="4d34b-123">Después de haber creado de forma asincrónica el `CoreWebView2` y `NewWindow` de establecer la propiedad de la `NewWindowRequestedEventArgs` , la solicitud `Complete` en el `Deferral` objeto se devolverá usando el `GetDeferral` método.</span><span class="sxs-lookup"><span data-stu-id="4d34b-123">After you have asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

<!-- links -->  
