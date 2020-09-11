---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2Settings
ms.openlocfilehash: 1ad6754d2ff59a92e107c66644e389582ff6053b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012707"
---
# <span data-ttu-id="ad211-104">interfaz ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="ad211-104">interface ICoreWebView2Settings</span></span> 

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="ad211-105">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="ad211-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="ad211-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ad211-106">Summary</span></span>

 <span data-ttu-id="ad211-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad211-107">Members</span></span>                        | <span data-ttu-id="ad211-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ad211-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ad211-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="ad211-110">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ad211-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>
[<span data-ttu-id="ad211-111">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-111">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="ad211-112">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ad211-112">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="ad211-113">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-113">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="ad211-114">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ad211-114">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="ad211-115">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ad211-115">get_AreHostObjectsAllowed</span></span>](#get_arehostobjectsallowed) | <span data-ttu-id="ad211-116">La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="ad211-116">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>
[<span data-ttu-id="ad211-117">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-117">get_IsBuiltInErrorPageEnabled</span></span>](#get_isbuiltinerrorpageenabled) | <span data-ttu-id="ad211-118">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="ad211-118">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>
[<span data-ttu-id="ad211-119">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-119">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="ad211-120">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="ad211-120">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="ad211-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="ad211-122">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="ad211-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="ad211-123">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-123">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="ad211-124">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ad211-124">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="ad211-125">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-125">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="ad211-126">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ad211-126">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="ad211-127">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-127">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="ad211-128">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-128">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="ad211-129">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-129">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="ad211-130">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-130">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="ad211-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="ad211-132">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-132">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="ad211-133">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ad211-133">put_AreHostObjectsAllowed</span></span>](#put_arehostobjectsallowed) | <span data-ttu-id="ad211-134">Establezca la propiedad AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="ad211-134">Set the AreHostObjectsAllowed property.</span></span>
[<span data-ttu-id="ad211-135">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-135">put_IsBuiltInErrorPageEnabled</span></span>](#put_isbuiltinerrorpageenabled) | <span data-ttu-id="ad211-136">Establezca la propiedad IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-136">Set the IsBuiltInErrorPageEnabled property.</span></span>
[<span data-ttu-id="ad211-137">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-137">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="ad211-138">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-138">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="ad211-139">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-139">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="ad211-140">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-140">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="ad211-141">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-141">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="ad211-142">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-142">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="ad211-143">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-143">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="ad211-144">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-144">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="ad211-145">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="ad211-145">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="ad211-146">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad211-146">Members</span></span>

#### <span data-ttu-id="ad211-147">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-147">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="ad211-148">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="ad211-148">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in WebView.</span></span>

> <span data-ttu-id="ad211-149">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-149">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="ad211-150">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-150">It is true by default.</span></span>

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

#### <span data-ttu-id="ad211-151">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-151">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="ad211-152">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ad211-152">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="ad211-153">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-153">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="ad211-154">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="ad211-154">If set to false, then WebView won't render the default JavaScript dialog box (Specifically those shown by the JavaScript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="ad211-155">En su lugar, si un controlador de eventos se establece a través de add_ScriptDialogOpening, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="ad211-155">Instead, if an event handler is set via add_ScriptDialogOpening, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span> <span data-ttu-id="ad211-156">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-156">It is true by default.</span></span>

#### <span data-ttu-id="ad211-157">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-157">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="ad211-158">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ad211-158">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="ad211-159">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-159">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="ad211-160">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-160">It is true by default.</span></span>

#### <span data-ttu-id="ad211-161">get_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ad211-161">get_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="ad211-162">La propiedad AreHostObjectsAllowed se usa para controlar si se puede acceder a los objetos host desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="ad211-162">The AreHostObjectsAllowed property is used to control whether host objects are accessible from the page in WebView.</span></span>

> <span data-ttu-id="ad211-163">[get_AreHostObjectsAllowed](#get_arehostobjectsallowed)de HRESULT público (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="ad211-163">public HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="ad211-164">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-164">It is true by default.</span></span>

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="ad211-165">get_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-165">get_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="ad211-166">La propiedad IsBuiltInErrorPageEnabled se usa para deshabilitar la página de error integrada para el error de navegación y el error del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="ad211-166">The IsBuiltInErrorPageEnabled property is used to disable built in error page for navigation failure and render process failure.</span></span>

> <span data-ttu-id="ad211-167">[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-167">public HRESULT [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="ad211-168">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-168">It is true by default.</span></span> <span data-ttu-id="ad211-169">Cuando se deshabilita, se muestra una página en blanco cuando se produce un error relacionado.</span><span class="sxs-lookup"><span data-stu-id="ad211-169">When disabled, blank page will be shown when related error happens.</span></span>

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

#### <span data-ttu-id="ad211-170">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-170">get_IsScriptEnabled</span></span> 

<span data-ttu-id="ad211-171">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="ad211-171">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="ad211-172">[get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-172">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="ad211-173">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ad211-173">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="ad211-174">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-174">It is true by default.</span></span>

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

#### <span data-ttu-id="ad211-175">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-175">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="ad211-176">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="ad211-176">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="ad211-177">[get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-177">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="ad211-178">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="ad211-178">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="ad211-179">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-179">It is true by default.</span></span>

#### <span data-ttu-id="ad211-180">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-180">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="ad211-181">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ad211-181">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="ad211-182">[get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-182">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="ad211-183">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="ad211-183">If set to true, communication from the host to the WebView's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="ad211-184">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host a través de la función PostMessage de window. Chrome. WebMessage y el método add_WebMessageReceived (consulte la documentación de add_WebMessageReceived para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="ad211-184">Communication from the WebView's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and add_WebMessageReceived method (see add_WebMessageReceived documentation for details).</span></span> <span data-ttu-id="ad211-185">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="ad211-185">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="ad211-186">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="ad211-186">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="ad211-187">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-187">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="ad211-188">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-188">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="ad211-189">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="ad211-189">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="ad211-190">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-190">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="ad211-191">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ad211-191">It is true by default.</span></span> <span data-ttu-id="ad211-192">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom puede establecerse a través de la API de ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="ad211-192">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via ZoomFactor API.</span></span>

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

#### <span data-ttu-id="ad211-193">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-193">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="ad211-194">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-194">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="ad211-195">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-195">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="ad211-196">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-196">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="ad211-197">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-197">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="ad211-198">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-198">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="ad211-199">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-199">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="ad211-200">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-200">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="ad211-201">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-201">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="ad211-202">put_AreHostObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="ad211-202">put_AreHostObjectsAllowed</span></span> 

<span data-ttu-id="ad211-203">Establezca la propiedad AreHostObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="ad211-203">Set the AreHostObjectsAllowed property.</span></span>

> <span data-ttu-id="ad211-204">[put_AreHostObjectsAllowed](#put_arehostobjectsallowed)de HRESULT público (se permite bool)</span><span class="sxs-lookup"><span data-stu-id="ad211-204">public HRESULT [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="ad211-205">put_IsBuiltInErrorPageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-205">put_IsBuiltInErrorPageEnabled</span></span> 

<span data-ttu-id="ad211-206">Establezca la propiedad IsBuiltInErrorPageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-206">Set the IsBuiltInErrorPageEnabled property.</span></span>

> <span data-ttu-id="ad211-207">[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-207">public HRESULT [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="ad211-208">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-208">put_IsScriptEnabled</span></span> 

<span data-ttu-id="ad211-209">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-209">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="ad211-210">[put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-210">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="ad211-211">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-211">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="ad211-212">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-212">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="ad211-213">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-213">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="ad211-214">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-214">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="ad211-215">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-215">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="ad211-216">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-216">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="ad211-217">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="ad211-217">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="ad211-218">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="ad211-218">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="ad211-219">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="ad211-219">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

