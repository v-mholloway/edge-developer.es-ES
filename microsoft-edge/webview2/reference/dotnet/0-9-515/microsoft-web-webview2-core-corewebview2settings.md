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
ms.openlocfilehash: f0ac0bf7ae3b237bca45b22ed97ec16513666922
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697556"
---
# <span data-ttu-id="17e80-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="17e80-104">Microsoft.Web.WebView2.Core.CoreWebView2Settings class</span></span> 

> [!NOTE]
> <span data-ttu-id="17e80-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="17e80-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="17e80-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="17e80-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="17e80-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="17e80-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="17e80-108">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="17e80-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="17e80-109">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="17e80-109">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="17e80-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="17e80-110">Summary</span></span>

 <span data-ttu-id="17e80-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="17e80-111">Members</span></span>                        | <span data-ttu-id="17e80-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17e80-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17e80-113">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-113">AreDefaultContextMenusEnabled</span></span>](#aredefaultcontextmenusenabled) | <span data-ttu-id="17e80-114">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="17e80-114">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="17e80-115">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-115">AreDefaultScriptDialogsEnabled</span></span>](#aredefaultscriptdialogsenabled) | <span data-ttu-id="17e80-116">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="17e80-116">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="17e80-117">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-117">AreDevToolsEnabled</span></span>](#aredevtoolsenabled) | <span data-ttu-id="17e80-118">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="17e80-118">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="17e80-119">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="17e80-119">AreHostObjectsAllowed</span></span>](#arehostobjectsallowed) | <span data-ttu-id="17e80-120">La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="17e80-120">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="17e80-121">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-121">IsBuiltInErrorPageEnabled</span></span>](#isbuiltinerrorpageenabled) | <span data-ttu-id="17e80-122">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="17e80-122">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="17e80-123">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-123">IsScriptEnabled</span></span>](#isscriptenabled) | <span data-ttu-id="17e80-124">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="17e80-124">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="17e80-125">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-125">IsStatusBarEnabled</span></span>](#isstatusbarenabled) | <span data-ttu-id="17e80-126">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="17e80-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="17e80-127">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-127">IsWebMessageEnabled</span></span>](#iswebmessageenabled) | <span data-ttu-id="17e80-128">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="17e80-128">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="17e80-129">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-129">IsZoomControlEnabled</span></span>](#iszoomcontrolenabled) | <span data-ttu-id="17e80-130">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="17e80-130">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

<span data-ttu-id="17e80-131">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="17e80-131">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="17e80-132">Miembros</span><span class="sxs-lookup"><span data-stu-id="17e80-132">Members</span></span>

#### <span data-ttu-id="17e80-133">AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-133">AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="17e80-134">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="17e80-134">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="17e80-135">Public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-135">public bool [AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled)</span></span>

<span data-ttu-id="17e80-136">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="17e80-136">Defaults to TRUE.</span></span>

#### <span data-ttu-id="17e80-137">AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-137">AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="17e80-138">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="17e80-138">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="17e80-139">Public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-139">public bool [AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled)</span></span>

<span data-ttu-id="17e80-140">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="17e80-140">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="17e80-141">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="17e80-141">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="17e80-142">AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-142">AreDevToolsEnabled</span></span> 

<span data-ttu-id="17e80-143">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="17e80-143">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="17e80-144">Public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-144">public bool [AreDevToolsEnabled](#aredevtoolsenabled)</span></span>

<span data-ttu-id="17e80-145">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e80-145">It is true by default.</span></span>

#### <span data-ttu-id="17e80-146">AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="17e80-146">AreHostObjectsAllowed</span></span> 

<span data-ttu-id="17e80-147">La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="17e80-147">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="17e80-148">Public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span><span class="sxs-lookup"><span data-stu-id="17e80-148">public bool [AreHostObjectsAllowed](#arehostobjectsallowed)</span></span>

<span data-ttu-id="17e80-149">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="17e80-149">Defaults to TRUE.</span></span>

#### <span data-ttu-id="17e80-150">IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-150">IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="17e80-151">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="17e80-151">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="17e80-152">Public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-152">public bool [IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled)</span></span>

<span data-ttu-id="17e80-153">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="17e80-153">Defaults to TRUE.</span></span> <span data-ttu-id="17e80-154">Cuando se deshabilita, se muestra una página en blanco cuando se produce un error relacionado.</span><span class="sxs-lookup"><span data-stu-id="17e80-154">When disabled, blank page will be shown when related error happens.</span></span>

#### <span data-ttu-id="17e80-155">IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-155">IsScriptEnabled</span></span> 

<span data-ttu-id="17e80-156">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="17e80-156">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="17e80-157">Public bool [IsScriptEnabled](#isscriptenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-157">public bool [IsScriptEnabled](#isscriptenabled)</span></span>

<span data-ttu-id="17e80-158">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="17e80-158">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="17e80-159">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e80-159">It is true by default.</span></span>

#### <span data-ttu-id="17e80-160">IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-160">IsStatusBarEnabled</span></span> 

<span data-ttu-id="17e80-161">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="17e80-161">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="17e80-162">Public bool [IsStatusBarEnabled](#isstatusbarenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-162">public bool [IsStatusBarEnabled](#isstatusbarenabled)</span></span>

<span data-ttu-id="17e80-163">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="17e80-163">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="17e80-164">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e80-164">It is true by default.</span></span>

#### <span data-ttu-id="17e80-165">IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-165">IsWebMessageEnabled</span></span> 

<span data-ttu-id="17e80-166">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="17e80-166">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="17e80-167">Public bool [IsWebMessageEnabled](#iswebmessageenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-167">public bool [IsWebMessageEnabled](#iswebmessageenabled)</span></span>

<span data-ttu-id="17e80-168">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="17e80-168">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="17e80-169">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="17e80-169">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="17e80-170">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="17e80-170">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="17e80-171">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="17e80-171">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="17e80-172">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e80-172">It is true by default.</span></span>

#### <span data-ttu-id="17e80-173">IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="17e80-173">IsZoomControlEnabled</span></span> 

<span data-ttu-id="17e80-174">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="17e80-174">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="17e80-175">Public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span><span class="sxs-lookup"><span data-stu-id="17e80-175">public bool [IsZoomControlEnabled](#iszoomcontrolenabled)</span></span>

<span data-ttu-id="17e80-176">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="17e80-176">Defaults to TRUE.</span></span> <span data-ttu-id="17e80-177">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom puede establecerse a través de la API de ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="17e80-177">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

