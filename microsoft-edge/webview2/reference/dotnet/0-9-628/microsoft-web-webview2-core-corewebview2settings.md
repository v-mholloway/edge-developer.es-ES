---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Settings
ms.openlocfilehash: 87b78956c29dac74bd023556a8c495222d248e9f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012633"
---
# <span data-ttu-id="963e1-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="963e1-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="963e1-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="963e1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="963e1-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="963e1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="963e1-107">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="963e1-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="963e1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="963e1-108">Summary</span></span>

 <span data-ttu-id="963e1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="963e1-109">Members</span></span>                        | <span data-ttu-id="963e1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="963e1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="963e1-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="963e1-112">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="963e1-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="963e1-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="963e1-114">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="963e1-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="963e1-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="963e1-116">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="963e1-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="963e1-117">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="963e1-117">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="963e1-118">La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="963e1-118">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="963e1-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="963e1-120">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="963e1-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="963e1-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="963e1-122">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="963e1-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="963e1-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="963e1-124">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="963e1-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="963e1-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="963e1-126">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="963e1-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="963e1-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="963e1-128">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="963e1-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="963e1-129">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="963e1-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="963e1-130">Miembros</span><span class="sxs-lookup"><span data-stu-id="963e1-130">Members</span></span>

#### <span data-ttu-id="963e1-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="963e1-132">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="963e1-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="963e1-133">Public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="963e1-134">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-134">It is true by default.</span></span>

#### <span data-ttu-id="963e1-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="963e1-136">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="963e1-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="963e1-137">Public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="963e1-138">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="963e1-138">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="963e1-139">Si se establece en true, también se puede suscribir al evento ScriptDialogOpening que contendrá toda la información del cuadro de diálogo y permitir que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="963e1-139">If set to true, one can also subscribe to ScriptDialogOpening event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="963e1-140">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-140">It is true by default.</span></span>

#### <span data-ttu-id="963e1-141">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-141">AreDevToolsEnabled</span></span> 

<span data-ttu-id="963e1-142">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="963e1-142">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="963e1-143">Public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-143">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="963e1-144">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-144">It is true by default.</span></span>

#### <span data-ttu-id="963e1-145">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="963e1-145">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="963e1-146">La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="963e1-146">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="963e1-147">Public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="963e1-147">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="963e1-148">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-148">It is true by default.</span></span>

#### <span data-ttu-id="963e1-149">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-149">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="963e1-150">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="963e1-150">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="963e1-151">Public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-151">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="963e1-152">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-152">It is true by default.</span></span> <span data-ttu-id="963e1-153">Cuando se deshabilita, se muestra una página en blanco cuando se produce un error relacionado.</span><span class="sxs-lookup"><span data-stu-id="963e1-153">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="963e1-154">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-154">IsScriptEnabled</span></span> 

<span data-ttu-id="963e1-155">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="963e1-155">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="963e1-156">Public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-156">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="963e1-157">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="963e1-157">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="963e1-158">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-158">It is true by default.</span></span>

#### <span data-ttu-id="963e1-159">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-159">IsStatusBarEnabled</span></span> 

<span data-ttu-id="963e1-160">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="963e1-160">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="963e1-161">Public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-161">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="963e1-162">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="963e1-162">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="963e1-163">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-163">It is true by default.</span></span>

#### <span data-ttu-id="963e1-164">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-164">IsWebMessageEnabled</span></span> 

<span data-ttu-id="963e1-165">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="963e1-165">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="963e1-166">Public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-166">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="963e1-167">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="963e1-167">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="963e1-168">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. la función PostMessage de WebView y el evento WebMessageReceived (consulte la documentación de WebMessageReceived para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="963e1-168">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the WebMessageReceived event (see WebMessageReceived documentation for details).</span></span> <span data-ttu-id="963e1-169">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="963e1-169">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="963e1-170">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="963e1-170">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="963e1-171">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-171">It is true by default.</span></span>

#### <span data-ttu-id="963e1-172">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="963e1-172">IsZoomControlEnabled</span></span> 

<span data-ttu-id="963e1-173">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="963e1-173">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="963e1-174">Public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="963e1-174">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="963e1-175">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="963e1-175">It is true by default.</span></span> <span data-ttu-id="963e1-176">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom puede establecerse a través de la API de ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="963e1-176">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

