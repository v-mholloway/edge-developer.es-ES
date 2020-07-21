---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 70ccef9e99b3649ceca49b736570ba416cf73ebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883990"
---
# <span data-ttu-id="7be46-104">0.9.430: ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="7be46-104">0.9.430 - interface ICoreWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

<span data-ttu-id="7be46-105">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="7be46-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="7be46-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7be46-106">Summary</span></span>

 <span data-ttu-id="7be46-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7be46-107">Members</span></span>                        | <span data-ttu-id="7be46-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7be46-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7be46-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="7be46-110">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="7be46-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="7be46-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="7be46-112">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="7be46-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="7be46-114">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="7be46-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="7be46-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="7be46-116">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="7be46-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="7be46-118">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="7be46-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="7be46-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="7be46-120">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="7be46-121">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-121">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="7be46-122">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7be46-122">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="7be46-123">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-123">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="7be46-124">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-124">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="7be46-125">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-125">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="7be46-126">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7be46-126">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="7be46-127">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-127">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="7be46-128">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-128">Set the AreDevToolsEnabled property.</span></span>
[<span data-ttu-id="7be46-129">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-129">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="7be46-130">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="7be46-130">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="7be46-131">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-131">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="7be46-132">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-132">Set the AreDefaultContextMenusEnabled property.</span></span>
[<span data-ttu-id="7be46-133">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="7be46-133">get_AreRemoteObjectsAllowed</span></span>](#get_areremoteobjectsallowed) | <span data-ttu-id="7be46-134">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede tener acceso a los objetos remotos desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="7be46-134">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>
[<span data-ttu-id="7be46-135">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="7be46-135">put_AreRemoteObjectsAllowed</span></span>](#put_areremoteobjectsallowed) | <span data-ttu-id="7be46-136">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="7be46-136">Set the AreRemoteObjectsAllowed property.</span></span>
[<span data-ttu-id="7be46-137">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-137">get_IsZoomControlEnabled</span></span>](#get_iszoomcontrolenabled) | <span data-ttu-id="7be46-138">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="7be46-138">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>
[<span data-ttu-id="7be46-139">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-139">put_IsZoomControlEnabled</span></span>](#put_iszoomcontrolenabled) | <span data-ttu-id="7be46-140">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-140">Set the IsZoomControlEnabled property.</span></span>

<span data-ttu-id="7be46-141">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="7be46-141">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="7be46-142">Miembros</span><span class="sxs-lookup"><span data-stu-id="7be46-142">Members</span></span>

#### <span data-ttu-id="7be46-143">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-143">get_IsScriptEnabled</span></span> 

<span data-ttu-id="7be46-144">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="7be46-144">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="7be46-145">[get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-145">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="7be46-146">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7be46-146">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="7be46-147">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7be46-147">It is true by default.</span></span>

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

#### <span data-ttu-id="7be46-148">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-148">put_IsScriptEnabled</span></span> 

<span data-ttu-id="7be46-149">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-149">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="7be46-150">[put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-150">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="7be46-151">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-151">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="7be46-152">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="7be46-152">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="7be46-153">[get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-153">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="7be46-154">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="7be46-154">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="7be46-155">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="7be46-155">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="7be46-156">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="7be46-156">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="7be46-157">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="7be46-157">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="7be46-158">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7be46-158">It is true by default.</span></span>

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="7be46-159">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-159">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="7be46-160">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-160">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="7be46-161">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-161">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="7be46-162">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-162">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="7be46-163">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="7be46-163">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="7be46-164">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-164">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="7be46-165">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las alertas de JavaScript, CONFIRM, prompt functions y beforeunload Event).</span><span class="sxs-lookup"><span data-stu-id="7be46-165">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, prompt functions and beforeunload event).</span></span> <span data-ttu-id="7be46-166">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="7be46-166">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="7be46-167">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-167">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="7be46-168">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-168">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="7be46-169">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-169">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="7be46-170">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-170">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="7be46-171">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7be46-171">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="7be46-172">[get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-172">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="7be46-173">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="7be46-173">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="7be46-174">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7be46-174">It is true by default.</span></span>

#### <span data-ttu-id="7be46-175">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-175">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="7be46-176">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-176">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="7be46-177">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-177">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="7be46-178">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-178">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="7be46-179">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7be46-179">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="7be46-180">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-180">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="7be46-181">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7be46-181">It is true by default.</span></span>

#### <span data-ttu-id="7be46-182">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-182">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="7be46-183">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-183">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="7be46-184">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-184">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>

#### <span data-ttu-id="7be46-185">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-185">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="7be46-186">La propiedad AreDefaultContextMenusEnabled se usa para evitar que los usuarios de la vista vean los menús contextuales predeterminados.</span><span class="sxs-lookup"><span data-stu-id="7be46-186">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="7be46-187">[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-187">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="7be46-188">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="7be46-188">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="7be46-189">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-189">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="7be46-190">Establezca la propiedad AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-190">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="7be46-191">[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-191">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

#### <span data-ttu-id="7be46-192">get_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="7be46-192">get_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="7be46-193">La propiedad AreRemoteObjectsAllowed se usa para controlar si se puede tener acceso a los objetos remotos desde la página de WebView.</span><span class="sxs-lookup"><span data-stu-id="7be46-193">The AreRemoteObjectsAllowed property is used to control whether remote objects are accessible from the page in webview.</span></span>

> <span data-ttu-id="7be46-194">[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)de HRESULT público (bool \* allowed)</span><span class="sxs-lookup"><span data-stu-id="7be46-194">public HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(BOOL \* allowed)</span></span>

<span data-ttu-id="7be46-195">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="7be46-195">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="7be46-196">put_AreRemoteObjectsAllowed</span><span class="sxs-lookup"><span data-stu-id="7be46-196">put_AreRemoteObjectsAllowed</span></span> 

<span data-ttu-id="7be46-197">Establezca la propiedad AreRemoteObjectsAllowed.</span><span class="sxs-lookup"><span data-stu-id="7be46-197">Set the AreRemoteObjectsAllowed property.</span></span>

> <span data-ttu-id="7be46-198">[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)de HRESULT público (se permite bool)</span><span class="sxs-lookup"><span data-stu-id="7be46-198">public HRESULT [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)(BOOL allowed)</span></span>

#### <span data-ttu-id="7be46-199">get_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-199">get_IsZoomControlEnabled</span></span> 

<span data-ttu-id="7be46-200">La propiedad IsZoomControlEnabled se usa para evitar que el usuario afecte al zoom de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="7be46-200">The IsZoomControlEnabled property is used to prevent the user from impacting the zoom of the WebView.</span></span>

> <span data-ttu-id="7be46-201">[get_IsZoomControlEnabled](#get_iszoomcontrolenabled)de HRESULT público (bool \* Enabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-201">public HRESULT [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="7be46-202">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="7be46-202">Defaults to TRUE.</span></span> <span data-ttu-id="7be46-203">Cuando está deshabilitado, el usuario no podrá hacer zoom con Ctrl +/o Ctrl + rueda del mouse, pero el zoom se puede establecer mediante put_ZoomFactor API.</span><span class="sxs-lookup"><span data-stu-id="7be46-203">When disabled, user will not be able to zoom using ctrl+/- or ctrl+mouse wheel, but the zoom can be set via put_ZoomFactor API.</span></span>

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

#### <span data-ttu-id="7be46-204">put_IsZoomControlEnabled</span><span class="sxs-lookup"><span data-stu-id="7be46-204">put_IsZoomControlEnabled</span></span> 

<span data-ttu-id="7be46-205">Establezca la propiedad IsZoomControlEnabled.</span><span class="sxs-lookup"><span data-stu-id="7be46-205">Set the IsZoomControlEnabled property.</span></span>

> <span data-ttu-id="7be46-206">[put_IsZoomControlEnabled](#put_iszoomcontrolenabled)de HRESULT público (bool Enabled)</span><span class="sxs-lookup"><span data-stu-id="7be46-206">public HRESULT [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)(BOOL enabled)</span></span>

