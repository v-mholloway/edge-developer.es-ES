---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties
ms.openlocfilehash: 72c85df7d2d58d74cf27e04eb7128fdfa14ca2d9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880258"
---
# <span data-ttu-id="61639-104">Clase Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="61639-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="61639-105">Espacio de nombres: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="61639-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="61639-106">Ensamblado: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="61639-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="61639-107">Esta clase es un paquete de los parámetros más comunes que se usan para crear un CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="61639-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="61639-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="61639-108">Summary</span></span>

 <span data-ttu-id="61639-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="61639-109">Members</span></span>                        | <span data-ttu-id="61639-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="61639-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61639-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="61639-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="61639-112">Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="61639-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="61639-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="61639-113">Language</span></span>](#language) | <span data-ttu-id="61639-114">Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="61639-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="61639-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="61639-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="61639-116">Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="61639-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="61639-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="61639-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="61639-118">Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="61639-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="61639-119">Su propósito principal es establecer [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) para personalizar el entorno usado por una [WebView2](microsoft-web-webview2-wpf-webview2.md) durante la inicialización implícita.</span><span class="sxs-lookup"><span data-stu-id="61639-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="61639-120">También es una buena utilidad de integración con WPF que permite que los parámetros de entorno usados comúnmente sean propiedades de dependencia y que se creen y usen en el marcado.</span><span class="sxs-lookup"><span data-stu-id="61639-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="61639-121">Esta clase no está pensada para contener todas las opciones de personalización del entorno.</span><span class="sxs-lookup"><span data-stu-id="61639-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="61639-122">Si necesitas controlar completamente el entorno usado por un control WebView2, tendrás que inicializar el control de forma explícita creando tu propio entorno con CoreWebView2Environment. CreateAsync y pasándolo a [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*antes* de establecer la propiedad [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) en cualquier cosa.</span><span class="sxs-lookup"><span data-stu-id="61639-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="61639-123">Consulta la documentación de la clase [WebView2](microsoft-web-webview2-wpf-webview2.md) para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="61639-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="61639-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="61639-124">Members</span></span>

#### <span data-ttu-id="61639-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="61639-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="61639-126">Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="61639-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="61639-127">cadena pública [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="61639-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="61639-128">Idioma</span><span class="sxs-lookup"><span data-stu-id="61639-128">Language</span></span> 

<span data-ttu-id="61639-129">Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="61639-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="61639-130">[lenguaje](#language) de cadenas pública</span><span class="sxs-lookup"><span data-stu-id="61639-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="61639-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="61639-131">UserDataFolder</span></span> 

<span data-ttu-id="61639-132">Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="61639-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="61639-133">cadena pública [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="61639-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="61639-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="61639-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="61639-135">Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="61639-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="61639-136">[CoreWebView2CreationProperties](#corewebview2creationproperties)pública ()</span><span class="sxs-lookup"><span data-stu-id="61639-136">public  [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

