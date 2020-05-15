---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 83193a6034184a630122864d5893ed6869ed88ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655420"
---
# <span data-ttu-id="ea426-104">interfaz ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="ea426-104">interface ICoreWebView2Settings</span></span> 

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="ea426-105">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="ea426-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="ea426-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ea426-106">Summary</span></span>

 <span data-ttu-id="ea426-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea426-107">Members</span></span>                        | <span data-ttu-id="ea426-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ea426-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea426-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="ea426-110">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ea426-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="ea426-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="ea426-112">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ea426-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="ea426-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="ea426-114">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea426-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="ea426-115">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ea426-115">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="ea426-116">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="ea426-116">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="ea426-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="ea426-118">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="ea426-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="ea426-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="ea426-120">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="ea426-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="ea426-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="ea426-122">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="ea426-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="ea426-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="ea426-124">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ea426-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="ea426-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="ea426-126">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ea426-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="ea426-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="ea426-128">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="ea426-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="ea426-130">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="ea426-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="ea426-132">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="ea426-133">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ea426-133">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="ea426-134">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="ea426-134">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="ea426-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="ea426-136">Establezca la propiedad IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="ea426-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="ea426-138">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="ea426-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="ea426-140">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="ea426-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="ea426-142">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="ea426-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="ea426-144">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="ea426-145">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="ea426-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="ea426-146">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea426-146">Members</span></span>

#### <span data-ttu-id="ea426-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="ea426-148">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ea426-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="ea426-149">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="ea426-150">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="ea426-150">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="ea426-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="ea426-152">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ea426-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="ea426-153">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="ea426-154">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="ea426-154">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="ea426-155">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="ea426-155">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="ea426-156">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-156">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="ea426-157">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea426-157">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="ea426-158">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-158">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="ea426-159">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ea426-159">It is true by default.</span></span>

#### <span data-ttu-id="ea426-160">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ea426-160">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="ea426-161">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="ea426-161">The AreRemoteObjectsAllowed property is used to control whether host objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="ea426-162">[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)de HRESULT público (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="ea426-162">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="ea426-163">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="ea426-163">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="ea426-164">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-164">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="ea426-165">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="ea426-165">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="ea426-166">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-166">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="ea426-167">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="ea426-167">Defaults to TRUE.</span></span> <span data-ttu-id="ea426-168">Cuando se deshabilita, se muestra una página en blanco cuando se produce un error relacionado.</span><span class="sxs-lookup"><span data-stu-id="ea426-168">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="ea426-169">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-169">get_IsScriptEnabled</span></span> 

<span data-ttu-id="ea426-170">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="ea426-170">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="ea426-171">[get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-171">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="ea426-172">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ea426-172">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="ea426-173">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ea426-173">It is true by default.</span></span>

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

#### <span data-ttu-id="ea426-174">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-174">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="ea426-175">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="ea426-175">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="ea426-176">[get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-176">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="ea426-177">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="ea426-177">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="ea426-178">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ea426-178">It is true by default.</span></span>

#### <span data-ttu-id="ea426-179">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-179">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="ea426-180">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ea426-180">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="ea426-181">[get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-181">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="ea426-182">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="ea426-182">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="ea426-183">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="ea426-183">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="ea426-184">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="ea426-184">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="ea426-185">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="ea426-185">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="ea426-186">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ea426-186">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="ea426-187">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-187">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="ea426-188">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ea426-188">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="ea426-189">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-189">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="ea426-190">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="ea426-190">Defaults to TRUE.</span></span> <span data-ttu-id="ea426-191">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom puede establecerse a través de la API de ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="ea426-191">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="ea426-192">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-192">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="ea426-193">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-193">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="ea426-194">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-194">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="ea426-195">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-195">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="ea426-196">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-196">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="ea426-197">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-197">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="ea426-198">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-198">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="ea426-199">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-199">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="ea426-200">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-200">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="ea426-201">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ea426-201">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="ea426-202">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="ea426-202">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="ea426-203">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)de HRESULT público (se permite bool)</span><span class="sxs-lookup"><span data-stu-id="ea426-203">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="ea426-204">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-204">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="ea426-205">Establezca la propiedad IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-205">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="ea426-206">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-206">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="ea426-207">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-207">put_IsScriptEnabled</span></span> 

<span data-ttu-id="ea426-208">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-208">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="ea426-209">[put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-209">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="ea426-210">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-210">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="ea426-211">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-211">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="ea426-212">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-212">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="ea426-213">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-213">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="ea426-214">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-214">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="ea426-215">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-215">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="ea426-216">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ea426-216">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="ea426-217">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="ea426-217">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="ea426-218">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="ea426-218">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

