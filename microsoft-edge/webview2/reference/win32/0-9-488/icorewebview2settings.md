---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a996660bb667ca0e556326e0bf2b71c15b9344c2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880335"
---
# <span data-ttu-id="696a8-104">0.9.515: ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="696a8-104">0.9.515 - interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="696a8-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="696a8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="696a8-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="696a8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="696a8-107">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="696a8-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="696a8-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="696a8-108">Summary</span></span>

 <span data-ttu-id="696a8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="696a8-109">Members</span></span>                        | <span data-ttu-id="696a8-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="696a8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="696a8-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="696a8-112">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="696a8-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="696a8-113">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-113">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="696a8-114">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="696a8-114">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="696a8-115">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-115">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="696a8-116">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="696a8-116">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="696a8-117">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="696a8-117">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="696a8-118">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="696a8-118">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="696a8-119">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-119">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="696a8-120">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="696a8-120">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="696a8-121">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-121">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="696a8-122">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="696a8-122">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="696a8-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="696a8-124">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="696a8-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="696a8-125">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-125">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="696a8-126">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="696a8-126">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="696a8-127">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-127">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="696a8-128">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="696a8-128">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="696a8-129">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-129">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="696a8-130">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-130">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="696a8-131">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-131">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="696a8-132">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-132">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="696a8-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="696a8-134">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-134">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="696a8-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="696a8-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="696a8-136">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="696a8-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="696a8-137">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-137">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="696a8-138">Establezca la propiedad IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-138">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="696a8-139">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-139">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="696a8-140">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-140">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="696a8-141">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-141">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="696a8-142">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-142">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="696a8-143">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-143">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="696a8-144">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-144">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="696a8-145">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-145">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="696a8-146">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-146">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="696a8-147">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="696a8-147">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="696a8-148">Miembros</span><span class="sxs-lookup"><span data-stu-id="696a8-148">Members</span></span>

#### <span data-ttu-id="696a8-149">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-149">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="696a8-150">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="696a8-150">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="696a8-151">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-151">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="696a8-152">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="696a8-152">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="696a8-153">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-153">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="696a8-154">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="696a8-154">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="696a8-155">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-155">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="696a8-156">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="696a8-156">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="696a8-157">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="696a8-157">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="696a8-158">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-158">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="696a8-159">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="696a8-159">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="696a8-160">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-160">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="696a8-161">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="696a8-161">It is true by default.</span></span>

#### <span data-ttu-id="696a8-162">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="696a8-162">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="696a8-163">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="696a8-163">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="696a8-164">[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)de HRESULT público (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="696a8-164">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="696a8-165">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="696a8-165">Defaults to TRUE.</span></span>

```cpp
            BOOL allowRemoteObjects;
            CHECK_FAILURE(m_settings->get_AreRemoteObjectsAllowed(&allowRemoteObjects));
            if (allowRemoteObjects)
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to remote objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to remote objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="696a8-166">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-166">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="696a8-167">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="696a8-167">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="696a8-168">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-168">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="696a8-169">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="696a8-169">Defaults to TRUE.</span></span> <span data-ttu-id="696a8-170">Cuando se deshabilita, se muestra una página en blanco cuando se produce un error relacionado.</span><span class="sxs-lookup"><span data-stu-id="696a8-170">When disabled, blank page will be shown when related error happens.</span></span>

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="696a8-171">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-171">get_IsScriptEnabled</span></span> 

<span data-ttu-id="696a8-172">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="696a8-172">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="696a8-173">[get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-173">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="696a8-174">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="696a8-174">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="696a8-175">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="696a8-175">It is true by default.</span></span>

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### <span data-ttu-id="696a8-176">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-176">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="696a8-177">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="696a8-177">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="696a8-178">[get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-178">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="696a8-179">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="696a8-179">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="696a8-180">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="696a8-180">It is true by default.</span></span>

#### <span data-ttu-id="696a8-181">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-181">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="696a8-182">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="696a8-182">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="696a8-183">[get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-183">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="696a8-184">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="696a8-184">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="696a8-185">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="696a8-185">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="696a8-186">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="696a8-186">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="696a8-187">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="696a8-187">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="696a8-188">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="696a8-188">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="696a8-189">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-189">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="696a8-190">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="696a8-190">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="696a8-191">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-191">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="696a8-192">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="696a8-192">Defaults to TRUE.</span></span> <span data-ttu-id="696a8-193">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom puede establecerse a través de la API de ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="696a8-193">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="696a8-194">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-194">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="696a8-195">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-195">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="696a8-196">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-196">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="696a8-197">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-197">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="696a8-198">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-198">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="696a8-199">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-199">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="696a8-200">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-200">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="696a8-201">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-201">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="696a8-202">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-202">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="696a8-203">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="696a8-203">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="696a8-204">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="696a8-204">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="696a8-205">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)de HRESULT público (se permite bool)</span><span class="sxs-lookup"><span data-stu-id="696a8-205">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="696a8-206">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-206">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="696a8-207">Establezca la propiedad IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-207">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="696a8-208">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-208">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="696a8-209">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-209">put_IsScriptEnabled</span></span> 

<span data-ttu-id="696a8-210">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-210">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="696a8-211">[put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-211">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="696a8-212">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-212">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="696a8-213">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-213">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="696a8-214">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-214">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="696a8-215">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-215">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="696a8-216">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-216">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="696a8-217">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-217">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="696a8-218">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="696a8-218">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="696a8-219">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="696a8-219">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="696a8-220">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="696a8-220">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

