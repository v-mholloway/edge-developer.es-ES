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
ms.openlocfilehash: 519ef71db87d49aaf5a8a80970ff0cda61dfebbf
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655165"
---
# <span data-ttu-id="38433-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="38433-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

<span data-ttu-id="38433-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="38433-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="38433-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="38433-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="38433-107">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="38433-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="38433-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="38433-108">Summary</span></span>

 <span data-ttu-id="38433-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="38433-109">Members</span></span>                        | <span data-ttu-id="38433-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="38433-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="38433-111">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-111">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="38433-112">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="38433-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="38433-113">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-113">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="38433-114">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="38433-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="38433-115">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-115">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="38433-116">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="38433-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="38433-117">AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="38433-117">AreRemoteObjectsAllowed</span></span>](#areremoteobjectsallowed) | <span data-ttu-id="38433-118">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede tener acceso a los objetos remotos desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="38433-118">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="38433-119">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-119">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="38433-120">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="38433-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="38433-121">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-121">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="38433-122">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="38433-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="38433-123">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-123">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="38433-124">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="38433-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="38433-125">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-125">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="38433-126">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="38433-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="38433-127">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-127">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="38433-128">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="38433-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="38433-129">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="38433-129">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="38433-130">Miembros</span><span class="sxs-lookup"><span data-stu-id="38433-130">Members</span></span>

#### <span data-ttu-id="38433-131">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-131">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="38433-132">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="38433-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="38433-133">Public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-133">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="38433-134">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="38433-134">Defaults to TRUE.</span></span>

#### <span data-ttu-id="38433-135">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-135">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="38433-136">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="38433-136">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="38433-137">Public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-137">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="38433-138">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="38433-138">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="38433-139">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="38433-139">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="38433-140">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-140">AreDevToolsEnabled</span></span> 

<span data-ttu-id="38433-141">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="38433-141">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="38433-142">Public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-142">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="38433-143">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38433-143">It is true by default.</span></span>

#### <span data-ttu-id="38433-144">AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="38433-144">AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="38433-145">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede tener acceso a los objetos remotos desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="38433-145">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="38433-146">Public bool [AreRemoteObjectsAllowed](#areremoteobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="38433-146">public bool [AreRemoteObjectsAllowed](#areremoteobjectsallowed)</span></span>

<span data-ttu-id="38433-147">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="38433-147">Defaults to TRUE.</span></span>

#### <span data-ttu-id="38433-148">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-148">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="38433-149">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="38433-149">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="38433-150">Public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-150">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="38433-151">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="38433-151">Defaults to TRUE.</span></span> <span data-ttu-id="38433-152">Cuando se deshabilita, se muestra una página en blanco cuando se produce un error relacionado.</span><span class="sxs-lookup"><span data-stu-id="38433-152">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="38433-153">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-153">IsScriptEnabled</span></span> 

<span data-ttu-id="38433-154">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="38433-154">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="38433-155">Public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-155">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="38433-156">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="38433-156">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="38433-157">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38433-157">It is true by default.</span></span>

#### <span data-ttu-id="38433-158">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-158">IsStatusBarEnabled</span></span> 

<span data-ttu-id="38433-159">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="38433-159">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="38433-160">Public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-160">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="38433-161">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="38433-161">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="38433-162">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38433-162">It is true by default.</span></span>

#### <span data-ttu-id="38433-163">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-163">IsWebMessageEnabled</span></span> 

<span data-ttu-id="38433-164">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="38433-164">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="38433-165">Public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-165">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="38433-166">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="38433-166">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="38433-167">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="38433-167">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="38433-168">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="38433-168">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="38433-169">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="38433-169">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="38433-170">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38433-170">It is true by default.</span></span>

#### <span data-ttu-id="38433-171">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="38433-171">IsZoomControlEnabled</span></span> 

<span data-ttu-id="38433-172">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="38433-172">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="38433-173">Public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="38433-173">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="38433-174">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="38433-174">Defaults to TRUE.</span></span> <span data-ttu-id="38433-175">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom puede establecerse a través de la API de ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="38433-175">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

