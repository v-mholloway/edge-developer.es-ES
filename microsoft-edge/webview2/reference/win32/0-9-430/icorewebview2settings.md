---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 2596b2352f36dce6773de2e60e0442ff5fa3b6d5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880223"
---
# <span data-ttu-id="422f1-104">0.9.430: ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="422f1-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="422f1-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="422f1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="422f1-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="422f1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="422f1-107">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="422f1-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="422f1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="422f1-108">Summary</span></span>

 <span data-ttu-id="422f1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="422f1-109">Members</span></span>                        | <span data-ttu-id="422f1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="422f1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="422f1-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="422f1-112">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="422f1-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="422f1-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="422f1-114">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="422f1-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="422f1-116">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="422f1-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="422f1-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="422f1-118">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="422f1-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="422f1-120">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="422f1-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="422f1-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="422f1-122">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="422f1-123">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-123">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="422f1-124">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="422f1-124">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="422f1-125">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-125">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="422f1-126">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-126">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="422f1-127">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-127">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="422f1-128">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="422f1-128">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="422f1-129">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-129">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="422f1-130">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-130">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="422f1-131">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-131">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="422f1-132">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="422f1-132">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="422f1-133">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-133">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="422f1-134">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-134">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="422f1-135">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="422f1-135">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="422f1-136">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede tener acceso a los objetos remotos desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="422f1-136">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="422f1-137">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="422f1-137">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="422f1-138">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="422f1-138">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="422f1-139">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-139">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="422f1-140">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="422f1-140">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="422f1-141">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-141">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="422f1-142">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-142">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="422f1-143">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="422f1-143">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="422f1-144">Miembros</span><span class="sxs-lookup"><span data-stu-id="422f1-144">Members</span></span>

#### <span data-ttu-id="422f1-145">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-145">get_IsScriptEnabled</span></span> 

<span data-ttu-id="422f1-146">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="422f1-146">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="422f1-147">[get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-147">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="422f1-148">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="422f1-148">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="422f1-149">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="422f1-149">It is true by default.</span></span>

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

#### <span data-ttu-id="422f1-150">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-150">put_IsScriptEnabled</span></span> 

<span data-ttu-id="422f1-151">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-151">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="422f1-152">[put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-152">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="422f1-153">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-153">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="422f1-154">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="422f1-154">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="422f1-155">[get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-155">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="422f1-156">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="422f1-156">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="422f1-157">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="422f1-157">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="422f1-158">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="422f1-158">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="422f1-159">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="422f1-159">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="422f1-160">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="422f1-160">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="422f1-161">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-161">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="422f1-162">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-162">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="422f1-163">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-163">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="422f1-164">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-164">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="422f1-165">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="422f1-165">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="422f1-166">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-166">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="422f1-167">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="422f1-167">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="422f1-168">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="422f1-168">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="422f1-169">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-169">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="422f1-170">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-170">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="422f1-171">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-171">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="422f1-172">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-172">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="422f1-173">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="422f1-173">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="422f1-174">[get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-174">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="422f1-175">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="422f1-175">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="422f1-176">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="422f1-176">It is true by default.</span></span>

#### <span data-ttu-id="422f1-177">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-177">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="422f1-178">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-178">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="422f1-179">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-179">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="422f1-180">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-180">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="422f1-181">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="422f1-181">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="422f1-182">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-182">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="422f1-183">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="422f1-183">It is true by default.</span></span>

#### <span data-ttu-id="422f1-184">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-184">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="422f1-185">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-185">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="422f1-186">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-186">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="422f1-187">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-187">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="422f1-188">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="422f1-188">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="422f1-189">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-189">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="422f1-190">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="422f1-190">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="422f1-191">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-191">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="422f1-192">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-192">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="422f1-193">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-193">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="422f1-194">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="422f1-194">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="422f1-195">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede tener acceso a los objetos remotos desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="422f1-195">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="422f1-196">[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)de HRESULT público (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="422f1-196">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="422f1-197">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="422f1-197">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="422f1-198">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="422f1-198">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="422f1-199">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="422f1-199">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="422f1-200">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)de HRESULT público (se permite bool)</span><span class="sxs-lookup"><span data-stu-id="422f1-200">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="422f1-201">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-201">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="422f1-202">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="422f1-202">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="422f1-203">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-203">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="422f1-204">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="422f1-204">Defaults to TRUE.</span></span> <span data-ttu-id="422f1-205">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom se puede establecer mediante put_ZoomFactor API.</span><span class="sxs-lookup"><span data-stu-id="422f1-205">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control is disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control is enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### <span data-ttu-id="422f1-206">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="422f1-206">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="422f1-207">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="422f1-207">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="422f1-208">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="422f1-208">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

