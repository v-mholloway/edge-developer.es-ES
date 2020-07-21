---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/17/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 04c80d3319c74d3461666b6f35fadd0481b45207
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885537"
---
# <span data-ttu-id="b8f24-104">Clase Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="b8f24-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="b8f24-105">Espacio de nombres: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="b8f24-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="b8f24-106">Ensamblado: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="b8f24-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="b8f24-107">Esta clase es un paquete de los parámetros más comunes que se usan para crear un CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="b8f24-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="b8f24-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b8f24-108">Summary</span></span>

 <span data-ttu-id="b8f24-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8f24-109">Members</span></span>                        | <span data-ttu-id="b8f24-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b8f24-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b8f24-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="b8f24-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="b8f24-112">Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b8f24-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="b8f24-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="b8f24-113">Language</span></span>](#language) | <span data-ttu-id="b8f24-114">Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b8f24-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="b8f24-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="b8f24-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="b8f24-116">Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b8f24-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="b8f24-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="b8f24-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="b8f24-118">Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8f24-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="b8f24-119">Su propósito principal es establecer [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) para personalizar el entorno usado por una [WebView2](microsoft-web-webview2-wpf-webview2.md) durante la inicialización implícita.</span><span class="sxs-lookup"><span data-stu-id="b8f24-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="b8f24-120">También es una buena utilidad de integración con WPF que permite que los parámetros de entorno usados comúnmente sean propiedades de dependencia y que se creen y usen en el marcado.</span><span class="sxs-lookup"><span data-stu-id="b8f24-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="b8f24-121">Esta clase no está pensada para contener todas las opciones de personalización del entorno.</span><span class="sxs-lookup"><span data-stu-id="b8f24-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="b8f24-122">Si necesitas controlar completamente el entorno usado por un control WebView2, tendrás que inicializar el control de forma explícita creando tu propio entorno con CoreWebView2Environment. CreateAsync y pasándolo a [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*antes* de establecer la propiedad [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) en cualquier cosa.</span><span class="sxs-lookup"><span data-stu-id="b8f24-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="b8f24-123">Consulta la documentación de la clase [WebView2](microsoft-web-webview2-wpf-webview2.md) para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="b8f24-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="b8f24-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8f24-124">Members</span></span>

#### <span data-ttu-id="b8f24-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="b8f24-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="b8f24-126">Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b8f24-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="b8f24-127">cadena pública [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="b8f24-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="b8f24-128">Idioma</span><span class="sxs-lookup"><span data-stu-id="b8f24-128">Language</span></span> 

<span data-ttu-id="b8f24-129">Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b8f24-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="b8f24-130">[lenguaje](#language) de cadenas pública</span><span class="sxs-lookup"><span data-stu-id="b8f24-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="b8f24-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="b8f24-131">UserDataFolder</span></span> 

<span data-ttu-id="b8f24-132">Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b8f24-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="b8f24-133">cadena pública [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="b8f24-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="b8f24-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="b8f24-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="b8f24-135">Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8f24-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="b8f24-136">[CoreWebView2CreationProperties](#corewebview2creationproperties)pública ()</span><span class="sxs-lookup"><span data-stu-id="b8f24-136">public [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

