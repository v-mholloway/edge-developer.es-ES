---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: d2c3b3ee179dec217418241031142549d170e440
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655065"
---
# <span data-ttu-id="2b9ae-104">Clase Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="2b9ae-104">Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties class</span></span> 

<span data-ttu-id="2b9ae-105">Espacio de nombres: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="2b9ae-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="2b9ae-106">Ensamblado: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="2b9ae-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties
  : public DependencyObject
```

<span data-ttu-id="2b9ae-107">Esta clase es un paquete de los parámetros más comunes que se usan para crear un CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-107">This class is a bundle of the most common parameters used to create a CoreWebView2Environment.</span></span>

## <span data-ttu-id="2b9ae-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2b9ae-108">Summary</span></span>

 <span data-ttu-id="2b9ae-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b9ae-109">Members</span></span>                        | <span data-ttu-id="2b9ae-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2b9ae-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2b9ae-111">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="2b9ae-111">BrowserExecutableFolder</span></span>](#browserexecutablefolder) | <span data-ttu-id="2b9ae-112">Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-112">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="2b9ae-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="2b9ae-113">Language</span></span>](#language) | <span data-ttu-id="2b9ae-114">Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-114">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="2b9ae-115">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="2b9ae-115">UserDataFolder</span></span>](#userdatafolder) | <span data-ttu-id="2b9ae-116">Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-116">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>
[<span data-ttu-id="2b9ae-117">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="2b9ae-117">CoreWebView2CreationProperties</span></span>](#corewebview2creationproperties) | <span data-ttu-id="2b9ae-118">Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-118">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

<span data-ttu-id="2b9ae-119">Su propósito principal es establecer [WebView2. CreationProperties](microsoft-web-webview2-wpf-webview2.md) para personalizar el entorno usado por una [WebView2](microsoft-web-webview2-wpf-webview2.md) durante la inicialización implícita.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-119">Its main purpose is to be set to [WebView2.CreationProperties](microsoft-web-webview2-wpf-webview2.md) in order to customize the environment used by a [WebView2](microsoft-web-webview2-wpf-webview2.md) during implicit initialization.</span></span> <span data-ttu-id="2b9ae-120">También es una buena utilidad de integración con WPF que permite que los parámetros de entorno usados comúnmente sean propiedades de dependencia y que se creen y usen en el marcado.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-120">It is also a nice WPF integration utility which allows commonly used environment parameters to be dependency properties and be created and used in markup.</span></span>

<span data-ttu-id="2b9ae-121">Esta clase no está pensada para contener todas las opciones de personalización del entorno.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-121">This class isn't intended to contain all possible environment customization options.</span></span> <span data-ttu-id="2b9ae-122">Si necesitas controlar completamente el entorno usado por un control WebView2, tendrás que inicializar el control de forma explícita creando tu propio entorno con CoreWebView2Environment. CreateAsync y pasándolo a [WebView2. EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*antes* de establecer la propiedad [WebView2. Source](microsoft-web-webview2-wpf-webview2.md) en cualquier cosa.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-122">If you need complete control over the environment used by a WebView2 control then you'll need to initialize the control explicitly by creating your own environment with CoreWebView2Environment.CreateAsync and passing it to [WebView2.EnsureCoreWebView2Async](microsoft-web-webview2-wpf-webview2.md)*before* you set the [WebView2.Source](microsoft-web-webview2-wpf-webview2.md) property to anything.</span></span> <span data-ttu-id="2b9ae-123">Consulta la documentación de la clase [WebView2](microsoft-web-webview2-wpf-webview2.md) para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-123">See the [WebView2](microsoft-web-webview2-wpf-webview2.md) class documentation for an initialization overview.</span></span>

## <span data-ttu-id="2b9ae-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b9ae-124">Members</span></span>

#### <span data-ttu-id="2b9ae-125">BrowserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="2b9ae-125">BrowserExecutableFolder</span></span> 

<span data-ttu-id="2b9ae-126">Obtiene o establece el valor que se va a pasar como el parámetro browserExecutableFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-126">Gets or sets the value to pass as the browserExecutableFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="2b9ae-127">cadena pública [BrowserExecutableFolder](#browserexecutablefolder)</span><span class="sxs-lookup"><span data-stu-id="2b9ae-127">public string [BrowserExecutableFolder](#browserexecutablefolder)</span></span>

#### <span data-ttu-id="2b9ae-128">Idioma</span><span class="sxs-lookup"><span data-stu-id="2b9ae-128">Language</span></span> 

<span data-ttu-id="2b9ae-129">Obtiene o establece el valor que se va a usar para la propiedad de idioma del parámetro CoreWebView2EnvironmentOptions que se pasa a CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-129">Gets or sets the value to use for the Language property of the CoreWebView2EnvironmentOptions parameter passed to CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="2b9ae-130">[lenguaje](#language) de cadenas pública</span><span class="sxs-lookup"><span data-stu-id="2b9ae-130">public string [Language](#language)</span></span>

#### <span data-ttu-id="2b9ae-131">UserDataFolder</span><span class="sxs-lookup"><span data-stu-id="2b9ae-131">UserDataFolder</span></span> 

<span data-ttu-id="2b9ae-132">Obtiene o establece el valor que se va a pasar como el parámetro userDataFolder de CoreWebView2Environment. CreateAsync al crear un entorno con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-132">Gets or sets the value to pass as the userDataFolder parameter of CoreWebView2Environment.CreateAsync when creating an environment with this instance.</span></span>

> <span data-ttu-id="2b9ae-133">cadena pública [UserDataFolder](#userdatafolder)</span><span class="sxs-lookup"><span data-stu-id="2b9ae-133">public string [UserDataFolder](#userdatafolder)</span></span>

#### <span data-ttu-id="2b9ae-134">CoreWebView2CreationProperties</span><span class="sxs-lookup"><span data-stu-id="2b9ae-134">CoreWebView2CreationProperties</span></span> 

<span data-ttu-id="2b9ae-135">Crea una nueva instancia de CoreWebView2CreationProperties con datos predeterminados para todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="2b9ae-135">Creates a new instance of CoreWebView2CreationProperties with default data for all properties.</span></span>

> <span data-ttu-id="2b9ae-136">[CoreWebView2CreationProperties](#corewebview2creationproperties)pública ()</span><span class="sxs-lookup"><span data-stu-id="2b9ae-136">public  [CoreWebView2CreationProperties](#corewebview2creationproperties)()</span></span>

